# Features and Pages

This covers all the visual and functional features of Glance. Starting from button presses to loading new pages. Basically, what the app does and delivers. 

## Installation

During installation, the app would have a custom installation window that is inlined with the design and themes of the app. The electron installer would be stripped down from the ground up, making it more simpler and modern.

The installation process should be as straight forward as ever: 
1.  Click on the **glance_setup.exe**.
2.  A small greeting for the user. There should be a button labeled **Terms & Agreements** which would get the user to the Terms & Agreements Page. And a **Next** or **Continue** button to proceed to the next process.
3.  After the welcome screen, the user should be able to select where to install the app on their drive. The default install is on the **C:/** drive.
4.  After selecting the installation path, the app should now be ready to install and can be initiated by clicking the **Install** button.
5.  After a successful installation, the installation window will show a **Installation was a Success!** message and a button labeled **Close** to exit the installer. There should also be a checkbox whether to start the app after closing the installer or not.

>   Fun illustrations are encouraged to make the installer and the app more appealing and modern. The installer window should be relatively close to the actual app window if possible.

## Launching the App

After a successful installtion, the can now be launched by searching **Glance** from the user's apps folder. Upon starting a splash screen of the Glance app's logo and name as a loading indicator or just startin the app, it should fade in and out of the scene.

### First Launch    
If the user is openning this app for the very first time, a different screen would show when the user launch the app. This would only appear one time during the app's first setup or as long as there is no user/account registered on the app.

This would feature a setup screen similar to when the user first install the windows OS:
1.  The very first thing a new user will see is a **Welcome Screen**. Showing a welcome message and an illustration. On the bottom left there should be a **Next** button to proceed to the next step of the setup.
2.  On the following step, the app asks the user **How will you be using Glance?** where the user picks what best fits their business operations.
    -   **Personal** - Great for managing the user's personal optical clinic.
    -   **Business/Team** - Great for larger enterprises where the clinic can have multiple branches and users.
3.  Next is the account creation, recovery, or linking.
    - **Personal** - During this set up the user can create an account or recover from a backup file.
        -   Creating an account would only need the user to enter their **Username**, **Email**, and **Password**.
        -   When recovering from a backup, the app needs the user to upload or import a back up file exported by the Glance app to restore the apps database and other essential things.
    -   **Business/Team** - On this set up, users can still create their own accounts or link up an already exisiting account. Two options are presented to the user whether the purpose is to create a **New Clinic Account** or link up an **Already exisiting Clinic Account**.
        -   If the user selects the **New Clinic Accoint**, creating an account is similar to a personal account registration where it would only need the user to enter their **Username**, **Email**, and **Password**.
        -   However, if the user selects **Aleardy Exisiting Clinic Account**, they need to follow a specific procedure:
            1.  After selecting the existing account options, a direction would be presented at the user asking to input their Supabase credentials. The input fields should be hidden and then scanned by the app to see if it's eligible for recovery. 

                Another case is for none Admin staffs, so they probably would not know the clinic's Supabase credentials (Unless it was given to them). What they can do is request for a QR code from the Admin for the Supabase credentials. This QR code is encrypted and can only be decrypted by the app. So the key is hardcoded (Shhh) that can only decrypt the QR code.

                To make it work since you it's hard to scan a QR code directly on a computer or a laptop without a camera. What the app can do is also show a QR code that a phone can scan to open up a simple webpage that activates the phones camera. This would be used to capture the QR code requested from the Admin, then after scanning the QR code, this gets sent to the app then process if this is a legit QR code and if the Supabase credentials are elegible for recovery.
            2.  After a successful linking, the user will get notified if they are connected from an exisiting database.
            3.  What happens afterwards is simply just the following app setup as the app already detects the database for your clinic, you basically just needs to log in.
4.  As for the final steps, the app set up ask the user for the themes they would like to use for the app. There are only two themes, **Light Mode** which is also the default mode and then there's **Dark Mode**.
5.  As for the final set up step, the app states their final greetings and welcomes you to use the Glance app as most of the basic configuration is now complete.

### How to Log in to your Glance account?
Now that the user has their own account either through a **New Clinic Account** or created for them by the **Admins** of their clinic. The user can continue to log in to their respective accounts. After the successfull initial set up, when you launch the Glance app again, the user will now only see the log in screen and not the entire initial set up screen. This goes consistent as long as there is a registered database and account for the app.

The log in process is as simple as any other Log in screen:
1.  It only requires the user to enter their **Username** and **Password** in the following fields.
2.  Then click the **Log in** button to contiue.
3.  Wait until it loads completely, then boom, the user is now logged in.

> Rate limiting is advised here to descourage multiple account log in request on a single moment on the same device. They would be disabled for 5 minutes if they reached 6 consecutive failed log in attempts.

### What if the user forgot their password?
Well eventually the user would input an incorrect password or completly forgot about them. Well there's still hope for them, they could try to recover their account through a password recovery method. 

They can recovery their account just only through the app itself:
1.  On the log in screen, there should be a button labeled **Forgot Password?**
2.  Clicking on the button would direct the user to a password recovery screen.
3.  There are two ways to identify the users account to the Glance app either by **Username** or **Email Address**.
4.  If one of those options is correct and have identified that an account is registered on the app's database, then it would send a 6-digit code to the users email inbox. This will be use to confirm that the user requesting for a password reset is the person itself.
5.  The user now copies the 6-digit code sent to them through their email and then they paste it on the 6-digit input field of the password recovery. This code would only last for about 5 minutes, any more than that will be unsable.
6.  If the 6-digit code is confirmed to be true then the app directs the user to the password reset screen where the user just needs to enter their new password and confirm it.
7.  Lastly, they can just copy their new password and continue to log in using their new password.

> Rate limiting is also advised here to descourage multiple account password request on a single moment on the same device. They would be disabled for 5 minutes if they reached 6 consecutive failed log in attempts.



