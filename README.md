This is a scratch of an Android app which listens for notifications and creates new/custom notifications out of the initial one.

The only reason I created this app is that I could not see the images of the notifications from my Nest cameras in my Samsung Galaxy Watch Active 2 (GWA2), just the text "Your Front Door camera noticed some activity" in my watch was useless, and that was bothering me for a long while.

The main images in a Nest camera notification are a sequence of images (so you can see some movement in between the frames in your phone), and those images are available in a location which the GWA2 doesn't use. There is also a single camera frame/image under in an EXTRA_PICTURE which becomes available if you create a WearableExtender out of the source notification, but that EXTRA_PICTURE is also not consumed by GWA2, however, it's in a good format to be used as a "bigPicture" in a regular Notification, and that, yes, gets consumed by the GWA2, **hurray!**

Hence, this app just extracts data from the source notification and creates a new simple/standard notification which works great with my GWA2.

With the current version of this app, I'm able to get all Nest camera notifications and see their text and images, so, so far, I had no need to improve it, but maybe someone out there is also looking for a way to solve the same problem I had, or maybe have some ideas and wants to extend this app. (*You read this far so, yeah, go for it and have fun!*)

Note that once you install it into your phone (push it to phone with Android Studio), you will need to find the app in the launcher and open it once and grand permission so it can retrieve notification images.

Pros: 
- Nest camera notifications show up with images in my GWA2.
- Once installed, it simply works. 

Cons:
- The new notifications don't show movement / multiple frames as the original Nest notification does - GWA2 does not support it (maybe updating the image of an existing notification in a loop would be interesting - but I don't believe it works for GWA2) 
- Nest notifications are duplicated, but it's possible to modify this app to clean up the source, but then you'll loose the cool Nest notification with "movement".