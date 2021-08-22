---
description: Um die Anpassungstransformation während einer Installation des Produkts anzuwenden, müssen Sie der Transformationsdatei MNPtrans.mst, die unter Generieren einer Anpassungstransformation generiert wurde, einen Zusammenfassungsinformationsstream hinzufügen.
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: Hinzufügen von Zusammenfassungsinformationen zur Anpassungstransformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ea4c9aa505d425bfd06fe5cac1f45666e794624618db14100ee5f517dd3048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639470"
---
# <a name="adding-summary-information-to-customization-transform"></a>Hinzufügen von Zusammenfassungsinformationen zur Anpassungstransformation

Um die Anpassungstransformation während einer Installation des [](summary-information-stream.md) Produkts anzuwenden, müssen Sie der Transformationsdatei MNPtrans.mst, die unter Generieren einer Anpassungstransformation generiert wurde, einen Zusammenfassungsinformationsstream [hinzufügen.](generating-a-customization-transform.md)

Sie können zusammenfassungsinformationen für eine Transformation mit [**msiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) oder der [**CreateTransformSummaryInfo-Methode generieren.**](database-createtransformsummaryinfo.md) Der folgende Codeausschnitt, Sum.vbs, veranschaulicht die [**CreateTransformSummaryInfo-Methode**](database-createtransformsummaryinfo.md) und ist für die Verwendung mit Windows Script Host. Beachten Sie, dass in diesem Beispiel keine Validierung und keine Fehlerbedingungen unterdrückt werden.


```VB
'Sum.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is sum.vbs [original database] [customized database] [transform]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
 
' Open databases and transform 
Dim database1 : Set database1 =
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 =
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
Dim transform : transform = Wscript.Arguments(2)
 
' Create and add Summary Information
Dim transinfo : transinfo =
    Database2.CreateTransformSummaryInfo(Database1, transform,0,0)
```



Ändern Sie zum Erstellen und Hinzufügen von Zusammenfassungsinformationen zur Transformationsdatei MNPtrans.mst, die Sie [in](generating-a-customization-transform.md)Generieren einer Anpassungstransformation erstellt haben, die Verzeichnisse in den Ordner mit Gen.vbs, der ursprünglichen Datenbank, der aktualisierten Datenbank und der Transformation, und geben Sie die folgende Befehlszeile ein.

**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**

Klicken Sie auf MNP2000.msi Symbol, um eine Installation zu starten oder die folgende Befehlszeile zu verwenden.

**msiexec /i MNP2000.msi**

Dadurch wird das Produkt ohne die Anpassungen installiert. Geben Sie die folgende Befehlszeile ein, um die Installation mit der Anpassung auszuführen. Beachten Sie, dass sich der Wert der [**TRANSFORMS-Eigenschaft**](transforms.md) auf die Transformationsdatei bezieht, die sich an der Quelle befindet.

**msiexec /i MNP2000.msi TRANSFORMS=MNPtrans.mst**

Das Gate-Feature wird nicht in der Funktionsauswahlstruktur angezeigt, und die Komponenten des Gate-Features werden nicht installiert, auch wenn auf der Benutzeroberfläche der Installationstyp Vollständig ausgewählt ist.

[Fortsetzen](embedding-customization-transforms-as-substorage.md)

 

 



