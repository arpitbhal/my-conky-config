my-conky-config
===============
background yes
alignment top_right
cpu_avg_samples 4
use_xft yes
xftfont daniel-9
update_interval 0.5
total_run_times 0
update_interval_on_battery 10
double_buffer yes
own_window yes
own_window_transparent yes
own_window_type normal
own_window_hints undecorated,below,sticky,skip_taskbar,skip_pager
default_bar_size 80 8
gap_y 80
gap_x 10
no_buffers no
uppercase no
net_avg_samples 1
override_utf8_locale yes
use_spacer left
pad_percents 3
temperature_unit Celsius

TEXT

${color yellow}$alignc$kernel $sysname
${color green}$alignc $nodename
$alignc $gw_ip
${hr}
$alignc CPU Usage
${hr}
${color grey}core_1: ${cpu cpu1}% ${cpubar cpu1}
${freq_g 1}Ghz

core_2: ${color grey}${cpu cpu2}% ${cpubar cpu2}
${freq_g 2}Ghz
Temperature: ${acpitemp}celsius
${color green}$hr
$alignc Memory
$hr
${color grey}Total: $memmax
In use: $mem
Free: $memfree
Using $memperc%${membar memperc}
${color green}$hr
$alignc Battery
$hr
${color grey}$battery BAT1}
${color green}$hr$alignc NETWORK
$hr${color grey}IP on eth0$alignr ${addr eth0}
Down$alignr${downspeed eth0}kb/s
Up$alignr${upspeed eth0}kb/s}
Downloaded:$alignr${totaldown eth0}
Uploaded:$alignr${totalup eth0}
