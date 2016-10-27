# Q0: Why is this error being thrown?
uninitialized constant HomeController::Pokemon"

Pokemon model/controller are not made/initialized


# Q1: How are the random Pokemon appearing? What is the common factor between all the possible Pokemon that appear? *

They are appearing based on a seed. it just populates the DB with pokemon, after one is "captures" it "spawns" the next.

Common Factor? The pokemon are the same 4 "pre-made" pokemon.

# Question 2a: What does the following line do "<%= button_to "Throw a Pokeball!", capture_path(id: @pokemon), :class => "button medium", :method => :patch %>"? Be specific about what "capture_path(id: @pokemon)" is doing. If you're having trouble, look at the Help section in the README.

It creates a button that allows for the capturing of Pokemon.
Capture_path calls the capture method in pokemon through a patch.
The pokemon caught is given by its pokemon ID.


# Question 3: What would you name your own Pokemon?

Robasaur

# Question 4: What did you pass into the redirect_to? If it is a path, what did that path need? If it is not a path, why is it okay not to have a path here?

redirects to trainers profile page:     
redirect_to trainer_path(id: @pokemon.trainer)
path needed the ID of the pokemon trainer.

# Question 5: Explain how putting this line "flash[:error] = @pokemon.errors.full_messages.to_sentence" shows error messages on your form.

This works because in views/layouts/application.html.erb, it is rendering something at the very end. Take a look at that file and see what it is doing

The very end part is:

<!-- <main role="main">
   <%= render 'layouts/messages' %>
   <%= yield %>
</main> -->

which redirects to _messages.html.erb

# Give us feedback on the project and decal below!

Awesome Project!

# Extra credit: Link your Heroku deployed app
https://intense-fjord-64275.herokuapp.com/
