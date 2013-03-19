CodeIgniter-Sample-Project
==========================

Sample administrator panel using CodeIgniter with Mysql and Twiter Boostrap.

<h2>Requirements</h2>
<ul>
<li>
<a href="http://twitter.github.com/bootstrap/" target="_blank">Bootstrap</a> 2.0.4+</li>
<li>
<a href="http://jquery.com/" target="_blank">jQuery</a> 1.7.1+</li>
</ul>


<h2>Functionalities:</h2>

<ul>
  <li>Login/Logout</li>
  <li>List data content with pagination, search, and filters</li>
  <li>All forms with back end validation</li>
  <li>Insert new data</li>
  <li>Edit data</li>
  <li>Delete data</li>
</ul>
------------------------------------------------------------------
<h2>Live preview in</h2>
<a href="http://cisample.brunosapienza.com" target="blank">cisample.brunosapienza.com</a>

login = admin <br />
password =  admin

------------------------------------------------------------------

<h2>Routes </h2>

```
/products
/products/id
/manufacturers
/manufacturers/id
```

------------------------------------------------------------------

<h2>Screenshots</h2>

<img src="http://cl.ly/image/040F053a0v07/Screen%20Shot%202013-03-19%20at%203.35.55%20PM.png"/>

<img src="http://cl.ly/image/3o1I3i3z0C0F/Screen%20Shot%202013-03-19%20at%203.40.43%20PM.png"/>

------------------------------------------------------------------

<h2>Mysql Dump</h2>

```
CREATE TABLE `ci_cookies` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `cookie_id` varchar(255) DEFAULT NULL,
  `netid` varchar(255) DEFAULT NULL,
  `ip_address` varchar(255) DEFAULT NULL,
  `user_agent` varchar(255) DEFAULT NULL,
  `orig_page_requested` varchar(120) DEFAULT NULL,
  `php_session_id` varchar(40) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` datetime DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

CREATE TABLE `ci_sessions` (
  `session_id` varchar(40) NOT NULL DEFAULT '0',
  `ip_address` varchar(45) NOT NULL DEFAULT '0',
  `user_agent` varchar(120) NOT NULL,
  `last_activity` int(10) unsigned NOT NULL DEFAULT '0',
  `user_data` text NOT NULL,
  PRIMARY KEY (`session_id`),
  KEY `last_activity_idx` (`last_activity`)
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

CREATE TABLE `manufacturers` (
  `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
  `name` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

CREATE TABLE `membership` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `first_name` varchar(255) DEFAULT NULL,
  `last_name` varchar(255) DEFAULT NULL,
  `email_addres` varchar(255) DEFAULT NULL,
  `user_name` varchar(255) DEFAULT NULL,
  `pass_word` varchar(32) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

CREATE TABLE `products` (
  `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
  `description` varchar(40) DEFAULT NULL,
  `stock` double DEFAULT NULL,
  `cost_price` double DEFAULT NULL,
  `sell_price` double DEFAULT NULL,
  `manufacture_id` int(11) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

```
