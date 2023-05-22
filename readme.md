# Data Tables Example

This is an example HTML file that demonstrates the usage of the Data Tables library for displaying and manipulating tabular data.

## Prerequisites

Before using this example, make sure you have the following prerequisites:

- [jQuery library](https://jquery.com/) version 3.6.0 or later.
- [Data Tables library](https://datatables.net/) version 1.13.4 or later.
- Internet connection to load the required CSS and JavaScript files from CDNs.

## Usage

1. Include the necessary CSS and JavaScript files in the `<head>` section of your HTML file:

```html
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdn.datatables.net/1.13.4/css/jquery.dataTables.css" />
    <title>Data Tables example</title>
</head>
```

2. Create a table with the desired structure and populate it with data:

```html
<body>
    <table data-order='[[1, "desc"]]' id="myTable" class="display">
        <thead>
            <tr>
                <th>Column 1</th>
                <th>Column 2</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Row 1 Data 1</td>
                <td>05/18/2023</td>
            </tr>
            <tr>
                <td>05/04/2023</td>
                <td>05/14/2023</td>
            </tr>
        </tbody>
    </table>
```

3. At the bottom of your HTML file, just before the closing </body> tag, include the jQuery library and the Data Tables library, followed by the initialization script:

```html
 <!-- At first we have to call the jQuery library -->
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <!-- Then call the CDN Data Tables library -->
    <script src="https://cdn.datatables.net/1.13.4/js/jquery.dataTables.js"></script>
    <!-- Finally, add the script that filters and adds features to the data table -->
    <script>
        $(document).ready(function () {
            $('#myTable').DataTable({
                language: {
                    lengthMenu: "Mostrar _MENU_ registros por página",
                    zeroRecords: "No encontrado - lo siento",
                    info: "Mostrando página _PAGE_ de _PAGES_",
                    infoEmpty: "No se encontró información",
                    infoFiltered: "(filtrado de _MAX_ total registros)",
                    paginate: {
                        "first": "Primero",
                        "last": "Último",
                        "next": "Siguiente",
                        "previous": "Anterior"
                    },
                },
                searching: false,
            });
        });
    </script>
```
