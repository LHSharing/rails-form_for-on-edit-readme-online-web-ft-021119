
navigate
  shows the title on the show page in a h1 tag (FAILED - 1)
  to post pages (FAILED - 2)
  shows the description on the show page in a p tag (FAILED - 3)

form
  shows a new form that submits content and redirects and prints out params (FAILED - 4)
  shows a new form that submits content and redirects and prints out params (FAILED - 5)

Failures:

  1) navigate shows the title on the show page in a h1 tag
     Failure/Error: visit "/posts/#{@post.id}"
     
     ActionController::RoutingError:
       No route matches [GET] "/posts/1"
 
  2) navigate to post pages
     Failure/Error: visit "/posts/#{@post.id}"
     
     ActionController::RoutingError:
       No route matches [GET] "/posts/1"
 
  3) navigate shows the description on the show page in a p tag
     Failure/Error: visit "/posts/#{@post.id}"
     
     ActionController::RoutingError:
       No route matches [GET] "/posts/1"

  4) form shows a new form that submits content and redirects and prints out params
     Failure/Error: visit new_post_path
     
     NameError:
       undefined local variable or method `new_post_path' for #<RSpec::ExampleGroups::Form:0x00007f96480cf900>
       Did you mean?  new_polymorphic_path
     # ./spec/features/post_spec.rb:26:in `block (2 levels) in <top (required)>'

  5) form shows a new form that submits content and redirects and prints out params
     Failure/Error: visit edit_post_path(@post)
     
     NoMethodError:
       undefined method `edit_post_path' for #<RSpec::ExampleGroups::Form:0x00007f96480d7830>
       Did you mean?  edit_polymorphic_path
     # ./spec/features/post_spec.rb:39:in `block (2 levels) in <top (required)>'

Finished in 0.08287 seconds (files took 3.14 seconds to load)
5 examples, 5 failures

Failed examples:

rspec ./spec/features/post_spec.rb:8 # navigate shows the title on the show page in a h1 tag
rspec ./spec/features/post_spec.rb:13 # navigate to post pages
rspec ./spec/features/post_spec.rb:18 # navigate shows the description on the show page in a p tag
rspec ./spec/features/post_spec.rb:25 # form shows a new form that submits content and redirects and prints out params
rspec ./spec/features/post_spec.rb:36 # form shows a new form that submits content and redirects and prints out params