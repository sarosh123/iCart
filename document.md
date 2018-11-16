Application Working 
----------------------
  This is the simple e-commerce application which allows user to signup based on their msisdn.
  This application starts by landing on a splash screen  with animation and after 3 seconds it redirects to Adsplash screen.This screen has several addvertisements and when we close the adds it redirects itself to SignIn Activity.If the Credentials are created then we can login from this screen and if user is not registered we can navigate from this screen to Sign Up Activity.User has to enter information and if the user enter its information App sends the request to server.
  When the User Sign In it saves the password in shared preferences and then lands itself to the main screen which displays the Top sellers and new arrivals list.Both of these lists are populated from the webservice.This screen also have a search option and a Shopping cart item from which we can go to the Cart screen where we can see all the items that have been selected by the user.
  In Shopping Cart screen we can see selected items from where either we can view the products or we can checkout.The checkout option opens up a form where a user can enter his personal information like name address etc and the select the payment option as paypal.This app then uses paypal sdk for the payment.
  This application uses two major sdks
  
    Facebook sdk (for login)

    Paypal sdk(for payment)

  Now moving toward the drawer on main activity.This drwaer has various feature like
  
    logout(it removes your credentials and closes the session) 

    help(User sends email to liguanzhu390@gmail.com incase of any issues via form displayed.)

    Order history maintain the history of the order by the user.
  
    Profile (User can chage is password information using this feature)
    
    Categories (USer can select the category of the product he is interested in like electronics etc)
    
  
  
  
  
Application PROs
---------------------
  This application is well written and with proper segregation of code.
  It has some good use of fragments and easily manageable code.
  Seperate folders for beans,fragemnts and adapter to display dynamic data in lists.
  Animation of cart in the splash screen is pretty neat.
  Used Shared preferences.
  

Application Issues
------------------------

Security Issues
----------------
This application has many security concers few of them are listed below.
Passwords,emails ,msisdn has no client side validations.
password is not encryted.(atleast should be base 64 and save in hash over server)
password sharing over GET service which should be POST in order to avoid sniffing.
API data is availble to all and from browser no user validation is required.

Performance Issues
-------------------
Image display default minion icon before loading the actual images.I would recomment to use some apis like glide for showing images and using its features.
No proper response it case of unsuccessful login and singup.
No proper information displayed while payment via paypal.

HCI Issues
--------------
Signin page has camera icon which does nothing.
Clicking on forgot password is not working as it is a text view.
cant sign in because of return; in  signin activity

Best Practices
-----------------
Constants should be declared in s seperate constants file, where server main URL shouldnt be repeated.
API should have proper validations.
Code Reptition couldve been avoided.





















