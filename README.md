# ifinodin_infra; slack ifinodin
ifinodin Infra repository
'''
bastion_IP = 35.195.203.112
someinternalhost_IP = 10.132.0.4
'''
'''### First bastion. Directly reachable
Host bastion
  HostName 35.195.203.112
    IdentityFile ~/.ssh/appuser
    User appuser
    ForwardAgent yes

### Host to jump to via bastion
Host someinternalhost
  HostName 10.132.0.4
    User appuser
    ProxyJump bastion
'''
