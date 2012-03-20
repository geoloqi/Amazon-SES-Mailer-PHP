Installation
============

Install the AWS SDK for PHP from http://aws.amazon.com/sdkforphp/

The easiest way is to use their PEAR channel
http://pear.amazonwebservices.com/

`# pear channel-discover pear.amazonwebservices.com`

`# pear install aws/sdk`

Usage
=====

First, make sure this library and the PEAR modules are in your include_path

    <?php
    require_once('AmazonSESMailer.php');
    
    // Create a mailer class with your Amazon ID/Secret in the constructor
    $mailer = new AmazonSESMailer('your id', 'your secret');
    
    // Then use this object like you would use PHPMailer normally!
    $mailer->AddAddress('recipient@example.com');
    $mailer->SetFrom('sender@example.com');
    $mailer->Subject = 'Sent from Amazon SES';
    $mailer->MsgHtml('This is a test');
    $mailer->Send();
    ?>

Compatibility
=======

Compatible with [AWS SDK for PHP 1.5 "Allegro"] [0] and newer.

License
=======

Copyright 2011 by Geoloqi.com

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

[0]: http://aws.amazon.com/releasenotes/PHP/3719565440874916 "Release Notes: AWS SDK for PHP 1.5 'Allegro'"