deduplicate-transmission

Control the doubles of the torrent seeds on two Transmissions (torrent clients).
For the duplicated torrent seeds in the two transmission: stop or remove doubles from one.
Written in the Perl.


Usage.
deduplicate-transmission [--remove|-r] login:password@mainhost login:password@secondhost
 where
 	mainhost is a host where double-torrent will be stopped or removed;
	secondhost is second host with the transmission;
	option "-r" (long form is "--remove") treats to remove doubles instead stop its.

The script ignores all seeds don't presents on both transmissions. If the seeds is exists on both "main" and "second" hosts,
the script stops or removes the seed on "mainhost" when percent of the data loaded less or equiv these on "secondhost".

Requirements.

Perl 5 with the modules (CPAN)
Transmission::Client (uses Moods)
Getopt::Long
