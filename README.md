First, follow this: https://developer.apple.com/cocoa/coredatatutorial/index.html

Even though it's from 2006, it's still (in 2012, and for Xcode 4.4 / OS X 10.8) very useful.

Then, watch "WWDC 2011: Session 120 - View Based NSTableView". This is where you learn the basics of the "new kid on the ^".

You might wanna have a look at screenshots taken from this Project:

http://lockerz.com/s/212777221
http://lockerz.com/s/212777439

Finally, when starting the app the first time, uncomment the 3 lines in applicationDidFinishLaunching:

This will create you a record. You might also want to use the amazing

http://christian-kienle.de/CoreDataEditor

and use the "CoreTable.coredataeditor" file to visualize & change data as well.

The "important" part (that differs from @rentzsch's Movies from 2006) are:

- I don't take the managedObjectContext (Binding) from the File's Owner, since it's not a Document-Based App. I simply take it from the AppDelegate
- You have to bind the Table Column as well, like for Cell-Based, but you should LEAVE BLANK the keypath, since it's not "finished"
- The "Table Field Cell - Table View Cell" has to be bound to the the "Table Cell View" and use objectValue.bar ("bar" being the name of the column) even though Xcode claims it "cannot resolve the entered KeyPath"

Enjoy!