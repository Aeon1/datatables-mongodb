# datatables-mongodb
server side mongoDB(datatables)

you can use this file to show collection in datatables

# example to use:

<p>you can use the file <b>datatables_mongodb.json</b> to load a colection example</p>

# create a simple table with headers
<table id="example" class="display" style="width:100%">
        <thead>
            <tr>
                <th>CAMPO 1</th>
                <th>CAMPO 2</th>
                <th>CAMPO 3</th>
                <th>CAMPO 4</th>
                <th>CAMPO 5</th>
            </tr>
        </thead>
    </table>

# how to call the dates similar how server side processing mysql, postgresql:

    $('#example').DataTable( {
        "processing": true,
        "serverSide": true,
        "ajax": {
            "url": "./server_processing_mongodb.php",
            "dataType": "jsonp",
        },
    //indicate the names of fields how apeart in mongo collection
    "columns": [
            { "data": "campo_1"},
            { "data": "campo_2"},
            { "data": "campo_3"},
            { "data": "campo_4"},
            { "data": "campo_5"}
        ]});

is important to indicate the columns with the name the fields in te collection, you can use data or name to indicate them
