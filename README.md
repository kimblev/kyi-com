# kyrealtorinstitute.com Drupal 8 codebase

This is the Drupal code base that powers kyrealtorinstitute.com.

##
The process here is a little unusual. 

Client cannot give me SSH access to their server, so I set up D8 site on my Dev machine. When I tried pulling migration data from the live site to my Dev server, the clients' hosting servers will not permit external DB connections.

I then copied the live site to my host and tried to pull migration data again but ISP blocked it (at least the error was signed by Comcast).

I then tried building the D* site on my Dev, becuase it must use Composer due to Commerce requirement, with plan to copy that site also to my host and then perform the migration.

Now I have discovered that Dreamhost allows shared hosting account to install Composer (and Drush). So maybe no need for my Dev machine at all

I tried migating by pulling migration from the live site to my dev machine but 

##
In this project synced folders are not working so I'm using this command to pull files from the guest to the host:
...
vagrant scp kyrealtor1111:/var/www/drupalvm/drupal ~/Desktop/Upwork/JonathanMoore/d8.kyrealtorinstitute.local/local-scp-copy/
...
This command must be run from the host directory which has the Vagrant file in it.

It may now be no longer necessary to use my Dev

##
Install instructions for Composer and Drush on Dreamhost
TODO:

Must use this:
php composer require drush/drush

