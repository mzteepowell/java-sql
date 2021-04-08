# Java SQL

A student that completes this project shows that they can:

* Query data from a single table
* Query data from multiple tables
* Create a new database using PostgreSQL

## Introduction

Working with SQL

## Instructions

Reimport the Northwind database into PostgreSQL using pgAdmin. This is the same data we used during the guided project. You can find a copy of the SQL script under the `assets` folder in this repository.

* [ ] ***pgAdmin data refresh***

* Select the northwind database created during the guided project.

* Tools -> Query Tool
  * Open file northwind.sql (you used this script during the guided project)
  * Execute

* Look under
  * northwind -> Schemas -> public -> tables

* Clear query windows

### Answer the following data queries. Keep track of the SQL you write by pasting it into this document under its appropriate header below in the provided SQL code block. You will be submitting that through the regular fork, change, pull process

* [ ] ***find all customers that live in London. Returns 6 records***

  <details><summary>hint</summary>

  * This can be done with SELECT and WHERE clauses
  </details>

```SQL
"AROUT"	"Around the Horn"	"Thomas Hardy"	"Sales Representative"	"120 Hanover Sq."	"London"		"WA1 1DP"	"UK"	"(171) 555-7788"	"(171) 555-6750"
"BSBEV"	"B's Beverages"	"Victoria Ashworth"	"Sales Representative"	"Fauntleroy Circus"	"London"		"EC2 5NT"	"UK"	"(171) 555-1212"	
"CONSH"	"Consolidated Holdings"	"Elizabeth Brown"	"Sales Representative"	"Berkeley Gardens 12  Brewery"	"London"		"WX1 6LT"	"UK"	"(171) 555-2282"	"(171) 555-9199"
"EASTC"	"Eastern Connection"	"Ann Devon"	"Sales Agent"	"35 King George"	"London"		"WX3 6FW"	"UK"	"(171) 555-0297"	"(171) 555-3373"
"NORTS"	"North/South"	"Simon Crowther"	"Sales Associate"	"South House 300 Queensbridge"	"London"		"SW7 1RZ"	"UK"	"(171) 555-7733"	"(171) 555-2530"
"SEVES"	"Seven Seas Imports"	"Hari Kumar"	"Sales Manager"	"90 Wadhurst Rd."	"London"		"OX15 4NB"	"UK"	"(171) 555-1717"	"(171) 555-5646"
```

* [ ] ***find all customers with postal code 1010. Returns 3 customers***

  <details><summary>hint</summary>

  * This can be done with SELECT and WHERE clauses
  </details>

```SQL
"CACTU"	"Cactus Comidas para llevar"	"Patricio Simpson"	"Sales Agent"	"Cerrito 333"	"Buenos Aires"		"1010"	"Argentina"	"(1) 135-5555"	"(1) 135-4892"
"OCEAN"	"Océano Atlántico Ltda."	"Yvonne Moncada"	"Sales Agent"	"Ing. Gustavo Moncada 8585 Piso 20-A"	"Buenos Aires"		"1010"	"Argentina"	"(1) 135-5333"	"(1) 135-5535"
"RANCH"	"Rancho grande"	"Sergio Gutiérrez"	"Sales Representative"	"Av. del Libertador 900"	"Buenos Aires"		"1010"	"Argentina"	"(1) 123-5555"	"(1) 123-5556"
```

* [ ] ***find the phone number for the supplier with the id 11. Should be (010) 9984510***

  <details><summary>hint</summary>

  * This can be done with SELECT and WHERE clauses
  </details>

```SQL
"(010) 9984510"
```

* [ ] ***list orders descending by the order date. The order with date 1998-05-06 should be at the top***

  <details><summary>hint</summary>

  * This can be done with SELECT, WHERE, and ORDER BY clauses
  </details>

