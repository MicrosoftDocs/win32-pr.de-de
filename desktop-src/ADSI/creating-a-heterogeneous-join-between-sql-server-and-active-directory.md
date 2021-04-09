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
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a>Erstellen eines heterogenen Joins zwischen SQL Server & Active Directory

Alle Mitarbeiter der Fabrikam Corporation werden alle sechs Monate überprüft. Review-Bewertungen werden in SQL Server in der Human Resource-Datenbank gespeichert. Um eine Ansicht dieser Daten zu erstellen, muss Joe von, der Unternehmens Administrator, zunächst eine Tabelle für die Überprüfung der Mitarbeiterleistung erstellen.

In SQL Query Analyzer erstellt Joe eine Tabelle namens EMP \_ Review, die drei Spalten enthält, die den Namen des Mitarbeiters, das Datum der Überprüfung und die Bewertung enthalten, die der Mitarbeiter erhalten hat.


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



Joe kann dann einige Datensätze einfügen.


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



Nun kann Joe die Active Directory User-Objekte mit der SQL Server Tabelle verknüpfen.

In diesem Beispiel enthält die [Select](https://msdn.microsoft.com/library/Aa259187.aspx) -Anweisung die Liste der Daten, die vom Verzeichnisdienst abgerufen werden, und SQL Server. Die [from](https://msdn.microsoft.com/library/Aa258869.aspx) -Anweisung enthält den Namen des Verbindungs Verzeichnis Servers, von dem diese Informationen abgerufen werden, in diesem Fall "viewadusers". Die [Where](https://msdn.microsoft.com/library/Aa260674.aspx) -Anweisung stellt die Suchbedingungen bereit. In diesem Beispiel sucht Sie nach dem Namen im Verzeichnisdienst, der auf den in der vorherigen Aufgabe eingegebenen SQL-Benutzernamen festgelegt ist.


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



Mit dem vorherigen Befehl wird das Ergebnis sowohl aus SQL Server als auch aus Active Directory abgerufen. ADsPath und Title stammen aus Active Directory, während username, ReviewDate und Rating aus der SQL-Tabelle stammen. Er kann sogar eine weitere Ansicht für diesen Join erstellen.


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




