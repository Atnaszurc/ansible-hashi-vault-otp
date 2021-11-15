# ansible-hashi-vault-otp
This playbook is a fork from the ansible-hashi-vault-otp project at: https://github.com/jritenour/ansible-hashi-vault-otp

The playbook.yml file accepts host and token from either the environment variables or from --extra-variables put into ansible. 
If the token has permission in policy to create a SSH OTP key, the token.yml can be used. If approle is wanted, then the token needs appropriate permissions to authenticate with approle, and the approle role needs permissions to generate & read dynamic OTP credentials.

The playbook.yml file is an example file only meant to show how to call the token.yml or approle.yml files, as well as how to use the dynamically created ansible_hosts that the secondary files create with the results from Vault. 

Here you can read about setting up approle in Vault
- https://www.vaultproject.io/docs/auth/approle

And here you can read about setting up the OTP password for SSH
- https://www.vaultproject.io/docs/secrets/ssh/one-time-ssh-passwords