```SQL
"order_id"	"customer_id"	"employee_id"	"order_date"	"required_date"	"shipped_date"	"ship_via"	"freight"	"ship_name"	"ship_address"	"ship_city"	"ship_region"	"ship_postal_code"	"ship_country"
11074	"SIMOB"	7	"1998-05-06"	"1998-06-03"		2	18.44	"Simons bistro"	"Vinbæltet 34"	"Kobenhavn"		"1734"	"Denmark"
11077	"RATTC"	1	"1998-05-06"	"1998-06-03"		2	8.53	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
11076	"BONAP"	4	"1998-05-06"	"1998-06-03"		2	38.28	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
11075	"RICSU"	8	"1998-05-06"	"1998-06-03"		2	6.19	"Richter Supermarkt"	"Starenweg 5"	"Genève"		"1204"	"Switzerland"
11071	"LILAS"	1	"1998-05-05"	"1998-06-02"		1	0.93	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
11073	"PERIC"	2	"1998-05-05"	"1998-06-02"		2	24.95	"Pericles Comidas clásicas"	"Calle Dr. Jorge Cash 321"	"México D.F."		"05033"	"Mexico"
11072	"ERNSH"	4	"1998-05-05"	"1998-06-02"		2	258.64	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
11070	"LEHMS"	2	"1998-05-05"	"1998-06-02"		1	136	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
11068	"QUEEN"	8	"1998-05-04"	"1998-06-01"		2	81.75	"Queen Cozinha"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"
11069	"TORTU"	1	"1998-05-04"	"1998-06-01"	"1998-05-06"	2	15.67	"Tortuga Restaurante"	"Avda. Azteca 123"	"México D.F."		"05033"	"Mexico"
11067	"DRACD"	1	"1998-05-04"	"1998-05-18"	"1998-05-06"	2	7.98	"Drachenblut Delikatessen"	"Walserweg 21"	"Aachen"		"52066"	"Germany"
11065	"LILAS"	8	"1998-05-01"	"1998-05-29"		1	12.91	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
11066	"WHITC"	7	"1998-05-01"	"1998-05-29"	"1998-05-04"	2	44.72	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
11064	"SAVEA"	1	"1998-05-01"	"1998-05-29"	"1998-05-04"	1	30.09	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
11061	"GREAL"	4	"1998-04-30"	"1998-06-11"		3	14.01	"Great Lakes Food Market"	"2732 Baker Blvd."	"Eugene"	"OR"	"97403"	"USA"
11063	"HUNGO"	3	"1998-04-30"	"1998-05-28"	"1998-05-06"	2	81.73	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
11062	"REGGC"	4	"1998-04-30"	"1998-05-28"		2	29.93	"Reggiani Caseifici"	"Strada Provinciale 124"	"Reggio Emilia"		"42100"	"Italy"
11060	"FRANS"	2	"1998-04-30"	"1998-05-28"	"1998-05-04"	2	10.98	"Franchi S.p.A."	"Via Monte Bianco 34"	"Torino"		"10100"	"Italy"
11058	"BLAUS"	9	"1998-04-29"	"1998-05-27"		3	31.14	"Blauer See Delikatessen"	"Forsterstr. 57"	"Mannheim"		"68306"	"Germany"
11059	"RICAR"	2	"1998-04-29"	"1998-06-10"		2	85.8	"Ricardo Adocicados"	"Av. Copacabana, 267"	"Rio de Janeiro"	"RJ"	"02389-890"	"Brazil"
11057	"NORTS"	3	"1998-04-29"	"1998-05-27"	"1998-05-01"	3	4.13	"North/South"	"South House 300 Queensbridge"	"London"		"SW7 1RZ"	"UK"
11054	"CACTU"	8	"1998-04-28"	"1998-05-26"		1	0.33	"Cactus Comidas para llevar"	"Cerrito 333"	"Buenos Aires"		"1010"	"Argentina"
11056	"EASTC"	8	"1998-04-28"	"1998-05-12"	"1998-05-01"	2	278.96	"Eastern Connection"	"35 King George"	"London"		"WX3 6FW"	"UK"
11055	"HILAA"	7	"1998-04-28"	"1998-05-26"	"1998-05-05"	2	120.92	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
11051	"LAMAI"	7	"1998-04-27"	"1998-05-25"		3	2.79	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
11053	"PICCO"	2	"1998-04-27"	"1998-05-25"	"1998-04-29"	2	53.05	"Piccolo und mehr"	"Geislweg 14"	"Salzburg"		"5020"	"Austria"
11052	"HANAR"	3	"1998-04-27"	"1998-05-25"	"1998-05-01"	1	67.26	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
11050	"FOLKO"	8	"1998-04-27"	"1998-05-25"	"1998-05-05"	2	59.41	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
11048	"BOTTM"	7	"1998-04-24"	"1998-05-22"	"1998-04-30"	3	24.12	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
11049	"GOURL"	3	"1998-04-24"	"1998-05-22"	"1998-05-04"	1	8.34	"Gourmet Lanchonetes"	"Av. Brasil, 442"	"Campinas"	"SP"	"04876-786"	"Brazil"
11047	"EASTC"	7	"1998-04-24"	"1998-05-22"	"1998-05-01"	3	46.62	"Eastern Connection"	"35 King George"	"London"		"WX3 6FW"	"UK"
11045	"BOTTM"	6	"1998-04-23"	"1998-05-21"		2	70.58	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
11046	"WANDK"	8	"1998-04-23"	"1998-05-21"	"1998-04-24"	2	71.64	"Die Wandernde Kuh"	"Adenauerallee 900"	"Stuttgart"		"70563"	"Germany"
11044	"WOLZA"	4	"1998-04-23"	"1998-05-21"	"1998-05-01"	1	8.72	"Wolski Zajazd"	"ul. Filtrowa 68"	"Warszawa"		"01-012"	"Poland"
11041	"CHOPS"	3	"1998-04-22"	"1998-05-20"	"1998-04-28"	2	48.22	"Chop-suey Chinese"	"Hauptstr. 31"	"Bern"		"3012"	"Switzerland"
11043	"SPECD"	5	"1998-04-22"	"1998-05-20"	"1998-04-29"	2	8.8	"Spécialités du monde"	"25, rue Lauriston"	"Paris"		"75016"	"France"
11042	"COMMI"	2	"1998-04-22"	"1998-05-06"	"1998-05-01"	1	29.99	"Comércio Mineiro"	"Av. dos Lusíadas, 23"	"Sao Paulo"	"SP"	"05432-043"	"Brazil"
11040	"GREAL"	4	"1998-04-22"	"1998-05-20"		3	18.84	"Great Lakes Food Market"	"2732 Baker Blvd."	"Eugene"	"OR"	"97403"	"USA"
11038	"SUPRD"	1	"1998-04-21"	"1998-05-19"	"1998-04-30"	2	29.59	"Suprêmes délices"	"Boulevard Tirou, 255"	"Charleroi"		"B-6000"	"Belgium"
11039	"LINOD"	1	"1998-04-21"	"1998-05-19"		2	65	"LINO-Delicateses"	"Ave. 5 de Mayo Porlamar"	"I. de Margarita"	"Nueva Esparta"	"4980"	"Venezuela"
11037	"GODOS"	7	"1998-04-21"	"1998-05-19"	"1998-04-27"	1	3.2	"Godos Cocina Típica"	"C/ Romero, 33"	"Sevilla"		"41101"	"Spain"
11035	"SUPRD"	2	"1998-04-20"	"1998-05-18"	"1998-04-24"	2	0.17	"Suprêmes délices"	"Boulevard Tirou, 255"	"Charleroi"		"B-6000"	"Belgium"
11036	"DRACD"	8	"1998-04-20"	"1998-05-18"	"1998-04-22"	3	149.47	"Drachenblut Delikatessen"	"Walserweg 21"	"Aachen"		"52066"	"Germany"
11034	"OLDWO"	8	"1998-04-20"	"1998-06-01"	"1998-04-27"	1	40.32	"Old World Delicatessen"	"2743 Bering St."	"Anchorage"	"AK"	"99508"	"USA"
11031	"SAVEA"	6	"1998-04-17"	"1998-05-15"	"1998-04-24"	2	227.22	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
11033	"RICSU"	7	"1998-04-17"	"1998-05-15"	"1998-04-23"	3	84.74	"Richter Supermarkt"	"Starenweg 5"	"Genève"		"1204"	"Switzerland"
11032	"WHITC"	2	"1998-04-17"	"1998-05-15"	"1998-04-23"	3	606.19	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
11030	"SAVEA"	7	"1998-04-17"	"1998-05-15"	"1998-04-27"	2	830.75	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
11028	"KOENE"	2	"1998-04-16"	"1998-05-14"	"1998-04-22"	1	29.59	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
11029	"CHOPS"	4	"1998-04-16"	"1998-05-14"	"1998-04-27"	1	47.84	"Chop-suey Chinese"	"Hauptstr. 31"	"Bern"		"3012"	"Switzerland"
11027	"BOTTM"	1	"1998-04-16"	"1998-05-14"	"1998-04-20"	1	52.52	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
11024	"EASTC"	4	"1998-04-15"	"1998-05-13"	"1998-04-20"	1	74.36	"Eastern Connection"	"35 King George"	"London"		"WX3 6FW"	"UK"
11026	"FRANS"	4	"1998-04-15"	"1998-05-13"	"1998-04-28"	1	47.09	"Franchi S.p.A."	"Via Monte Bianco 34"	"Torino"		"10100"	"Italy"
11025	"WARTH"	6	"1998-04-15"	"1998-05-13"	"1998-04-24"	3	29.17	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
11020	"OTTIK"	2	"1998-04-14"	"1998-05-12"	"1998-04-16"	2	43.3	"Ottilies Käseladen"	"Mehrheimerstr. 369"	"Köln"		"50739"	"Germany"
11023	"BSBEV"	1	"1998-04-14"	"1998-04-28"	"1998-04-24"	2	123.83	"B's Beverages"	"Fauntleroy Circus"	"London"		"EC2 5NT"	"UK"
11022	"HANAR"	9	"1998-04-14"	"1998-05-12"	"1998-05-04"	2	6.27	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
11021	"QUICK"	3	"1998-04-14"	"1998-05-12"	"1998-04-21"	1	297.18	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
11018	"LONEP"	4	"1998-04-13"	"1998-05-11"	"1998-04-16"	2	11.65	"Lonesome Pine Restaurant"	"89 Chiaroscuro Rd."	"Portland"	"OR"	"97219"	"USA"
11019	"RANCH"	6	"1998-04-13"	"1998-05-11"		3	3.17	"Rancho grande"	"Av. del Libertador 900"	"Buenos Aires"		"1010"	"Argentina"
11017	"ERNSH"	9	"1998-04-13"	"1998-05-11"	"1998-04-20"	2	754.26	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
11015	"SANTG"	2	"1998-04-10"	"1998-04-24"	"1998-04-20"	2	4.62	"Santé Gourmet"	"Erling Skakkes gate 78"	"Stavern"		"4110"	"Norway"
11016	"AROUT"	9	"1998-04-10"	"1998-05-08"	"1998-04-13"	2	33.8	"Around the Horn"	"Brook Farm Stratford St. Mary"	"Colchester"	"Essex"	"CO7 6JX"	"UK"
11014	"LINOD"	2	"1998-04-10"	"1998-05-08"	"1998-04-15"	3	23.6	"LINO-Delicateses"	"Ave. 5 de Mayo Porlamar"	"I. de Margarita"	"Nueva Esparta"	"4980"	"Venezuela"
11011	"ALFKI"	3	"1998-04-09"	"1998-05-07"	"1998-04-13"	1	1.21	"Alfred's Futterkiste"	"Obere Str. 57"	"Berlin"		"12209"	"Germany"
11013	"ROMEY"	2	"1998-04-09"	"1998-05-07"	"1998-04-10"	1	32.99	"Romero y tomillo"	"Gran Vía, 1"	"Madrid"		"28001"	"Spain"
11012	"FRANK"	1	"1998-04-09"	"1998-04-23"	"1998-04-17"	3	242.95	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
11010	"REGGC"	2	"1998-04-09"	"1998-05-07"	"1998-04-21"	2	28.71	"Reggiani Caseifici"	"Strada Provinciale 124"	"Reggio Emilia"		"42100"	"Italy"
11008	"ERNSH"	7	"1998-04-08"	"1998-05-06"		3	79.46	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
11009	"GODOS"	2	"1998-04-08"	"1998-05-06"	"1998-04-10"	1	59.11	"Godos Cocina Típica"	"C/ Romero, 33"	"Sevilla"		"41101"	"Spain"
11007	"PRINI"	8	"1998-04-08"	"1998-05-06"	"1998-04-13"	2	202.24	"Princesa Isabel Vinhos"	"Estrada da saúde n. 58"	"Lisboa"		"1756"	"Portugal"
11005	"WILMK"	2	"1998-04-07"	"1998-05-05"	"1998-04-10"	1	0.75	"Wilman Kala"	"Keskuskatu 45"	"Helsinki"		"21240"	"Finland"
11006	"GREAL"	3	"1998-04-07"	"1998-05-05"	"1998-04-15"	2	25.19	"Great Lakes Food Market"	"2732 Baker Blvd."	"Eugene"	"OR"	"97403"	"USA"
11004	"MAISD"	3	"1998-04-07"	"1998-05-05"	"1998-04-20"	1	44.84	"Maison Dewey"	"Rue Joseph-Bens 532"	"Bruxelles"		"B-1180"	"Belgium"
11002	"SAVEA"	4	"1998-04-06"	"1998-05-04"	"1998-04-16"	1	141.16	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
11003	"THECR"	3	"1998-04-06"	"1998-05-04"	"1998-04-08"	3	14.91	"The Cracker Box"	"55 Grizzly Peak Rd."	"Butte"	"MT"	"59801"	"USA"
11001	"FOLKO"	2	"1998-04-06"	"1998-05-04"	"1998-04-14"	2	197.3	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
11000	"RATTC"	2	"1998-04-06"	"1998-05-04"	"1998-04-14"	3	55.12	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10999	"OTTIK"	6	"1998-04-03"	"1998-05-01"	"1998-04-10"	2	96.35	"Ottilies Käseladen"	"Mehrheimerstr. 369"	"Köln"		"50739"	"Germany"
10998	"WOLZA"	8	"1998-04-03"	"1998-04-17"	"1998-04-17"	2	20.31	"Wolski Zajazd"	"ul. Filtrowa 68"	"Warszawa"		"01-012"	"Poland"
10997	"LILAS"	8	"1998-04-03"	"1998-05-15"	"1998-04-13"	2	73.91	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
10994	"VAFFE"	2	"1998-04-02"	"1998-04-16"	"1998-04-09"	3	65.53	"Vaffeljernet"	"Smagsloget 45"	"Århus"		"8200"	"Denmark"
10996	"QUICK"	4	"1998-04-02"	"1998-04-30"	"1998-04-10"	2	1.12	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10995	"PERIC"	1	"1998-04-02"	"1998-04-30"	"1998-04-06"	3	46	"Pericles Comidas clásicas"	"Calle Dr. Jorge Cash 321"	"México D.F."		"05033"	"Mexico"
10991	"QUICK"	1	"1998-04-01"	"1998-04-29"	"1998-04-07"	1	38.51	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10993	"FOLKO"	7	"1998-04-01"	"1998-04-29"	"1998-04-10"	3	8.81	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10992	"THEBI"	1	"1998-04-01"	"1998-04-29"	"1998-04-03"	3	4.27	"The Big Cheese"	"89 Jefferson Way Suite 2"	"Portland"	"OR"	"97201"	"USA"
10990	"ERNSH"	2	"1998-04-01"	"1998-05-13"	"1998-04-07"	3	117.61	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10988	"RATTC"	3	"1998-03-31"	"1998-04-28"	"1998-04-10"	2	61.14	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10989	"QUEDE"	2	"1998-03-31"	"1998-04-28"	"1998-04-02"	1	34.76	"Que Delícia"	"Rua da Panificadora, 12"	"Rio de Janeiro"	"RJ"	"02389-673"	"Brazil"
10987	"EASTC"	8	"1998-03-31"	"1998-04-28"	"1998-04-06"	1	185.48	"Eastern Connection"	"35 King George"	"London"		"WX3 6FW"	"UK"
10985	"HUNGO"	2	"1998-03-30"	"1998-04-27"	"1998-04-02"	1	91.51	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10986	"OCEAN"	8	"1998-03-30"	"1998-04-27"	"1998-04-21"	2	217.86	"Océano Atlántico Ltda."	"Ing. Gustavo Moncada 8585 Piso 20-A"	"Buenos Aires"		"1010"	"Argentina"
10984	"SAVEA"	1	"1998-03-30"	"1998-04-27"	"1998-04-03"	3	211.22	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10981	"HANAR"	1	"1998-03-27"	"1998-04-24"	"1998-04-02"	2	193.37	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
10983	"SAVEA"	2	"1998-03-27"	"1998-04-24"	"1998-04-06"	2	657.54	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10982	"BOTTM"	2	"1998-03-27"	"1998-04-24"	"1998-04-08"	1	14.01	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
10980	"FOLKO"	4	"1998-03-27"	"1998-05-08"	"1998-04-17"	1	1.26	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10979	"ERNSH"	8	"1998-03-26"	"1998-04-23"	"1998-03-31"	2	353.07	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10978	"MAISD"	9	"1998-03-26"	"1998-04-23"	"1998-04-23"	2	32.82	"Maison Dewey"	"Rue Joseph-Bens 532"	"Bruxelles"		"B-1180"	"Belgium"
10977	"FOLKO"	8	"1998-03-26"	"1998-04-23"	"1998-04-10"	3	208.5	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10976	"HILAA"	1	"1998-03-25"	"1998-05-06"	"1998-04-03"	1	37.97	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10975	"BOTTM"	1	"1998-03-25"	"1998-04-22"	"1998-03-27"	3	32.27	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
10974	"SPLIR"	3	"1998-03-25"	"1998-04-08"	"1998-04-03"	3	12.96	"Split Rail Beer & Ale"	"P.O. Box 555"	"Lander"	"WY"	"82520"	"USA"
10971	"FRANR"	2	"1998-03-24"	"1998-04-21"	"1998-04-02"	2	121.82	"France restauration"	"54, rue Royale"	"Nantes"		"44000"	"France"
10973	"LACOR"	6	"1998-03-24"	"1998-04-21"	"1998-03-27"	2	15.17	"La corne d'abondance"	"67, avenue de l'Europe"	"Versailles"		"78000"	"France"
10972	"LACOR"	4	"1998-03-24"	"1998-04-21"	"1998-03-26"	2	0.02	"La corne d'abondance"	"67, avenue de l'Europe"	"Versailles"		"78000"	"France"
10970	"BOLID"	9	"1998-03-24"	"1998-04-07"	"1998-04-24"	1	16.16	"Bólido Comidas preparadas"	"C/ Araquil, 67"	"Madrid"		"28023"	"Spain"
10968	"ERNSH"	1	"1998-03-23"	"1998-04-20"	"1998-04-01"	3	74.6	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10969	"COMMI"	1	"1998-03-23"	"1998-04-20"	"1998-03-30"	2	0.21	"Comércio Mineiro"	"Av. dos Lusíadas, 23"	"Sao Paulo"	"SP"	"05432-043"	"Brazil"
10967	"TOMSP"	2	"1998-03-23"	"1998-04-20"	"1998-04-02"	2	62.22	"Toms Spezialitäten"	"Luisenstr. 48"	"Münster"		"44087"	"Germany"
10965	"OLDWO"	6	"1998-03-20"	"1998-04-17"	"1998-03-30"	3	144.38	"Old World Delicatessen"	"2743 Bering St."	"Anchorage"	"AK"	"99508"	"USA"
10966	"CHOPS"	4	"1998-03-20"	"1998-04-17"	"1998-04-08"	1	27.19	"Chop-suey Chinese"	"Hauptstr. 31"	"Bern"		"3012"	"Switzerland"
10964	"SPECD"	3	"1998-03-20"	"1998-04-17"	"1998-03-24"	2	87.38	"Spécialités du monde"	"25, rue Lauriston"	"Paris"		"75016"	"France"
10961	"QUEEN"	8	"1998-03-19"	"1998-04-16"	"1998-03-30"	1	104.47	"Queen Cozinha"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"
10963	"FURIB"	9	"1998-03-19"	"1998-04-16"	"1998-03-26"	3	2.7	"Furia Bacalhau e Frutos do Mar"	"Jardim das rosas n. 32"	"Lisboa"		"1675"	"Portugal"
10962	"QUICK"	8	"1998-03-19"	"1998-04-16"	"1998-03-23"	2	275.79	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10960	"HILAA"	3	"1998-03-19"	"1998-04-02"	"1998-04-08"	1	2.08	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10958	"OCEAN"	7	"1998-03-18"	"1998-04-15"	"1998-03-27"	2	49.56	"Océano Atlántico Ltda."	"Ing. Gustavo Moncada 8585 Piso 20-A"	"Buenos Aires"		"1010"	"Argentina"
10959	"GOURL"	6	"1998-03-18"	"1998-04-29"	"1998-03-23"	2	4.98	"Gourmet Lanchonetes"	"Av. Brasil, 442"	"Campinas"	"SP"	"04876-786"	"Brazil"
10957	"HILAA"	8	"1998-03-18"	"1998-04-15"	"1998-03-27"	3	105.36	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10955	"FOLKO"	8	"1998-03-17"	"1998-04-14"	"1998-03-20"	2	3.26	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10956	"BLAUS"	6	"1998-03-17"	"1998-04-28"	"1998-03-20"	2	44.65	"Blauer See Delikatessen"	"Forsterstr. 57"	"Mannheim"		"68306"	"Germany"
10954	"LINOD"	5	"1998-03-17"	"1998-04-28"	"1998-03-20"	1	27.91	"LINO-Delicateses"	"Ave. 5 de Mayo Porlamar"	"I. de Margarita"	"Nueva Esparta"	"4980"	"Venezuela"
10951	"RICSU"	9	"1998-03-16"	"1998-04-27"	"1998-04-07"	2	30.85	"Richter Supermarkt"	"Starenweg 5"	"Genève"		"1204"	"Switzerland"
10953	"AROUT"	9	"1998-03-16"	"1998-03-30"	"1998-03-25"	2	23.72	"Around the Horn"	"Brook Farm Stratford St. Mary"	"Colchester"	"Essex"	"CO7 6JX"	"UK"
10952	"ALFKI"	1	"1998-03-16"	"1998-04-27"	"1998-03-24"	1	40.42	"Alfred's Futterkiste"	"Obere Str. 57"	"Berlin"		"12209"	"Germany"
10950	"MAGAA"	1	"1998-03-16"	"1998-04-13"	"1998-03-23"	2	2.5	"Magazzini Alimentari Riuniti"	"Via Ludovico il Moro 22"	"Bergamo"		"24100"	"Italy"
10949	"BOTTM"	2	"1998-03-13"	"1998-04-10"	"1998-03-17"	3	74.44	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
10948	"GODOS"	3	"1998-03-13"	"1998-04-10"	"1998-03-19"	3	23.39	"Godos Cocina Típica"	"C/ Romero, 33"	"Sevilla"		"41101"	"Spain"
10947	"BSBEV"	3	"1998-03-13"	"1998-04-10"	"1998-03-16"	2	3.26	"B's Beverages"	"Fauntleroy Circus"	"London"		"EC2 5NT"	"UK"
10944	"BOTTM"	6	"1998-03-12"	"1998-03-26"	"1998-03-13"	3	52.92	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
10946	"VAFFE"	1	"1998-03-12"	"1998-04-09"	"1998-03-19"	2	27.2	"Vaffeljernet"	"Smagsloget 45"	"Århus"		"8200"	"Denmark"
10945	"MORGK"	4	"1998-03-12"	"1998-04-09"	"1998-03-18"	1	10.22	"Morgenstern Gesundkost"	"Heerstr. 22"	"Leipzig"		"04179"	"Germany"
10941	"SAVEA"	7	"1998-03-11"	"1998-04-08"	"1998-03-20"	2	400.81	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10943	"BSBEV"	4	"1998-03-11"	"1998-04-08"	"1998-03-19"	2	2.17	"B's Beverages"	"Fauntleroy Circus"	"London"		"EC2 5NT"	"UK"
10942	"REGGC"	9	"1998-03-11"	"1998-04-08"	"1998-03-18"	3	17.95	"Reggiani Caseifici"	"Strada Provinciale 124"	"Reggio Emilia"		"42100"	"Italy"
10940	"BONAP"	8	"1998-03-11"	"1998-04-08"	"1998-03-23"	3	19.77	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10938	"QUICK"	3	"1998-03-10"	"1998-04-07"	"1998-03-16"	2	31.89	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10939	"MAGAA"	2	"1998-03-10"	"1998-04-07"	"1998-03-13"	2	76.33	"Magazzini Alimentari Riuniti"	"Via Ludovico il Moro 22"	"Bergamo"		"24100"	"Italy"
10937	"CACTU"	7	"1998-03-10"	"1998-03-24"	"1998-03-13"	3	31.51	"Cactus Comidas para llevar"	"Cerrito 333"	"Buenos Aires"		"1010"	"Argentina"
10935	"WELLI"	4	"1998-03-09"	"1998-04-06"	"1998-03-18"	3	47.59	"Wellington Importadora"	"Rua do Mercado, 12"	"Resende"	"SP"	"08737-363"	"Brazil"
10936	"GREAL"	3	"1998-03-09"	"1998-04-06"	"1998-03-18"	2	33.68	"Great Lakes Food Market"	"2732 Baker Blvd."	"Eugene"	"OR"	"97403"	"USA"
10934	"LEHMS"	3	"1998-03-09"	"1998-04-06"	"1998-03-12"	3	32.01	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10931	"RICSU"	4	"1998-03-06"	"1998-03-20"	"1998-03-19"	2	13.6	"Richter Supermarkt"	"Starenweg 5"	"Genève"		"1204"	"Switzerland"
10933	"ISLAT"	6	"1998-03-06"	"1998-04-03"	"1998-03-16"	3	54.15	"Island Trading"	"Garden House Crowther Way"	"Cowes"	"Isle of Wight"	"PO31 7PJ"	"UK"
10932	"BONAP"	8	"1998-03-06"	"1998-04-03"	"1998-03-24"	1	134.64	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10930	"SUPRD"	4	"1998-03-06"	"1998-04-17"	"1998-03-18"	3	15.55	"Suprêmes délices"	"Boulevard Tirou, 255"	"Charleroi"		"B-6000"	"Belgium"
10927	"LACOR"	4	"1998-03-05"	"1998-04-02"	"1998-04-08"	1	19.79	"La corne d'abondance"	"67, avenue de l'Europe"	"Versailles"		"78000"	"France"
10929	"FRANK"	6	"1998-03-05"	"1998-04-02"	"1998-03-12"	1	33.93	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10928	"GALED"	1	"1998-03-05"	"1998-04-02"	"1998-03-18"	1	1.36	"Galería del gastronómo"	"Rambla de Cataluña, 23"	"Barcelona"		"8022"	"Spain"
10924	"BERGS"	3	"1998-03-04"	"1998-04-01"	"1998-04-08"	2	151.52	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10926	"ANATR"	4	"1998-03-04"	"1998-04-01"	"1998-03-11"	3	39.92	"Ana Trujillo Emparedados y helados"	"Avda. de la Constitución 2222"	"México D.F."		"05021"	"Mexico"
10925	"HANAR"	3	"1998-03-04"	"1998-04-01"	"1998-03-13"	1	2.27	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
10921	"VAFFE"	1	"1998-03-03"	"1998-04-14"	"1998-03-09"	1	176.48	"Vaffeljernet"	"Smagsloget 45"	"Århus"		"8200"	"Denmark"
10923	"LAMAI"	7	"1998-03-03"	"1998-04-14"	"1998-03-13"	3	68.26	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
10922	"HANAR"	5	"1998-03-03"	"1998-03-31"	"1998-03-05"	3	62.74	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
10920	"AROUT"	4	"1998-03-03"	"1998-03-31"	"1998-03-09"	2	29.61	"Around the Horn"	"Brook Farm Stratford St. Mary"	"Colchester"	"Essex"	"CO7 6JX"	"UK"
10918	"BOTTM"	3	"1998-03-02"	"1998-03-30"	"1998-03-11"	3	48.83	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
10919	"LINOD"	2	"1998-03-02"	"1998-03-30"	"1998-03-04"	2	19.8	"LINO-Delicateses"	"Ave. 5 de Mayo Porlamar"	"I. de Margarita"	"Nueva Esparta"	"4980"	"Venezuela"
10917	"ROMEY"	4	"1998-03-02"	"1998-03-30"	"1998-03-11"	2	8.29	"Romero y tomillo"	"Gran Vía, 1"	"Madrid"		"28001"	"Spain"
10915	"TORTU"	2	"1998-02-27"	"1998-03-27"	"1998-03-02"	2	3.51	"Tortuga Restaurante"	"Avda. Azteca 123"	"México D.F."		"05033"	"Mexico"
10916	"RANCH"	1	"1998-02-27"	"1998-03-27"	"1998-03-09"	2	63.77	"Rancho grande"	"Av. del Libertador 900"	"Buenos Aires"		"1010"	"Argentina"
10914	"QUEEN"	6	"1998-02-27"	"1998-03-27"	"1998-03-02"	1	21.19	"Queen Cozinha"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"
10909	"SANTG"	1	"1998-02-26"	"1998-03-26"	"1998-03-10"	2	53.05	"Santé Gourmet"	"Erling Skakkes gate 78"	"Stavern"		"4110"	"Norway"
10913	"QUEEN"	4	"1998-02-26"	"1998-03-26"	"1998-03-04"	1	33.05	"Queen Cozinha"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"
10912	"HUNGO"	2	"1998-02-26"	"1998-03-26"	"1998-03-18"	2	580.91	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10911	"GODOS"	3	"1998-02-26"	"1998-03-26"	"1998-03-05"	1	38.19	"Godos Cocina Típica"	"C/ Romero, 33"	"Sevilla"		"41101"	"Spain"
10910	"WILMK"	1	"1998-02-26"	"1998-03-26"	"1998-03-04"	3	38.11	"Wilman Kala"	"Keskuskatu 45"	"Helsinki"		"21240"	"Finland"
10908	"REGGC"	4	"1998-02-26"	"1998-03-26"	"1998-03-06"	2	32.96	"Reggiani Caseifici"	"Strada Provinciale 124"	"Reggio Emilia"		"42100"	"Italy"
10907	"SPECD"	6	"1998-02-25"	"1998-03-25"	"1998-02-27"	3	9.19	"Spécialités du monde"	"25, rue Lauriston"	"Paris"		"75016"	"France"
10906	"WOLZA"	4	"1998-02-25"	"1998-03-11"	"1998-03-03"	3	26.29	"Wolski Zajazd"	"ul. Filtrowa 68"	"Warszawa"		"01-012"	"Poland"
10904	"WHITC"	3	"1998-02-24"	"1998-03-24"	"1998-02-27"	3	162.95	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
10905	"WELLI"	9	"1998-02-24"	"1998-03-24"	"1998-03-06"	2	13.72	"Wellington Importadora"	"Rua do Mercado, 12"	"Resende"	"SP"	"08737-363"	"Brazil"
10903	"HANAR"	3	"1998-02-24"	"1998-03-24"	"1998-03-04"	3	36.71	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
10902	"FOLKO"	1	"1998-02-23"	"1998-03-23"	"1998-03-03"	1	44.15	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10901	"HILAA"	4	"1998-02-23"	"1998-03-23"	"1998-02-26"	1	62.09	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10899	"LILAS"	5	"1998-02-20"	"1998-03-20"	"1998-02-26"	3	1.21	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
10900	"WELLI"	1	"1998-02-20"	"1998-03-20"	"1998-03-04"	2	1.66	"Wellington Importadora"	"Rua do Mercado, 12"	"Resende"	"SP"	"08737-363"	"Brazil"
10898	"OCEAN"	4	"1998-02-20"	"1998-03-20"	"1998-03-06"	2	1.27	"Océano Atlántico Ltda."	"Ing. Gustavo Moncada 8585 Piso 20-A"	"Buenos Aires"		"1010"	"Argentina"
10896	"MAISD"	7	"1998-02-19"	"1998-03-19"	"1998-02-27"	3	32.45	"Maison Dewey"	"Rue Joseph-Bens 532"	"Bruxelles"		"B-1180"	"Belgium"
10897	"HUNGO"	3	"1998-02-19"	"1998-03-19"	"1998-02-25"	2	603.54	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10895	"ERNSH"	3	"1998-02-18"	"1998-03-18"	"1998-02-23"	1	162.75	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10894	"SAVEA"	1	"1998-02-18"	"1998-03-18"	"1998-02-20"	1	116.13	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10893	"KOENE"	9	"1998-02-18"	"1998-03-18"	"1998-02-20"	2	77.78	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
10891	"LEHMS"	7	"1998-02-17"	"1998-03-17"	"1998-02-19"	2	20.37	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10892	"MAISD"	4	"1998-02-17"	"1998-03-17"	"1998-02-19"	2	120.27	"Maison Dewey"	"Rue Joseph-Bens 532"	"Bruxelles"		"B-1180"	"Belgium"
10889	"RATTC"	9	"1998-02-16"	"1998-03-16"	"1998-02-23"	3	280.61	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10890	"DUMON"	7	"1998-02-16"	"1998-03-16"	"1998-02-18"	1	32.76	"Du monde entier"	"67, rue des Cinquante Otages"	"Nantes"		"44000"	"France"
10888	"GODOS"	1	"1998-02-16"	"1998-03-16"	"1998-02-23"	2	51.87	"Godos Cocina Típica"	"C/ Romero, 33"	"Sevilla"		"41101"	"Spain"
10887	"GALED"	8	"1998-02-13"	"1998-03-13"	"1998-02-16"	3	1.25	"Galería del gastronómo"	"Rambla de Cataluña, 23"	"Barcelona"		"8022"	"Spain"
10886	"HANAR"	1	"1998-02-13"	"1998-03-13"	"1998-03-02"	1	4.99	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
10884	"LETSS"	4	"1998-02-12"	"1998-03-12"	"1998-02-13"	2	90.97	"Let's Stop N Shop"	"87 Polk St. Suite 5"	"San Francisco"	"CA"	"94117"	"USA"
10885	"SUPRD"	6	"1998-02-12"	"1998-03-12"	"1998-02-18"	3	5.64	"Suprêmes délices"	"Boulevard Tirou, 255"	"Charleroi"		"B-6000"	"Belgium"
10883	"LONEP"	8	"1998-02-12"	"1998-03-12"	"1998-02-20"	3	0.53	"Lonesome Pine Restaurant"	"89 Chiaroscuro Rd."	"Portland"	"OR"	"97219"	"USA"
10882	"SAVEA"	4	"1998-02-11"	"1998-03-11"	"1998-02-20"	3	23.1	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10881	"CACTU"	4	"1998-02-11"	"1998-03-11"	"1998-02-18"	1	2.84	"Cactus Comidas para llevar"	"Cerrito 333"	"Buenos Aires"		"1010"	"Argentina"
10879	"WILMK"	3	"1998-02-10"	"1998-03-10"	"1998-02-12"	3	8.5	"Wilman Kala"	"Keskuskatu 45"	"Helsinki"		"21240"	"Finland"
10880	"FOLKO"	7	"1998-02-10"	"1998-03-24"	"1998-02-18"	1	88.01	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10878	"QUICK"	4	"1998-02-10"	"1998-03-10"	"1998-02-12"	1	46.69	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10877	"RICAR"	1	"1998-02-09"	"1998-03-09"	"1998-02-19"	1	38.06	"Ricardo Adocicados"	"Av. Copacabana, 267"	"Rio de Janeiro"	"RJ"	"02389-890"	"Brazil"
10876	"BONAP"	7	"1998-02-09"	"1998-03-09"	"1998-02-12"	3	60.42	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10874	"GODOS"	5	"1998-02-06"	"1998-03-06"	"1998-02-11"	2	19.58	"Godos Cocina Típica"	"C/ Romero, 33"	"Sevilla"		"41101"	"Spain"
10873	"WILMK"	4	"1998-02-06"	"1998-03-06"	"1998-02-09"	1	0.82	"Wilman Kala"	"Keskuskatu 45"	"Helsinki"		"21240"	"Finland"
10875	"BERGS"	4	"1998-02-06"	"1998-03-06"	"1998-03-03"	2	32.37	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10872	"GODOS"	5	"1998-02-05"	"1998-03-05"	"1998-02-09"	2	175.32	"Godos Cocina Típica"	"C/ Romero, 33"	"Sevilla"		"41101"	"Spain"
10871	"BONAP"	9	"1998-02-05"	"1998-03-05"	"1998-02-10"	2	112.27	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10870	"WOLZA"	5	"1998-02-04"	"1998-03-04"	"1998-02-13"	3	12.04	"Wolski Zajazd"	"ul. Filtrowa 68"	"Warszawa"		"01-012"	"Poland"
10869	"SEVES"	5	"1998-02-04"	"1998-03-04"	"1998-02-09"	1	143.28	"Seven Seas Imports"	"90 Wadhurst Rd."	"London"		"OX15 4NB"	"UK"
10868	"QUEEN"	7	"1998-02-04"	"1998-03-04"	"1998-02-23"	2	191.27	"Queen Cozinha"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"
10866	"BERGS"	5	"1998-02-03"	"1998-03-03"	"1998-02-12"	1	109.11	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10867	"LONEP"	6	"1998-02-03"	"1998-03-17"	"1998-02-11"	1	1.93	"Lonesome Pine Restaurant"	"89 Chiaroscuro Rd."	"Portland"	"OR"	"97219"	"USA"
10864	"AROUT"	4	"1998-02-02"	"1998-03-02"	"1998-02-09"	2	3.04	"Around the Horn"	"Brook Farm Stratford St. Mary"	"Colchester"	"Essex"	"CO7 6JX"	"UK"
10865	"QUICK"	2	"1998-02-02"	"1998-02-16"	"1998-02-12"	1	348.14	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10863	"HILAA"	4	"1998-02-02"	"1998-03-02"	"1998-02-17"	2	30.26	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10862	"LEHMS"	8	"1998-01-30"	"1998-03-13"	"1998-02-02"	2	53.23	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10861	"WHITC"	4	"1998-01-30"	"1998-02-27"	"1998-02-17"	2	14.93	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
10859	"FRANK"	1	"1998-01-29"	"1998-02-26"	"1998-02-02"	2	76.1	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10860	"FRANR"	3	"1998-01-29"	"1998-02-26"	"1998-02-04"	3	19.26	"France restauration"	"54, rue Royale"	"Nantes"		"44000"	"France"
10858	"LACOR"	2	"1998-01-29"	"1998-02-26"	"1998-02-03"	1	52.51	"La corne d'abondance"	"67, avenue de l'Europe"	"Versailles"		"78000"	"France"
10857	"BERGS"	8	"1998-01-28"	"1998-02-25"	"1998-02-06"	2	188.85	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10856	"ANTON"	3	"1998-01-28"	"1998-02-25"	"1998-02-10"	2	58.43	"Antonio Moreno Taquería"	"Mataderos  2312"	"México D.F."		"05023"	"Mexico"
10854	"ERNSH"	3	"1998-01-27"	"1998-02-24"	"1998-02-05"	2	100.22	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10855	"OLDWO"	3	"1998-01-27"	"1998-02-24"	"1998-02-04"	1	170.97	"Old World Delicatessen"	"2743 Bering St."	"Anchorage"	"AK"	"99508"	"USA"
10853	"BLAUS"	9	"1998-01-27"	"1998-02-24"	"1998-02-03"	2	53.83	"Blauer See Delikatessen"	"Forsterstr. 57"	"Mannheim"		"68306"	"Germany"
10852	"RATTC"	8	"1998-01-26"	"1998-02-09"	"1998-01-30"	1	174.05	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10851	"RICAR"	5	"1998-01-26"	"1998-02-23"	"1998-02-02"	1	160.55	"Ricardo Adocicados"	"Av. Copacabana, 267"	"Rio de Janeiro"	"RJ"	"02389-890"	"Brazil"
10849	"KOENE"	9	"1998-01-23"	"1998-02-20"	"1998-01-30"	2	0.56	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
10850	"VICTE"	1	"1998-01-23"	"1998-03-06"	"1998-01-30"	1	49.19	"Victuailles en stock"	"2, rue du Commerce"	"Lyon"		"69004"	"France"
10848	"CONSH"	7	"1998-01-23"	"1998-02-20"	"1998-01-29"	2	38.24	"Consolidated Holdings"	"Berkeley Gardens 12  Brewery"	"London"		"WX1 6LT"	"UK"
10847	"SAVEA"	4	"1998-01-22"	"1998-02-05"	"1998-02-10"	3	487.57	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10846	"SUPRD"	2	"1998-01-22"	"1998-03-05"	"1998-01-23"	3	56.46	"Suprêmes délices"	"Boulevard Tirou, 255"	"Charleroi"		"B-6000"	"Belgium"
10845	"QUICK"	8	"1998-01-21"	"1998-02-04"	"1998-01-30"	1	212.98	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10844	"PICCO"	8	"1998-01-21"	"1998-02-18"	"1998-01-26"	2	25.22	"Piccolo und mehr"	"Geislweg 14"	"Salzburg"		"5020"	"Austria"
10843	"VICTE"	4	"1998-01-21"	"1998-02-18"	"1998-01-26"	2	9.26	"Victuailles en stock"	"2, rue du Commerce"	"Lyon"		"69004"	"France"
10841	"SUPRD"	5	"1998-01-20"	"1998-02-17"	"1998-01-29"	2	424.3	"Suprêmes délices"	"Boulevard Tirou, 255"	"Charleroi"		"B-6000"	"Belgium"
10842	"TORTU"	1	"1998-01-20"	"1998-02-17"	"1998-01-29"	3	54.42	"Tortuga Restaurante"	"Avda. Azteca 123"	"México D.F."		"05033"	"Mexico"
10839	"TRADH"	3	"1998-01-19"	"1998-02-16"	"1998-01-22"	3	35.43	"Tradiçao Hipermercados"	"Av. Inês de Castro, 414"	"Sao Paulo"	"SP"	"05634-030"	"Brazil"
10840	"LINOD"	4	"1998-01-19"	"1998-03-02"	"1998-02-16"	2	2.71	"LINO-Delicateses"	"Ave. 5 de Mayo Porlamar"	"I. de Margarita"	"Nueva Esparta"	"4980"	"Venezuela"
10838	"LINOD"	3	"1998-01-19"	"1998-02-16"	"1998-01-23"	3	59.28	"LINO-Delicateses"	"Ave. 5 de Mayo Porlamar"	"I. de Margarita"	"Nueva Esparta"	"4980"	"Venezuela"
10837	"BERGS"	9	"1998-01-16"	"1998-02-13"	"1998-01-23"	3	13.32	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10836	"ERNSH"	7	"1998-01-16"	"1998-02-13"	"1998-01-21"	1	411.88	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10834	"TRADH"	1	"1998-01-15"	"1998-02-12"	"1998-01-19"	3	29.78	"Tradiçao Hipermercados"	"Av. Inês de Castro, 414"	"Sao Paulo"	"SP"	"05634-030"	"Brazil"
10835	"ALFKI"	1	"1998-01-15"	"1998-02-12"	"1998-01-21"	3	69.53	"Alfred's Futterkiste"	"Obere Str. 57"	"Berlin"		"12209"	"Germany"
10833	"OTTIK"	6	"1998-01-15"	"1998-02-12"	"1998-01-23"	2	71.49	"Ottilies Käseladen"	"Mehrheimerstr. 369"	"Köln"		"50739"	"Germany"
10832	"LAMAI"	2	"1998-01-14"	"1998-02-11"	"1998-01-19"	2	43.26	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
10831	"SANTG"	3	"1998-01-14"	"1998-02-11"	"1998-01-23"	2	72.19	"Santé Gourmet"	"Erling Skakkes gate 78"	"Stavern"		"4110"	"Norway"
10829	"ISLAT"	9	"1998-01-13"	"1998-02-10"	"1998-01-23"	1	154.72	"Island Trading"	"Garden House Crowther Way"	"Cowes"	"Isle of Wight"	"PO31 7PJ"	"UK"
10830	"TRADH"	4	"1998-01-13"	"1998-02-24"	"1998-01-21"	2	81.83	"Tradiçao Hipermercados"	"Av. Inês de Castro, 414"	"Sao Paulo"	"SP"	"05634-030"	"Brazil"
10828	"RANCH"	9	"1998-01-13"	"1998-01-27"	"1998-02-04"	1	90.85	"Rancho grande"	"Av. del Libertador 900"	"Buenos Aires"		"1010"	"Argentina"
10827	"BONAP"	1	"1998-01-12"	"1998-01-26"	"1998-02-06"	2	63.54	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10826	"BLONP"	6	"1998-01-12"	"1998-02-09"	"1998-02-06"	1	7.09	"Blondel père et fils"	"24, place Kléber"	"Strasbourg"		"67000"	"France"
10823	"LILAS"	5	"1998-01-09"	"1998-02-06"	"1998-01-13"	2	163.97	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
10825	"DRACD"	1	"1998-01-09"	"1998-02-06"	"1998-01-14"	1	79.25	"Drachenblut Delikatessen"	"Walserweg 21"	"Aachen"		"52066"	"Germany"
10824	"FOLKO"	8	"1998-01-09"	"1998-02-06"	"1998-01-30"	1	1.23	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10821	"SPLIR"	1	"1998-01-08"	"1998-02-05"	"1998-01-15"	1	36.68	"Split Rail Beer & Ale"	"P.O. Box 555"	"Lander"	"WY"	"82520"	"USA"
10822	"TRAIH"	6	"1998-01-08"	"1998-02-05"	"1998-01-16"	3	7	"Trail's Head Gourmet Provisioners"	"722 DaVinci Blvd."	"Kirkland"	"WA"	"98034"	"USA"
10820	"RATTC"	3	"1998-01-07"	"1998-02-04"	"1998-01-13"	2	37.52	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10819	"CACTU"	2	"1998-01-07"	"1998-02-04"	"1998-01-16"	3	19.76	"Cactus Comidas para llevar"	"Cerrito 333"	"Buenos Aires"		"1010"	"Argentina"
10818	"MAGAA"	7	"1998-01-07"	"1998-02-04"	"1998-01-12"	3	65.48	"Magazzini Alimentari Riuniti"	"Via Ludovico il Moro 22"	"Bergamo"		"24100"	"Italy"
10816	"GREAL"	4	"1998-01-06"	"1998-02-03"	"1998-02-04"	2	719.78	"Great Lakes Food Market"	"2732 Baker Blvd."	"Eugene"	"OR"	"97403"	"USA"
10817	"KOENE"	3	"1998-01-06"	"1998-01-20"	"1998-01-13"	2	306.07	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
10814	"VICTE"	3	"1998-01-05"	"1998-02-02"	"1998-01-14"	3	130.94	"Victuailles en stock"	"2, rue du Commerce"	"Lyon"		"69004"	"France"
10815	"SAVEA"	2	"1998-01-05"	"1998-02-02"	"1998-01-14"	3	14.62	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10813	"RICAR"	1	"1998-01-05"	"1998-02-02"	"1998-01-09"	1	47.38	"Ricardo Adocicados"	"Av. Copacabana, 267"	"Rio de Janeiro"	"RJ"	"02389-890"	"Brazil"
10812	"REGGC"	5	"1998-01-02"	"1998-01-30"	"1998-01-12"	1	59.78	"Reggiani Caseifici"	"Strada Provinciale 124"	"Reggio Emilia"		"42100"	"Italy"
10811	"LINOD"	8	"1998-01-02"	"1998-01-30"	"1998-01-08"	1	31.22	"LINO-Delicateses"	"Ave. 5 de Mayo Porlamar"	"I. de Margarita"	"Nueva Esparta"	"4980"	"Venezuela"
10809	"WELLI"	7	"1998-01-01"	"1998-01-29"	"1998-01-07"	1	4.87	"Wellington Importadora"	"Rua do Mercado, 12"	"Resende"	"SP"	"08737-363"	"Brazil"
10810	"LAUGB"	2	"1998-01-01"	"1998-01-29"	"1998-01-07"	3	4.33	"Laughing Bacchus Wine Cellars"	"2319 Elm St."	"Vancouver"	"BC"	"V3F 2K1"	"Canada"
10808	"OLDWO"	2	"1998-01-01"	"1998-01-29"	"1998-01-09"	3	45.53	"Old World Delicatessen"	"2743 Bering St."	"Anchorage"	"AK"	"99508"	"USA"
10807	"FRANS"	4	"1997-12-31"	"1998-01-28"	"1998-01-30"	1	1.36	"Franchi S.p.A."	"Via Monte Bianco 34"	"Torino"		"10100"	"Italy"
10806	"VICTE"	3	"1997-12-31"	"1998-01-28"	"1998-01-05"	2	22.11	"Victuailles en stock"	"2, rue du Commerce"	"Lyon"		"69004"	"France"
10804	"SEVES"	6	"1997-12-30"	"1998-01-27"	"1998-01-07"	2	27.33	"Seven Seas Imports"	"90 Wadhurst Rd."	"London"		"OX15 4NB"	"UK"
10805	"THEBI"	2	"1997-12-30"	"1998-01-27"	"1998-01-09"	3	237.34	"The Big Cheese"	"89 Jefferson Way Suite 2"	"Portland"	"OR"	"97201"	"USA"
10803	"WELLI"	4	"1997-12-30"	"1998-01-27"	"1998-01-06"	1	55.23	"Wellington Importadora"	"Rua do Mercado, 12"	"Resende"	"SP"	"08737-363"	"Brazil"
10802	"SIMOB"	4	"1997-12-29"	"1998-01-26"	"1998-01-02"	2	257.26	"Simons bistro"	"Vinbæltet 34"	"Kobenhavn"		"1734"	"Denmark"
10801	"BOLID"	4	"1997-12-29"	"1998-01-26"	"1997-12-31"	2	97.09	"Bólido Comidas preparadas"	"C/ Araquil, 67"	"Madrid"		"28023"	"Spain"
10799	"KOENE"	9	"1997-12-26"	"1998-02-06"	"1998-01-05"	3	30.76	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
10800	"SEVES"	1	"1997-12-26"	"1998-01-23"	"1998-01-05"	3	137.44	"Seven Seas Imports"	"90 Wadhurst Rd."	"London"		"OX15 4NB"	"UK"
10798	"ISLAT"	2	"1997-12-26"	"1998-01-23"	"1998-01-05"	1	2.33	"Island Trading"	"Garden House Crowther Way"	"Cowes"	"Isle of Wight"	"PO31 7PJ"	"UK"
10796	"HILAA"	3	"1997-12-25"	"1998-01-22"	"1998-01-14"	1	26.52	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10797	"DRACD"	7	"1997-12-25"	"1998-01-22"	"1998-01-05"	2	33.35	"Drachenblut Delikatessen"	"Walserweg 21"	"Aachen"		"52066"	"Germany"
10795	"ERNSH"	8	"1997-12-24"	"1998-01-21"	"1998-01-20"	2	126.66	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10794	"QUEDE"	6	"1997-12-24"	"1998-01-21"	"1998-01-02"	1	21.49	"Que Delícia"	"Rua da Panificadora, 12"	"Rio de Janeiro"	"RJ"	"02389-673"	"Brazil"
10793	"AROUT"	3	"1997-12-24"	"1998-01-21"	"1998-01-08"	3	4.52	"Around the Horn"	"Brook Farm Stratford St. Mary"	"Colchester"	"Essex"	"CO7 6JX"	"UK"
10791	"FRANK"	6	"1997-12-23"	"1998-01-20"	"1998-01-01"	2	16.85	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10792	"WOLZA"	1	"1997-12-23"	"1998-01-20"	"1997-12-31"	3	23.79	"Wolski Zajazd"	"ul. Filtrowa 68"	"Warszawa"		"01-012"	"Poland"
10789	"FOLIG"	1	"1997-12-22"	"1998-01-19"	"1997-12-31"	2	100.6	"Folies gourmandes"	"184, chaussée de Tournai"	"Lille"		"59000"	"France"
10790	"GOURL"	6	"1997-12-22"	"1998-01-19"	"1997-12-26"	1	28.23	"Gourmet Lanchonetes"	"Av. Brasil, 442"	"Campinas"	"SP"	"04876-786"	"Brazil"
10788	"QUICK"	1	"1997-12-22"	"1998-01-19"	"1998-01-19"	2	42.7	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10787	"LAMAI"	2	"1997-12-19"	"1998-01-02"	"1997-12-26"	1	249.93	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
10786	"QUEEN"	8	"1997-12-19"	"1998-01-16"	"1997-12-23"	1	110.87	"Queen Cozinha"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"
10784	"MAGAA"	4	"1997-12-18"	"1998-01-15"	"1997-12-22"	3	70.09	"Magazzini Alimentari Riuniti"	"Via Ludovico il Moro 22"	"Bergamo"		"24100"	"Italy"
10785	"GROSR"	1	"1997-12-18"	"1998-01-15"	"1997-12-24"	3	1.51	"GROSELLA-Restaurante"	"5ª Ave. Los Palos Grandes"	"Caracas"	"DF"	"1081"	"Venezuela"
10783	"HANAR"	4	"1997-12-18"	"1998-01-15"	"1997-12-19"	2	124.98	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
10782	"CACTU"	9	"1997-12-17"	"1998-01-14"	"1997-12-22"	3	1.1	"Cactus Comidas para llevar"	"Cerrito 333"	"Buenos Aires"		"1010"	"Argentina"
10781	"WARTH"	2	"1997-12-17"	"1998-01-14"	"1997-12-19"	3	73.16	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10779	"MORGK"	3	"1997-12-16"	"1998-01-13"	"1998-01-14"	2	58.13	"Morgenstern Gesundkost"	"Heerstr. 22"	"Leipzig"		"04179"	"Germany"
10780	"LILAS"	2	"1997-12-16"	"1997-12-30"	"1997-12-25"	1	42.13	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
10778	"BERGS"	3	"1997-12-16"	"1998-01-13"	"1997-12-24"	1	6.79	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10776	"ERNSH"	1	"1997-12-15"	"1998-01-12"	"1997-12-18"	3	351.53	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10777	"GOURL"	7	"1997-12-15"	"1997-12-29"	"1998-01-21"	2	3.01	"Gourmet Lanchonetes"	"Av. Brasil, 442"	"Campinas"	"SP"	"04876-786"	"Brazil"
10775	"THECR"	7	"1997-12-12"	"1998-01-09"	"1997-12-26"	1	20.25	"The Cracker Box"	"55 Grizzly Peak Rd."	"Butte"	"MT"	"59801"	"USA"
10774	"FOLKO"	4	"1997-12-11"	"1997-12-25"	"1997-12-12"	1	48.2	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10773	"ERNSH"	1	"1997-12-11"	"1998-01-08"	"1997-12-16"	3	96.43	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10771	"ERNSH"	9	"1997-12-10"	"1998-01-07"	"1998-01-02"	2	11.19	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10772	"LEHMS"	3	"1997-12-10"	"1998-01-07"	"1997-12-19"	2	91.28	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10770	"HANAR"	8	"1997-12-09"	"1998-01-06"	"1997-12-17"	3	5.32	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
10768	"AROUT"	3	"1997-12-08"	"1998-01-05"	"1997-12-15"	2	146.32	"Around the Horn"	"Brook Farm Stratford St. Mary"	"Colchester"	"Essex"	"CO7 6JX"	"UK"
10769	"VAFFE"	3	"1997-12-08"	"1998-01-05"	"1997-12-12"	1	65.06	"Vaffeljernet"	"Smagsloget 45"	"Århus"		"8200"	"Denmark"
10767	"SUPRD"	4	"1997-12-05"	"1998-01-02"	"1997-12-15"	3	1.59	"Suprêmes délices"	"Boulevard Tirou, 255"	"Charleroi"		"B-6000"	"Belgium"
10766	"OTTIK"	4	"1997-12-05"	"1998-01-02"	"1997-12-09"	1	157.55	"Ottilies Käseladen"	"Mehrheimerstr. 369"	"Köln"		"50739"	"Germany"
10765	"QUICK"	3	"1997-12-04"	"1998-01-01"	"1997-12-09"	3	42.74	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10763	"FOLIG"	3	"1997-12-03"	"1997-12-31"	"1997-12-08"	3	37.35	"Folies gourmandes"	"184, chaussée de Tournai"	"Lille"		"59000"	"France"
10764	"ERNSH"	6	"1997-12-03"	"1997-12-31"	"1997-12-08"	3	145.45	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10761	"RATTC"	5	"1997-12-02"	"1997-12-30"	"1997-12-08"	2	18.66	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10762	"FOLKO"	3	"1997-12-02"	"1997-12-30"	"1997-12-09"	1	328.74	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10760	"MAISD"	4	"1997-12-01"	"1997-12-29"	"1997-12-10"	1	155.64	"Maison Dewey"	"Rue Joseph-Bens 532"	"Bruxelles"		"B-1180"	"Belgium"
10759	"ANATR"	3	"1997-11-28"	"1997-12-26"	"1997-12-12"	3	11.99	"Ana Trujillo Emparedados y helados"	"Avda. de la Constitución 2222"	"México D.F."		"05021"	"Mexico"
10758	"RICSU"	3	"1997-11-28"	"1997-12-26"	"1997-12-04"	3	138.17	"Richter Supermarkt"	"Starenweg 5"	"Genève"		"1204"	"Switzerland"
10756	"SPLIR"	8	"1997-11-27"	"1997-12-25"	"1997-12-02"	2	73.21	"Split Rail Beer & Ale"	"P.O. Box 555"	"Lander"	"WY"	"82520"	"USA"
10757	"SAVEA"	6	"1997-11-27"	"1997-12-25"	"1997-12-15"	1	8.19	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10755	"BONAP"	4	"1997-11-26"	"1997-12-24"	"1997-11-28"	2	16.71	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10754	"MAGAA"	6	"1997-11-25"	"1997-12-23"	"1997-11-27"	3	2.38	"Magazzini Alimentari Riuniti"	"Via Ludovico il Moro 22"	"Bergamo"		"24100"	"Italy"
10753	"FRANS"	3	"1997-11-25"	"1997-12-23"	"1997-11-27"	1	7.7	"Franchi S.p.A."	"Via Monte Bianco 34"	"Torino"		"10100"	"Italy"
10751	"RICSU"	3	"1997-11-24"	"1997-12-22"	"1997-12-03"	3	130.79	"Richter Supermarkt"	"Starenweg 5"	"Genève"		"1204"	"Switzerland"
10752	"NORTS"	2	"1997-11-24"	"1997-12-22"	"1997-11-28"	3	1.39	"North/South"	"South House 300 Queensbridge"	"London"		"SW7 1RZ"	"UK"
10750	"WARTH"	9	"1997-11-21"	"1997-12-19"	"1997-11-24"	1	79.3	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10749	"ISLAT"	4	"1997-11-20"	"1997-12-18"	"1997-12-19"	2	61.53	"Island Trading"	"Garden House Crowther Way"	"Cowes"	"Isle of Wight"	"PO31 7PJ"	"UK"
10748	"SAVEA"	3	"1997-11-20"	"1997-12-18"	"1997-11-28"	1	232.55	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10746	"CHOPS"	1	"1997-11-19"	"1997-12-17"	"1997-11-21"	3	31.43	"Chop-suey Chinese"	"Hauptstr. 31"	"Bern"		"3012"	"Switzerland"
10747	"PICCO"	6	"1997-11-19"	"1997-12-17"	"1997-11-26"	1	117.33	"Piccolo und mehr"	"Geislweg 14"	"Salzburg"		"5020"	"Austria"
10745	"QUICK"	9	"1997-11-18"	"1997-12-16"	"1997-11-27"	1	3.52	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10743	"AROUT"	1	"1997-11-17"	"1997-12-15"	"1997-11-21"	2	23.72	"Around the Horn"	"Brook Farm Stratford St. Mary"	"Colchester"	"Essex"	"CO7 6JX"	"UK"
10744	"VAFFE"	6	"1997-11-17"	"1997-12-15"	"1997-11-24"	1	69.19	"Vaffeljernet"	"Smagsloget 45"	"Århus"		"8200"	"Denmark"
10742	"BOTTM"	3	"1997-11-14"	"1997-12-12"	"1997-11-18"	3	243.73	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
10741	"AROUT"	4	"1997-11-14"	"1997-11-28"	"1997-11-18"	3	10.96	"Around the Horn"	"Brook Farm Stratford St. Mary"	"Colchester"	"Essex"	"CO7 6JX"	"UK"
10740	"WHITC"	4	"1997-11-13"	"1997-12-11"	"1997-11-25"	2	81.88	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
10738	"SPECD"	2	"1997-11-12"	"1997-12-10"	"1997-11-18"	1	2.91	"Spécialités du monde"	"25, rue Lauriston"	"Paris"		"75016"	"France"
10739	"VINET"	3	"1997-11-12"	"1997-12-10"	"1997-11-17"	3	11.08	"Vins et alcools Chevalier"	"59 rue de l'Abbaye"	"Reims"		"51100"	"France"
10736	"HUNGO"	9	"1997-11-11"	"1997-12-09"	"1997-11-21"	2	44.1	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10737	"VINET"	2	"1997-11-11"	"1997-12-09"	"1997-11-18"	2	7.79	"Vins et alcools Chevalier"	"59 rue de l'Abbaye"	"Reims"		"51100"	"France"
10735	"LETSS"	6	"1997-11-10"	"1997-12-08"	"1997-11-21"	2	45.97	"Let's Stop N Shop"	"87 Polk St. Suite 5"	"San Francisco"	"CA"	"94117"	"USA"
10734	"GOURL"	2	"1997-11-07"	"1997-12-05"	"1997-11-12"	3	1.63	"Gourmet Lanchonetes"	"Av. Brasil, 442"	"Campinas"	"SP"	"04876-786"	"Brazil"
10733	"BERGS"	1	"1997-11-07"	"1997-12-05"	"1997-11-10"	3	110.11	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10731	"CHOPS"	7	"1997-11-06"	"1997-12-04"	"1997-11-14"	1	96.65	"Chop-suey Chinese"	"Hauptstr. 31"	"Bern"		"3012"	"Switzerland"
10732	"BONAP"	3	"1997-11-06"	"1997-12-04"	"1997-11-07"	1	16.97	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10730	"BONAP"	5	"1997-11-05"	"1997-12-03"	"1997-11-14"	1	20.12	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10729	"LINOD"	8	"1997-11-04"	"1997-12-16"	"1997-11-14"	3	141.06	"LINO-Delicateses"	"Ave. 5 de Mayo Porlamar"	"I. de Margarita"	"Nueva Esparta"	"4980"	"Venezuela"
10728	"QUEEN"	4	"1997-11-04"	"1997-12-02"	"1997-11-11"	2	58.33	"Queen Cozinha"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"
10726	"EASTC"	4	"1997-11-03"	"1997-11-17"	"1997-12-05"	1	16.56	"Eastern Connection"	"35 King George"	"London"		"WX3 6FW"	"UK"
10727	"REGGC"	2	"1997-11-03"	"1997-12-01"	"1997-12-05"	1	89.9	"Reggiani Caseifici"	"Strada Provinciale 124"	"Reggio Emilia"		"42100"	"Italy"
10725	"FAMIA"	4	"1997-10-31"	"1997-11-28"	"1997-11-05"	3	10.83	"Familia Arquibaldo"	"Rua Orós, 92"	"Sao Paulo"	"SP"	"05442-030"	"Brazil"
10724	"MEREP"	8	"1997-10-30"	"1997-12-11"	"1997-11-05"	2	57.75	"Mère Paillarde"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"
10723	"WHITC"	3	"1997-10-30"	"1997-11-27"	"1997-11-25"	1	21.72	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
10721	"QUICK"	5	"1997-10-29"	"1997-11-26"	"1997-10-31"	3	48.92	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10722	"SAVEA"	8	"1997-10-29"	"1997-12-10"	"1997-11-04"	1	74.58	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10720	"QUEDE"	8	"1997-10-28"	"1997-11-11"	"1997-11-05"	2	9.53	"Que Delícia"	"Rua da Panificadora, 12"	"Rio de Janeiro"	"RJ"	"02389-673"	"Brazil"
10719	"LETSS"	8	"1997-10-27"	"1997-11-24"	"1997-11-05"	2	51.44	"Let's Stop N Shop"	"87 Polk St. Suite 5"	"San Francisco"	"CA"	"94117"	"USA"
10718	"KOENE"	1	"1997-10-27"	"1997-11-24"	"1997-10-29"	3	170.88	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
10717	"FRANK"	1	"1997-10-24"	"1997-11-21"	"1997-10-29"	2	59.25	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10716	"RANCH"	4	"1997-10-24"	"1997-11-21"	"1997-10-27"	2	22.57	"Rancho grande"	"Av. del Libertador 900"	"Buenos Aires"		"1010"	"Argentina"
10715	"BONAP"	3	"1997-10-23"	"1997-11-06"	"1997-10-29"	1	63.2	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10714	"SAVEA"	5	"1997-10-22"	"1997-11-19"	"1997-10-27"	3	24.49	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10713	"SAVEA"	1	"1997-10-22"	"1997-11-19"	"1997-10-24"	1	167.05	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10712	"HUNGO"	3	"1997-10-21"	"1997-11-18"	"1997-10-31"	1	89.93	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10711	"SAVEA"	5	"1997-10-21"	"1997-12-02"	"1997-10-29"	2	52.41	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10710	"FRANS"	1	"1997-10-20"	"1997-11-17"	"1997-10-23"	1	4.98	"Franchi S.p.A."	"Via Monte Bianco 34"	"Torino"		"10100"	"Italy"
10709	"GOURL"	1	"1997-10-17"	"1997-11-14"	"1997-11-20"	3	210.8	"Gourmet Lanchonetes"	"Av. Brasil, 442"	"Campinas"	"SP"	"04876-786"	"Brazil"
10708	"THEBI"	6	"1997-10-17"	"1997-11-28"	"1997-11-05"	2	2.96	"The Big Cheese"	"89 Jefferson Way Suite 2"	"Portland"	"OR"	"97201"	"USA"
10706	"OLDWO"	8	"1997-10-16"	"1997-11-13"	"1997-10-21"	3	135.63	"Old World Delicatessen"	"2743 Bering St."	"Anchorage"	"AK"	"99508"	"USA"
10707	"AROUT"	4	"1997-10-16"	"1997-10-30"	"1997-10-23"	3	21.74	"Around the Horn"	"Brook Farm Stratford St. Mary"	"Colchester"	"Essex"	"CO7 6JX"	"UK"
10705	"HILAA"	9	"1997-10-15"	"1997-11-12"	"1997-11-18"	2	3.52	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10704	"QUEEN"	6	"1997-10-14"	"1997-11-11"	"1997-11-07"	1	4.78	"Queen Cozinha"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"
10703	"FOLKO"	6	"1997-10-14"	"1997-11-11"	"1997-10-20"	2	152.3	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10701	"HUNGO"	6	"1997-10-13"	"1997-10-27"	"1997-10-15"	3	220.31	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10702	"ALFKI"	4	"1997-10-13"	"1997-11-24"	"1997-10-21"	1	23.94	"Alfred's Futterkiste"	"Obere Str. 57"	"Berlin"		"12209"	"Germany"
10700	"SAVEA"	3	"1997-10-10"	"1997-11-07"	"1997-10-16"	1	65.1	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10699	"MORGK"	3	"1997-10-09"	"1997-11-06"	"1997-10-13"	3	0.58	"Morgenstern Gesundkost"	"Heerstr. 22"	"Leipzig"		"04179"	"Germany"
10698	"ERNSH"	4	"1997-10-09"	"1997-11-06"	"1997-10-17"	1	272.47	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10696	"WHITC"	8	"1997-10-08"	"1997-11-19"	"1997-10-14"	3	102.55	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
10697	"LINOD"	3	"1997-10-08"	"1997-11-05"	"1997-10-14"	1	45.52	"LINO-Delicateses"	"Ave. 5 de Mayo Porlamar"	"I. de Margarita"	"Nueva Esparta"	"4980"	"Venezuela"
10695	"WILMK"	7	"1997-10-07"	"1997-11-18"	"1997-10-14"	1	16.72	"Wilman Kala"	"Keskuskatu 45"	"Helsinki"		"21240"	"Finland"
10694	"QUICK"	8	"1997-10-06"	"1997-11-03"	"1997-10-09"	3	398.36	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10693	"WHITC"	3	"1997-10-06"	"1997-10-20"	"1997-10-10"	3	139.34	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
10691	"QUICK"	2	"1997-10-03"	"1997-11-14"	"1997-10-22"	2	810.05	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10692	"ALFKI"	4	"1997-10-03"	"1997-10-31"	"1997-10-13"	2	61.02	"Alfred's Futterkiste"	"Obere Str. 57"	"Berlin"		"12209"	"Germany"
10690	"HANAR"	1	"1997-10-02"	"1997-10-30"	"1997-10-03"	1	15.8	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
10689	"BERGS"	1	"1997-10-01"	"1997-10-29"	"1997-10-07"	2	13.42	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10688	"VAFFE"	4	"1997-10-01"	"1997-10-15"	"1997-10-07"	2	299.09	"Vaffeljernet"	"Smagsloget 45"	"Århus"		"8200"	"Denmark"
10687	"HUNGO"	9	"1997-09-30"	"1997-10-28"	"1997-10-30"	2	296.43	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10686	"PICCO"	2	"1997-09-30"	"1997-10-28"	"1997-10-08"	1	96.5	"Piccolo und mehr"	"Geislweg 14"	"Salzburg"		"5020"	"Austria"
10685	"GOURL"	4	"1997-09-29"	"1997-10-13"	"1997-10-03"	2	33.75	"Gourmet Lanchonetes"	"Av. Brasil, 442"	"Campinas"	"SP"	"04876-786"	"Brazil"
10684	"OTTIK"	3	"1997-09-26"	"1997-10-24"	"1997-09-30"	1	145.63	"Ottilies Käseladen"	"Mehrheimerstr. 369"	"Köln"		"50739"	"Germany"
10683	"DUMON"	2	"1997-09-26"	"1997-10-24"	"1997-10-01"	1	4.4	"Du monde entier"	"67, rue des Cinquante Otages"	"Nantes"		"44000"	"France"
10681	"GREAL"	3	"1997-09-25"	"1997-10-23"	"1997-09-30"	3	76.13	"Great Lakes Food Market"	"2732 Baker Blvd."	"Eugene"	"OR"	"97403"	"USA"
10682	"ANTON"	3	"1997-09-25"	"1997-10-23"	"1997-10-01"	2	36.13	"Antonio Moreno Taquería"	"Mataderos  2312"	"México D.F."		"05023"	"Mexico"
10680	"OLDWO"	1	"1997-09-24"	"1997-10-22"	"1997-09-26"	1	26.61	"Old World Delicatessen"	"2743 Bering St."	"Anchorage"	"AK"	"99508"	"USA"
10679	"BLONP"	8	"1997-09-23"	"1997-10-21"	"1997-09-30"	3	27.94	"Blondel père et fils"	"24, place Kléber"	"Strasbourg"		"67000"	"France"
10678	"SAVEA"	7	"1997-09-23"	"1997-10-21"	"1997-10-16"	3	388.98	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10676	"TORTU"	2	"1997-09-22"	"1997-10-20"	"1997-09-29"	2	2.01	"Tortuga Restaurante"	"Avda. Azteca 123"	"México D.F."		"05033"	"Mexico"
10677	"ANTON"	1	"1997-09-22"	"1997-10-20"	"1997-09-26"	3	4.03	"Antonio Moreno Taquería"	"Mataderos  2312"	"México D.F."		"05023"	"Mexico"
10675	"FRANK"	5	"1997-09-19"	"1997-10-17"	"1997-09-23"	2	31.85	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10674	"ISLAT"	4	"1997-09-18"	"1997-10-16"	"1997-09-30"	2	0.9	"Island Trading"	"Garden House Crowther Way"	"Cowes"	"Isle of Wight"	"PO31 7PJ"	"UK"
10673	"WILMK"	2	"1997-09-18"	"1997-10-16"	"1997-09-19"	1	22.76	"Wilman Kala"	"Keskuskatu 45"	"Helsinki"		"21240"	"Finland"
10671	"FRANR"	1	"1997-09-17"	"1997-10-15"	"1997-09-24"	1	30.34	"France restauration"	"54, rue Royale"	"Nantes"		"44000"	"France"
10672	"BERGS"	9	"1997-09-17"	"1997-10-01"	"1997-09-26"	2	95.75	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10670	"FRANK"	4	"1997-09-16"	"1997-10-14"	"1997-09-18"	1	203.48	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10669	"SIMOB"	2	"1997-09-15"	"1997-10-13"	"1997-09-22"	1	24.39	"Simons bistro"	"Vinbæltet 34"	"Kobenhavn"		"1734"	"Denmark"
10668	"WANDK"	1	"1997-09-15"	"1997-10-13"	"1997-09-23"	2	47.22	"Die Wandernde Kuh"	"Adenauerallee 900"	"Stuttgart"		"70563"	"Germany"
10666	"RICSU"	7	"1997-09-12"	"1997-10-10"	"1997-09-22"	2	232.42	"Richter Supermarkt"	"Starenweg 5"	"Genève"		"1204"	"Switzerland"
10667	"ERNSH"	7	"1997-09-12"	"1997-10-10"	"1997-09-19"	1	78.09	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10665	"LONEP"	1	"1997-09-11"	"1997-10-09"	"1997-09-17"	2	26.31	"Lonesome Pine Restaurant"	"89 Chiaroscuro Rd."	"Portland"	"OR"	"97219"	"USA"
10663	"BONAP"	2	"1997-09-10"	"1997-09-24"	"1997-10-03"	2	113.15	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10664	"FURIB"	1	"1997-09-10"	"1997-10-08"	"1997-09-19"	3	1.27	"Furia Bacalhau e Frutos do Mar"	"Jardim das rosas n. 32"	"Lisboa"		"1675"	"Portugal"
10662	"LONEP"	3	"1997-09-09"	"1997-10-07"	"1997-09-18"	2	1.28	"Lonesome Pine Restaurant"	"89 Chiaroscuro Rd."	"Portland"	"OR"	"97219"	"USA"
10661	"HUNGO"	7	"1997-09-09"	"1997-10-07"	"1997-09-15"	3	17.55	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10660	"HUNGC"	8	"1997-09-08"	"1997-10-06"	"1997-10-15"	1	111.29	"Hungry Coyote Import Store"	"City Center Plaza 516 Main St."	"Elgin"	"OR"	"97827"	"USA"
10658	"QUICK"	4	"1997-09-05"	"1997-10-03"	"1997-09-08"	1	364.15	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10659	"QUEEN"	7	"1997-09-05"	"1997-10-03"	"1997-09-10"	2	105.81	"Queen Cozinha"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"
10656	"GREAL"	6	"1997-09-04"	"1997-10-02"	"1997-09-10"	1	57.15	"Great Lakes Food Market"	"2732 Baker Blvd."	"Eugene"	"OR"	"97403"	"USA"
10657	"SAVEA"	2	"1997-09-04"	"1997-10-02"	"1997-09-15"	2	352.69	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10655	"REGGC"	1	"1997-09-03"	"1997-10-01"	"1997-09-11"	2	4.41	"Reggiani Caseifici"	"Strada Provinciale 124"	"Reggio Emilia"		"42100"	"Italy"
10654	"BERGS"	5	"1997-09-02"	"1997-09-30"	"1997-09-11"	1	55.26	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10653	"FRANK"	1	"1997-09-02"	"1997-09-30"	"1997-09-19"	1	93.25	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10651	"WANDK"	8	"1997-09-01"	"1997-09-29"	"1997-09-11"	2	20.6	"Die Wandernde Kuh"	"Adenauerallee 900"	"Stuttgart"		"70563"	"Germany"
10652	"GOURL"	4	"1997-09-01"	"1997-09-29"	"1997-09-08"	2	7.14	"Gourmet Lanchonetes"	"Av. Brasil, 442"	"Campinas"	"SP"	"04876-786"	"Brazil"
10650	"FAMIA"	5	"1997-08-29"	"1997-09-26"	"1997-09-03"	3	176.81	"Familia Arquibaldo"	"Rua Orós, 92"	"Sao Paulo"	"SP"	"05442-030"	"Brazil"
10649	"MAISD"	5	"1997-08-28"	"1997-09-25"	"1997-08-29"	3	6.2	"Maison Dewey"	"Rue Joseph-Bens 532"	"Bruxelles"		"B-1180"	"Belgium"
10648	"RICAR"	5	"1997-08-28"	"1997-10-09"	"1997-09-09"	2	14.25	"Ricardo Adocicados"	"Av. Copacabana, 267"	"Rio de Janeiro"	"RJ"	"02389-890"	"Brazil"
10646	"HUNGO"	9	"1997-08-27"	"1997-10-08"	"1997-09-03"	3	142.33	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10647	"QUEDE"	4	"1997-08-27"	"1997-09-10"	"1997-09-03"	2	45.54	"Que Delícia"	"Rua da Panificadora, 12"	"Rio de Janeiro"	"RJ"	"02389-673"	"Brazil"
10645	"HANAR"	4	"1997-08-26"	"1997-09-23"	"1997-09-02"	1	12.41	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
10644	"WELLI"	3	"1997-08-25"	"1997-09-22"	"1997-09-01"	2	0.14	"Wellington Importadora"	"Rua do Mercado, 12"	"Resende"	"SP"	"08737-363"	"Brazil"
10643	"ALFKI"	6	"1997-08-25"	"1997-09-22"	"1997-09-02"	1	29.46	"Alfreds Futterkiste"	"Obere Str. 57"	"Berlin"		"12209"	"Germany"
10641	"HILAA"	4	"1997-08-22"	"1997-09-19"	"1997-08-26"	2	179.61	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10642	"SIMOB"	7	"1997-08-22"	"1997-09-19"	"1997-09-05"	3	41.89	"Simons bistro"	"Vinbæltet 34"	"Kobenhavn"		"1734"	"Denmark"
10640	"WANDK"	4	"1997-08-21"	"1997-09-18"	"1997-08-28"	1	23.55	"Die Wandernde Kuh"	"Adenauerallee 900"	"Stuttgart"		"70563"	"Germany"
10639	"SANTG"	7	"1997-08-20"	"1997-09-17"	"1997-08-27"	3	38.64	"Santé Gourmet"	"Erling Skakkes gate 78"	"Stavern"		"4110"	"Norway"
10638	"LINOD"	3	"1997-08-20"	"1997-09-17"	"1997-09-01"	1	158.44	"LINO-Delicateses"	"Ave. 5 de Mayo Porlamar"	"I. de Margarita"	"Nueva Esparta"	"4980"	"Venezuela"
10637	"QUEEN"	6	"1997-08-19"	"1997-09-16"	"1997-08-26"	1	201.29	"Queen Cozinha"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"
10636	"WARTH"	4	"1997-08-19"	"1997-09-16"	"1997-08-26"	1	1.15	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10635	"MAGAA"	8	"1997-08-18"	"1997-09-15"	"1997-08-21"	3	47.46	"Magazzini Alimentari Riuniti"	"Via Ludovico il Moro 22"	"Bergamo"		"24100"	"Italy"
10633	"ERNSH"	7	"1997-08-15"	"1997-09-12"	"1997-08-18"	3	477.9	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10634	"FOLIG"	4	"1997-08-15"	"1997-09-12"	"1997-08-21"	3	487.38	"Folies gourmandes"	"184, chaussée de Tournai"	"Lille"		"59000"	"France"
10631	"LAMAI"	8	"1997-08-14"	"1997-09-11"	"1997-08-15"	1	0.87	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
10632	"WANDK"	8	"1997-08-14"	"1997-09-11"	"1997-08-19"	1	41.38	"Die Wandernde Kuh"	"Adenauerallee 900"	"Stuttgart"		"70563"	"Germany"
10630	"KOENE"	1	"1997-08-13"	"1997-09-10"	"1997-08-19"	2	32.35	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
10629	"GODOS"	4	"1997-08-12"	"1997-09-09"	"1997-08-20"	3	85.46	"Godos Cocina Típica"	"C/ Romero, 33"	"Sevilla"		"41101"	"Spain"
10628	"BLONP"	4	"1997-08-12"	"1997-09-09"	"1997-08-20"	3	30.36	"Blondel père et fils"	"24, place Kléber"	"Strasbourg"		"67000"	"France"
10626	"BERGS"	1	"1997-08-11"	"1997-09-08"	"1997-08-20"	2	138.69	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10627	"SAVEA"	8	"1997-08-11"	"1997-09-22"	"1997-08-21"	3	107.46	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10625	"ANATR"	3	"1997-08-08"	"1997-09-05"	"1997-08-14"	1	43.9	"Ana Trujillo Emparedados y helados"	"Avda. de la Constitución 2222"	"México D.F."		"05021"	"Mexico"
10623	"FRANK"	8	"1997-08-07"	"1997-09-04"	"1997-08-12"	2	97.18	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10624	"THECR"	4	"1997-08-07"	"1997-09-04"	"1997-08-19"	2	94.8	"The Cracker Box"	"55 Grizzly Peak Rd."	"Butte"	"MT"	"59801"	"USA"
10622	"RICAR"	4	"1997-08-06"	"1997-09-03"	"1997-08-11"	3	50.97	"Ricardo Adocicados"	"Av. Copacabana, 267"	"Rio de Janeiro"	"RJ"	"02389-890"	"Brazil"
10621	"ISLAT"	4	"1997-08-05"	"1997-09-02"	"1997-08-11"	2	23.73	"Island Trading"	"Garden House Crowther Way"	"Cowes"	"Isle of Wight"	"PO31 7PJ"	"UK"
10620	"LAUGB"	2	"1997-08-05"	"1997-09-02"	"1997-08-14"	3	0.94	"Laughing Bacchus Wine Cellars"	"2319 Elm St."	"Vancouver"	"BC"	"V3F 2K1"	"Canada"
10619	"MEREP"	3	"1997-08-04"	"1997-09-01"	"1997-08-07"	3	91.05	"Mère Paillarde"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"
10618	"MEREP"	1	"1997-08-01"	"1997-09-12"	"1997-08-08"	1	154.68	"Mère Paillarde"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"
10616	"GREAL"	1	"1997-07-31"	"1997-08-28"	"1997-08-05"	2	116.53	"Great Lakes Food Market"	"2732 Baker Blvd."	"Eugene"	"OR"	"97403"	"USA"
10617	"GREAL"	4	"1997-07-31"	"1997-08-28"	"1997-08-04"	2	18.53	"Great Lakes Food Market"	"2732 Baker Blvd."	"Eugene"	"OR"	"97403"	"USA"
10615	"WILMK"	2	"1997-07-30"	"1997-08-27"	"1997-08-06"	3	0.75	"Wilman Kala"	"Keskuskatu 45"	"Helsinki"		"21240"	"Finland"
10613	"HILAA"	4	"1997-07-29"	"1997-08-26"	"1997-08-01"	2	8.11	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10614	"BLAUS"	8	"1997-07-29"	"1997-08-26"	"1997-08-01"	3	1.93	"Blauer See Delikatessen"	"Forsterstr. 57"	"Mannheim"		"68306"	"Germany"
10612	"SAVEA"	1	"1997-07-28"	"1997-08-25"	"1997-08-01"	2	544.08	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10611	"WOLZA"	6	"1997-07-25"	"1997-08-22"	"1997-08-01"	2	80.65	"Wolski Zajazd"	"ul. Filtrowa 68"	"Warszawa"		"01-012"	"Poland"
10610	"LAMAI"	8	"1997-07-25"	"1997-08-22"	"1997-08-06"	1	26.78	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
10609	"DUMON"	7	"1997-07-24"	"1997-08-21"	"1997-07-30"	2	1.85	"Du monde entier"	"67, rue des Cinquante Otages"	"Nantes"		"44000"	"France"
10608	"TOMSP"	4	"1997-07-23"	"1997-08-20"	"1997-08-01"	2	27.79	"Toms Spezialitäten"	"Luisenstr. 48"	"Münster"		"44087"	"Germany"
10606	"TRADH"	4	"1997-07-22"	"1997-08-19"	"1997-07-31"	3	79.4	"Tradiçao Hipermercados"	"Av. Inês de Castro, 414"	"Sao Paulo"	"SP"	"05634-030"	"Brazil"
10607	"SAVEA"	5	"1997-07-22"	"1997-08-19"	"1997-07-25"	1	200.24	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10605	"MEREP"	1	"1997-07-21"	"1997-08-18"	"1997-07-29"	2	379.13	"Mère Paillarde"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"
10603	"SAVEA"	8	"1997-07-18"	"1997-08-15"	"1997-08-08"	2	48.77	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10604	"FURIB"	1	"1997-07-18"	"1997-08-15"	"1997-07-29"	1	7.46	"Furia Bacalhau e Frutos do Mar"	"Jardim das rosas n. 32"	"Lisboa"		"1675"	"Portugal"
10602	"VAFFE"	8	"1997-07-17"	"1997-08-14"	"1997-07-22"	2	2.92	"Vaffeljernet"	"Smagsloget 45"	"Århus"		"8200"	"Denmark"
10601	"HILAA"	7	"1997-07-16"	"1997-08-27"	"1997-07-22"	1	58.3	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10600	"HUNGC"	4	"1997-07-16"	"1997-08-13"	"1997-07-21"	1	45.13	"Hungry Coyote Import Store"	"City Center Plaza 516 Main St."	"Elgin"	"OR"	"97827"	"USA"
10599	"BSBEV"	6	"1997-07-15"	"1997-08-26"	"1997-07-21"	3	29.98	"B's Beverages"	"Fauntleroy Circus"	"London"		"EC2 5NT"	"UK"
10598	"RATTC"	1	"1997-07-14"	"1997-08-11"	"1997-07-18"	3	44.42	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10596	"WHITC"	8	"1997-07-11"	"1997-08-08"	"1997-08-12"	1	16.34	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
10597	"PICCO"	7	"1997-07-11"	"1997-08-08"	"1997-07-18"	3	35.12	"Piccolo und mehr"	"Geislweg 14"	"Salzburg"		"5020"	"Austria"
10595	"ERNSH"	2	"1997-07-10"	"1997-08-07"	"1997-07-14"	1	96.78	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10593	"LEHMS"	7	"1997-07-09"	"1997-08-06"	"1997-08-13"	2	174.2	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10594	"OLDWO"	3	"1997-07-09"	"1997-08-06"	"1997-07-16"	2	5.24	"Old World Delicatessen"	"2743 Bering St."	"Anchorage"	"AK"	"99508"	"USA"
10592	"LEHMS"	3	"1997-07-08"	"1997-08-05"	"1997-07-16"	1	32.1	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10590	"MEREP"	4	"1997-07-07"	"1997-08-04"	"1997-07-14"	3	44.77	"Mère Paillarde"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"
10591	"VAFFE"	1	"1997-07-07"	"1997-07-21"	"1997-07-16"	1	55.92	"Vaffeljernet"	"Smagsloget 45"	"Århus"		"8200"	"Denmark"
10589	"GREAL"	8	"1997-07-04"	"1997-08-01"	"1997-07-14"	2	4.42	"Great Lakes Food Market"	"2732 Baker Blvd."	"Eugene"	"OR"	"97403"	"USA"
10588	"QUICK"	2	"1997-07-03"	"1997-07-31"	"1997-07-10"	3	194.67	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10587	"QUEDE"	1	"1997-07-02"	"1997-07-30"	"1997-07-09"	1	62.52	"Que Delícia"	"Rua da Panificadora, 12"	"Rio de Janeiro"	"RJ"	"02389-673"	"Brazil"
10586	"REGGC"	9	"1997-07-02"	"1997-07-30"	"1997-07-09"	1	0.48	"Reggiani Caseifici"	"Strada Provinciale 124"	"Reggio Emilia"		"42100"	"Italy"
10585	"WELLI"	7	"1997-07-01"	"1997-07-29"	"1997-07-10"	1	13.41	"Wellington Importadora"	"Rua do Mercado, 12"	"Resende"	"SP"	"08737-363"	"Brazil"
10584	"BLONP"	4	"1997-06-30"	"1997-07-28"	"1997-07-04"	1	59.14	"Blondel père et fils"	"24, place Kléber"	"Strasbourg"		"67000"	"France"
10583	"WARTH"	2	"1997-06-30"	"1997-07-28"	"1997-07-04"	2	7.28	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10582	"BLAUS"	3	"1997-06-27"	"1997-07-25"	"1997-07-14"	2	27.71	"Blauer See Delikatessen"	"Forsterstr. 57"	"Mannheim"		"68306"	"Germany"
10581	"FAMIA"	3	"1997-06-26"	"1997-07-24"	"1997-07-02"	1	3.01	"Familia Arquibaldo"	"Rua Orós, 92"	"Sao Paulo"	"SP"	"05442-030"	"Brazil"
10580	"OTTIK"	4	"1997-06-26"	"1997-07-24"	"1997-07-01"	3	75.89	"Ottilies Käseladen"	"Mehrheimerstr. 369"	"Köln"		"50739"	"Germany"
10579	"LETSS"	1	"1997-06-25"	"1997-07-23"	"1997-07-04"	2	13.73	"Let's Stop N Shop"	"87 Polk St. Suite 5"	"San Francisco"	"CA"	"94117"	"USA"
10578	"BSBEV"	4	"1997-06-24"	"1997-07-22"	"1997-07-25"	3	29.6	"B's Beverages"	"Fauntleroy Circus"	"London"		"EC2 5NT"	"UK"
10576	"TORTU"	3	"1997-06-23"	"1997-07-07"	"1997-06-30"	3	18.56	"Tortuga Restaurante"	"Avda. Azteca 123"	"México D.F."		"05033"	"Mexico"
10577	"TRAIH"	9	"1997-06-23"	"1997-08-04"	"1997-06-30"	2	25.41	"Trail's Head Gourmet Provisioners"	"722 DaVinci Blvd."	"Kirkland"	"WA"	"98034"	"USA"
10575	"MORGK"	5	"1997-06-20"	"1997-07-04"	"1997-06-30"	1	127.34	"Morgenstern Gesundkost"	"Heerstr. 22"	"Leipzig"		"04179"	"Germany"
10573	"ANTON"	7	"1997-06-19"	"1997-07-17"	"1997-06-20"	3	84.84	"Antonio Moreno Taquería"	"Mataderos  2312"	"México D.F."		"05023"	"Mexico"
10574	"TRAIH"	4	"1997-06-19"	"1997-07-17"	"1997-06-30"	2	37.6	"Trail's Head Gourmet Provisioners"	"722 DaVinci Blvd."	"Kirkland"	"WA"	"98034"	"USA"
10572	"BERGS"	3	"1997-06-18"	"1997-07-16"	"1997-06-25"	2	116.43	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10571	"ERNSH"	8	"1997-06-17"	"1997-07-29"	"1997-07-04"	3	26.06	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10570	"MEREP"	3	"1997-06-17"	"1997-07-15"	"1997-06-19"	3	188.99	"Mère Paillarde"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"
10569	"RATTC"	5	"1997-06-16"	"1997-07-14"	"1997-07-11"	1	58.98	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10568	"GALED"	3	"1997-06-13"	"1997-07-11"	"1997-07-09"	3	6.54	"Galería del gastronómo"	"Rambla de Cataluña, 23"	"Barcelona"		"8022"	"Spain"
10566	"BLONP"	9	"1997-06-12"	"1997-07-10"	"1997-06-18"	1	88.4	"Blondel père et fils"	"24, place Kléber"	"Strasbourg"		"67000"	"France"
10567	"HUNGO"	1	"1997-06-12"	"1997-07-10"	"1997-06-17"	1	33.97	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10565	"MEREP"	8	"1997-06-11"	"1997-07-09"	"1997-06-18"	2	7.15	"Mère Paillarde"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"
10563	"RICAR"	2	"1997-06-10"	"1997-07-22"	"1997-06-24"	2	60.43	"Ricardo Adocicados"	"Av. Copacabana, 267"	"Rio de Janeiro"	"RJ"	"02389-890"	"Brazil"
10564	"RATTC"	4	"1997-06-10"	"1997-07-08"	"1997-06-16"	3	13.75	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10562	"REGGC"	1	"1997-06-09"	"1997-07-07"	"1997-06-12"	1	22.95	"Reggiani Caseifici"	"Strada Provinciale 124"	"Reggio Emilia"		"42100"	"Italy"
10561	"FOLKO"	2	"1997-06-06"	"1997-07-04"	"1997-06-09"	2	242.21	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10560	"FRANK"	8	"1997-06-06"	"1997-07-04"	"1997-06-09"	1	36.65	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10559	"BLONP"	6	"1997-06-05"	"1997-07-03"	"1997-06-13"	1	8.05	"Blondel père et fils"	"24, place Kléber"	"Strasbourg"		"67000"	"France"
10558	"AROUT"	1	"1997-06-04"	"1997-07-02"	"1997-06-10"	2	72.97	"Around the Horn"	"Brook Farm Stratford St. Mary"	"Colchester"	"Essex"	"CO7 6JX"	"UK"
10557	"LEHMS"	9	"1997-06-03"	"1997-06-17"	"1997-06-06"	2	96.72	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10556	"SIMOB"	2	"1997-06-03"	"1997-07-15"	"1997-06-13"	1	9.8	"Simons bistro"	"Vinbæltet 34"	"Kobenhavn"		"1734"	"Denmark"
10555	"SAVEA"	6	"1997-06-02"	"1997-06-30"	"1997-06-04"	3	252.49	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10553	"WARTH"	2	"1997-05-30"	"1997-06-27"	"1997-06-03"	2	149.49	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10554	"OTTIK"	4	"1997-05-30"	"1997-06-27"	"1997-06-05"	3	120.97	"Ottilies Käseladen"	"Mehrheimerstr. 369"	"Köln"		"50739"	"Germany"
10552	"HILAA"	2	"1997-05-29"	"1997-06-26"	"1997-06-05"	1	83.22	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10551	"FURIB"	4	"1997-05-28"	"1997-07-09"	"1997-06-06"	3	72.95	"Furia Bacalhau e Frutos do Mar"	"Jardim das rosas n. 32"	"Lisboa"		"1675"	"Portugal"
10550	"GODOS"	7	"1997-05-28"	"1997-06-25"	"1997-06-06"	3	4.32	"Godos Cocina Típica"	"C/ Romero, 33"	"Sevilla"		"41101"	"Spain"
10549	"QUICK"	5	"1997-05-27"	"1997-06-10"	"1997-05-30"	1	171.24	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10548	"TOMSP"	3	"1997-05-26"	"1997-06-23"	"1997-06-02"	2	1.43	"Toms Spezialitäten"	"Luisenstr. 48"	"Münster"		"44087"	"Germany"
10546	"VICTE"	1	"1997-05-23"	"1997-06-20"	"1997-05-27"	3	194.72	"Victuailles en stock"	"2, rue du Commerce"	"Lyon"		"69004"	"France"
10547	"SEVES"	3	"1997-05-23"	"1997-06-20"	"1997-06-02"	2	178.43	"Seven Seas Imports"	"90 Wadhurst Rd."	"London"		"OX15 4NB"	"UK"
10545	"LAZYK"	8	"1997-05-22"	"1997-06-19"	"1997-06-26"	2	11.92	"Lazy K Kountry Store"	"12 Orchestra Terrace"	"Walla Walla"	"WA"	"99362"	"USA"
10543	"LILAS"	8	"1997-05-21"	"1997-06-18"	"1997-05-23"	2	48.17	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
10544	"LONEP"	4	"1997-05-21"	"1997-06-18"	"1997-05-30"	1	24.91	"Lonesome Pine Restaurant"	"89 Chiaroscuro Rd."	"Portland"	"OR"	"97219"	"USA"
10542	"KOENE"	1	"1997-05-20"	"1997-06-17"	"1997-05-26"	3	10.95	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
10541	"HANAR"	2	"1997-05-19"	"1997-06-16"	"1997-05-29"	1	68.65	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
10540	"QUICK"	3	"1997-05-19"	"1997-06-16"	"1997-06-13"	3	1007.64	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10539	"BSBEV"	6	"1997-05-16"	"1997-06-13"	"1997-05-23"	3	12.36	"B's Beverages"	"Fauntleroy Circus"	"London"		"EC2 5NT"	"UK"
10538	"BSBEV"	9	"1997-05-15"	"1997-06-12"	"1997-05-16"	3	4.87	"B's Beverages"	"Fauntleroy Circus"	"London"		"EC2 5NT"	"UK"
10537	"RICSU"	1	"1997-05-14"	"1997-05-28"	"1997-05-19"	1	78.85	"Richter Supermarkt"	"Starenweg 5"	"Genève"		"1204"	"Switzerland"
10536	"LEHMS"	3	"1997-05-14"	"1997-06-11"	"1997-06-06"	2	58.88	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10535	"ANTON"	4	"1997-05-13"	"1997-06-10"	"1997-05-21"	1	15.64	"Antonio Moreno Taquería"	"Mataderos  2312"	"México D.F."		"05023"	"Mexico"
10533	"FOLKO"	8	"1997-05-12"	"1997-06-09"	"1997-05-22"	1	188.04	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10534	"LEHMS"	8	"1997-05-12"	"1997-06-09"	"1997-05-14"	2	27.94	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10532	"EASTC"	7	"1997-05-09"	"1997-06-06"	"1997-05-12"	3	74.46	"Eastern Connection"	"35 King George"	"London"		"WX3 6FW"	"UK"
10531	"OCEAN"	7	"1997-05-08"	"1997-06-05"	"1997-05-19"	1	8.12	"Océano Atlántico Ltda."	"Ing. Gustavo Moncada 8585 Piso 20-A"	"Buenos Aires"		"1010"	"Argentina"
10530	"PICCO"	3	"1997-05-08"	"1997-06-05"	"1997-05-12"	2	339.22	"Piccolo und mehr"	"Geislweg 14"	"Salzburg"		"5020"	"Austria"
10529	"MAISD"	5	"1997-05-07"	"1997-06-04"	"1997-05-09"	2	66.69	"Maison Dewey"	"Rue Joseph-Bens 532"	"Bruxelles"		"B-1180"	"Belgium"
10528	"GREAL"	6	"1997-05-06"	"1997-05-20"	"1997-05-09"	2	3.35	"Great Lakes Food Market"	"2732 Baker Blvd."	"Eugene"	"OR"	"97403"	"USA"
10526	"WARTH"	4	"1997-05-05"	"1997-06-02"	"1997-05-15"	2	58.59	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10527	"QUICK"	7	"1997-05-05"	"1997-06-02"	"1997-05-07"	1	41.9	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10525	"BONAP"	1	"1997-05-02"	"1997-05-30"	"1997-05-23"	2	11.06	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10523	"SEVES"	7	"1997-05-01"	"1997-05-29"	"1997-05-30"	2	77.63	"Seven Seas Imports"	"90 Wadhurst Rd."	"London"		"OX15 4NB"	"UK"
10524	"BERGS"	1	"1997-05-01"	"1997-05-29"	"1997-05-07"	2	244.79	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10522	"LEHMS"	4	"1997-04-30"	"1997-05-28"	"1997-05-06"	1	45.33	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10521	"CACTU"	8	"1997-04-29"	"1997-05-27"	"1997-05-02"	2	17.22	"Cactus Comidas para llevar"	"Cerrito 333"	"Buenos Aires"		"1010"	"Argentina"
10520	"SANTG"	7	"1997-04-29"	"1997-05-27"	"1997-05-01"	1	13.37	"Santé Gourmet"	"Erling Skakkes gate 78"	"Stavern"		"4110"	"Norway"
10519	"CHOPS"	6	"1997-04-28"	"1997-05-26"	"1997-05-01"	3	91.76	"Chop-suey Chinese"	"Hauptstr. 31"	"Bern"		"3012"	"Switzerland"
10518	"TORTU"	4	"1997-04-25"	"1997-05-09"	"1997-05-05"	2	218.15	"Tortuga Restaurante"	"Avda. Azteca 123"	"México D.F."		"05033"	"Mexico"
10516	"HUNGO"	2	"1997-04-24"	"1997-05-22"	"1997-05-01"	3	62.78	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10517	"NORTS"	3	"1997-04-24"	"1997-05-22"	"1997-04-29"	3	32.07	"North/South"	"South House 300 Queensbridge"	"London"		"SW7 1RZ"	"UK"
10515	"QUICK"	2	"1997-04-23"	"1997-05-07"	"1997-05-23"	1	204.47	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10513	"WANDK"	7	"1997-04-22"	"1997-06-03"	"1997-04-28"	1	105.65	"Die Wandernde Kuh"	"Adenauerallee 900"	"Stuttgart"		"70563"	"Germany"
10514	"ERNSH"	3	"1997-04-22"	"1997-05-20"	"1997-05-16"	2	789.95	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10512	"FAMIA"	7	"1997-04-21"	"1997-05-19"	"1997-04-24"	2	3.53	"Familia Arquibaldo"	"Rua Orós, 92"	"Sao Paulo"	"SP"	"05442-030"	"Brazil"
10511	"BONAP"	4	"1997-04-18"	"1997-05-16"	"1997-04-21"	3	350.64	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10510	"SAVEA"	6	"1997-04-18"	"1997-05-16"	"1997-04-28"	3	367.63	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10509	"BLAUS"	4	"1997-04-17"	"1997-05-15"	"1997-04-29"	1	0.15	"Blauer See Delikatessen"	"Forsterstr. 57"	"Mannheim"		"68306"	"Germany"
10508	"OTTIK"	1	"1997-04-16"	"1997-05-14"	"1997-05-13"	2	4.99	"Ottilies Käseladen"	"Mehrheimerstr. 369"	"Köln"		"50739"	"Germany"
10507	"ANTON"	7	"1997-04-15"	"1997-05-13"	"1997-04-22"	1	47.45	"Antonio Moreno Taquería"	"Mataderos  2312"	"México D.F."		"05023"	"Mexico"
10506	"KOENE"	9	"1997-04-15"	"1997-05-13"	"1997-05-02"	2	21.19	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
10505	"MEREP"	3	"1997-04-14"	"1997-05-12"	"1997-04-21"	3	7.13	"Mère Paillarde"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"
10504	"WHITC"	4	"1997-04-11"	"1997-05-09"	"1997-04-18"	3	59.13	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
10503	"HUNGO"	6	"1997-04-11"	"1997-05-09"	"1997-04-16"	2	16.74	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10502	"PERIC"	2	"1997-04-10"	"1997-05-08"	"1997-04-29"	1	69.32	"Pericles Comidas clásicas"	"Calle Dr. Jorge Cash 321"	"México D.F."		"05033"	"Mexico"
10501	"BLAUS"	9	"1997-04-09"	"1997-05-07"	"1997-04-16"	3	8.85	"Blauer See Delikatessen"	"Forsterstr. 57"	"Mannheim"		"68306"	"Germany"
10500	"LAMAI"	6	"1997-04-09"	"1997-05-07"	"1997-04-17"	1	42.68	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
10499	"LILAS"	4	"1997-04-08"	"1997-05-06"	"1997-04-16"	2	102.02	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
10498	"HILAA"	8	"1997-04-07"	"1997-05-05"	"1997-04-11"	2	29.75	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10496	"TRADH"	7	"1997-04-04"	"1997-05-02"	"1997-04-07"	2	46.77	"Tradiçao Hipermercados"	"Av. Inês de Castro, 414"	"Sao Paulo"	"SP"	"05634-030"	"Brazil"
10497	"LEHMS"	7	"1997-04-04"	"1997-05-02"	"1997-04-07"	1	36.21	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10495	"LAUGB"	3	"1997-04-03"	"1997-05-01"	"1997-04-11"	3	4.65	"Laughing Bacchus Wine Cellars"	"2319 Elm St."	"Vancouver"	"BC"	"V3F 2K1"	"Canada"
10493	"LAMAI"	4	"1997-04-02"	"1997-04-30"	"1997-04-10"	3	10.64	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
10494	"COMMI"	4	"1997-04-02"	"1997-04-30"	"1997-04-09"	2	65.99	"Comércio Mineiro"	"Av. dos Lusíadas, 23"	"Sao Paulo"	"SP"	"05432-043"	"Brazil"
10492	"BOTTM"	3	"1997-04-01"	"1997-04-29"	"1997-04-11"	1	62.89	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
10491	"FURIB"	8	"1997-03-31"	"1997-04-28"	"1997-04-08"	3	16.96	"Furia Bacalhau e Frutos do Mar"	"Jardim das rosas n. 32"	"Lisboa"		"1675"	"Portugal"
10490	"HILAA"	7	"1997-03-31"	"1997-04-28"	"1997-04-03"	2	210.19	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10489	"PICCO"	6	"1997-03-28"	"1997-04-25"	"1997-04-09"	2	5.29	"Piccolo und mehr"	"Geislweg 14"	"Salzburg"		"5020"	"Austria"
10488	"FRANK"	8	"1997-03-27"	"1997-04-24"	"1997-04-02"	2	4.93	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10486	"HILAA"	1	"1997-03-26"	"1997-04-23"	"1997-04-02"	2	30.53	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10487	"QUEEN"	2	"1997-03-26"	"1997-04-23"	"1997-03-28"	2	71.07	"Queen Cozinha"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"
10485	"LINOD"	4	"1997-03-25"	"1997-04-08"	"1997-03-31"	2	64.45	"LINO-Delicateses"	"Ave. 5 de Mayo Porlamar"	"I. de Margarita"	"Nueva Esparta"	"4980"	"Venezuela"
10484	"BSBEV"	3	"1997-03-24"	"1997-04-21"	"1997-04-01"	3	6.88	"B's Beverages"	"Fauntleroy Circus"	"London"		"EC2 5NT"	"UK"
10483	"WHITC"	7	"1997-03-24"	"1997-04-21"	"1997-04-25"	2	15.28	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
10482	"LAZYK"	1	"1997-03-21"	"1997-04-18"	"1997-04-10"	3	7.48	"Lazy K Kountry Store"	"12 Orchestra Terrace"	"Walla Walla"	"WA"	"99362"	"USA"
10481	"RICAR"	8	"1997-03-20"	"1997-04-17"	"1997-03-25"	2	64.33	"Ricardo Adocicados"	"Av. Copacabana, 267"	"Rio de Janeiro"	"RJ"	"02389-890"	"Brazil"
10480	"FOLIG"	6	"1997-03-20"	"1997-04-17"	"1997-03-24"	2	1.35	"Folies gourmandes"	"184, chaussée de Tournai"	"Lille"		"59000"	"France"
10479	"RATTC"	3	"1997-03-19"	"1997-04-16"	"1997-03-21"	3	708.95	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10478	"VICTE"	2	"1997-03-18"	"1997-04-01"	"1997-03-26"	3	4.81	"Victuailles en stock"	"2, rue du Commerce"	"Lyon"		"69004"	"France"
10476	"HILAA"	8	"1997-03-17"	"1997-04-14"	"1997-03-24"	3	4.41	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10477	"PRINI"	5	"1997-03-17"	"1997-04-14"	"1997-03-25"	2	13.02	"Princesa Isabel Vinhos"	"Estrada da saúde n. 58"	"Lisboa"		"1756"	"Portugal"
10475	"SUPRD"	9	"1997-03-14"	"1997-04-11"	"1997-04-04"	1	68.52	"Suprêmes délices"	"Boulevard Tirou, 255"	"Charleroi"		"B-6000"	"Belgium"
10473	"ISLAT"	1	"1997-03-13"	"1997-03-27"	"1997-03-21"	3	16.37	"Island Trading"	"Garden House Crowther Way"	"Cowes"	"Isle of Wight"	"PO31 7PJ"	"UK"
10474	"PERIC"	5	"1997-03-13"	"1997-04-10"	"1997-03-21"	2	83.49	"Pericles Comidas clásicas"	"Calle Dr. Jorge Cash 321"	"México D.F."		"05033"	"Mexico"
10472	"SEVES"	8	"1997-03-12"	"1997-04-09"	"1997-03-19"	1	4.2	"Seven Seas Imports"	"90 Wadhurst Rd."	"London"		"OX15 4NB"	"UK"
10471	"BSBEV"	2	"1997-03-11"	"1997-04-08"	"1997-03-18"	3	45.59	"B's Beverages"	"Fauntleroy Circus"	"London"		"EC2 5NT"	"UK"
10470	"BONAP"	4	"1997-03-11"	"1997-04-08"	"1997-03-14"	2	64.56	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10469	"WHITC"	1	"1997-03-10"	"1997-04-07"	"1997-03-14"	1	60.18	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
10468	"KOENE"	3	"1997-03-07"	"1997-04-04"	"1997-03-12"	3	44.12	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
10466	"COMMI"	4	"1997-03-06"	"1997-04-03"	"1997-03-13"	1	11.93	"Comércio Mineiro"	"Av. dos Lusíadas, 23"	"Sao Paulo"	"SP"	"05432-043"	"Brazil"
10467	"MAGAA"	8	"1997-03-06"	"1997-04-03"	"1997-03-11"	2	4.93	"Magazzini Alimentari Riuniti"	"Via Ludovico il Moro 22"	"Bergamo"		"24100"	"Italy"
10465	"VAFFE"	1	"1997-03-05"	"1997-04-02"	"1997-03-14"	3	145.04	"Vaffeljernet"	"Smagsloget 45"	"Århus"		"8200"	"Denmark"
10463	"SUPRD"	5	"1997-03-04"	"1997-04-01"	"1997-03-06"	3	14.78	"Suprêmes délices"	"Boulevard Tirou, 255"	"Charleroi"		"B-6000"	"Belgium"
10464	"FURIB"	4	"1997-03-04"	"1997-04-01"	"1997-03-14"	2	89	"Furia Bacalhau e Frutos do Mar"	"Jardim das rosas n. 32"	"Lisboa"		"1675"	"Portugal"
10462	"CONSH"	2	"1997-03-03"	"1997-03-31"	"1997-03-18"	1	6.17	"Consolidated Holdings"	"Berkeley Gardens 12  Brewery"	"London"		"WX1 6LT"	"UK"
10461	"LILAS"	1	"1997-02-28"	"1997-03-28"	"1997-03-05"	3	148.61	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
10460	"FOLKO"	8	"1997-02-28"	"1997-03-28"	"1997-03-03"	1	16.27	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10459	"VICTE"	4	"1997-02-27"	"1997-03-27"	"1997-02-28"	2	25.09	"Victuailles en stock"	"2, rue du Commerce"	"Lyon"		"69004"	"France"
10458	"SUPRD"	7	"1997-02-26"	"1997-03-26"	"1997-03-04"	3	147.06	"Suprêmes délices"	"Boulevard Tirou, 255"	"Charleroi"		"B-6000"	"Belgium"
10456	"KOENE"	8	"1997-02-25"	"1997-04-08"	"1997-02-28"	2	8.12	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
10457	"KOENE"	2	"1997-02-25"	"1997-03-25"	"1997-03-03"	1	11.57	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
10455	"WARTH"	8	"1997-02-24"	"1997-04-07"	"1997-03-03"	2	180.45	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10454	"LAMAI"	4	"1997-02-21"	"1997-03-21"	"1997-02-25"	3	2.74	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
10453	"AROUT"	1	"1997-02-21"	"1997-03-21"	"1997-02-26"	2	25.36	"Around the Horn"	"Brook Farm Stratford St. Mary"	"Colchester"	"Essex"	"CO7 6JX"	"UK"
10452	"SAVEA"	8	"1997-02-20"	"1997-03-20"	"1997-02-26"	1	140.26	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10450	"VICTE"	8	"1997-02-19"	"1997-03-19"	"1997-03-11"	2	7.23	"Victuailles en stock"	"2, rue du Commerce"	"Lyon"		"69004"	"France"
10451	"QUICK"	4	"1997-02-19"	"1997-03-05"	"1997-03-12"	3	189.09	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10449	"BLONP"	3	"1997-02-18"	"1997-03-18"	"1997-02-27"	2	53.3	"Blondel père et fils"	"24, place Kléber"	"Strasbourg"		"67000"	"France"
10448	"RANCH"	4	"1997-02-17"	"1997-03-17"	"1997-02-24"	2	38.82	"Rancho grande"	"Av. del Libertador 900"	"Buenos Aires"		"1010"	"Argentina"
10446	"TOMSP"	6	"1997-02-14"	"1997-03-14"	"1997-02-19"	1	14.68	"Toms Spezialitäten"	"Luisenstr. 48"	"Münster"		"44087"	"Germany"
10447	"RICAR"	4	"1997-02-14"	"1997-03-14"	"1997-03-07"	2	68.66	"Ricardo Adocicados"	"Av. Copacabana, 267"	"Rio de Janeiro"	"RJ"	"02389-890"	"Brazil"
10445	"BERGS"	3	"1997-02-13"	"1997-03-13"	"1997-02-20"	1	9.3	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10443	"REGGC"	8	"1997-02-12"	"1997-03-12"	"1997-02-14"	1	13.95	"Reggiani Caseifici"	"Strada Provinciale 124"	"Reggio Emilia"		"42100"	"Italy"
10444	"BERGS"	3	"1997-02-12"	"1997-03-12"	"1997-02-21"	3	3.5	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10442	"ERNSH"	3	"1997-02-11"	"1997-03-11"	"1997-02-18"	2	47.94	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10441	"OLDWO"	3	"1997-02-10"	"1997-03-24"	"1997-03-14"	2	73.02	"Old World Delicatessen"	"2743 Bering St."	"Anchorage"	"AK"	"99508"	"USA"
10440	"SAVEA"	4	"1997-02-10"	"1997-03-10"	"1997-02-28"	2	86.53	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10439	"MEREP"	6	"1997-02-07"	"1997-03-07"	"1997-02-10"	3	4.07	"Mère Paillarde"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"
10438	"TOMSP"	3	"1997-02-06"	"1997-03-06"	"1997-02-14"	2	8.24	"Toms Spezialitäten"	"Luisenstr. 48"	"Münster"		"44087"	"Germany"
10436	"BLONP"	3	"1997-02-05"	"1997-03-05"	"1997-02-11"	2	156.66	"Blondel père et fils"	"24, place Kléber"	"Strasbourg"		"67000"	"France"
10437	"WARTH"	8	"1997-02-05"	"1997-03-05"	"1997-02-12"	1	19.97	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10435	"CONSH"	8	"1997-02-04"	"1997-03-18"	"1997-02-07"	2	9.21	"Consolidated Holdings"	"Berkeley Gardens 12  Brewery"	"London"		"WX1 6LT"	"UK"
10433	"PRINI"	3	"1997-02-03"	"1997-03-03"	"1997-03-04"	3	73.83	"Princesa Isabel Vinhos"	"Estrada da saúde n. 58"	"Lisboa"		"1756"	"Portugal"
10434	"FOLKO"	3	"1997-02-03"	"1997-03-03"	"1997-02-13"	2	17.92	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10432	"SPLIR"	3	"1997-01-31"	"1997-02-14"	"1997-02-07"	2	4.34	"Split Rail Beer & Ale"	"P.O. Box 555"	"Lander"	"WY"	"82520"	"USA"
10431	"BOTTM"	4	"1997-01-30"	"1997-02-13"	"1997-02-07"	2	44.17	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
10430	"ERNSH"	4	"1997-01-30"	"1997-02-13"	"1997-02-03"	1	458.78	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10429	"HUNGO"	3	"1997-01-29"	"1997-03-12"	"1997-02-07"	2	56.63	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10428	"REGGC"	7	"1997-01-28"	"1997-02-25"	"1997-02-04"	1	11.09	"Reggiani Caseifici"	"Strada Provinciale 124"	"Reggio Emilia"		"42100"	"Italy"
10427	"PICCO"	4	"1997-01-27"	"1997-02-24"	"1997-03-03"	2	31.29	"Piccolo und mehr"	"Geislweg 14"	"Salzburg"		"5020"	"Austria"
10426	"GALED"	4	"1997-01-27"	"1997-02-24"	"1997-02-06"	1	18.69	"Galería del gastronómo"	"Rambla de Cataluña, 23"	"Barcelona"		"8022"	"Spain"
10425	"LAMAI"	6	"1997-01-24"	"1997-02-21"	"1997-02-14"	2	7.93	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
10423	"GOURL"	6	"1997-01-23"	"1997-02-06"	"1997-02-24"	3	24.5	"Gourmet Lanchonetes"	"Av. Brasil, 442"	"Campinas"	"SP"	"04876-786"	"Brazil"
10424	"MEREP"	7	"1997-01-23"	"1997-02-20"	"1997-01-27"	2	370.61	"Mère Paillarde"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"
10422	"FRANS"	2	"1997-01-22"	"1997-02-19"	"1997-01-31"	1	3.02	"Franchi S.p.A."	"Via Monte Bianco 34"	"Torino"		"10100"	"Italy"
10421	"QUEDE"	8	"1997-01-21"	"1997-03-04"	"1997-01-27"	1	99.23	"Que Delícia"	"Rua da Panificadora, 12"	"Rio de Janeiro"	"RJ"	"02389-673"	"Brazil"
10420	"WELLI"	3	"1997-01-21"	"1997-02-18"	"1997-01-27"	1	44.12	"Wellington Importadora"	"Rua do Mercado, 12"	"Resende"	"SP"	"08737-363"	"Brazil"
10419	"RICSU"	4	"1997-01-20"	"1997-02-17"	"1997-01-30"	2	137.35	"Richter Supermarkt"	"Starenweg 5"	"Genève"		"1204"	"Switzerland"
10418	"QUICK"	4	"1997-01-17"	"1997-02-14"	"1997-01-24"	1	17.55	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10416	"WARTH"	8	"1997-01-16"	"1997-02-13"	"1997-01-27"	3	22.72	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10417	"SIMOB"	4	"1997-01-16"	"1997-02-13"	"1997-01-28"	3	70.29	"Simons bistro"	"Vinbæltet 34"	"Kobenhavn"		"1734"	"Denmark"
10415	"HUNGC"	3	"1997-01-15"	"1997-02-12"	"1997-01-24"	1	0.2	"Hungry Coyote Import Store"	"City Center Plaza 516 Main St."	"Elgin"	"OR"	"97827"	"USA"
10413	"LAMAI"	3	"1997-01-14"	"1997-02-11"	"1997-01-16"	2	95.66	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
10414	"FAMIA"	2	"1997-01-14"	"1997-02-11"	"1997-01-17"	3	21.48	"Familia Arquibaldo"	"Rua Orós, 92"	"Sao Paulo"	"SP"	"05442-030"	"Brazil"
10412	"WARTH"	8	"1997-01-13"	"1997-02-10"	"1997-01-15"	2	3.77	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10411	"BOTTM"	9	"1997-01-10"	"1997-02-07"	"1997-01-21"	3	23.65	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
10410	"BOTTM"	3	"1997-01-10"	"1997-02-07"	"1997-01-15"	3	2.4	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
10409	"OCEAN"	3	"1997-01-09"	"1997-02-06"	"1997-01-14"	1	29.83	"Océano Atlántico Ltda."	"Ing. Gustavo Moncada 8585 Piso 20-A"	"Buenos Aires"		"1010"	"Argentina"
10408	"FOLIG"	8	"1997-01-08"	"1997-02-05"	"1997-01-14"	1	11.26	"Folies gourmandes"	"184, chaussée de Tournai"	"Lille"		"59000"	"France"
10406	"QUEEN"	7	"1997-01-07"	"1997-02-18"	"1997-01-13"	1	108.04	"Queen Cozinha"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"
10407	"OTTIK"	2	"1997-01-07"	"1997-02-04"	"1997-01-30"	2	91.48	"Ottilies Käseladen"	"Mehrheimerstr. 369"	"Köln"		"50739"	"Germany"
10405	"LINOD"	1	"1997-01-06"	"1997-02-03"	"1997-01-22"	1	34.82	"LINO-Delicateses"	"Ave. 5 de Mayo Porlamar"	"I. de Margarita"	"Nueva Esparta"	"4980"	"Venezuela"
10403	"ERNSH"	4	"1997-01-03"	"1997-01-31"	"1997-01-09"	3	73.79	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10404	"MAGAA"	2	"1997-01-03"	"1997-01-31"	"1997-01-08"	1	155.97	"Magazzini Alimentari Riuniti"	"Via Ludovico il Moro 22"	"Bergamo"		"24100"	"Italy"
10402	"ERNSH"	8	"1997-01-02"	"1997-02-13"	"1997-01-10"	2	67.88	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10401	"RATTC"	1	"1997-01-01"	"1997-01-29"	"1997-01-10"	1	12.51	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10400	"EASTC"	1	"1997-01-01"	"1997-01-29"	"1997-01-16"	3	83.93	"Eastern Connection"	"35 King George"	"London"		"WX3 6FW"	"UK"
10399	"VAFFE"	8	"1996-12-31"	"1997-01-14"	"1997-01-08"	3	27.36	"Vaffeljernet"	"Smagsloget 45"	"Århus"		"8200"	"Denmark"
10398	"SAVEA"	2	"1996-12-30"	"1997-01-27"	"1997-01-09"	3	89.16	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10396	"FRANK"	1	"1996-12-27"	"1997-01-10"	"1997-01-06"	3	135.35	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10397	"PRINI"	5	"1996-12-27"	"1997-01-24"	"1997-01-02"	1	60.26	"Princesa Isabel Vinhos"	"Estrada da saúde n. 58"	"Lisboa"		"1756"	"Portugal"
10395	"HILAA"	6	"1996-12-26"	"1997-01-23"	"1997-01-03"	1	184.41	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10393	"SAVEA"	1	"1996-12-25"	"1997-01-22"	"1997-01-03"	3	126.56	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10394	"HUNGC"	1	"1996-12-25"	"1997-01-22"	"1997-01-03"	3	30.34	"Hungry Coyote Import Store"	"City Center Plaza 516 Main St."	"Elgin"	"OR"	"97827"	"USA"
10392	"PICCO"	2	"1996-12-24"	"1997-01-21"	"1997-01-01"	3	122.46	"Piccolo und mehr"	"Geislweg 14"	"Salzburg"		"5020"	"Austria"
10391	"DRACD"	3	"1996-12-23"	"1997-01-20"	"1996-12-31"	3	5.45	"Drachenblut Delikatessen"	"Walserweg 21"	"Aachen"		"52066"	"Germany"
10390	"ERNSH"	6	"1996-12-23"	"1997-01-20"	"1996-12-26"	1	126.38	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10389	"BOTTM"	4	"1996-12-20"	"1997-01-17"	"1996-12-24"	2	47.42	"Bottom-Dollar Markets"	"23 Tsawassen Blvd."	"Tsawassen"	"BC"	"T2F 8M4"	"Canada"
10388	"SEVES"	2	"1996-12-19"	"1997-01-16"	"1996-12-20"	1	34.86	"Seven Seas Imports"	"90 Wadhurst Rd."	"London"		"OX15 4NB"	"UK"
10386	"FAMIA"	9	"1996-12-18"	"1997-01-01"	"1996-12-25"	3	13.99	"Familia Arquibaldo"	"Rua Orós, 92"	"Sao Paulo"	"SP"	"05442-030"	"Brazil"
10387	"SANTG"	1	"1996-12-18"	"1997-01-15"	"1996-12-20"	2	93.63	"Santé Gourmet"	"Erling Skakkes gate 78"	"Stavern"		"4110"	"Norway"
10385	"SPLIR"	1	"1996-12-17"	"1997-01-14"	"1996-12-23"	2	30.96	"Split Rail Beer & Ale"	"P.O. Box 555"	"Lander"	"WY"	"82520"	"USA"
10383	"AROUT"	8	"1996-12-16"	"1997-01-13"	"1996-12-18"	3	34.24	"Around the Horn"	"Brook Farm Stratford St. Mary"	"Colchester"	"Essex"	"CO7 6JX"	"UK"
10384	"BERGS"	3	"1996-12-16"	"1997-01-13"	"1996-12-20"	3	168.64	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10382	"ERNSH"	4	"1996-12-13"	"1997-01-10"	"1996-12-16"	1	94.77	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10381	"LILAS"	3	"1996-12-12"	"1997-01-09"	"1996-12-13"	3	7.99	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
10380	"HUNGO"	8	"1996-12-12"	"1997-01-09"	"1997-01-16"	3	35.03	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10379	"QUEDE"	2	"1996-12-11"	"1997-01-08"	"1996-12-13"	1	45.03	"Que Delícia"	"Rua da Panificadora, 12"	"Rio de Janeiro"	"RJ"	"02389-673"	"Brazil"
10378	"FOLKO"	5	"1996-12-10"	"1997-01-07"	"1996-12-19"	3	5.44	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10377	"SEVES"	1	"1996-12-09"	"1997-01-06"	"1996-12-13"	3	22.21	"Seven Seas Imports"	"90 Wadhurst Rd."	"London"		"OX15 4NB"	"UK"
10376	"MEREP"	1	"1996-12-09"	"1997-01-06"	"1996-12-13"	2	20.39	"Mère Paillarde"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"
10375	"HUNGC"	3	"1996-12-06"	"1997-01-03"	"1996-12-09"	2	20.12	"Hungry Coyote Import Store"	"City Center Plaza 516 Main St."	"Elgin"	"OR"	"97827"	"USA"
10374	"WOLZA"	1	"1996-12-05"	"1997-01-02"	"1996-12-09"	3	3.94	"Wolski Zajazd"	"ul. Filtrowa 68"	"Warszawa"		"01-012"	"Poland"
10373	"HUNGO"	4	"1996-12-05"	"1997-01-02"	"1996-12-11"	3	124.12	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10372	"QUEEN"	5	"1996-12-04"	"1997-01-01"	"1996-12-09"	2	890.78	"Queen Cozinha"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"
10371	"LAMAI"	1	"1996-12-03"	"1996-12-31"	"1996-12-24"	1	0.45	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
10370	"CHOPS"	6	"1996-12-03"	"1996-12-31"	"1996-12-27"	2	1.17	"Chop-suey Chinese"	"Hauptstr. 31"	"Bern"		"3012"	"Switzerland"
10369	"SPLIR"	8	"1996-12-02"	"1996-12-30"	"1996-12-09"	2	195.68	"Split Rail Beer & Ale"	"P.O. Box 555"	"Lander"	"WY"	"82520"	"USA"
10368	"ERNSH"	2	"1996-11-29"	"1996-12-27"	"1996-12-02"	2	101.95	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10366	"GALED"	8	"1996-11-28"	"1997-01-09"	"1996-12-30"	2	10.14	"Galería del gastronómo"	"Rambla de Cataluña, 23"	"Barcelona"		"8022"	"Spain"
10367	"VAFFE"	7	"1996-11-28"	"1996-12-26"	"1996-12-02"	3	13.55	"Vaffeljernet"	"Smagsloget 45"	"Århus"		"8200"	"Denmark"
10365	"ANTON"	3	"1996-11-27"	"1996-12-25"	"1996-12-02"	2	22	"Antonio Moreno Taquería"	"Mataderos  2312"	"México D.F."		"05023"	"Mexico"
10363	"DRACD"	4	"1996-11-26"	"1996-12-24"	"1996-12-04"	3	30.54	"Drachenblut Delikatessen"	"Walserweg 21"	"Aachen"		"52066"	"Germany"
10364	"EASTC"	1	"1996-11-26"	"1997-01-07"	"1996-12-04"	1	71.97	"Eastern Connection"	"35 King George"	"London"		"WX3 6FW"	"UK"
10362	"BONAP"	3	"1996-11-25"	"1996-12-23"	"1996-11-28"	1	96.04	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10360	"BLONP"	4	"1996-11-22"	"1996-12-20"	"1996-12-02"	3	131.7	"Blondel père et fils"	"24, place Kléber"	"Strasbourg"		"67000"	"France"
10361	"QUICK"	1	"1996-11-22"	"1996-12-20"	"1996-12-03"	2	183.17	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10359	"SEVES"	5	"1996-11-21"	"1996-12-19"	"1996-11-26"	3	288.43	"Seven Seas Imports"	"90 Wadhurst Rd."	"London"		"OX15 4NB"	"UK"
10358	"LAMAI"	5	"1996-11-20"	"1996-12-18"	"1996-11-27"	1	19.64	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
10357	"LILAS"	1	"1996-11-19"	"1996-12-17"	"1996-12-02"	3	34.88	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
10356	"WANDK"	6	"1996-11-18"	"1996-12-16"	"1996-11-27"	2	36.71	"Die Wandernde Kuh"	"Adenauerallee 900"	"Stuttgart"		"70563"	"Germany"
10355	"AROUT"	6	"1996-11-15"	"1996-12-13"	"1996-11-20"	1	41.95	"Around the Horn"	"Brook Farm Stratford St. Mary"	"Colchester"	"Essex"	"CO7 6JX"	"UK"
10354	"PERIC"	8	"1996-11-14"	"1996-12-12"	"1996-11-20"	3	53.8	"Pericles Comidas clásicas"	"Calle Dr. Jorge Cash 321"	"México D.F."		"05033"	"Mexico"
10353	"PICCO"	7	"1996-11-13"	"1996-12-11"	"1996-11-25"	3	360.63	"Piccolo und mehr"	"Geislweg 14"	"Salzburg"		"5020"	"Austria"
10352	"FURIB"	3	"1996-11-12"	"1996-11-26"	"1996-11-18"	3	1.3	"Furia Bacalhau e Frutos do Mar"	"Jardim das rosas n. 32"	"Lisboa"		"1675"	"Portugal"
10351	"ERNSH"	1	"1996-11-11"	"1996-12-09"	"1996-11-20"	1	162.33	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10350	"LAMAI"	6	"1996-11-11"	"1996-12-09"	"1996-12-03"	2	64.19	"La maison d'Asie"	"1 rue Alsace-Lorraine"	"Toulouse"		"31000"	"France"
10349	"SPLIR"	7	"1996-11-08"	"1996-12-06"	"1996-11-15"	1	8.63	"Split Rail Beer & Ale"	"P.O. Box 555"	"Lander"	"WY"	"82520"	"USA"
10348	"WANDK"	4	"1996-11-07"	"1996-12-05"	"1996-11-15"	2	0.78	"Die Wandernde Kuh"	"Adenauerallee 900"	"Stuttgart"		"70563"	"Germany"
10347	"FAMIA"	4	"1996-11-06"	"1996-12-04"	"1996-11-08"	3	3.1	"Familia Arquibaldo"	"Rua Orós, 92"	"Sao Paulo"	"SP"	"05442-030"	"Brazil"
10346	"RATTC"	3	"1996-11-05"	"1996-12-17"	"1996-11-08"	3	142.08	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10345	"QUICK"	2	"1996-11-04"	"1996-12-02"	"1996-11-11"	2	249.06	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10344	"WHITC"	4	"1996-11-01"	"1996-11-29"	"1996-11-05"	2	23.29	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
10343	"LEHMS"	4	"1996-10-31"	"1996-11-28"	"1996-11-06"	1	110.37	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10342	"FRANK"	4	"1996-10-30"	"1996-11-13"	"1996-11-04"	2	54.83	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10341	"SIMOB"	7	"1996-10-29"	"1996-11-26"	"1996-11-05"	3	26.78	"Simons bistro"	"Vinbæltet 34"	"Kobenhavn"		"1734"	"Denmark"
10340	"BONAP"	1	"1996-10-29"	"1996-11-26"	"1996-11-08"	3	166.31	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10339	"MEREP"	2	"1996-10-28"	"1996-11-25"	"1996-11-04"	2	15.66	"Mère Paillarde"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"
10338	"OLDWO"	4	"1996-10-25"	"1996-11-22"	"1996-10-29"	3	84.21	"Old World Delicatessen"	"2743 Bering St."	"Anchorage"	"AK"	"99508"	"USA"
10337	"FRANK"	4	"1996-10-24"	"1996-11-21"	"1996-10-29"	3	108.26	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10336	"PRINI"	7	"1996-10-23"	"1996-11-20"	"1996-10-25"	2	15.51	"Princesa Isabel Vinhos"	"Estrada da saúde n. 58"	"Lisboa"		"1756"	"Portugal"
10335	"HUNGO"	7	"1996-10-22"	"1996-11-19"	"1996-10-24"	2	42.11	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10334	"VICTE"	8	"1996-10-21"	"1996-11-18"	"1996-10-28"	2	8.56	"Victuailles en stock"	"2, rue du Commerce"	"Lyon"		"69004"	"France"
10333	"WARTH"	5	"1996-10-18"	"1996-11-15"	"1996-10-25"	3	0.59	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10332	"MEREP"	3	"1996-10-17"	"1996-11-28"	"1996-10-21"	2	52.84	"Mère Paillarde"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"
10331	"BONAP"	9	"1996-10-16"	"1996-11-27"	"1996-10-21"	1	10.19	"Bon app'"	"12, rue des Bouchers"	"Marseille"		"13008"	"France"
10330	"LILAS"	3	"1996-10-16"	"1996-11-13"	"1996-10-28"	1	12.75	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
10329	"SPLIR"	4	"1996-10-15"	"1996-11-26"	"1996-10-23"	2	191.67	"Split Rail Beer & Ale"	"P.O. Box 555"	"Lander"	"WY"	"82520"	"USA"
10328	"FURIB"	4	"1996-10-14"	"1996-11-11"	"1996-10-17"	3	87.03	"Furia Bacalhau e Frutos do Mar"	"Jardim das rosas n. 32"	"Lisboa"		"1675"	"Portugal"
10327	"FOLKO"	2	"1996-10-11"	"1996-11-08"	"1996-10-14"	1	63.36	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10326	"BOLID"	4	"1996-10-10"	"1996-11-07"	"1996-10-14"	2	77.92	"Bólido Comidas preparadas"	"C/ Araquil, 67"	"Madrid"		"28023"	"Spain"
10325	"KOENE"	1	"1996-10-09"	"1996-10-23"	"1996-10-14"	3	64.86	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
10324	"SAVEA"	9	"1996-10-08"	"1996-11-05"	"1996-10-10"	1	214.27	"Save-a-lot Markets"	"187 Suffolk Ln."	"Boise"	"ID"	"83720"	"USA"
10323	"KOENE"	4	"1996-10-07"	"1996-11-04"	"1996-10-14"	1	4.88	"Königlich Essen"	"Maubelstr. 90"	"Brandenburg"		"14776"	"Germany"
10322	"PERIC"	7	"1996-10-04"	"1996-11-01"	"1996-10-23"	3	0.4	"Pericles Comidas clásicas"	"Calle Dr. Jorge Cash 321"	"México D.F."		"05033"	"Mexico"
10320	"WARTH"	5	"1996-10-03"	"1996-10-17"	"1996-10-18"	3	34.57	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10321	"ISLAT"	3	"1996-10-03"	"1996-10-31"	"1996-10-11"	2	3.43	"Island Trading"	"Garden House Crowther Way"	"Cowes"	"Isle of Wight"	"PO31 7PJ"	"UK"
10319	"TORTU"	7	"1996-10-02"	"1996-10-30"	"1996-10-11"	3	64.5	"Tortuga Restaurante"	"Avda. Azteca 123"	"México D.F."		"05033"	"Mexico"
10318	"ISLAT"	8	"1996-10-01"	"1996-10-29"	"1996-10-04"	2	4.73	"Island Trading"	"Garden House Crowther Way"	"Cowes"	"Isle of Wight"	"PO31 7PJ"	"UK"
10317	"LONEP"	6	"1996-09-30"	"1996-10-28"	"1996-10-10"	1	12.69	"Lonesome Pine Restaurant"	"89 Chiaroscuro Rd."	"Portland"	"OR"	"97219"	"USA"
10316	"RATTC"	1	"1996-09-27"	"1996-10-25"	"1996-10-08"	3	150.15	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10315	"ISLAT"	4	"1996-09-26"	"1996-10-24"	"1996-10-03"	2	41.76	"Island Trading"	"Garden House Crowther Way"	"Cowes"	"Isle of Wight"	"PO31 7PJ"	"UK"
10314	"RATTC"	1	"1996-09-25"	"1996-10-23"	"1996-10-04"	2	74.16	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10313	"QUICK"	2	"1996-09-24"	"1996-10-22"	"1996-10-04"	2	1.96	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10312	"WANDK"	2	"1996-09-23"	"1996-10-21"	"1996-10-03"	2	40.26	"Die Wandernde Kuh"	"Adenauerallee 900"	"Stuttgart"		"70563"	"Germany"
10311	"DUMON"	1	"1996-09-20"	"1996-10-04"	"1996-09-26"	3	24.69	"Du monde entier"	"67, rue des Cinquante Otages"	"Nantes"		"44000"	"France"
10310	"THEBI"	8	"1996-09-20"	"1996-10-18"	"1996-09-27"	2	17.52	"The Big Cheese"	"89 Jefferson Way Suite 2"	"Portland"	"OR"	"97201"	"USA"
10309	"HUNGO"	3	"1996-09-19"	"1996-10-17"	"1996-10-23"	1	47.3	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10308	"ANATR"	7	"1996-09-18"	"1996-10-16"	"1996-09-24"	3	1.61	"Ana Trujillo Emparedados y helados"	"Avda. de la Constitución 2222"	"México D.F."		"05021"	"Mexico"
10307	"LONEP"	2	"1996-09-17"	"1996-10-15"	"1996-09-25"	2	0.56	"Lonesome Pine Restaurant"	"89 Chiaroscuro Rd."	"Portland"	"OR"	"97219"	"USA"
10306	"ROMEY"	1	"1996-09-16"	"1996-10-14"	"1996-09-23"	3	7.56	"Romero y tomillo"	"Gran Vía, 1"	"Madrid"		"28001"	"Spain"
10305	"OLDWO"	8	"1996-09-13"	"1996-10-11"	"1996-10-09"	3	257.62	"Old World Delicatessen"	"2743 Bering St."	"Anchorage"	"AK"	"99508"	"USA"
10304	"TORTU"	1	"1996-09-12"	"1996-10-10"	"1996-09-17"	2	63.79	"Tortuga Restaurante"	"Avda. Azteca 123"	"México D.F."		"05033"	"Mexico"
10303	"GODOS"	7	"1996-09-11"	"1996-10-09"	"1996-09-18"	2	107.83	"Godos Cocina Típica"	"C/ Romero, 33"	"Sevilla"		"41101"	"Spain"
10302	"SUPRD"	4	"1996-09-10"	"1996-10-08"	"1996-10-09"	2	6.27	"Suprêmes délices"	"Boulevard Tirou, 255"	"Charleroi"		"B-6000"	"Belgium"
10300	"MAGAA"	2	"1996-09-09"	"1996-10-07"	"1996-09-18"	2	17.68	"Magazzini Alimentari Riuniti"	"Via Ludovico il Moro 22"	"Bergamo"		"24100"	"Italy"
10301	"WANDK"	8	"1996-09-09"	"1996-10-07"	"1996-09-17"	2	45.08	"Die Wandernde Kuh"	"Adenauerallee 900"	"Stuttgart"		"70563"	"Germany"
10299	"RICAR"	4	"1996-09-06"	"1996-10-04"	"1996-09-13"	2	29.76	"Ricardo Adocicados"	"Av. Copacabana, 267"	"Rio de Janeiro"	"RJ"	"02389-890"	"Brazil"
10298	"HUNGO"	6	"1996-09-05"	"1996-10-03"	"1996-09-11"	2	168.22	"Hungry Owl All-Night Grocers"	"8 Johnstown Road"	"Cork"	"Co. Cork"		"Ireland"
10297	"BLONP"	5	"1996-09-04"	"1996-10-16"	"1996-09-10"	2	5.74	"Blondel père et fils"	"24, place Kléber"	"Strasbourg"		"67000"	"France"
10296	"LILAS"	6	"1996-09-03"	"1996-10-01"	"1996-09-11"	1	0.12	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
10295	"VINET"	2	"1996-09-02"	"1996-09-30"	"1996-09-10"	2	1.15	"Vins et alcools Chevalier"	"59 rue de l'Abbaye"	"Reims"		"51100"	"France"
10294	"RATTC"	4	"1996-08-30"	"1996-09-27"	"1996-09-05"	2	147.26	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10293	"TORTU"	1	"1996-08-29"	"1996-09-26"	"1996-09-11"	3	21.18	"Tortuga Restaurante"	"Avda. Azteca 123"	"México D.F."		"05033"	"Mexico"
10292	"TRADH"	1	"1996-08-28"	"1996-09-25"	"1996-09-02"	2	1.35	"Tradiçao Hipermercados"	"Av. Inês de Castro, 414"	"Sao Paulo"	"SP"	"05634-030"	"Brazil"
10291	"QUEDE"	6	"1996-08-27"	"1996-09-24"	"1996-09-04"	2	6.4	"Que Delícia"	"Rua da Panificadora, 12"	"Rio de Janeiro"	"RJ"	"02389-673"	"Brazil"
10290	"COMMI"	8	"1996-08-27"	"1996-09-24"	"1996-09-03"	1	79.7	"Comércio Mineiro"	"Av. dos Lusíadas, 23"	"Sao Paulo"	"SP"	"05432-043"	"Brazil"
10289	"BSBEV"	7	"1996-08-26"	"1996-09-23"	"1996-08-28"	3	22.77	"B's Beverages"	"Fauntleroy Circus"	"London"		"EC2 5NT"	"UK"
10288	"REGGC"	4	"1996-08-23"	"1996-09-20"	"1996-09-03"	1	7.45	"Reggiani Caseifici"	"Strada Provinciale 124"	"Reggio Emilia"		"42100"	"Italy"
10287	"RICAR"	8	"1996-08-22"	"1996-09-19"	"1996-08-28"	3	12.76	"Ricardo Adocicados"	"Av. Copacabana, 267"	"Rio de Janeiro"	"RJ"	"02389-890"	"Brazil"
10286	"QUICK"	8	"1996-08-21"	"1996-09-18"	"1996-08-30"	3	229.24	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10285	"QUICK"	1	"1996-08-20"	"1996-09-17"	"1996-08-26"	2	76.83	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10284	"LEHMS"	4	"1996-08-19"	"1996-09-16"	"1996-08-27"	1	76.56	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10283	"LILAS"	3	"1996-08-16"	"1996-09-13"	"1996-08-23"	3	84.81	"LILA-Supermercado"	"Carrera 52 con Ave. Bolívar #65-98 Llano Largo"	"Barquisimeto"	"Lara"	"3508"	"Venezuela"
10282	"ROMEY"	4	"1996-08-15"	"1996-09-12"	"1996-08-21"	1	12.69	"Romero y tomillo"	"Gran Vía, 1"	"Madrid"		"28001"	"Spain"
10280	"BERGS"	2	"1996-08-14"	"1996-09-11"	"1996-09-12"	1	8.98	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10281	"ROMEY"	4	"1996-08-14"	"1996-08-28"	"1996-08-21"	1	2.94	"Romero y tomillo"	"Gran Vía, 1"	"Madrid"		"28001"	"Spain"
10279	"LEHMS"	8	"1996-08-13"	"1996-09-10"	"1996-08-16"	2	25.83	"Lehmanns Marktstand"	"Magazinweg 7"	"Frankfurt a.M."		"60528"	"Germany"
10278	"BERGS"	8	"1996-08-12"	"1996-09-09"	"1996-08-16"	2	92.69	"Berglunds snabbköp"	"Berguvsvägen  8"	"Luleå"		"S-958 22"	"Sweden"
10277	"MORGK"	2	"1996-08-09"	"1996-09-06"	"1996-08-13"	3	125.77	"Morgenstern Gesundkost"	"Heerstr. 22"	"Leipzig"		"04179"	"Germany"
10276	"TORTU"	8	"1996-08-08"	"1996-08-22"	"1996-08-14"	3	13.84	"Tortuga Restaurante"	"Avda. Azteca 123"	"México D.F."		"05033"	"Mexico"
10275	"MAGAA"	1	"1996-08-07"	"1996-09-04"	"1996-08-09"	1	26.93	"Magazzini Alimentari Riuniti"	"Via Ludovico il Moro 22"	"Bergamo"		"24100"	"Italy"
10274	"VINET"	6	"1996-08-06"	"1996-09-03"	"1996-08-16"	1	6.01	"Vins et alcools Chevalier"	"59 rue de l'Abbaye"	"Reims"		"51100"	"France"
10273	"QUICK"	3	"1996-08-05"	"1996-09-02"	"1996-08-12"	3	76.07	"QUICK-Stop"	"Taucherstraße 10"	"Cunewalde"		"01307"	"Germany"
10272	"RATTC"	6	"1996-08-02"	"1996-08-30"	"1996-08-06"	2	98.03	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10271	"SPLIR"	6	"1996-08-01"	"1996-08-29"	"1996-08-30"	2	4.54	"Split Rail Beer & Ale"	"P.O. Box 555"	"Lander"	"WY"	"82520"	"USA"
10270	"WARTH"	1	"1996-08-01"	"1996-08-29"	"1996-08-02"	1	136.54	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10269	"WHITC"	5	"1996-07-31"	"1996-08-14"	"1996-08-09"	1	4.56	"White Clover Markets"	"1029 - 12th Ave. S."	"Seattle"	"WA"	"98124"	"USA"
10268	"GROSR"	8	"1996-07-30"	"1996-08-27"	"1996-08-02"	3	66.29	"GROSELLA-Restaurante"	"5ª Ave. Los Palos Grandes"	"Caracas"	"DF"	"1081"	"Venezuela"
10267	"FRANK"	4	"1996-07-29"	"1996-08-26"	"1996-08-06"	1	208.58	"Frankenversand"	"Berliner Platz 43"	"München"		"80805"	"Germany"
10266	"WARTH"	3	"1996-07-26"	"1996-09-06"	"1996-07-31"	3	25.73	"Wartian Herkku"	"Torikatu 38"	"Oulu"		"90110"	"Finland"
10265	"BLONP"	2	"1996-07-25"	"1996-08-22"	"1996-08-12"	1	55.28	"Blondel père et fils"	"24, place Kléber"	"Strasbourg"		"67000"	"France"
10264	"FOLKO"	6	"1996-07-24"	"1996-08-21"	"1996-08-23"	3	3.67	"Folk och fä HB"	"Åkergatan 24"	"Bräcke"		"S-844 67"	"Sweden"
10263	"ERNSH"	9	"1996-07-23"	"1996-08-20"	"1996-07-31"	3	146.06	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10262	"RATTC"	8	"1996-07-22"	"1996-08-19"	"1996-07-25"	3	48.29	"Rattlesnake Canyon Grocery"	"2817 Milton Dr."	"Albuquerque"	"NM"	"87110"	"USA"
10261	"QUEDE"	4	"1996-07-19"	"1996-08-16"	"1996-07-30"	2	3.05	"Que Delícia"	"Rua da Panificadora, 12"	"Rio de Janeiro"	"RJ"	"02389-673"	"Brazil"
10260	"OTTIK"	4	"1996-07-19"	"1996-08-16"	"1996-07-29"	1	55.09	"Ottilies Käseladen"	"Mehrheimerstr. 369"	"Köln"		"50739"	"Germany"
10259	"CENTC"	4	"1996-07-18"	"1996-08-15"	"1996-07-25"	3	3.25	"Centro comercial Moctezuma"	"Sierras de Granada 9993"	"México D.F."		"05022"	"Mexico"
10258	"ERNSH"	1	"1996-07-17"	"1996-08-14"	"1996-07-23"	1	140.51	"Ernst Handel"	"Kirchgasse 6"	"Graz"		"8010"	"Austria"
10257	"HILAA"	4	"1996-07-16"	"1996-08-13"	"1996-07-22"	3	81.91	"HILARION-Abastos"	"Carrera 22 con Ave. Carlos Soublette #8-35"	"San Cristóbal"	"Táchira"	"5022"	"Venezuela"
10256	"WELLI"	3	"1996-07-15"	"1996-08-12"	"1996-07-17"	2	13.97	"Wellington Importadora"	"Rua do Mercado, 12"	"Resende"	"SP"	"08737-363"	"Brazil"
10255	"RICSU"	9	"1996-07-12"	"1996-08-09"	"1996-07-15"	3	148.33	"Richter Supermarkt"	"Starenweg 5"	"Genève"		"1204"	"Switzerland"
10254	"CHOPS"	5	"1996-07-11"	"1996-08-08"	"1996-07-23"	2	22.98	"Chop-suey Chinese"	"Hauptstr. 31"	"Bern"		"3012"	"Switzerland"
10253	"HANAR"	3	"1996-07-10"	"1996-07-24"	"1996-07-16"	2	58.17	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
10252	"SUPRD"	4	"1996-07-09"	"1996-08-06"	"1996-07-11"	2	51.3	"Suprêmes délices"	"Boulevard Tirou, 255"	"Charleroi"		"B-6000"	"Belgium"
10251	"VICTE"	3	"1996-07-08"	"1996-08-05"	"1996-07-15"	1	41.34	"Victuailles en stock"	"2, rue du Commerce"	"Lyon"		"69004"	"France"
10250	"HANAR"	4	"1996-07-08"	"1996-08-05"	"1996-07-12"	2	65.83	"Hanari Carnes"	"Rua do Paço, 67"	"Rio de Janeiro"	"RJ"	"05454-876"	"Brazil"
10249	"TOMSP"	6	"1996-07-05"	"1996-08-16"	"1996-07-10"	1	11.61	"Toms Spezialitäten"	"Luisenstr. 48"	"Münster"		"44087"	"Germany"
10248	"VINET"	5	"1996-07-04"	"1996-08-01"	"1996-07-16"	3	32.38	"Vins et alcools Chevalier"	"59 rue de l'Abbaye"	"Reims"		"51100"	"France"
```

