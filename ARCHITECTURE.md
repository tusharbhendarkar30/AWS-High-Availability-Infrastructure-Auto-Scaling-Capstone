                        [ Internet User / Client ]
                                   |
                                   v
                     [ AWS Internet Gateway (IGW) ]
                                   |
                                   v
             +-------------------------------------------+
             |         Public Subnet (AZ-A & AZ-B)       |
             |                                           |
             |   [ Application Load Balancer (ALB) ]     |
             |            /                   \          |
             |           /                     \         |
             |    [ Bastion Host ]        [ NAT Gateway ]|
             +-------------------------------------------+
                                                   |
             +-------------------------------------v-----+
             |         Private Subnet (AZ-A & AZ-B)      |
             |                                           |
             |   +-----------------------------------+   |
             |   |      Auto Scaling Group (ASG)     |   |
             |   |                                   |   |
             |   |   [ Apache EC2 ]   [ Apache EC2 ] |   |
             |   |    (Desired: 2)     (Auto-Heal)   |   |
             |   +-----------------------------------+   |
             +-------------------------------------------+
