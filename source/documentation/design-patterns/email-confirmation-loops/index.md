## Email confirmation loops

This guide explains when and how to use an email confirmation loop to check that a user has access to a specific email account.


### When to use email confirmation loops

Avoid using email confirmation loops unless:

- critical functionality in the service is only available via email (for example, a password reset)
- accidentally using the wrong email address would give someone else access to sensitive information about another user

Email confirmation loops can be disruptive because they force users to switch from your service to their email account and back again.

They can mean users drop out because they:

- get confused
- don’t have access to their email account - or don’t have an email account
- don’t receive the confirmation email quickly
- don’t see the confirmation email (for example, because it goes to their spam folder)

You must design your service to reduce these issues for users.

Remember that confirmed emails don’t prove a person’s identity, just that they have access to that email address at the time they confirmed.


### If you use email confirmation loops

If you use email confirmation loops you should consider:

- any expiry conditions you set on the email link
- letting users resend their email
- using blocking or non-blocking loops (whether you want to let users use the service without confirming their email, or block their access until they do)
- the design of the ‘activate your account’ page


### Setting expiry conditions

You must set an expiry date on the email you send, so that the link can’t be used after a certain time period.

You should also set the link to expire when:

- it’s been used once
- it’s superseded by a new link
- the user has changed the email address on their account

If a user attempts to use an expired link or a link that’s already been used then you should tell them this.


### Letting users resend the email

You should let users resend the email confirmation link in case they entered the wrong email address previously or the email didn’t arrive for some other reason.


### Using blocking or non-blocking loops

There are 2 versions of the email confirmation loop, ‘blocking’ and ‘non-blocking’.

In a ‘blocking’ version, the user can’t use the service until they’ve confirmed their email address.

In the ‘non-blocking’ version, they can continue to use the service but will be reminded regularly that they need to confirm their email. Some functionality may not be available until they’ve done this.

Blocking loops have a slightly simpler flow, but if a user can’t complete the loop then they’re unable to use the service at all. It’s especially important that you send the emails instantly if you use blocking loops.

Non-blocking loops need more careful design because you can’t guarantee that all users will confirm their email. This could stop people from accessing your service.

Some services start users in a non-blocking loop initially and then change to a blocking loop.


### Designing the ‘activate your account’ page

This page should explain what the user needs to do to activate their account.

Typically, your service should show this page immediately after the user provides their email address or if they try to sign in before confirming their email.

The page should:

- show the user the email address that you sent their activation email to
- explain that they need to click the link in the email to proceed
- let them resend the activation email (to a different email address, if necessary)

For ‘blocking loops’ this should be the only page the user sees if they try to sign in before activating their account.

For ‘non-blocking loops’, if a user signs in before activating their account then you should:

- let them use the service
- remind them that they need to activate their account
- tell them where the activation email has been sent
- let them resend the activation email
- let them change their email address and confirm that instead

When a user clicks on the link in the activation email, send them to a page that confirms they’ve activated their account. You may or may not require them to sign in at this stage, depending on where in the flow the ‘activate your account’ screen appears.


### Discuss email confirmation loops

[Discuss email confirmation loops on the design patterns wiki](https://designpatterns.hackpad.com/Email-confirmation-loops-rJlwfm9N3QA).



