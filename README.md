make self ca and key, then sign server certificate by ansible

commands

1. Generate new SelfCA site

`ansible-playbook -i inventory/inventory.ini ca_setup.yml`

2. Generate CSR in all target hosts which need to create certificate
`ansible-playbook -i inventory/inventory.ini gen_csr.yml`

3. Sign certificate from all target csr
`ansible-playbook -i inventory/inventory.ini gen_cert.yml`

