# ExcelDiff Workflow

This project provides a GitHub Actions workflow that automatically converts XLSX files to CSV format whenever changes are detected in a specified directory. It is designed to facilitate the management of Excel data in a more accessible format.

## Features

- Automatically triggers on changes to XLSX files in the specified directory.
- Converts the first worksheet of the XLSX file to a CSV file.
- Easy integration with GitHub workflows.

## Installation

1. Fork the repository.
2. Add the `.github/workflows/excel-diff.yml` file to your repository.
3. Ensure that the `tools/convert_xlsx_to_csv.py` script is in the correct path.
4. **Configure GitHub Token**: The workflow uses `GITHUB_TOKEN` which is automatically provided by GitHub Actions. However, you need to ensure that your repository has the correct permissions:
   - Go to your repository settings
   - Navigate to "Actions" → "General"
   - Under "Workflow permissions", ensure that "Read and write permissions" is selected
   - This allows the workflow to commit and push the generated CSV files back to your repository

## Usage

Once the workflow is set up, it will automatically run whenever an XLSX file in the specified directory is modified. The converted CSV files will be saved in the `data/csv` directory.

### Example

1. Make changes to an XLSX file in the `data/xlsx` directory.
2. Commit and push your changes to the repository.
3. The GitHub Actions workflow will trigger and convert the modified XLSX file to CSV.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
