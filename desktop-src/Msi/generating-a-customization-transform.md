---
description: Sie können eine Transformations Datei mithilfe von "msidatabasegeneratetransform" oder der GenerateTransform-Methode des Datenbankobjekts generieren.
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: Erstellen einer Anpassungs Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f73609b7be60dbfe236d31ed5a865e86ff6e310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347666"
---
# <a name="generating-a-customization-transform"></a>Erstellen einer Anpassungs Transformation

Sie können eine Transformations Datei mithilfe von " [**msidatabasegeneratetransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) " oder der [**GenerateTransform-Methode**](database-generatetransform.md) des [**Datenbankobjekts**](database-object.md)generieren. Ein Beispiel hierfür finden Sie im Windows Installer SDK als Dienstprogramm WiGenXfm.vbs. Der folgende Code Ausschnitt, Gen.vbs, veranschaulicht auch die **GenerateTransform** -Methode und ist für die Verwendung mit Windows Script Host vorgesehen.


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



Um die Transformations Datei mnptrans. MST aus der ursprünglichen MNP2000.msi Datenbank und die MNP2000t.msi Datenbank zu generieren, die Sie beim [Anpassen einer ursprünglichen Datenbank](customizing-an-original-database.md)geändert haben, ändern Sie die Verzeichnisse in den Ordner, der Gen.vbs, die ursprüngliche Datenbank und die aktualisierte Installer-Datenbank enthält, und geben Sie die folgende Befehlszeile ein.

**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi mnptrans. MST**

[Fortsetzen](adding-summary-information-to-customization-transform.md)

 

 



