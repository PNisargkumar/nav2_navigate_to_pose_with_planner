# navigate_to_pose_with_planner : Navigation Plugin for ROS 2

This plugin provides additional functionality to the nav_to_pose pluginh bu enabling selection of planner when using the /navigation_to_pose_with_planner action.

The customised action and messages are defined the package nav2_custom_msgs.

## Features

- Navigation to specified poses using behavior trees.
- Custom message types for representing poses with planner IDs from the planner server.

## Installation

Clone this repository into your ROS 2 workspace:

```bash
git clone https://github.com/PNisargkumar/nav2_navigate_to_pose_with_planner.git
```

## Usage

Add the navigators in the nav2_params file

```yaml
    navigators: ["navigate_to_pose","navigate_to_pose_with_planner"]
    navigate_to_pose:
      plugin: "nav2_bt_navigator/NavigateToPoseNavigator"
    navigate_to_pose_with_planner:
      plugin: "nav2_navigate_to_pose_with_planner/NavigateToPoseNavigatorWithPlanner"
```

the default behavior tree can be found in "nav2_navigate_to_pose_with_planner/behavior_trees/navigate_to_pose_w_replanning_and_recovery_with_planner.xml"


