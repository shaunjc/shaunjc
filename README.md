G'Day, My name is Shaun.

I'm a PHP, HTML, SQL, Javascript and CSS developer who has experience with a large number of frameworks and APIs,
including WordPress, SilverStripe, jQuery and Bootstrap to name a few.

I like to format my code to match the framework I'm working with. For example, when developing WordPress themes
or plugins, I'll put spaces inside the opening and closing brackets of function definitions and calls, while if
I work on a custom SilverStripe module, I'll make sure I place the opening brackets for my class methods onto
new lines and define my arrays using square brackets.

My current long term project is a scalable series of classes and traits that can be combined to easily make WordPress
plugins or themes.

- When you define the `$_settings` property as a simple associative array, It'll automatically create a settings
page that displays a field for each key/value. These settings can then be read using magic getters or ArrayAccess.
- You can easily add actions, filters, shortcodes, ajax actions, cron tasks and rest enpoints by defining new methods.
- It comes with full support for customising the settings page, as well as hooking into the activation and
deactivation of itself, loading templates, and managing transients.

The following snippet is an example of how the class may behave.

      // Example class
      class Test extends BaseFramework {
        /**
         * This will create a settings page with a field labeled "Setting Name".
         */
        protected $_settings = array(
          'setting_name' => DEFAULT_VALUE, // This variable type will be enforced.
        );
        
        /**
         * All three of the following methods will create the same action.
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

I do have experience with Java, C, Pearl, Pascal and Basic, however I have not used any of them recently.
I'm currently in the process of learning how to use React.
