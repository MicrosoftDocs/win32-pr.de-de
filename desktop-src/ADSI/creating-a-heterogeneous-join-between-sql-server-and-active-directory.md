---
title: Erstellen eines heterogenen Joins zwischen SQL Server & Active Directory
description: Alle Mitarbeiter der Fabrikam Corporation werden alle sechs Monate überprüft.
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e4e6b7f3bfd9c853d9ff262365d49c1f3a8d5c
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103948455"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a><span data-ttu-id="75687-103">Erstellen eines heterogenen Joins zwischen SQL Server & Active Directory</span><span class="sxs-lookup"><span data-stu-id="75687-103">Creating a Heterogeneous Join between SQL Server & Active Directory</span></span>

<span data-ttu-id="75687-104">Alle Mitarbeiter der Fabrikam Corporation werden alle sechs Monate überprüft.</span><span class="sxs-lookup"><span data-stu-id="75687-104">All employees at the Fabrikam corporation are reviewed every six months.</span></span> <span data-ttu-id="75687-105">Review-Bewertungen werden in SQL Server in der Human Resource-Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="75687-105">Review ratings are stored in the Human Resource database in SQL Server.</span></span> <span data-ttu-id="75687-106">Um eine Ansicht dieser Daten zu erstellen, muss Joe von, der Unternehmens Administrator, zunächst eine Tabelle für die Überprüfung der Mitarbeiterleistung erstellen.</span><span class="sxs-lookup"><span data-stu-id="75687-106">To create a view of this data, Joe Worden, the enterprise administrator, must first create an employee performance review table.</span></span>

<span data-ttu-id="75687-107">In SQL Query Analyzer erstellt Joe eine Tabelle namens EMP \_ Review, die drei Spalten enthält, die den Namen des Mitarbeiters, das Datum der Überprüfung und die Bewertung enthalten, die der Mitarbeiter erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="75687-107">In the SQL Query Analyzer, Joe is going to create a table called EMP\_REVIEW that will contain three columns to hold the name of the employee, the date of the review, and the rating that the employee received.</span></span>


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



<span data-ttu-id="75687-108">Joe kann dann einige Datensätze einfügen.</span><span class="sxs-lookup"><span data-stu-id="75687-108">Joe can then insert a few records.</span></span>


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



<span data-ttu-id="75687-109">Nun kann Joe die Active Directory User-Objekte mit der SQL Server Tabelle verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="75687-109">Now Joe can join the Active Directory user objects to the SQL Server table.</span></span>

<span data-ttu-id="75687-110">In diesem Beispiel enthält die [Select](https://msdn.microsoft.com/library/Aa259187.aspx) -Anweisung die Liste der Daten, die vom Verzeichnisdienst abgerufen werden, und SQL Server.</span><span class="sxs-lookup"><span data-stu-id="75687-110">In this example, the [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service and SQL Server.</span></span> <span data-ttu-id="75687-111">Die [from](https://msdn.microsoft.com/library/Aa258869.aspx) -Anweisung enthält den Namen des Verbindungs Verzeichnis Servers, von dem diese Informationen abgerufen werden, in diesem Fall "viewadusers".</span><span class="sxs-lookup"><span data-stu-id="75687-111">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from, in this case, viewADUsers.</span></span> <span data-ttu-id="75687-112">Die [Where](https://msdn.microsoft.com/library/Aa260674.aspx) -Anweisung stellt die Suchbedingungen bereit.</span><span class="sxs-lookup"><span data-stu-id="75687-112">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="75687-113">In diesem Beispiel sucht Sie nach dem Namen im Verzeichnisdienst, der auf den in der vorherigen Aufgabe eingegebenen SQL-Benutzernamen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="75687-113">In this example, it is searching by the name in the directory service, which is set to the SQL userName entered in the previous task.</span></span>


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



<span data-ttu-id="75687-114">Mit dem vorherigen Befehl wird das Ergebnis sowohl aus SQL Server als auch aus Active Directory abgerufen.</span><span class="sxs-lookup"><span data-stu-id="75687-114">The previous command gets the result from both SQL Server and Active Directory.</span></span> <span data-ttu-id="75687-115">ADsPath und Title stammen aus Active Directory, während username, ReviewDate und Rating aus der SQL-Tabelle stammen.</span><span class="sxs-lookup"><span data-stu-id="75687-115">AdsPath and title are from Active Directory, whereas userName, ReviewDate, and Rating are from the SQL table.</span></span> <span data-ttu-id="75687-116">Er kann sogar eine weitere Ansicht für diesen Join erstellen.</span><span class="sxs-lookup"><span data-stu-id="75687-116">He can even create another view for this join.</span></span>


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




