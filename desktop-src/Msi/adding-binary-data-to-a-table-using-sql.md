---
description: Binärdaten können nicht direkt mithilfe der INSERT INTO-oder Update SQL-Abfragen in eine Tabelle eingefügt werden.
ms.assetid: cc055de8-eaba-48eb-a982-4d584ac7a881
title: Hinzufügen von Binärdaten zu einer Tabelle mithilfe von SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491bfe57354b4faf9f7c385bc4e14c64ad366f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864524"
---
# <a name="adding-binary-data-to-a-table-using-sql"></a>Hinzufügen von Binärdaten zu einer Tabelle mithilfe von SQL

Binärdaten können nicht direkt mithilfe der INSERT INTO-oder Update SQL-Abfragen in eine Tabelle eingefügt werden. Um einer Tabelle Binärdaten hinzuzufügen, müssen Sie zuerst die Parameter Markierung (?) in der Abfrage als Platzhalter für den binären Wert verwenden. Die Ausführung der Abfrage sollte einen Datensatz einschließen, der die Binärdaten in einem der Felder enthält.

Ein Marker ist ein Parameter Verweis auf einen Wert, der von einem mit der Abfrage übermittelten Datensatz bereitgestellt wird. Sie wird in der SQL-Anweisung durch ein Fragezeichen (?) dargestellt.

Der folgende Beispielcode fügt einer Tabelle Binärdaten hinzu.


```C++
#include <windows.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")


int main()  
{ 

PMSIHANDLE hDatabase = 0;
PMSIHANDLE hView = 0;
PMSIHANDLE hRec = 0;

if (ERROR_SUCCESS == MsiOpenDatabase(_T("c:\\temp\\testdb.msi"), MSIDBOPEN_TRANSACT, &hDatabase))
{
    //
    // Open view on Binary table so that we can add a new row, must use '?' to represent Binary data
    //

    if (ERROR_SUCCESS == MsiDatabaseOpenView(hDatabase, _T("INSERT INTO `Binary` (`Name`, `Data`) VALUES ('NewBlob', ?)"), &hView))
    {

        //
        // Create record with binary data in 1st field (must match up with '?' in query)
        //

        hRec = MsiCreateRecord(1);
        if (ERROR_SUCCESS == MsiRecordSetStream(hRec, 1, _T("c:\\temp\\data.bin")))
        {

            //
            // Execute view with record containing binary data value; commit database to save changes
            //

            if (ERROR_SUCCESS == MsiViewExecute(hView, hRec)
              && ERROR_SUCCESS == MsiViewClose(hView)
              && ERROR_SUCCESS == MsiDatabaseCommit(hDatabase))
            {
                //
                // New binary data successfully committed to the database
                //
            }
        }
    }
}

return 0;  
}
```



Das folgende Beispielskript fügt einer Tabelle Binärdaten hinzu.


```VB
Dim Installer
Dim Database
Dim View
Dim Record

Set Installer = CreateObject("WindowsInstaller.Installer")

Set Record = Installer.CreateRecord(1)
Record.SetStream 1, "c:\temp\data.bin"

Set Database = Installer.OpenDatabase("c:\temp\testdb.msi", msiOpenDatabaseModeTransact)
Set View = Database.OpenView("INSERT INTO `Binary` (`Name`, `Data`) VALUES ('NewBlob', ?)")
View.Execute Record
Database.Commit ' save changes
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Abfragen](working-with-queries.md)
</dt> <dt>

[SQL-Syntax](sql-syntax.md)
</dt> <dt>

[Beispiele für Datenbankabfragen mit SQL und Skript](examples-of-database-queries-using-sql-and-script.md)
</dt> </dl>

 

 



