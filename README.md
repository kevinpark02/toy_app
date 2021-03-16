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

## Exercises 3
1. (For readers who know CSS) Create a new micropost, then use your browser’s HTML inspector to determine the CSS id for the text “Micropost was successfully created.” What happens when you refresh your browser?
* CSS ID for "User was successfully created" is "notice"
* When refreshing the browser, the message disappears
2. Try to create a micropost with empty content and no user id.
* Allowed to create a micropost with empty content and no user id
3. Try to create a micropost with over 140 characters of content (say, the first paragraph from the Wikipedia article on Ruby).
* You can create a micropost with more than 140 characters
4. Destroy the microposts from the previous exercises.

## Exercises 4
1. Try to create a micropost with the same long content used in a previous exercise (Section 2.3.1.1). How has the behavior changed?
* There is an error message that prevents content longer than 140 characters to not be created
2. (For readers who know CSS) Use your browser’s HTML inspector to determine the CSS id of the error message produced by the previous exercise.
* css id is "error_explanation"

## Exercises 5
1. Edit the user show page to display the content of the user’s first micropost. (Use your technical sophistication (Box 1.2) to guess the syntax based on the other content in the file.) Confirm by visiting /users/1 that it worked.
* See show.html.erb in /views/users/
2. 