* [ ] ***find all suppliers who have names longer than 20 characters. Returns 11 records***

  <details><summary>hint</summary>

  * This can be done with SELECT and WHERE clauses
  * You can use `length(company_name)` to get the length of the name
  </details>

```SQL
"supplier_id"	"company_name"	"contact_name"	"contact_title"	"address"	"city"	"region"	"postal_code"	"country"	"phone"	"fax"	"homepage"
2	"New Orleans Cajun Delights"	"Shelley Burke"	"Order Administrator"	"P.O. Box 78934"	"New Orleans"	"LA"	"70117"	"USA"	"(100) 555-4822"		"#CAJUN.HTM#"
3	"Grandma Kelly's Homestead"	"Regina Murphy"	"Sales Representative"	"707 Oxford Rd."	"Ann Arbor"	"MI"	"48104"	"USA"	"(313) 555-5735"	"(313) 555-3349"	
5	"Cooperativa de Quesos 'Las Cabras'"	"Antonio del Valle Saavedra"	"Export Administrator"	"Calle del Rosal 4"	"Oviedo"	"Asturias"	"33007"	"Spain"	"(98) 598 76 54"		
8	"Specialty Biscuits, Ltd."	"Peter Wilson"	"Sales Representative"	"29 King's Way"	"Manchester"		"M14 GSD"	"UK"	"(161) 555-4448"		
10	"Refrescos Americanas LTDA"	"Carlos Diaz"	"Marketing Manager"	"Av. das Americanas 12.890"	"Sao Paulo"		"5442"	"Brazil"	"(11) 555 4640"		
11	"Heli Süßwaren GmbH & Co. KG"	"Petra Winkler"	"Sales Manager"	"Tiergartenstraße 5"	"Berlin"		"10785"	"Germany"	"(010) 9984510"		
12	"Plutzer Lebensmittelgroßmärkte AG"	"Martin Bein"	"International Marketing Mgr."	"Bogenallee 51"	"Frankfurt"		"60439"	"Germany"	"(069) 992755"		"Plutzer (on the World Wide Web)#http://www.microsoft.com/accessdev/sampleapps/plutzer.htm#"
13	"Nord-Ost-Fisch Handelsgesellschaft mbH"	"Sven Petersen"	"Coordinator Foreign Markets"	"Frahmredder 112a"	"Cuxhaven"		"27478"	"Germany"	"(04721) 8713"	"(04721) 8714"	
14	"Formaggi Fortini s.r.l."	"Elio Rossi"	"Sales Representative"	"Viale Dante, 75"	"Ravenna"		"48100"	"Italy"	"(0544) 60323"	"(0544) 60603"	"#FORMAGGI.HTM#"
18	"Aux joyeux ecclésiastiques"	"Guylène Nodier"	"Sales Manager"	"203, Rue des Francs-Bourgeois"	"Paris"		"75004"	"France"	"(1) 03.83.00.68"	"(1) 03.83.00.62"	
19	"New England Seafood Cannery"	"Robb Merchant"	"Wholesale Account Agent"	"Order Processing Dept. 2100 Paul Revere Blvd."	"Boston"	"MA"	"02134"	"USA"	"(617) 555-3267"	"(617) 555-3389"	
```

