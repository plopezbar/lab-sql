![Ironhack logo](https://i.imgur.com/1QgrNNw.png)

# Lab | MySQL

## Introduction

As a data expert you work at a car dealership company which sells new cars of various brands and models. Your company is small and new but it has branches in several countries. Since the establishment of the company your colleagues have sold several cars to the customers. Now your boss realized your company imperatively needs a database to keep the records about the cars, salespersons, customers, and invoices and spare parts. Your boss trusts you very much so he assigned you the challenge to design, create, and manage the database.

## Challenge 1 - Design the Database

Using pen and paper (or computer software if you are skillful at creating digital diagrams), design a database to meet the minimal requirements of your boss. The minimal information to be recorded is described below:

1. **Cars** - e.g. the vehicle identification number (VIN), manufacturer, model, year, and color of the cars in your company's inventory.

1. **Customers** - e.g. the customer ID, name, phone number, email, address, city, state/province, country, and zip/postal code of the customers.

1. **Salespersons** - e.g. staff ID, name, and the store at your company.

1. **Invoices** - e.g. the invoice number, date, car, spare part, customer, and salesperson related to each car sale or spare part

1. **Spare parts** - e.g. the spare part id, manufacaturer, model, description


Before solving this challenge, review your lesson about database structure and design then ask yourself:

* **What entities and attributes should be included in the database?**
	* For each attribute, what data type is most suitable?
	* Also note that some attributes are required while other ones can be blank.

* **What are the relations between these entities? Which relations are one-to-one vs one-to-many vs many-to-many?**

Your end product of this challenge should look something like below, though it doesn't have to be that complicated:

![ERD](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/data-static/images/erd.png)

Take a picture with your phone and send the image to yourself. The image will be submitted as one of the deliverables.

## Challenge 2 - Create the Database and Tables

1. **Create a database for this lab.** 

	In BigQuery you will a 'dataset' called 'car_dealership'. You will create all tables under this.


1. **Now, based on the database design you created, write the SQL query to create the tables and columns.** You will be using the `CREATE TABLE` statement for which you can find reference [here](https://cloud.google.com/bigquery/docs/reference/standard-sql/data-definition-language).

	 Now split yourselves in pairs and decide which table you want to create. Each pair should create one table. Once you have created the table, go to the BigQuery interface and make sure that the table was created correctly. 

## Challenge 3 - Seeding the Database

The purpose of *database seeding* is to provide some dummy data for an empty database so that software development can be started based on the dummy data. In this challenge you will insert dummy data rows into the tables of your new database.

You'll be using the `INSERT INTO` statement for this purpose. You can some info [here](https://cloud.google.com/bigquery/docs/reference/standard-sql/dml-syntax).

For your convenience, we provide you some example dummy data. These dummy data may not readily work with your database depending on how you have designed your database. You may need to change them to the appropriate form. You should only insert data into the table you have created. 

### Cars

| VIN | Manufacturer | Model | Year | Color |
| --- | --- | --- | --- | --- |
| 3K096I98581DHSNUP | Volkswagen | Tiguan | 2019 | Blue |
| ZM8G7BEUQZ97IH46V | Peugeot | Rifter | 2019 | Red |
| RKXVNNIHLVVZOUB4M | Ford | Fusion | 2018 | White |
| HKNDGS7CU31E9Z7JW | Toyota | RAV4 | 2018 | Silver |
| DAM41UDN3CHU2WVF6 | Volvo | V60 | 2019 | Gray |
| DAM41UDN3CHU2WVF6 | Volvo | V60 Cross Country | 2019 | Gray |

### Customers

| Customer ID | Name | Phone | Email | Address | City | State/Province | Country | Postal |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 10001 | Pablo Picasso | +34 636 17 63 82 | - | Paseo de la Chopera, 14 | Madrid | Madrid | Spain | 28045 |
| 20001 | Abraham Lincoln | +1 305 907 7086 | - | 120 SW 8th St | Miami | Florida | United States | 33130 |
| 30001 | Napoléon Bonaparte | +33 1 79 75 40 00 | - | 40 Rue du Colisée | Paris | Île-de-France | France | 75008 |

### Salespersons

| Staff ID | Name | Store |
| --- | --- | --- |
| 00001 | Petey Cruiser | Madrid |
| 00002 | Anna Sthesia | Barcelona |
| 00003 | Paul Molive | Berlin |
| 00004 | Gail Forcewind | Paris |
| 00005 | Paige Turner | Mimia |
| 00006 | Bob Frapples | Mexico City |
| 00007 | Walter Melon | Amsterdam |
| 00008 | Shonda Leer | São Paulo |

### Invoices

| Invoice Number | Date | Car | Spare part | Customer | Sales Person |
| --- | --- | --- | --- | --- | --- |
| 852399038 | 22-08-2018 | 0 | 1 | 3 | 2 |
| 731166526 | 31-12-2018 | 3 | 0 |   | 1 |
| 271135104 | 22-01-2019 | 2 | 2 |   | 2 |

### Spare parts

| Spare part ID | Manufacturer | Model | Description 
| --- | --- | --- | --- | --- |
| 1 | Volkswagen | Tiguan | Left Back Door | 
| 2 | Peugeot | Rifter | 2019 | Left Mirror |
| 8 | Ford | Fusion | 2018 | Fridge |

## Bonus Challenge - Updating and Deleting Database Records

Now you find an error you need to fix in your existing data - in the Salespersons table, you mistakenly spelled *Miami* as *Mimia* for Paige Turner. Also, you received the email addresses of the three customers:

| Name | Email |
| --- | ---|
| Pablo Picasso | ppicasso@gmail.com |
| Abraham Lincoln | lincoln@us.gov |
| Napoléon Bonaparte | hello@napoleon.me |

Update those records. 

In addition, you also find a duplicated car entry for VIN `DAM41UDN3CHU2WVF6`. You want to delete car ID #4 from the database. 

You can some info [here](https://cloud.google.com/bigquery/docs/updating-data).

## Deliverables

- Your database structure design diagram in the form of image.

- Your notebook

