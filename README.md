# WPMU-DEV-test

<ol>
  <li>
    <pre>
       $results = $wpdb->get_results($wpdb->prepare( "SELECT * FROM $wpdb->postmeta WHERE meta_key = %s", $my_option_name) , ARRAY_N  );
    </pre>
  </li>
  <li>
    it's missing `>` just after  "_e('Your name', 'test'); ?"
  </li>
  <li>
    <pre>
       echo _n( 'We have %s apples!', $apples, 'test' );
    </pre>
  </li>
  <li>
    it's not necessary to declare an array if it's to store only one variable inside it.
    <pre>
      update_option('my_option_key', isset( $_POST['option1'] ) ? sanitize_text_field($_POST['option1']) : "");
    </pre>
  </li>
  <li>
    YES if you remove the ARRAY_A.
  </li>
  <li>
    if stuff is a property of the object it could return true. for my part I use <pre>a.hasOwnProperty("stuff")</pre>
  </li>
  <li>
    Yes, if the first character of the parameter sent to the function is a string it may have a bug. 
  </li>
  <li>
    I can't find the error in this code.
  </li>
  <li>
    this code can be written in a single line
    <pre>
      $names = array_column($map, "name");
    </pre>
  </li>
  <li>
     It is necessary to avoid declaring variables uselessly in order to optimize php's resources.
    <pre>
       $path = '/test/dir1/'. str_replace( '\\', '/', 'subdir2\file.txt' );
    </pre>
  </li>
  <li>
    <pre>
      function my_admin_scripts_inclusion_proc ($hook_suffix) { 
        if("edit.php" == $hook_suffix){
          wp_enqueue_script('my-custom-posts-script', plugins_url( 'js/my-custom-posts-script.js',FILE ) ); 
        }
      }
      add_action('admin_enqueue_scripts', 'my_admin_scripts_inclusion_proc');
    </pre>
  </li>
</ol>
