#include "ros/ros.h"
#include "arm/angles.h"

void chatterCallback(const arm::angles::ConstPtr& msg)
{
  ROS_INFO("I heard");
  // here will lie code for managing servomotor
}

int main(int argc, char **argv)
{
  ros::init(argc, argv, "pwm_sender");

  ros::NodeHandle n;

  ros::Subscriber sub = n.subscribe("ang_chatter", 1000, chatterCallback);

  ros::spin();

  return 0;
}
