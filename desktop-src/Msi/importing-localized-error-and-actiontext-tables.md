---
description: Lokalisierte Sprachversionen der Tabelle Error und der ActionText-Tabelle werden vom Windows Installer SDK bereitgestellt. Die französischen Sprachversionen dieser Tabellen, Error.FRA und ActionTe.FRA, befinden sich im Ordner Intl des Windows Installer SDK.
ms.assetid: 8de687c8-c7da-497e-8a90-2404096ad100
title: Importieren lokalisierter Fehler- und ActionText-Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda0916f634d986874cd17f9871fa602277b180e1ba436e9d9786fb061f3ac4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142235"
---
# <a name="importing-localized-error-and-actiontext-tables"></a>Importieren lokalisierter Fehler- und ActionText-Tabellen

Lokalisierte Sprachversionen der [Tabelle Error](error-table.md) und der [ActionText-Tabelle](actiontext-table.md) werden vom Windows Installer SDK bereitgestellt. Die französischen Sprachversionen dieser Tabellen, Error.FRA und ActionTe.FRA, befinden sich im Ordner Intl des Windows Installer SDK.

Sie können den Tabellen-Editor Orca oder das mit dem SDK bereitgestellte Hilfsprogramm Msidb.exe verwenden, um die französischen Versionen dieser Tabellen in die Datenbank zu importieren.

Ein Beispiel für die Verwendung von [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) und der [**Import-Methode**](database-import.md) des [**Database-Objekts**](database-object.md) finden Sie im Windows Installer SDK als Hilfsprogramm WiImport.vbs. Der folgende Codeausschnitt Imp.vbs veranschaulicht auch die Verwendung der Import-Methode und ist für die Verwendung mit Windows Script Host vorgesehen.


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



Zum Importieren und Ersetzen der Error-Tabelle durch Error.FRA können Sie eine Befehlszeile wie die folgende verwenden.

**Cscript Imp.vbs MNPFren.msi C: \\ Hinweis \_ Installer Französisch \\ Error.FRA**

Zum Importieren und Ersetzen der ActionText-Tabelle durch ActionTe.FRA können Sie eine Befehlszeile wie die folgende verwenden.

**Cscript Imp.vbs MNPFren.msi C: \\ Hinweis Installer Französisch \_ \\ ActionTe.FRA**

Führen Sie die Überprüfung auf MNPFren.msi erneut aus, wie unter [Überprüfen eines Installationsupgrades](validating-an-installation-upgrade.md)beschrieben.

[Fortsetzen](localizing-database-columns.md)

 

 



