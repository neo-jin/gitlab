#redhat centos 7

yum install curl policycoreutils openssh-server openssh-clients 

systemctl enable sshd 

systemctl start sshd 

yum install postfix 

systemctl enable postfix 

systemctl start postfix

curl -sS http://packages.gitlab.cc/install/gitlab-ce/script.rpm.sh > script.rpm.sh 

Vim script.rpm.sh 

#把所有--enablerepo=‘gitlab_gitlab-ce’ 改成 --enablerepo='gitlab-ce‘

wget https://mirrors.tuna.tsinghua.edu.cn/gitlab-ce/yum/el7/gitlab-ce-8.17.3-ce.0.el7.x86_64.rpm

rpm –ivh gitlab-ce-8.17.3-ce.0.el7.x86_64.rpm

#启动GitLab

sudo gitlab-ctl reconfigure

