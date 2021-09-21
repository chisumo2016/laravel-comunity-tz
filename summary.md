## DATABASE DESIGN
    # Tables 
     1. Users
        - id(int)
        -name(string)
        -email(string)
        -email_verify_at(datetime)
        -profile_photo_path(string)
        -provider_id(string)
        -created_at(datetime)
        -update_at(datetime)

     2. Categories
        - id(int)
        - user_id(bigInt)
        - name(string)
        - description(text)
        - created_at(datetime)
        - update_at(datetime)
        -$table->foreignId('user_id')->constrained();
         
    3. Posts
        - id(int)
        - user_id(bigInt)
        - category_id(bigInt)
        - title(string)
        - body(text)
        - thumnail(string)
        - comment_count(string)
        - visits(int)
        - best_comment_id(int)
        - created_at(datetime)
        - update_at(datetime)
         -$table->foreignId('user_id')->constrained();
         -$table->foreignId('category_id')->constrained();

    4. Comments
        - id(int)
        - user_id(bigInt)
        - post_id(bigInt)
        - description(text)
        - created_at(datetime)
        - update_at(datetime)
        -$table->foreignId('post_id')->constrained();
        -$table->foreignId('user_id')->constrained();

    5. Tags 
         - id(int)
        - name(string)

    7.  PostTags 
         - id(int)
        - tag_id(string)
        - post_id(string)
        - $table->foreignId('post_id')->index();
        - $table->foreignId('tag_id')->index();

    5. Events
        - id(int)
        - user_id(bigInt)
        - title(string)
        - description(text)
        - start_date(datetime)
        - end_date(datetime)
        - visits(int)
        - created_at(datetime)
        - update_at(datetime)
        -$table->foreignId('user_id')->constrained();

    6. Favorities
        - id(int)
        - user_id(bigInt)
        - favorated_id(int)
        - favorated_type(string)
        - created_at(datetime)
        - update_at(datetime)  
        - $table->foreignId('user_id')->constrained();

    7. Subscriptions
        - id(int)
        - category_id(bigint)
        - user_id(bigInt)
        - created_at(datetime)
        - update_at(datetime)
        - $table->foreignId('category_id')->constrained();
        - $table->foreignId('user_id')->constrained();

    7. Subscribers
        - id(int)
        - email(String)
        - created_at(datetime)
        - update_at(datetime)
    
    8. Testimonials
        - id(int)
        - name(String)
        - description(text)
        - created_at(datetime)
        - update_at(datetime)

     8. Newsletters
        - id(int)
        - user_id(bigInt)
        - slug(String)
        - title(String)
        - body(text)
        - thumnail(text)
        - created_at(datetime)
        - update_at(datetime)
        - $table->foreignId('user_id')->constrained();
   
 
