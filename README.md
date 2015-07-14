# SCV PSR-2
Sublime Cool Version are configurations for Sublime Text 3 and PHP developers inspired in Laravel community. Include snippets for PSR-2 coding standard used by Laravel 5.1.

## Configurations
1. Clone this repo into Sublime Text Packages directory. **Preferences -> Browse Packages...**
2. Basic configuration
3. Packages
4. Snippets and Key Bindings
    4.1 Show/Hide line numbers

## 2. Basic configuration
Add this configuration

    // Line padding like Taylor Otwel
    "line_padding_bottom": 6,
    "line_padding_top": 6,

    // Set ruler to 80 characters
    "rulers":
    [
        80
    ],

    // Spaces better than tabs
    "translate_tabs_to_spaces": true,

into Preferences file **Preferences -> Settings-User**

    Packages/User/Preferences.sublime-settings


## 3. Packages
This is the list of useful packages for Sublime Text, you can install all of them via Package Control.

### 3.1 SideBarEnhancements 
This is the best sidebar for sublime text, includes many options missing in the original sidebar.

### 3.2 AdvancedNewFile 
Fast file creator typing the path and filename.

#### Configuration
Copy this code

    {
        "keys": ["super+n"], "command": "advanced_new_file_new"
    },

into

    Package/User/Default (linux).sublime-keymap 

and type **super + n** for launch the file creator box.

### 3.3 Dayle Rees Color Schemes
Huge [color scheme repository](https://daylerees.github.io/) for Sublime Text.

**Peacock** theme looks like Laravel website.

### 3.4 DocBlockr 
Easy PHP and JS documentation generator.

#### Configuration

Copy this file
    
    Packages/scv-psr2/User/Base File.sublime-settings 

into this folder

    Packages/User/

This configuration generates documentation like this:

    /**
     * [sendSmsMessage description]
     *
     * @param  SmsCourierInterface $courier
     * @param  [type] $message
     * @return [type]
     */
    public function sendSmsMessage(SmsCourierInterface $courier, $message)
    {
        $courier->sendMessage($this->phone_number, $message);

        return $this->sms()->create([
            'to' => $this->phone_number,
            'message' => $message;
        ]);     
    }

### 3.5 PHP Getters and Setters 
Getters and Setters generator


## 4. Snippets and Key Bindings

### 4.1 Show/Hide line numbers
Go to **Preferences -> Key Bindings - User** and add this code:

    {
        "keys": ["ctrl+shift+l"],
        "command": "toggle_setting",
        "args":
        {
            "setting": "line_numbers"
        }
    }

| Key binding | Description |
|----------|------|
| cc + tab | class |
| ci + tab | class implements |
| ce + tab | class extends |
| ct + tab | class extends TestCase (Laravel) |
| cp + tab | class extends PHPUnit_Framework_TestCase |
| _c + tab | construct |
| ii + tab | interface |
| tt + tab | trait |
| pubf + tab | public function |
| prof + tab | protected function |
| prif + tab | private function |
| ipubf + tab | inline public function definition |
| ctrl + shift + click | Go to class/method definition |
| ctrl + shift + l | Show/hide line numbers |
| phpn + tab | In a new php file, open php tag and namespace holder |

