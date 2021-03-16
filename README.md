# Toy App

## Exercises 1

1. (For readers who know CSS) Create a new user, then use your browser’s HTML inspector to determine the CSS id for the text “User was successfully created.” What happens when you refresh your browser?
* CSS ID for "User was successfully created" is "notice"
* When refreshing the browser, the message disappears
2. What happens if you try to create a user with a name but no email address?
* I am still able to create a new user without an email address
3. What happens if you try create a user with an invalid email address, like “@example.com”?
* I am still able to create a new user with an invalid email address
4. Destroy each of the users created in the previous exercises. Does Rails display a message by default when a user is destroyed?
* It displays the "Are you sure?" message, and once I click "OK", it deletes the specified user and the message "User was successfully destryoed" appears. 

## Exercises 2
1. By referring to Figure 2.12, write out the analogous steps for visiting the URL /users/1/edit.
* The browser issues a request for the users/1/edit
* Rails routes /users/1/edit to the edit action in the Users controller
* The edit action renders the edit view
* The view uses embedded Ruby to render the page as HTML
* The controller passes the HTML back to the browser
2. Find the line in the scaffolding code that retrieves the user from the database in the previous exercise. Hint: It’s in a special location called set_user.
```
    def set_user
      @user = User.find(params[:id])
    end
```
3. What is the name of the view file for the user edit page?
* edit.html.erb