from jetbot import Robot
import traitlets

robot = Robot()

left_link = traitlets.dlink((controller.axes[1], 'value'), (robot.left_motor, 'value'), transform=lambda x: -x)
right_link = traitlets.dlink((controller.axes[3], 'value'), (robot.right_motor, 'value'), transform=lambda x: -x)
