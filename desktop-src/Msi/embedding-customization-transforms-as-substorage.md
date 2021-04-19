---
description: Die Anpassungs Transformation kann in einem Speicher des Windows Installer Pakets gespeichert werden, um sicherzustellen, dass die Transformation immer verfügbar ist, wenn das Installationspaket verfügbar ist.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Einbetten von Anpassungs Transformationen als unter Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362527"
---
# <a name="embedding-customization-transforms-as-substorage"></a>Einbetten von Anpassungs Transformationen als unter Speicher

Die Anpassungs Transformation kann in einem Speicher des Windows Installer Pakets gespeichert werden, um sicherzustellen, dass die Transformation immer verfügbar ist, wenn das Installationspaket verfügbar ist. Siehe [eingebettete Transformationen](embedded-transforms.md). Ein Beispiel hierfür finden Sie im Windows Installer SDK als Dienstprogramm WiSubStg.vbs. Der folgende Code Ausschnitt, Emb.vbs, veranschaulicht auch die Verwendung der [Tabelle Storages](-storages-table.md) zum Hinzufügen einer eingebetteten Transformation und ist für die Verwendung mit Windows Script Host vorgesehen.


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



Wechseln Sie zum Hinzufügen eines Speichers mit dem Namen MNPtrans1 zu MNP2000.msi und mit der Transformation, die Sie unter [Hinzufügen von Zusammenfassungs Informationen zur Anpassungs Transformation](adding-summary-information-to-customization-transform.md)erstellt haben, um Verzeichnisse in den Ordner mit Emb.vbs, die ursprüngliche Datenbank und die Transformations Datei zu ändern, und geben Sie dann die folgende Befehlszeile ein

**Cscript.exe Emb.vbs MNP2000.msi mnptrans. MST MNPtrans1**

Dadurch wird das Beispiel für die Anpassungs Transformation abgeschlossen. Nach dem Einbetten der Transformation in mnptrans. MST ist die Transformation immer mit dem Installationspaket verfügbar. Die Datei "mnptrans. mst" muss sich nicht an der Quelle befinden, um die Transformation anzuwenden.

Entfernen Sie mnptrans. MST aus dem Ordner, der das Beispiel Installationspaket enthält. Klicken Sie auf das MNP2000.msi Symbol, um eine Installation zu starten, oder verwenden Sie die folgende Befehlszeile.

**msiexec/i MNP2000.msi**

Beachten Sie, dass dadurch das Produkt ohne Anpassungen installiert wird. Um mit den Anpassungen zu installieren, geben Sie die folgende Befehlszeile ein. Verwenden Sie einen Doppelpunkt, um anzugeben, dass der Wert der [**Transformationen**](transforms.md) -Eigenschaft auf eine eingebettete Transformation verweist.

msiexec/i MNP2000.msi Transformationen =: MNPtrans1

Beachten Sie, dass die Gate-Funktion nicht in der Funktionsauswahl Struktur angezeigt wird und dass die Komponenten der Gate-Funktion nicht installiert werden, auch wenn ein kompletter Installationstyp in der Benutzeroberfläche ausgewählt ist.

## <a name="next-example"></a>Nächstes Beispiel

[Beispiel für ein kleines Update-Patching](a-small-update-patching-example.md)

 

 



