---
description: Sie können eine Transformationsdatei mithilfe von MsiDatabaseGenerateTransform oder der GenerateTransform-Methode des Database-Objekts generieren.
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: Generieren einer Anpassungstransformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b790917100cc06da97e09fd8aabf45b580e62008d23c9fc5065e6005112d8d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635998"
---
# <a name="generating-a-customization-transform"></a>Generieren einer Anpassungstransformation

Sie können eine Transformationsdatei generieren, indem Sie [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) oder die [**GenerateTransform-Methode**](database-generatetransform.md) des [**Database-Objekts verwenden.**](database-object.md) Ein Beispiel hierfür finden Sie im Windows Installer SDK als Hilfsprogramm WiGenXfm.vbs. Der folgende Codeausschnitt Gen.vbs veranschaulicht auch die **GenerateTransform-Methode** und ist für die Verwendung mit Windows Script Host vorgesehen.


```VB
'Gen.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is gen.vbs [original database] [customized database] [transform file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
' Open databases
Dim database1 : Set database1 = 
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 = 
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
' Generate transform
Dim transform : transform = Database2.GenerateTransform(Database1,
    Wscript.Arguments(2))
```



Um die Transformationsdatei MNPtrans.mst aus der ursprünglichen MNP2000.msi Datenbank und der MNP2000t.msi Datenbank zu generieren, die Sie unter [Anpassen einer ursprünglichen Datenbank](customizing-an-original-database.md)geändert haben, ändern Sie die Verzeichnisse in den Ordner mit Gen.vbs, der ursprünglichen Datenbank und der aktualisierten Installationsprogrammdatenbank, und geben Sie die folgende Befehlszeile ein.

**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**

[Fortsetzen](adding-summary-information-to-customization-transform.md)

 

 



