

This is the monolithic version of this demo. 
For the micro-services version, please see the microservices branch: https://github.com/Pivotal-Field-Engineering/PCF-demo/tree/micro-services

PCF Demo
=========

Push the application initially with no service bound.
Notice it will alert no RabbitMQ service is bound.. the link "Stream Data" will not work either.

Now, bind a RabbitMQ service. Re-push the app.
Click "Stream Data" and see the fun start. Click on a state to detail orders going throw it.

Additional fun: click "Kill App" and watch the application crashing.. it will show as "crashed" when you visualize events (cf events <app_name>). Health manager will automatically restart the app for you. => makes a good demo, too.

Branding: If you want a specific company logo and color for the header you can create a user-provided service with credentials 'color' and 'logo', and those values will ne used instead of the default ones (black and "Best Retailer, Inc") in the UI.
You can create this environment configuration using cf cups. Example:
    cf cups pcfdemo-config -p '{"logo":"http://sweregionb.org/wp_files/wp-content/uploads/2014/10/Honeywell-logo.jpg", "color":"red"}' 
