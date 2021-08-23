---
description: Sie können die Anpassungstransformation in einem Speicher des Pakets Windows Installer speichern, um zu gewährleisten, dass die Transformation immer verfügbar ist, wenn das Installationspaket verfügbar ist.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Einbetten von Anpassungstransformationen als Unterstorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 175c2bd1e52a58d6c73e1e46f8b95501b016bc0e4e1069b86c9c53f47859f20c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947001"
---
# <a name="embedding-customization-transforms-as-substorage"></a>Einbetten von Anpassungstransformationen als Unterstorage

Sie können die Anpassungstransformation in einem Speicher des Pakets Windows Installer speichern, um zu gewährleisten, dass die Transformation immer verfügbar ist, wenn das Installationspaket verfügbar ist. Weitere Informationen [finden Sie unter Eingebettete Transformationen.](embedded-transforms.md) Ein Beispiel hierfür finden Sie im Windows Installer SDK als WiSubStg.vbs. Der folgende Codeausschnitt Emb.vbs veranschaulicht auch die Verwendung der Tabelle ["Speicher"](-storages-table.md) zum Hinzufügen einer eingebetteten Transformation und ist für die Verwendung mit Windows Skripthosts.


```VB
'Emb.vbs. Argument(0) is the original database. Argument(1) is the
'    path to the transform file. Argument(2) is the name of the storage.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
 WScript.Echo "Usage is emb.vbs [original database] [transform] [storage name]"
 WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
 
' Evaluate command-line arguments and set open and update modes
Dim databasePath: databasePath = Wscript.Arguments(0)
Dim importPath  : importPath = Wscript.Arguments(1)
Dim storageName : storageName = Wscript.Arguments(2)
 
' Open database and create a view on the _Storages table
Dim sqlQuery : sqlQuery = "SELECT `Name`,`Data` FROM _Storages"
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim view     : Set view = database.OpenView(sqlQuery)
 
'Create and Insert the row.
Dim record   : Set record = installer.CreateRecord(2)
record.StringData(1) = storageName
view.Execute record
 
'Insert storage - copy data into stream
record.SetStream 2, importPath
view.Modify 3, record
database.Commit
Set view = Nothing
Set database = Nothing
```



Um einen Speicher namens MNPtrans1 zu MNP2000.msi hinzuzufügen und die Transformation zu enthalten, die Sie [in](adding-summary-information-to-customization-transform.md)Hinzufügen von Zusammenfassungsinformationen zur Anpassungstransformation erstellt haben, ändern Sie die Verzeichnisse in den Ordner mit Emb.vbs, der ursprünglichen Datenbank und der Transformationsdatei, und geben Sie dann die folgende Befehlszeile ein.

**Cscript.exe Emb.vbs MNP2000.msi MNPtrans.mst MNPtrans1**

Dadurch wird das Beispiel für die Anpassungstransformation abgeschlossen. Nach dem Einbetten der Transformation in MNPtrans.mst ist die Transformation immer mit dem Installationspaket verfügbar. Die Datei MNPtrans.mst muss sich nicht an der Quelle befinden, um die Transformation anzuwenden.

Entfernen Sie MNPtrans.mst aus dem Ordner, der das Beispielinstallationspaket enthält. Klicken Sie auf MNP2000.msi Symbol, um eine Installation zu starten oder die folgende Befehlszeile zu verwenden.

**msiexec /i MNP2000.msi**

Beachten Sie, dass dadurch das Produkt ohne die Anpassungen installiert wird. Geben Sie die folgende Befehlszeile ein, um die Installation mit den Anpassungen auszuführen. Verwenden Sie einen Doppelpunkt, um anzugeben, dass der Wert der [**TRANSFORMS-Eigenschaft**](transforms.md) auf eine eingebettete Transformation verweist.

msiexec /i MNP2000.msi TRANSFORMS=:MNPtrans1

Beachten Sie, dass das Gate-Feature nicht in der Funktionsauswahlstruktur angezeigt wird und dass die Komponenten des Gate-Features nicht installiert sind, auch wenn auf der Benutzeroberfläche der Installationstyp Vollständig ausgewählt ist.

## <a name="next-example"></a>Nächstes Beispiel

[Ein Beispiel für ein kleines Updatepatching](a-small-update-patching-example.md)

 

 



