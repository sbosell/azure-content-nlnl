<properties
   pageTitle="Query’s uitvoeren bij Azure SQL datawarehouse (Visual Studio) | Microsoft Azure"
   description="Query’s uitvoeren bij SQL Data Warehouse met Visual Studio."
   services="sql-data-warehouse"
   documentationCenter="NA"
   authors="sonyam"
   manager="barbkess"
   editor=""/>

<tags
   ms.service="sql-data-warehouse"
   ms.devlang="NA"
   ms.topic="get-started-article"
   ms.tgt_pltfrm="NA"
   ms.workload="data-services"
   ms.date="06/16/2016"
   ms.author="sonyama;barbkess"/>

# Query’s uitvoeren bij Azure SQL Data Warehouse (Visual Studio)

> [AZURE.SELECTOR]
- [Power BI](sql-data-warehouse-get-started-visualize-with-power-bi.md)
- [Azure Machine Learning](sql-data-warehouse-get-started-analyze-with-azure-machine-learning.md)
- [Visual Studio](sql-data-warehouse-query-visual-studio.md)
- [sqlcmd](sql-data-warehouse-get-started-connect-sqlcmd.md) 

Gebruik Visual Studio om binnen enkele minuten query’s uit te voeren bij Azure SQL Data Warehouse. Bij deze methode wordt gebruikgemaakt van de SSDT-uitbreiding (SQL Server Data Tools) in Visual Studio. 

## Vereisten

Voor deze zelfstudie hebt u het volgende nodig:

+ Een bestaande SQL-datawarehouse. Zie [Een SQL Data Warehouse maken][] als u er een wilt maken.
+ SSDT voor Visual Studio. Als u Visual Studio hebt, hebt u dit waarschijnlijk al. Voor installatie-instructies en -opties raadpleegt u [Visual Studio en SSDT installeren][].
+ De volledig gekwalificeerde SQL-servernaam. Zie [Verbinding maken met SQL Data Warehouse][] om dit te vinden.

## 1. Verbinding maken met uw SQL Data Warehouse

1. Open Visual Studio 2013 of 2015.
2. Open SQL Server-objectverkenner. Daartoe selecteert u **View** > **SQL Server Object Explorer**.

    ![SQL Server-objectverkenner][1]

3. Klik op het pictogram **SQL Server toevoegen**.

    ![SQL Server toevoegen][2]

4. Vul de velden in het venster Connect to Server (Verbinding maken met server) in.

    ![Verbinding maken met server][3]

    - **Server name** (Servernaam). Voer de eerder vastgestelde **servernaam** in.
    - **Authentication** (Verificatie). Selecteer **SQL Server Authentication** (SQL Server-verificatie) of **Active Directory Integrated Authentication** (Geïntegreerde Active Directory-verificatie).
    - **User Name** (Gebruikersnaam) en **Password** (Wachtwoord). Voer de gebruikersnaam en het wachtwoord in als u hierboven SQL Server-verificatie hebt geselecteerd.
    - Klik op **Connect** (Verbinden).

5. U kunt de Azure SQL-server uitvouwen als u deze wilt verkennen. U kunt de databases weergeven die aan de server zijn gekoppeld. Vouw AdventureWorksDW uit als u de tabellen in de voorbeelddatabase wilt zien.

    ![AdventureWorksDW verkennen][4]

## 2. Een voorbeeldquery uitvoeren

Nu er een verbinding met uw database is ingesteld, gaat u een query schrijven.

1. Klik met de rechtermuisknop op de database in SQL Server-objectverkenner.

2. Selecteer **New Query** (Nieuwe query). Een nieuwe queryvenster wordt geopend.

    ![Nieuwe query][5]

3. Kopieer de volgende TSQL-query naar het queryvenster:

    ```sql
    SELECT COUNT(*) FROM dbo.FactInternetSales;
    ```

4. Voer de query uit. Daartoe klikt u op de groene pijl of gebruikt u de volgende snelkoppeling: `CTRL`+`SHIFT`+`E`.

    ![Query uitvoeren][6]

5. Bekijk de resultaten van de query. In dit voorbeeld heeft de tabel FactInternetSales 60398 rijen.

    ![Queryresultaten][7]

## Volgende stappen

Nu u weet hoe u verbinding maakt en een query uitvoert, kunt u proberen [de gegevens te visualiseren met Power BI][].

Zie [Verifiëren bij SQL Data Warehouse][] om uw omgeving te configureren voor Azure Active Directory-verificatie.

<!--Arcticles-->
[Verbinding maken met SQL Data Warehouse]: sql-data-warehouse-connect-overview.md
[Een SQL Data Warehouse maken]: sql-data-warehouse-get-started-provision.md
[Visual Studio en SSDT installeren]: sql-data-warehouse-install-visual-studio.md
[Verifiëren bij SQL Data Warehouse]: sql-data-warehouse-authentication.md
[de gegevens te visualiseren met Power BI]: sql-data-warehouse-get-started-visualize-with-power-bi.md  

<!--Other-->
[Azure-portal]: https://portal.azure.com

<!--Image references-->

[1]: media/sql-data-warehouse-query-visual-studio/open-ssdt.png
[2]: media/sql-data-warehouse-query-visual-studio/add-server.png
[3]: media/sql-data-warehouse-query-visual-studio/connection-dialog.png
[4]: media/sql-data-warehouse-query-visual-studio/explore-sample.png
[5]: media/sql-data-warehouse-query-visual-studio/new-query2.png
[6]: media/sql-data-warehouse-query-visual-studio/run-query.png
[7]: media/sql-data-warehouse-query-visual-studio/query-results.png



<!--HONumber=ago16_HO4-->


