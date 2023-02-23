G'Day, My name is Shaun.

I'm a PHP, HTML, SQL, Javascript and CSS developer who has experience with a large number of frameworks and APIs,
including WordPress, SilverStripe, jQuery, React and Bootstrap to name a few.

I like to format my code to match the framework I'm working with. For example, when developing WordPress themes
or plugins, I'll put spaces inside the opening and closing brackets of function definitions and calls, while if
I work on a custom SilverStripe module, I'll make sure I place the opening brackets for my class methods onto
new lines and define my arrays using square brackets.

My current long term project is a scalable series of classes and traits that can be combined to easily make WordPress
plugins or themes with a myriad number of features. For example:

- When you define the `$_settings` property as a simple associative array, It'll automatically create a settings
page that displays a field for each key/value. These settings can then be read using magic getters or ArrayAccess.
- It comes with full support for customising the settings page, as well as hooking into the activation and
deactivation of itself, loading templates, and managing transients.
- You can easily add actions, filters, shortcodes, ajax actions, cron tasks and rest enpoints by defining new methods.

The following snippet is an example of how the class can be created.

      // Example class
      class Test extends BaseFramework {
        /**
         * This will create a settings page, found by going to Settings > Test, with a field labeled "Setting Name".
         */
        protected $_settings = array(
          'setting_name' => DEFAULT_VALUE, // This variable type will be enforced.
        );
        
        /**
         * All three of the following methods will hook into the same action with the same priority.
         * @action init
         * @priority 10
         * @arguments 1
         */
        public function _action_init{}
        public function _action_init_10{}
        public function _action_init_10_1{}
      }
      $test = Test::instance();
      $test->setting_name === $test['setting_name']; // True

I do have experience with Java, C, Pearl, Pascal and Basic, however I do not used any of them very frequently. Regardless, I'm able to pick up most programming languages without too much difficulty.
