# SSH Safety measures

> This is unfinished, barely tested work.   
You could end up locked out of target!!!

This role enables a more tight security for ssh cconnections on target Ubuntu environment.

Credits to posts that were reference for this:  
@plusbryan [twitter] for https://plusbryan.com/my-first-5-minutes-on-a-server-or-essential-security-for-linux-servers   
Vivek Gite for https://www.cyberciti.biz/tips/linux-unix-bsd-openssh-server-best-practices.html

## Requirements

SSH public keys of the Ansible server and possibly other macines on the target.

## Role Variables

There is one required variable:

|         var | default | required? |    description |
|-------------|---------|-----------|----------------|
|SSH_LOG_EMAIL| _empty_ |       yes | email to where the notifications will be sent to|

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
         - { role: ssh-safety, SSH_LOG_EMAIL: kirk@enterprise.ufp }

## License

MIT

## Author Information

@mashimom