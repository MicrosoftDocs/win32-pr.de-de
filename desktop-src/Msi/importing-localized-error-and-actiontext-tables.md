---
description: Lokalisierte Sprachversionen der Fehler Tabelle und der Aktions Text Tabelle werden vom Windows Installer SDK bereitgestellt. Die französischen Sprachversionen dieser Tabellen, Error. fra und aktionte. fra, befinden sich im Ordner Intl des Windows Installer SDK.
ms.assetid: 8de687c8-c7da-497e-8a90-2404096ad100
title: Importieren lokalisierter Fehler-und Aktions Text Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d48a68ca1053a1a1c66899a17802ac337c3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357896"
---
# <a name="importing-localized-error-and-actiontext-tables"></a><span data-ttu-id="802af-104">Importieren lokalisierter Fehler-und Aktions Text Tabellen</span><span class="sxs-lookup"><span data-stu-id="802af-104">Importing Localized Error and ActionText Tables</span></span>

<span data-ttu-id="802af-105">Lokalisierte Sprachversionen der [Fehler Tabelle](error-table.md) und der [Aktions Text Tabelle](actiontext-table.md) werden vom Windows Installer SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="802af-105">Localized language versions of the [Error table](error-table.md) and [ActionText table](actiontext-table.md) are provided by the Windows Installer SDK.</span></span> <span data-ttu-id="802af-106">Die französischen Sprachversionen dieser Tabellen, Error. fra und aktionte. fra, befinden sich im Ordner Intl des Windows Installer SDK.</span><span class="sxs-lookup"><span data-stu-id="802af-106">The French language versions of these tables, Error.FRA and ActionTe.FRA, are located in the Intl folder of the Windows Installer SDK.</span></span>

<span data-ttu-id="802af-107">Sie können den Tabellen-Editor Orca oder das-Hilfsprogramm verwenden Msidb.exe mit dem SDK bereitgestellt, um die französischen Versionen dieser Tabellen in die-Datenbank zu importieren.</span><span class="sxs-lookup"><span data-stu-id="802af-107">You may use the table editor Orca or the utility Msidb.exe provided with the SDK to import the French versions of these tables into the database.</span></span>

<span data-ttu-id="802af-108">Ein Beispiel für die Verwendung von [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) und der [**Import-Methode**](database-import.md) des [**Datenbankobjekts**](database-object.md) finden Sie im Windows Installer SDK als Dienstprogramm WiImport.vbs.</span><span class="sxs-lookup"><span data-stu-id="802af-108">An example of using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) and the [**Import Method**](database-import.md) of the [**Database object**](database-object.md) is provided in the Windows Installer SDK as the utility WiImport.vbs.</span></span> <span data-ttu-id="802af-109">Der folgende Code Ausschnitt, Imp.vbs, veranschaulicht auch die Verwendung der Import Methode und ist für die Verwendung mit Windows Script Host vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="802af-109">The following snippet, Imp.vbs, also illustrates the use of the Import method and is for use with Windows Script Host.</span></span>


```VB
'Imp.vbs. Argument(0) is the original database. Argument(1) is the
'    path of the folder containing the file to be imported. Argument(2) is the name of the file to be imported.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is imp.vbs [original database] [folder path] [import file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
Dim databasePath : databasePath = Wscript.Arguments(0)
Dim folder : folder = Wscript.Arguments(1)
 
' Open database and process file
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim table : table = Wscript.Arguments(2)
database.Import folder, table 
 
' Commit database changes
database.Commit 'commit changes
Wscript.Quit 0
```



<span data-ttu-id="802af-110">Wenn Sie die Fehler Tabelle mit Error. fra importieren und ersetzen möchten, können Sie eine Befehlszeile wie die folgende verwenden.</span><span class="sxs-lookup"><span data-stu-id="802af-110">To import and replace the Error table with Error.FRA you may use a command line such as the following.</span></span>

<span data-ttu-id="802af-111">**Cscript Imp.vbs MNPFren.msi C: \\ Hinweis \_ Installationsprogramm \\ französischer Fehler. fra**</span><span class="sxs-lookup"><span data-stu-id="802af-111">**Cscript Imp.vbs MNPFren.msi C:\\Note\_Installer\\French Error.FRA**</span></span>

<span data-ttu-id="802af-112">Zum Importieren und Ersetzen der Tabelle "aktiontext" mit "aktionte. fra" können Sie eine Befehlszeile wie die folgende verwenden.</span><span class="sxs-lookup"><span data-stu-id="802af-112">To import and replace the ActionText table with ActionTe.FRA you may use a command line such as the following.</span></span>

<span data-ttu-id="802af-113">**Cscript Imp.vbs MNPFren.msi C: \\ Note \_ Installer \\ Französisch aktionte. fra**</span><span class="sxs-lookup"><span data-stu-id="802af-113">**Cscript Imp.vbs MNPFren.msi C:\\Note\_Installer\\French ActionTe.FRA**</span></span>

<span data-ttu-id="802af-114">Führen Sie die Überprüfung auf MNPFren.msi wie unter [Validieren eines Installations Upgrades](validating-an-installation-upgrade.md)beschrieben erneut aus.</span><span class="sxs-lookup"><span data-stu-id="802af-114">Rerun validation on MNPFren.msi as described in [Validating an Installation Upgrade](validating-an-installation-upgrade.md).</span></span>

[<span data-ttu-id="802af-115">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="802af-115">Continue</span></span>](localizing-database-columns.md)

 

 



