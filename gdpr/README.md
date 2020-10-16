#Français

##RGPD

Afin de respecter le caractère privé des données personnelles, il est recommandé de ne pas utiliser celles-ci dans 
les environnements de développement ou de recette.

Voilà 3 requêtes permettant la suppression de ces données. 


**Attention à ne pas faire sur une base de production !**

```sql 

update ps_customer
set firstname='firstname',
    lastname='lastname',
    company='company',
    siret='',
    email=CONCAT('email', id_customer, '@fakemail.com')
where 1;

update ps_address
set firstname='firstname',
    lastname='lastname',
    address1='12 impasse des ours',
    phone='0606060606',
    phone_mobile='0606060606',
    vat_number=''
where 1;

update ps_connections
set ip_address = 1
where 1;

```

#English

##GDPR

In order to respect the GDPR, you are encouraged to not use any personal data in development or testing environment. 

Here are 3 sql queries allowing you to remove those personal data.

**Never use thoses in production environment !**

```sql 

update ps_customer
set firstname='firstname',
    lastname='lastname',
    company='company',
    siret='',
    email=CONCAT('email', id_customer, '@fakemail.com')
where 1;

update ps_address
set firstname='firstname',
    lastname='lastname',
    address1='12 impasse des ours',
    phone='0606060606',
    phone_mobile='0606060606',
    vat_number=''
where 1;

update ps_connections
set ip_address = 1
where 1;

```