# S3 Syncer

A Linux based tool for syncing your local files with Amazon S3.  This syncer attempts to create a new bucket in S3 and sync your files in a specific folder with that bucket.  


## Prerequisites

	-s3cmd (sudo apt-get install s3cmd)
	-crontab
	-an Amazon Web Service account (can be obtained [*here*](http://aws.amazon.com)

## Instructions

Simply download the file, s3syncer.cpp, and compile it using g++ (sudo apt-get install g++) by running: 'g++ s3syncer.cpp -o s3syncer

Run s3syncer with: './s3syncer' and follow the instructions.


If successfully configured, your folder with the files should be available in your S3 account.  If you add a new file to your folder locally, it should automatically sync to your s3 account.  

## Customizations

By default, the syncer checks your folder every minute for updates.  Since this syncer uses crontab, you can easily modify the time and date at which the syncer checks.  This can be accomplished by modifying the crontab configuration file.  This is done by running: 'crontab -e'

Select an editor and modify the file accordingly:

* * * * * *
| | | | | | 
| | | | | +-- Command to execute
| | | | +---- Day of the Week   (range: 1-7, 1 standing for Monday)
| | | +------ Month of the Year (range: 1-12)
| | +-------- Day of the Month  (range: 1-31)
| +---------- Hour              (range: 0-23)
+------------ Minute            (range: 0-59)





# License: [bwht.mit-license.org](bwht.mit-license.org)
  