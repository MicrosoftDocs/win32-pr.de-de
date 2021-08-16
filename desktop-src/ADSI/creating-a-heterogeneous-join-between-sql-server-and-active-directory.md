---
title: Erstellen eines heterogenen Joins zwischen SQL Server & Active Directory
description: Alle Mitarbeiter des Fabrikam-Unternehmens werden alle sechs Monate überprüft.
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8620706db56124b83c8cd8151c067a548d5a73d557fa6523ed82167647450b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840290"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a>Erstellen eines heterogenen Joins zwischen SQL Server & Active Directory

Alle Mitarbeiter des Fabrikam-Unternehmens werden alle sechs Monate überprüft. Überprüfungsbewertungen werden in der Human Resource-Datenbank in SQL Server. Um eine Ansicht dieser Daten zu erstellen, muss Joe Worden, der Unternehmensadministrator, zunächst eine Tabelle für die Leistungsüberprüfung von Mitarbeitern erstellen.

Im SQL Query Analyzer erstellt Joe eine Tabelle namens EMP REVIEW, die drei Spalten enthält, die den Namen des Mitarbeiters, das Datum der Überprüfung und die Bewertung enthalten, die der Mitarbeiter erhalten \_ hat.


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



Jetzt kann Joe die Active Directory-Benutzerobjekte mit der tabelle SQL Server verbinden.

In diesem Beispiel enthält die [SELECT-Anweisung](https://msdn.microsoft.com/library/Aa259187.aspx) die Liste der Daten, die vom Verzeichnisdienst und dem Verzeichnisdienst SQL Server. Die [FROM-Anweisung](https://msdn.microsoft.com/library/Aa258869.aspx) enthält den Namen des Verknüpften Verzeichnisservers, von dem diese Informationen in diesem Fall von viewADUsers erhalten werden. Die [WHERE-Anweisung](https://msdn.microsoft.com/library/Aa260674.aspx) stellt die Suchbedingungen zurEntzuge. In diesem Beispiel wird nach dem Namen im Verzeichnisdienst gesucht, der auf den in der vorherigen Aufgabe eingegebenen SQL userName festgelegt ist.


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



Der vorherige Befehl ruft das Ergebnis sowohl von SQL Server als auch von Active Directory ab. AdsPath und title sind aus Active Directory, während userName, ReviewDate und Rating aus der SQL werden. Er kann sogar eine weitere Ansicht für diesen Join erstellen.


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




