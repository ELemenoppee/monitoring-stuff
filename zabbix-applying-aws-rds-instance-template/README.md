# Applying AWS RDS (PostgreSQL) Instance Template in Zabbix

This guide provides step-by-step instructions for applying an AWS RDS PostgreSQL instance template in Zabbix. This setup allows for effective monitoring of your RDS PostgreSQL instances, enabling you to track performance metrics and manage alerts efficiently.

## Prerequisites :-

+ Zabbix Server: A running Zabbix server instance with access to the Zabbix web interface.

+ AWS RDS PostgreSQL Instance: An existing RDS PostgreSQL instance that you want to monitor.

## Steps :- 

### Adding a Template

Access your Zabbix server

![alt text](images/image.png)

Click on "Data collection" and then select "Hosts".

![alt text](images/image-1.png)

Select the target host you want to monitor.

Click the "Select" button to choose a template.

![alt text](images/image-2.png)

Under the "Templates" group, select "AWS RDS Instance by HTTP" and click the "Select" button.

![alt text](images/image-3.png)

Go to the "Macros" section, then select "Inherited and host macros". Update the following macros as necessary:

+ {$AWS.ACCESS.KEY.ID}
+ {$AWS.REGION}
+ {$AWS.SECRET.ACCESS.KEY}
+ {$AWS.RDS.INSTANCE.ID}

![alt text](images/image-5.png)

Once you have made the necessary changes, save your updates by clicking the "Update" button.

![alt text](images/image-4.png)

### Adding a Dashboard Widget

Click on the Zabbix logo to return to the main dashboard, then select "Edit Dashboard".

![alt text](images/image-6.png)

Click the "+ Add" button and configure the widget settings as shown in the following images/image.

![alt text](images/image-7.png)

Configure the columns according to your requirements.

![alt text](images/image-8.png)

Set up the CPU utilization widget as needed.

![alt text](images/image-9.png)

Lastly, configure the connections widget.

![alt text](images/image-10.png)

Once everything is configured, click "Apply" to finalize your dashboard setup.
