# jims-chroot-scripts
flexible set of scripts that build and tear down a chroot

the two scripts that do the work, are domount and dounmount. domount builds up 
a chroot, on the directory root in the dir you cloned from github. you need to 
create that directory in order to make this whole thing work. right now it's 
assumed that /, /boot, /usr and /var are all separate partitions -- TODO to make
these scripts even more flexible, I will eliminate those assumptions.

So, the basic operations (after definitions.sh is setup properly) are:

  1, built the chroot with domount
  2, now you can chroot into the newly formed filesystem
  3, when you're done, exit from the chroot, and run dounmount
  
and that's it.

Let me know if everything's clear and understandable.

-Jim
