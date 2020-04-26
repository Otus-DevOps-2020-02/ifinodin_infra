# ifinodin_infra; slack ifinodin
ifinodin Infra repository<br/>

bastion_IP = 35.195.203.112<br/>
someinternalhost_IP = 10.132.0.4<br/>

ssh config:<br/>
```Host bastion
  HostName 35.195.203.112
    IdentityFile ~/.ssh/appuser
    User appuser
    ForwardAgent yes

Host someinternalhost
  HostName 10.132.0.4
    User appuser
    ProxyJump bastion
```
