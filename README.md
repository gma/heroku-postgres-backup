heroku-postgres-backup
======================

This script has been written to regularly download and verify backup
copies of PostgreSQL databases that are running on Heroku.

It doesn't replace Heroku's pgbackups functionality; it simply downloads
your database backups from Heroku and stores them on your own disk.

What's the point?
-----------------

1. **Flexibility and Control.** Heroku runs in the cloud. Cloud services
   shouldn't go offline at any point, but (through no fault of their
   own) Heroku has been known to go offline for considerable periods of
   time. Wouldn't it be nice to know that you've got the option to
   restore your business's or customers' database on different hardware?

2. **Verification.** If you're not verifying that you can restore from
   your backups, you're not really backing your data up. These scripts
   won't just keep a local stash of your recent Heroku database
   backups, they'll also verify that they're not corrupt. (TODO)

Setting up PostgreSQL backups on Heroku
---------------------------------------

You can find out everything you need to know about how to setup backups
on Heroku in their [PG Backups][] docs.

[PG Backups]: https://devcenter.heroku.com/articles/pgbackups
