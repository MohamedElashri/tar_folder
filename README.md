# tar_folder

A convenient shell script to create tar archives with advanced options for file inclusion/exclusion, dry run, verbose output, and more.

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/MohamedElashri/tar_folder
   ```
2. Navigate to the cloned directory:
   ```
   cd tar_folder
   ```
3. Make the script executable:
   ```
   chmod +x tar_folder
   ```
4. Add the script to your system's PATH:
   ```
   sudo ln -s $(pwd)/tar_folder /usr/local/bin/tar_folder
   ```
   Alternatively, you can copy the script to a directory that is already in your PATH:
   ```
   sudo cp tar_folder /usr/local/bin/
   ```

## Usage

```
tar_folder <folder> [output_file] [options]
```

Options:
  - `--exclude=<patterns>`    Exclude files or directories matching the patterns (comma-separated)
  - `--include=<patterns>`    Include files or directories matching the patterns (comma-separated)
  - `--dry-run`, `-n`         Perform a dry run without creating the archive
  - `--verbose`, `-v`         Enable verbose output
  - `--quiet`, `-q`           Enable quiet mode (suppress non-essential output)
  - `--help`, `-h`            Show the help message
  - `--version`               Show the version information

## Examples

Create a tar archive of a folder:
```
tar_folder /path/to/folder
```

Create a tar archive with a specific output file name:
```
tar_folder /path/to/folder output.tar
```

Exclude files matching specific patterns:
```
tar_folder /path/to/folder --exclude="*.log,temp/"
```

Include only specific file patterns:
```
tar_folder /path/to/folder --include="*.txt,*.py"
```

Perform a dry run without creating the archive:
```
tar_folder /path/to/folder --dry-run
```

Enable verbose output:
```
tar_folder /path/to/folder --verbose
```

Enable quiet mode:
```
tar_folder /path/to/folder --quiet
```

Include only specific file types:
```
tar_folder /path/to/folder --include="*.py,*.js,*.tsx"
```

## Directory Structure

The `tar_folder` script includes a `dir_structure.txt` file in the generated tar archive, which contains the directory structure of the included files. The list of included files is also printed to the terminal output after a successful operation.

Example output:
```
Tar file created: output.tar
Files included:
├── src/app/layout.tsx
├── src/app/page.tsx
├── src/components/Header.tsx
├── src/styles/globals.css
Directory structure added to: dir_structure.txt (included in the tar file)
```

The `dir_structure.txt` file in the tar archive will contain:
```
Directory Structure:
-------------------
├── src/app/layout.tsx
├── src/app/page.tsx
├── src/components/Header.tsx
├── src/styles/globals.css
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


