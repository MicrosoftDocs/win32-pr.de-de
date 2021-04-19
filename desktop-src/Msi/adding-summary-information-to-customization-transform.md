---
description: Wenn Sie die Anpassungs Transformation während einer Installation des Produkts anwenden möchten, müssen Sie der Transformations Datei mnptrans. MST, die beim Generieren einer Anpassungs Transformation generiert wurde, einen Zusammenfassungs Informationsdaten Strom hinzufügen.
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: Hinzufügen von Zusammenfassungs Informationen zur Anpassungs Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64957fcf8f29ab8793517015c7018292ba9a6e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348556"
---
# <a name="adding-summary-information-to-customization-transform"></a>Hinzufügen von Zusammenfassungs Informationen zur Anpassungs Transformation

Wenn Sie die Anpassungs Transformation während einer Installation des Produkts anwenden möchten, müssen Sie der Transformations Datei mnptrans. MST, die beim [Generieren einer Anpassungs Transformation](generating-a-customization-transform.md)generiert wurde, einen [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) hinzufügen.

Sie können zusammenfassende Informationen für eine Transformation mithilfe von " [**msikreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) " oder der [**Methode "kreatetransformsummaryinfo**](database-createtransformsummaryinfo.md)" generieren. Der folgende Code Ausschnitt, Sum.vbs, veranschaulicht die [**Methode**](database-createtransformsummaryinfo.md) "" der Methode "Methode" und "Windows Script Host". Beachten Sie, dass in diesem Beispiel keine Validierung durchführt und keine Fehlerbedingungen unterdrückt werden.


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



Zum Erstellen und Hinzufügen von Zusammenfassungs Informationen zur Transformations Datei mnptrans. MST, die Sie beim Erstellen [einer Anpassungs Transformation](generating-a-customization-transform.md)erstellt haben, ändern Sie die Verzeichnisse in den Ordner, der Gen.vbs enthält, die ursprüngliche Datenbank, die aktualisierte Datenbank und die Transformation, und geben Sie die folgende Befehlszeile ein.

**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi mnptrans. MST**

Klicken Sie auf das MNP2000.msi Symbol, um eine Installation zu starten, oder verwenden Sie die folgende Befehlszeile.

**msiexec/i MNP2000.msi**

Dadurch wird das Produkt ohne Anpassungen installiert. Um mit der Anpassung zu installieren, geben Sie die folgende Befehlszeile ein. Beachten Sie, dass sich der Wert der [**Transformationen**](transforms.md) -Eigenschaft auf die Transformations Datei bezieht, die sich in der Quelle befindet.

**msiexec/i MNP2000.msi Transformationen = mnptrans. MST**

Das Gate-Feature wird nicht in der Funktionsauswahl Struktur angezeigt, und die Komponenten der Gate-Funktion werden nicht installiert, auch wenn auf der Benutzeroberfläche ein kompletter Installationstyp ausgewählt ist.

[Fortsetzen](embedding-customization-transforms-as-substorage.md)

 

 



