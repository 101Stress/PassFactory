# PassFactoryDev

## What is recommended:

1. **Clone the repository:**
   ```bash
   git clone xxx
   cd PassFactory/
   ```

2. **Set up aliases for convenience:**
   ```bash
   alias pf="'$(pwd)/passfactory' \$@"
   ```
### NAME
   PassFactory

### SYNOPSIS
   `pf [OPTION]`

### DESCRIPTION
   PassFactory is a versatile tool for generating passwords with customizable options.

### OPTIONS
   - `-h, --help`               Display this help message and exit.
   - `-L, --length <x>`         Choose the length of the generated password (default: 32).
   - `-l, --length-range <x:y>` Choose the range of the length of the generated password (default: 32).
   - `-s, --disable-symbols`    Disable symbols in the generated password (enabled by default).
   - `-n, --generate-n <n>`     Generate n passwords.
   - `-v, --verbose`            Implement verbose mode and enhance password strength estimation with entropy calculation.

Sure, here are some examples of how to use the `PassFactory` command:

1. **Generate a password with default settings:**
   ```bash
   pf
   ```

2. **Generate a password with a specified length (e.g., 16 characters):**
   ```bash
   pf -L 16
   ```

3. **Generate a password with a length range (e.g., between 12 and 20 characters):**
   ```bash
   pf -l 12:20
   ```

4. **Generate a password without symbols and copy it to clipboard:**
    
   Make sure you have xclip installed for this command to work properly.
   ```bash
   pf | tr -d '\n' | xclip -selection clipboard; 


5. **Combine options to customize the generated passwords (e.g., 10 passwords with a length range of 8 to 12 characters and symbols disabled):**
   ```bash
   pf -n 10 -l 8:12 -s 
   ```

6. **Generate 20 passwords with lengths between 5 and 40 characters, and it will display the generated passwords on the terminal.:**
   ```bash
   pf -v -l 5:40 -n 20
   ```
## To-Do:
- Provide an option to exclude specific characters.