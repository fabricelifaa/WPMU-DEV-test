# WPMU-DEV-test

<ol>
  <li>
    <pre>
       $results = $wpdb->get_results($wpdb->prepare( "SELECT * FROM $wpdb->postmeta WHERE meta_key = %s", $my_option_name) , ARRAY_N  );
    </pre>
  </li>
</ol>
