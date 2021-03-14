
dres-test
=========

This is role for testing DRES host

What is this role do:
- test and change for user  password time elapse
- test status of user acount
- test  haproxy service working on DRES
- test connection for choosen port from DRES to any end point machine


Role Variables
--------------

To use this role please check and set variable in var/main.yml
--------------------------------------------------------------
--------------------------------------------------------------


Put  user name you would like to process
---------------------------------------

users: 'autom802'

For how long password should be valid
-------------------------------------

user_password_valid_time: 9999

Put here endpoint host you would like test  port is open or not. If DNS not available , put ip address
-------------------------------------------------------------------------------------------------------

end_point_host: 192.168.88.1 

Put here port you would like to test on endpoint
-------------------------------------------------

end_point_host_port: 8081

Please choose which task you would like to run yes/no
-----------------------------------------------------

user_manage: yes

user_status: yes

check_haproxy: yes

test_remote: yes



Example Playbook
----------------



    - hosts: all
      become: true
      roles:
          - dres-test

License
-------
BSD

Author Information
------------------
slawomir.jach1@ibm.com