* [ ] ***find all customers that include the word 'MARKET' in the contact title. Should return 19 records***

  <details><summary>hint</summary>

  * This can be done with SELECT and a WHERE clause using the LIKE keyword
  * Don't forget the wildcard '%' symbols at the beginning and end of your substring to denote it can appear anywhere in the string in question
  * Remember to convert your contact title to all upper case for case insensitive comparing so upper(contact_title)
  </details>

```SQL
"customer_id"	"company_name"	"contact_name"	"contact_title"	"address"	"city"	"region"	"postal_code"	"country"	"phone"	"fax"
"BLONP"	"Blondesddsl père et fils"	"Frédérique Citeaux"	"Marketing Manager"	"24, place Kléber"	"Strasbourg"		"67000"	"France"	"88.60.15.31"	"88.60.15.32"
"CENTC"	"Centro comercial Moctezuma"	"Francisco Chang"	"Marketing Manager"	"Sierras de Granada 9993"	"México D.F."		"05022"	"Mexico"	"(5) 555-3392"	"(5) 555-7293"
"FAMIA"	"Familia Arquibaldo"	"Aria Cruz"	"Marketing Assistant"	"Rua Orós, 92"	"Sao Paulo"	"SP"	"05442-030"	"Brazil"	"(11) 555-9857"	
"FRANK"	"Frankenversand"	"Peter Franken"	"Marketing Manager"	"Berliner Platz 43"	"München"		"80805"	"Germany"	"089-0877310"	"089-0877451"
"FRANR"	"France restauration"	"Carine Schmitt"	"Marketing Manager"	"54, rue Royale"	"Nantes"		"44000"	"France"	"40.32.21.21"	"40.32.21.20"
"GALED"	"Galería del gastrónomo"	"Eduardo Saavedra"	"Marketing Manager"	"Rambla de Cataluña, 23"	"Barcelona"		"08022"	"Spain"	"(93) 203 4560"	"(93) 203 4561"
"GREAL"	"Great Lakes Food Market"	"Howard Snyder"	"Marketing Manager"	"2732 Baker Blvd."	"Eugene"	"OR"	"97403"	"USA"	"(503) 555-7555"	
"ISLAT"	"Island Trading"	"Helen Bennett"	"Marketing Manager"	"Garden House Crowther Way"	"Cowes"	"Isle of Wight"	"PO31 7PJ"	"UK"	"(198) 555-8888"	
"LAUGB"	"Laughing Bacchus Wine Cellars"	"Yoshi Tannamuri"	"Marketing Assistant"	"1900 Oak St."	"Vancouver"	"BC"	"V3F 2K1"	"Canada"	"(604) 555-3392"	"(604) 555-7293"
"LAZYK"	"Lazy K Kountry Store"	"John Steel"	"Marketing Manager"	"12 Orchestra Terrace"	"Walla Walla"	"WA"	"99362"	"USA"	"(509) 555-7969"	"(509) 555-6221"
"MAGAA"	"Magazzini Alimentari Riuniti"	"Giovanni Rovelli"	"Marketing Manager"	"Via Ludovico il Moro 22"	"Bergamo"		"24100"	"Italy"	"035-640230"	"035-640231"
"MEREP"	"Mère Paillarde"	"Jean Fresnière"	"Marketing Assistant"	"43 rue St. Laurent"	"Montréal"	"Québec"	"H1J 1C3"	"Canada"	"(514) 555-8054"	"(514) 555-8055"
"MORGK"	"Morgenstern Gesundkost"	"Alexander Feuer"	"Marketing Assistant"	"Heerstr. 22"	"Leipzig"		"04179"	"Germany"	"0342-023176"	
"QUEEN"	"Queen Cozinha"	"Lúcia Carvalho"	"Marketing Assistant"	"Alameda dos Canàrios, 891"	"Sao Paulo"	"SP"	"05487-020"	"Brazil"	"(11) 555-1189"	
"SPECD"	"Spécialités du monde"	"Dominique Perrier"	"Marketing Manager"	"25, rue Lauriston"	"Paris"		"75016"	"France"	"(1) 47.55.60.10"	"(1) 47.55.60.20"
"THEBI"	"The Big Cheese"	"Liz Nixon"	"Marketing Manager"	"89 Jefferson Way Suite 2"	"Portland"	"OR"	"97201"	"USA"	"(503) 555-3612"	
"THECR"	"The Cracker Box"	"Liu Wong"	"Marketing Assistant"	"55 Grizzly Peak Rd."	"Butte"	"MT"	"59801"	"USA"	"(406) 555-5834"	"(406) 555-8083"
"TOMSP"	"Toms Spezialitäten"	"Karin Josephs"	"Marketing Manager"	"Luisenstr. 48"	"Münster"		"44087"	"Germany"	"0251-031259"	"0251-035695"
"WILMK"	"Wilman Kala"	"Matti Karttunen"	"Owner/Marketing Assistant"	"Keskuskatu 45"	"Helsinki"		"21240"	"Finland"	"90-224 8858"	"90-224 8858"
```

