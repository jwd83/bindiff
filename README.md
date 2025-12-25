# Binary Diff Tool

A simple web-based binary diff tool for comparing files byte-by-byte.

## Why I Built This

I created this tool while comparing different VBIOS (Video BIOS) files. I needed a quick way to see exactly which bytes differed between versions, particularly at the bit level. Existing tools were either too complex for quick comparisons or didn't clearly show which specific bits had changed within each byte.

This tool runs entirely in the browser—no server needed—making it fast and secure for comparing any binary files.

## Features

- **Side-by-side binary comparison**: Compare any two files byte-by-byte
- **Bit-level highlighting**: See exactly which bits differ within each byte (highlighted in red)
- **Dual display format**: Shows differences in both hexadecimal and binary
- **Address tracking**: Each difference shows its hexadecimal address
- **Limit to 1000 differences**: Prevents browser overload with large, very different files
- **Client-side only**: Files never leave your browser—privacy-focused and secure

## How to Use

1. Open `index.html` in any modern web browser
2. Select the first file to compare (File A)
3. Select the second file to compare (File B)
4. Click "Diff Files"
5. View the results in a table showing:
   - Address (hexadecimal)
   - File A byte value (hex)
   - File B byte value (hex)
   - File A byte value (binary with bit differences highlighted)
   - File B byte value (binary with bit differences highlighted)

## Example Use Cases

- Comparing VBIOS versions (the original use case)
- Analyzing firmware updates
- Debugging binary file changes
- Reverse engineering file format modifications
- Validating file integrity after transfers

## Technical Details

- Pure HTML/CSS/JavaScript—no dependencies
- Uses the File API to read files in the browser
- Processes up to 1,000 differences to maintain performance
- Shows bit-level differences within bytes for precise analysis

## License

Feel free to use and modify as needed.
