/These playbooks are run from Ansible Tower. 

I have the following variables defined in my job template for the provision_lab_generic.yml playbook.

---
student_count_start: 1
student_count_end: 3
ec2_name_prefix: test
tower_install: false
system_user: student
workshop_password: r3dh4t
workshop_dns_zone: rhdemo.io
route53_state: present
tower_install: false
ec2_key_name: lrich-key               # SSH key in AWS to put in all the instances
#ec2_zone: us-east-1a
ec2_region: us-east-1                 # region where the nodes will live
ec2_name_prefix: WS-LRICH         # name prefix for all the VMs
ec2_vpc_id: vpc-37d1504f
ec2_vpc_subnet_id: subnet-7e169435
#ec2_vpc_id: vpc-70548214              # EC2 VPC ID in your region
#ec2_vpc_subnet_id: subnet-c0d9ec99    # EC2 subnet ID in your VPC
sendgrid_api_key:             # Instead of username and password, you may use an API key. Don't define both.
instructor_email:   # address you want the emails to arrive from
admin_password: r3dh4t          # Set this to something better if you'd like. Defaults to 'LearnAnsible[two digit month][two digit year]', e.g., LearnAnsible0416
email: no
ssh_port: 22
admin_password_hash: "{{ admin_password | password_hash(salt='sRvXWmR5BBwqRlih') }}"
ec2_lab_node_types:
  - name: control
    type: rhel7-tower
  - name: node1
    type: rhel7
  - name: node2
    type: rhel7
    
  I have the following variable defined in my job template for the install_guacamole.yml playbook:
  
  ---
host_addr: 54.147.16.75


I have the following variables defined in my job template for the install_guacamole.yml playbook:

---
host_addr: 54.147.16.75
workshop_dns_zone: rhdemo.io
route53_state: present

/
