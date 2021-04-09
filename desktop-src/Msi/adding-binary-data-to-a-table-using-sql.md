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
# <a name="adding-binary-data-to-a-table-using-sql"></a><span data-ttu-id="106d7-103">Hinzufügen von Binärdaten zu einer Tabelle mithilfe von SQL</span><span class="sxs-lookup"><span data-stu-id="106d7-103">Adding Binary Data to a Table Using SQL</span></span>

<span data-ttu-id="106d7-104">Binärdaten können nicht direkt mithilfe der INSERT INTO-oder Update SQL-Abfragen in eine Tabelle eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="106d7-104">Binary data cannot be inserted into a table directly using the INSERT INTO or UPDATE SQL queries.</span></span> <span data-ttu-id="106d7-105">Um einer Tabelle Binärdaten hinzuzufügen, müssen Sie zuerst die Parameter Markierung (?) in der Abfrage als Platzhalter für den binären Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="106d7-105">In order to add binary data to a table, you must first use the parameter marker (?) in the query as a placeholder for the binary value.</span></span> <span data-ttu-id="106d7-106">Die Ausführung der Abfrage sollte einen Datensatz einschließen, der die Binärdaten in einem der Felder enthält.</span><span class="sxs-lookup"><span data-stu-id="106d7-106">The execution of the query should include a record that contains the binary data in one of its fields.</span></span>

<span data-ttu-id="106d7-107">Ein Marker ist ein Parameter Verweis auf einen Wert, der von einem mit der Abfrage übermittelten Datensatz bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="106d7-107">A marker is a parameter reference to a value supplied by a record submitted with the query.</span></span> <span data-ttu-id="106d7-108">Sie wird in der SQL-Anweisung durch ein Fragezeichen (?) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="106d7-108">It is represented in the SQL statement by a question mark (?).</span></span>

<span data-ttu-id="106d7-109">Der folgende Beispielcode fügt einer Tabelle Binärdaten hinzu.</span><span class="sxs-lookup"><span data-stu-id="106d7-109">The following sample code adds binary data to a table.</span></span>


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



<span data-ttu-id="106d7-110">Das folgende Beispielskript fügt einer Tabelle Binärdaten hinzu.</span><span class="sxs-lookup"><span data-stu-id="106d7-110">The following sample script adds binary data to a table.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="106d7-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="106d7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="106d7-112">Arbeiten mit Abfragen</span><span class="sxs-lookup"><span data-stu-id="106d7-112">Working with Queries</span></span>](working-with-queries.md)
</dt> <dt>

[<span data-ttu-id="106d7-113">SQL-Syntax</span><span class="sxs-lookup"><span data-stu-id="106d7-113">SQL Syntax</span></span>](sql-syntax.md)
</dt> <dt>

[<span data-ttu-id="106d7-114">Beispiele für Datenbankabfragen mit SQL und Skript</span><span class="sxs-lookup"><span data-stu-id="106d7-114">Examples of Database Queries Using SQL and Script</span></span>](examples-of-database-queries-using-sql-and-script.md)
</dt> </dl>

 

 



