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
# <a name="importing-localized-error-and-actiontext-tables"></a>Importieren lokalisierter Fehler-und Aktions Text Tabellen

Lokalisierte Sprachversionen der [Fehler Tabelle](error-table.md) und der [Aktions Text Tabelle](actiontext-table.md) werden vom Windows Installer SDK bereitgestellt. Die französischen Sprachversionen dieser Tabellen, Error. fra und aktionte. fra, befinden sich im Ordner Intl des Windows Installer SDK.

Sie können den Tabellen-Editor Orca oder das-Hilfsprogramm verwenden Msidb.exe mit dem SDK bereitgestellt, um die französischen Versionen dieser Tabellen in die-Datenbank zu importieren.

Ein Beispiel für die Verwendung von [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) und der [**Import-Methode**](database-import.md) des [**Datenbankobjekts**](database-object.md) finden Sie im Windows Installer SDK als Dienstprogramm WiImport.vbs. Der folgende Code Ausschnitt, Imp.vbs, veranschaulicht auch die Verwendung der Import Methode und ist für die Verwendung mit Windows Script Host vorgesehen.


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



Wenn Sie die Fehler Tabelle mit Error. fra importieren und ersetzen möchten, können Sie eine Befehlszeile wie die folgende verwenden.

**Cscript Imp.vbs MNPFren.msi C: \\ Hinweis \_ Installationsprogramm \\ französischer Fehler. fra**

Zum Importieren und Ersetzen der Tabelle "aktiontext" mit "aktionte. fra" können Sie eine Befehlszeile wie die folgende verwenden.

**Cscript Imp.vbs MNPFren.msi C: \\ Note \_ Installer \\ Französisch aktionte. fra**

Führen Sie die Überprüfung auf MNPFren.msi wie unter [Validieren eines Installations Upgrades](validating-an-installation-upgrade.md)beschrieben erneut aus.

[Fortsetzen](localizing-database-columns.md)

 

 



