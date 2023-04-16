# Setting-up-for-a-Mod2-IC

### Getting started with setting yourself up for a successful IC
  - ##### fork the repo and then git clone
  - ##### check gems
      if using ShouldaMatchers make sure that the following is included at the *bottom* of `rails_helper.rb`
        
          Shoulda::Matchers.configure.do |config|
            config.integrate do |with|
              with.test_framework :rspec
              
              with.library :rails
            end
          end
      
      if using Simplecov make sure that the following is included at the *top* of `rails_helper.rb`
      
          require 'simplecov'
            SimpleCov.start
  - ##### run bundle (bundle install) and possibly bundle update
  - ##### check read me here and follow for next steps
  - ##### review existing schemes.rb
      you may want to import schema to db.diagram if a visual is needed
  ### Table and Model Time!
      once you are clear on the tables that need to be made and the relationships they will have
      in the terminal run the following command:
      
      `rails generate model TableName attribute:datatype attribute:datatype othertable:references`
      
  - ##### To Note: 
    the many to many join table usually only needs references(foreign keys),
    it does not need attributes,
    parents do not need foreign keys
    
  
          
  
