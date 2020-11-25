# cloud-1
A devops project from the 42 curriculum.

## How to setup up this project

If you are using a private account make sure you research the free tier thoroughly: https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc

For educate accounts refer to the following restrictions https://awseducate-starter-account-services.s3.amazonaws.com/AWS_Educate_Starter_Account_Services_Supported.pdf

### AWS docs guide

Use this guide to setup your elasticbeanstalk environment: 
https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/php-hawordpress-tutorial.html

### Database

DB options are Aurora and MySQL, MySQL is the only free tier option.
Please only use the free tier option when creating your RDS DB, 
if you don’t see this option during creation, don’t create it, you will get charged. 
Once you are happy with your environment you can always create a multi AZ DB 
on AWS educate later, but not on your private account 
(unless you are fine with heavy charges). If you want to delete a DB make sure 
to NOT save snapshots, you will get billed for these, unless you want to save them of course. 


### CDN

Cloudfront is unavailable on the educate account but there are many alternatives for CDNs, eg Shift8 CDN WP plugin, 
please follow their guide on the WP plugin page: https://wordpress.org/plugins/shift8-cdn/ 
If you are having trouble installing plugins please refer to the troubleshooting guide below.

### Loadtesting

https://app.k6.io

### Trouble shooting

You may get an “incorrect format / JSON” error when uploading posts/images from WP. 
This may be due to the block editor plugin, try installing the Classic editor plugin.

If you have trouble installing plugins on the wordpress dashboard you will need to: 
Download the plugin directly from the WP website. 
Unzip the plugin directory, place the directory in wordpress-beanstalk/wp-content/plugins/ and then 
redeploy to your EBS env. On the WP dashboard activate the plugin.
