# ros2.fish
Integrate ROS2 with the fish-shell, and add interactive goodies to make you robotics workflow a little more fluid.

You may get most of the functionality (and possibly better completion of a command's options) by simply putting `register-python-argcomplete --shell fish ros2 | source ` into your `config.fish`. However, this package has quite a few other advantages, see the list below. You can still add the argcomplete-line into your config, but then the completions may get a bit more crowded.

- Complete message/request type (`ros2 topic pub`, `ros2 service call`) by simply pressing tab after completing the topic/service name
- Complete message/request structure (`ros2 topic pub`, `ros2 service call`) with all their fields and default values, making it simple to publish/call complex message/service-request types. Note that fish of version 4.0 
  ![image](https://github.com/user-attachments/assets/54e15b0d-c452-4906-a975-128db0e1116f)

- Complete launch file arguments
  ![image](https://github.com/user-attachments/assets/7973e69b-569b-4b6d-8250-5e702b8b3d29)

- Complete available transitions for `ros2 lifecycle set <node name>`

  ![image](https://github.com/user-attachments/assets/cc4033e1-46f8-4ec8-8cdf-c9a2a8f85bb3)

- Abbreviations for commands, such as
  - `rnl` to get a tree of running nodes

  ![Screenshot from 2025-04-02 17-16-13](https://github.com/user-attachments/assets/754322eb-7c05-445a-a336-1e76917d53d6)


  - `rtl` to get a tree of topics

  ![Screenshot from 2025-04-02 17-14-58](https://github.com/user-attachments/assets/475d2afb-5c5c-4782-b4cf-0eab9e45c16a)


  - `rti` to get an interactive display of topics and show their type, number of subscribers/publishers for the selected topic (this requires [fzf](https://github.com/junegunn/fzf) to be installed!)

  ![image](https://github.com/user-attachments/assets/5a714cb9-52af-4183-ba3a-bed668afc61e)




## Requirements

- [fish ^3.6.0](https://github.com/fish-shell/fish-shell/releases/tag/3.6.0) enhanced the capabilities of `abbr` which this plugin makes use of. Note that for proper completion of message/request contents, you'll need [fish ^4.0.0](https://github.com/fish-shell/fish-shell/releases/tag/4.0.0)!
- Optional for the interactive view of topic info: [fzf](https://github.com/junegunn/fzf)

## Installation

Using [fisher](https://github.com/jorgebucaran/fisher)

```sh
fisher install sven-hoek/ros2.fish
```
