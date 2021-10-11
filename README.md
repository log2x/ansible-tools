# ansible-tools
ansible-tools for working

# DEV UAT
alias hpdevm235='cd /usr/share/nginx/html/m234.newap.hpstore.cc/'
alias hpdevin='cd /usr/share/nginx/html/in.upgrade.hpstore.cc'

# lam uat
/usr/share/nginx/html/cl.hp.php9.cc/

# Upgrade
/usr/share/nginx/html/in.upgrade.hpstore.cc


# Production  AP
/usr/share/nginx/html/www.hpshopping.in

/usr/share/nginx/html/new.hpstore.cn

/usr/share/nginx/html/new.hpshopping.hk

/usr/share/nginx/html/kr.apjonlinecdn.com

/usr/share/nginx/html/new.hpshopping.id.22

/usr/share/nginx/html/new.hpstorethailand.com.22

/usr/share/nginx/html/my.apjonlinecdn.com

/usr/share/nginx/html/sg.apjonlinecdn.com

/usr/share/nginx/html/au.apjonlinecdn.com

/usr/share/nginx/html/nz.apjonlinecdn.com


# Production LAM
/usr/share/nginx/html/ar.hp.php9.cc

/usr/share/nginx/html/br.hp.php9.cc

/usr/share/nginx/html/cl.hp.php9.cc

/usr/share/nginx/html/mx.hp.php9.cc



- name: Apply patch to multiple files under basedir
  patch:
    src: /tmp/customize.patch
    basedir: /var/www
    strip: 1

ansible pro_in -m patch -a "become=yes ansible_become_user=ubuntu src=/home/johnshi/Downloads/0001-Jira-HPST-38130-Add-categories-name-mapping.patch basedir=/usr/share/nginx/html/www.hpshopping.in  strip=1"

ansible pro_hk -m patch -a "src=/home/johnshi/Downloads/0001-Jira-HPST-38130-Add-categories-name-mapping.patch basedir=/usr/share/nginx/html/new.hpshopping.hk  strip=1"

ansible pro_kr -m patch -a "src=/home/johnshi/Downloads/0001-Jira-HPST-38130-Add-categories-name-mapping.patch basedir=/usr/share/nginx/html/kr.apjonlinecdn.com  strip=1"

ansible pro_id_th -m patch -a "src=/home/johnshi/Downloads/0001-Jira-HPST-38130-Add-categories-name-mapping.patch basedir=/usr/share/nginx/html/new.hpshopping.id.22  strip=1"

ansible pro_id_th -m patch -a "src=/home/johnshi/Downloads/0001-Jira-HPST-38130-Add-categories-name-mapping.patch basedir=/usr/share/nginx/html/new.hpstorethailand.com.22  strip=1"


ansible pro_my_sg -m patch -a "src=/home/johnshi/Downloads/0001-Jira-HPST-38130-Add-categories-name-mapping.patch basedir=/usr/share/nginx/html/my.apjonlinecdn.com  strip=1"

ansible pro_my_sg -m patch -a "src=/home/johnshi/Downloads/0001-Jira-HPST-38130-Add-categories-name-mapping.patch basedir=/usr/share/nginx/html/sg.apjonlinecdn.com  strip=1"


ansible pro_au -m patch -a "src=/home/johnshi/Downloads/0001-Jira-HPST-38130-Add-categories-name-mapping.patch basedir=/usr/share/nginx/html/au.apjonlinecdn.com  strip=1"

