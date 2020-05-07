# check-server-hack
1. Show a listing of last logged in users: `w`

2. Use the command last: `last`

3. Last cmd by a user: 

`tail -n 200 ~/.bash_history | more`

`cat ~/.bash_history | more`

4. System files that have changed recently. : `sudo find /etc /var -mtime -2`

5. Verify_the_current_connections_from_your_computer_and_or_server: 

`netstat | more`

`netstat -ntu|awk '{print $5}'|cut -d: -f1 -s|sort|uniq -c|sort -nk1 -r`

6. lsof will list all networked processes: `lsof -i`

7. `ps aux`

8. Check_SSH_attempt_connections: 

`tail -n 300 /var/log/auth.log`

`tail -n 300 /var/log/auth.log | grep sshd`

9. Common attack points: 

`ls /tmp -la` 

`ls /dev/shm -la` 

`ls /var/tmp -la`

10. Crontab_scheduled_jobs: `less /etc/crontab`

11. Listing_users_cron_jobs_when_using_systemd_timers: `systemctl list-timers`