* [ ] ***add a customer record for***
* customer id is 'SHIRE'
* company name is 'The Shire'
* contact name is 'Bilbo Baggins'
* the address is '1 Hobbit-Hole'
* the city is 'Bag End'
* the postal code is '111'
* the country is 'Middle Earth'
  <details><summary>hint</summary>

  * This can be done with the INSERT INTO clause
  </details>

```SQL
"customer_id"	"company_name"	"contact_name"	"contact_title"	"address"	"city"	"region"	"postal_code"	"country"	"phone"	"fax"
"SHIRE"	"The Shire"	"Bilbo Baggins"		"1 Hobbit-Hole"	"Bag End"		"111"	"Middle Earth"		
```

* [ ] ***update _Bilbo Baggins_ record so that the postal code changes to _"11122"_***

  <details><summary>hint</summary>

  * This can be done with UPDATE and WHERE clauses
  </details>

```SQL
"customer_id"	"company_name"	"contact_name"	"contact_title"	"address"	"city"	"region"	"postal_code"	"country"	"phone"	"fax"
"SHIRE"	"The Shire"	"Bilbo Baggins"		"1 Hobbit-Hole"	"Bag End"		"11122"	"Middle Earth"		
```

* [ ] ***list orders grouped and ordered by customer company name showing the number of orders per customer company name. _Rattlesnake Canyon Grocery_ should have 18 orders***

  <details><summary>hint</summary>

  * This can be done with SELECT, COUNT, JOIN and GROUP BY clauses. Your count should focus on a field in the Orders table, not the Customer table
  * There is more information about the COUNT clause on [W3 Schools](https://www.w3schools.com/sql/sql_count_avg_sum.asp)
  </details>

```SQL
"count"	"company_name"
7	"Wilman Kala"
10	"Magazzini Alimentari Riuniti"
3	"The Cracker Box"
9	"Wellington Importadora"
4	"Let's Stop N Shop"
8	"Furia Bacalhau e Frutos do Mar"
6	"Toms Spezialitäten"
15	"Lehmanns Marktstand"
13	"Mère Paillarde"
18	"Rattlesnake Canyon Grocery"
9	"Que Delícia"
4	"The Big Cheese"
19	"Hungry Owl All-Night Grocers"
14	"Königlich Essen"
3	"North/South"
2	"GROSELLA-Restaurante"
15	"Frankenversand"
5	"Folies gourmandes"
13	"Around the Horn"
9	"Split Rail Beer & Ale"
5	"Comércio Mineiro"
9	"Gourmet Lanchonetes"
6	"Santé Gourmet"
10	"Victuailles en stock"
8	"Chop-suey Chinese"
6	"Alfreds Futterkiste"
8	"Lonesome Pine Restaurant"
18	"HILARION-Abastos"
4	"La corne d'abondance"
10	"Old World Delicatessen"
14	"LILA-Supermercado"
7	"Wolski  Zajazd"
10	"Godos Cocina Típica"
10	"Die Wandernde Kuh"
11	"Blondesddsl père et fils"
5	"Morgenstern Gesundkost"
11	"Ricardo Adocicados"
4	"Spécialités du monde"
14	"La maison d'Asie"
3	"Bólido Comidas preparadas"
15	"Wartian Herkku"
17	"Bon app'"
18	"Berglunds snabbköp"
8	"Eastern Connection"
9	"Seven Seas Imports"
5	"Océano Atlántico Ltda."
6	"Drachenblut Delikatessen"
12	"Suprêmes délices"
30	"Ernst Handel"
12	"LINO-Delicateses"
7	"Antonio Moreno Taquería"
10	"Ottilies Käseladen"
6	"Cactus Comidas para llevar"
5	"Princesa Isabel Vinhos"
5	"Galería del gastrónomo"
6	"Tradição Hipermercados"
5	"Hungry Coyote Import Store"
11	"Great Lakes Food Market"
31	"Save-a-lot Markets"
12	"Reggiani Caseifici"
7	"Maison Dewey"
13	"Queen Cozinha"
7	"Simons bistro"
3	"Laughing Bacchus Wine Cellars"
28	"QUICK-Stop"
10	"Richter Supermarkt"
10	"Tortuga Restaurante"
3	"Consolidated Holdings"
5	"Vins et alcools Chevalier"
6	"Franchi S.p.A."
19	"Folk och fä HB"
14	"Hanari Carnes"
7	"Blauer See Delikatessen"
3	"Trail's Head Gourmet Provisioners"
5	"Rancho grande"
7	"Familia Arquibaldo"
2	"Lazy K Kountry Store"
11	"Vaffeljernet"
6	"Pericles Comidas clásicas"
4	"Ana Trujillo Emparedados y helados"
1	"Centro comercial Moctezuma"
3	"France restauration"
14	"Bottom-Dollar Markets"
10	"B's Beverages"
5	"Romero y tomillo"
14	"White Clover Markets"
10	"Piccolo und mehr"
10	"Island Trading"
4	"Du monde entier"
```

* [ ] ***list customers by contact name and the number of orders per contact name. Sort the list by the number of orders in descending order. _Jose Pavarotti_ should be at the top with 31 orders followed by _Roland Mendal_ with 30 orders. Last should be _Francisco Chang_ with 1 order***

  <details><summary>hint</summary>

  * This can be done by adding an ORDER BY clause to the previous answer and changing the group by field
  </details>

```SQL
"count"	"contact_name"
31	"Jose Pavarotti"
30	"Roland Mendel"
28	"Horst Kloss"
19	"Patricia McKenna"
19	"Maria Larsson"
18	"Paula Wilson"
18	"Carlos Hernández"
18	"Christina Berglund"
17	"Laurence Lebihan"
15	"Renate Messner"
15	"Pirkko Koskitalo"
15	"Peter Franken"
14	"Carlos González"
14	"Philip Cramer"
14	"Karl Jablonski"
14	"Elizabeth Lincoln"
14	"Annette Roulet"
14	"Mario Pontes"
13	"Thomas Hardy"
13	"Lúcia Carvalho"
13	"Jean Fresnière"
12	"Pascale Cartrain"
12	"Felipe Izquierdo"
12	"Maurizio Moroni"
11	"Howard Snyder"
11	"Janete Limeira"
11	"Frédérique Citeaux"
11	"Palle Ibsen"
10	"Miguel Angel Paolino"
10	"Rene Phillips"
10	"Rita Müller"
10	"José Pedro Freyre"
10	"Mary Saveley"
10	"Georg Pipps"
10	"Helen Bennett"
10	"Victoria Ashworth"
10	"Giovanni Rovelli"
10	"Michael Holz"
10	"Henriette Pfalzheim"
9	"Hari Kumar"
9	"Bernardo Batista"
9	"Art Braunschweiger"
9	"André Fonseca"
9	"Paula Parente"
8	"Fran Wilson"
8	"Lino Rodriguez"
8	"Yang Wang"
8	"Ann Devon"
7	"Hanna Moos"
7	"Aria Cruz"
7	"Zbyszek Piestrzeniewicz"
7	"Catherine Dewey"
7	"Jytte Petersen"
7	"Antonio Moreno"
7	"Matti Karttunen"
6	"Karin Josephs"
6	"Jonas Bergulfsen"
6	"Maria Anders"
6	"Sven Ottlieb"
6	"Guillermo Fernández"
6	"Anabela Domingues"
6	"Patricio Simpson"
6	"Paolo Accorti"
5	"Martine Rancé"
5	"Yvonne Moncada"
5	"Isabel de Castro"
5	"Sergio Gutiérrez"
5	"Alejandra Camino"
5	"Eduardo Saavedra"
5	"Pedro Afonso"
5	"Alexander Feuer"
5	"Yoshi Latimer"
5	"Paul Henriot"
4	"Jaime Yorres"
4	"Janine Labrune"
4	"Daniel Tonini"
4	"Ana Trujillo"
4	"Liz Nixon"
4	"Dominique Perrier"
3	"Elizabeth Brown"
3	"Simon Crowther"
3	"Carine Schmitt"
3	"Yoshi Tannamuri"
3	"Martín Sommer"
3	"Liu Wong"
3	"Helvetius Nagy"
2	"John Steel"
2	"Manuel Pereira"
1	"Francisco Chang"
```

* [ ] ***list orders grouped by customer's city showing the number of orders per city. Returns 69 Records with _Aachen_ showing 6 orders and _Albuquerque_ showing 18 orders***

  <details><summary>hint</summary>

  * This is very similar to the previous two queries, however, it focuses on the City rather than the Customer Names
  </details>

```SQL
"count"	"city"
46	"London"
34	"Rio de Janeiro"
31	"Boise"
31	"Sao Paulo"
30	"Graz"
28	"México D.F."
28	"Cunewalde"
19	"Bräcke"
19	"Cork"
18	"Luleå"
18	"Albuquerque"
18	"San Cristóbal"
17	"Marseille"
16	"Buenos Aires"
15	"Frankfurt a.M."
15	"Oulu"
15	"München"
14	"Tsawassen"
14	"Brandenburg"
14	"Seattle"
14	"Barquisimeto"
14	"Toulouse"
13	"Montréal"
13	"Lisboa"
12	"Portland"
12	"Reggio Emilia"
12	"I. de Margarita"
12	"Charleroi"
11	"Eugene"
11	"Århus"
11	"Strasbourg"
10	"Anchorage"
10	"Salzburg"
10	"Stuttgart"
10	"Sevilla"
10	"Köln"
10	"Cowes"
10	"Lyon"
10	"Genève"
10	"Bergamo"
9	"Lander"
9	"Campinas"
9	"Resende"
8	"Madrid"
8	"Bern"
7	"Kobenhavn"
7	"Mannheim"
7	"Nantes"
7	"Helsinki"
7	"Warszawa"
7	"Bruxelles"
6	"Stavern"
6	"Torino"
6	"Berlin"
6	"Münster"
6	"Aachen"
5	"Lille"
5	"Elgin"
5	"Reims"
5	"Barcelona"
5	"Leipzig"
4	"Paris"
4	"San Francisco"
4	"Versailles"
3	"Butte"
3	"Kirkland"
3	"Vancouver"
2	"Walla Walla"
2	"Caracas"
```

## Data Normalization

Note: This step does not use PostgreSQL!

* [ ] ***Take the following data and normalize it into a 3NF database***

| Person Name | Pet Name | Pet Type | Pet Name 2 | Pet Type 2 | Pet Name 3 | Pet Type 3 | Fenced Yard | City Dweller |
|-------------|----------|----------|------------|------------|------------|------------|-------------|--------------|
| Jane        | Ellie    | Dog      | Tiger      | Cat        | Toby       | Turtle     | No          | Yes          |
| Bob         | Joe      | Horse    |            |            |            |            | No          | No           |
| Sam         | Ginger   | Dog      | Miss Kitty | Cat        | Bubble     | Fish       | Yes         | No           |

Below are some empty tables to be used to normalize the database

* Not all of the cells will contain data in the final solution
* Feel free to edit these tables as necessary

Table Name: Resident Table

|Resident_Id |Name        |Fencing_Id  |Location_Id |            |            |            |            |            |
|------------|------------|------------|------------|------------|------------|------------|------------|------------|
| 1          | Jane       | 2          |1           |            |            |            |            |            |
| 2          | Bob        | 2          |2           |            |            |            |            |            |
| 3          | Sam        | 1          |2           |            |            |            |            |            |
|            |            |            |            |            |            |            |            |            |
|            |            |            |            |            |            |            |            |            |
|            |            |            |            |            |            |            |            |            |

Table Name: Pets Table

| Pet_Id     |Resident_Id |Pet_Name    |Pet_Type    |            |            |            |            |            |
|------------|------------|------------|------------|------------|------------|------------|------------|------------|
| 1          |1           | Ellie      |Dog         |            |            |            |            |            |
| 2          |1           | Tiger      |Cat         |            |            |            |            |            |
| 3          |1           | Toby       |Turtle      |            |            |            |            |            |
| 4          |2           | Joe        |Horse       |            |            |            |            |            |
| 5          |3           | Ginger     |Dog         |            |            |            |            |            |
| 6          |3           | Miss Kitty |Cat         |            |            |            |            |            |
| 7          |3           | Bubble     |Fish        |            |            |            |            |            |

Table Name: Fencing Table

| Fencing_Id | isFenced   |            |            |            |            |            |            |            |
|------------|------------|------------|------------|------------|------------|------------|------------|------------|
|1           |Yes         |            |            |            |            |            |            |            |
|2           |No          |            |            |            |            |            |            |            |
|            |            |            |            |            |            |            |            |            |
|            |            |            |            |            |            |            |            |            |
|            |            |            |            |            |            |            |            |            |
|            |            |            |            |            |            |            |            |            |
|            |            |            |            |            |            |            |            |            |

Table Name: Location Table

|Location_Id | isInCity   |            |            |            |            |            |            |            |
|------------|------------|------------|------------|------------|------------|------------|------------|------------|
|1           | Yes        |            |            |            |            |            |            |            |
|2           | No         |            |            |            |            |            |            |            |
|            |            |            |            |            |            |            |            |            |
|            |            |            |            |            |            |            |            |            |
|            |            |            |            |            |            |            |            |            |
|            |            |            |            |            |            |            |            |            |
|            |            |            |            |            |            |            |            |            |

---

### Stretch Goals

* [ ] ***delete all customers that have no orders. Should delete 2 (or 3 if you haven't deleted the record added) records***

```SQL
"count"
89

```

* [ ] ***Create Database and Table: After creating the database, tables, columns, and constraint, generate the script necessary to recreate the database. This script is what you will submit for review***

* use pgAdmin to create a database, naming it `budget`.
* add an `accounts` table with the following _schema_:

  * `id`, numeric value with no decimal places that should autoincrement.
  * `name`, string, add whatever is necessary to make searching by name faster.
  * `budget` numeric value.

* constraints
  * the `id` should be the primary key for the table.
  * account `name` should be unique.
  * account `budget` is required.

```SQL
--
-- PostgreSQL database dump
--

-- Dumped from database version 13.2
-- Dumped by pg_dump version 13.2

-- Started on 2021-04-07 21:33:31

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- TOC entry 201 (class 1259 OID 17078)
-- Name: accounts; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.accounts (
    id integer NOT NULL,
    name text,
    budget numeric NOT NULL
);


ALTER TABLE public.accounts OWNER TO postgres;

--
-- TOC entry 200 (class 1259 OID 17076)
-- Name: accounts_id_seq; Type: SEQUENCE; Schema: public; Owner: postgres
--

CREATE SEQUENCE public.accounts_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.accounts_id_seq OWNER TO postgres;

--
-- TOC entry 2992 (class 0 OID 0)
-- Dependencies: 200
-- Name: accounts_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: postgres
--

ALTER SEQUENCE public.accounts_id_seq OWNED BY public.accounts.id;


--
-- TOC entry 2850 (class 2604 OID 17081)
-- Name: accounts id; Type: DEFAULT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.accounts ALTER COLUMN id SET DEFAULT nextval('public.accounts_id_seq'::regclass);


--
-- TOC entry 2986 (class 0 OID 17078)
-- Dependencies: 201
-- Data for Name: accounts; Type: TABLE DATA; Schema: public; Owner: postgres
--

COPY public.accounts (id, name, budget) FROM stdin;
\.


--
-- TOC entry 2993 (class 0 OID 0)
-- Dependencies: 200
-- Name: accounts_id_seq; Type: SEQUENCE SET; Schema: public; Owner: postgres
--

SELECT pg_catalog.setval('public.accounts_id_seq', 1, false);


--
-- TOC entry 2852 (class 2606 OID 17088)
-- Name: accounts accounts_name_key; Type: CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.accounts
    ADD CONSTRAINT accounts_name_key UNIQUE (name);


--
-- TOC entry 2854 (class 2606 OID 17086)
-- Name: accounts accounts_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.accounts
    ADD CONSTRAINT accounts_pkey PRIMARY KEY (id);


-- Completed on 2021-04-07 21:33:32

--
-- PostgreSQL database dump complete
--


```

To see the script

* Right Click on the database name
  * Select Backup...
    * Set a filename
      * To put the file backup.sql in your home directory, you could use `backup.sql`
    * Set format to `Plain`
* The script you want is now in the text file named above.
  * Copy the script from the text file into the SQL code block above!

![Database Script](assets/jx-12-m3-script.gif)
