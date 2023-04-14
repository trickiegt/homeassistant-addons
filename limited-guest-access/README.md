Updated 4-14-2023
### What is this?

This add-on gives you the opportunity to give a guest user access
to certain home assistant devices. It works just like the view "services"
in developer tools in home assistant.

When a link is created and service calls added the guest user gets a button
in the user view (visit the link to view)

You can set a time frame to the actions, as well as make an action "one time use"

### How to use

First open the admin-interface (default port 8899),
click the "create new link" button

Select which service you want to make public and
enter the data that is required by the service (for example entity_id)

Within the valid time frame chosen when you created the action,
your guest can access the external_link/name_of_link 
(for example http://your-external-url.tld:8888/adf12345)
to be able to trigger the actions using a button.
-- These links are saved as json files and can be manually found/edited in /addons/limited-guest-access/data


### Inject code into user view

There are four custom entry points into the user view, that you 
can use these to modify the design of the end user page
- style.css
- script.js
- header.htm
- footer.htm

The first two are injected into the `<head>` section of the page, just above `</head>`
The two latter are injected into the `<body>` section, the first of which just after the opening tag,
and the footer just before closing the body.

To make use of this, you should create the files in the 
/share/limited-guest-access/ directory and adjust them to fit your needs.

### Install instructions

In home assistant, head to Supervisor -> add-on store 
and press the [...] menu, then click repositories and paste
`https://github.com/TekniskSupport/homeassistant-addons`

The add-on will now show up as a card along with the other add-ons

Hit install, then edit configuration value and hit start.

If you are unable to start the add-on make sure nothing else is running
on the selected ports.
