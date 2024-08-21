End-Point Explanation:

I. USER AUTHENTICATION:

    /auth/sendRegisterMail --> Create the New User Data and send the registration link to activate account. [ 2- STEP VERIFICATION PURPOSE ] [ REQUIRED - firstname, lastname, email, password ]
    /auth/checkRegisterUser/:registerToken --> To confirm the registration and account activation.
    /auth/login --> To login the registered User after verifying the registered account. [ Required : email, password ]
    /auth/resetPass --> Verify user email and send password reset token with url. [ Required : email
    /auth/checkResetPass/:passResetToken --> Verify token and redirect to update password page.
    /auth/updatePass/:passResetToken --> Update new Password. [ Required : newPassword ]

II. URL ROUTES [ REQUIRED: BEARER TOKEN -- CREATE WHEN LOG-IN ]:

    /url/get --> Get all created Shorten URL's by Logged-In User.
    /url/create --> Create new Shorten URL.
    /url/redirect/:shortURL --> To increase the URL Click Count and redirect User to Actual URL.
    /url/delete/:UrlId --> To delete the URL by its ID.
