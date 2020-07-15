# raspberrypi-cpu-cooling-fan-control

## To read raspberry pi cpu tempreture:
```
$ cat /sys/class/thermal/thermal_zone0/temp
```

## Configure to auto-run fan after reboot
`$ crontab -e`

Then add these lines and save:
```
# run fan cooling cpu tempreture
@reboot python <raspberrypi-cpu-cooling-fan-control folder>/fan_ctrl.py
```
References:
- Run a task on reboot (https://www.raspberrypi.org/documentation/linux/usage/cron.md)
- This project was made base on this tutorial (https://www.instructables.com/id/PWM-Regulated-Fan-Based-on-CPU-Temperature-for-Ras/)
