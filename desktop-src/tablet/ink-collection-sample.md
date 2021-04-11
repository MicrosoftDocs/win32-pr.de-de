---
description: Diese Anwendung basiert auf dem InkCollector-Objekt und veranschaulicht die Auflistung von frei Hand Eingaben.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Ink Collection-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f31ce83a55b6f352d76ad1cb8d184b41618c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128996"
---
# <a name="ink-collection-sample"></a>Ink Collection-Beispiel

Diese Anwendung basiert auf dem [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt und veranschaulicht die Auflistung von frei Hand Eingaben. Die Anwendung erstellt ein Fenster, fügt ein InkCollector-Objekt an Sie an und stellt dem Benutzermenü Optionen zur Verfügung, die zum Ändern der frei Hand Farbe, der frei Handbreite und zum Aktivieren und Deaktivieren der frei Hand Eingabe verwendet werden können.

> [!Note]  
> Die in diesem Abschnitt erörterte Version ist Visual Basic .net. Die Konzepte sind zwischen anderen Sprachversionen in der Samples Library identisch.

 

## <a name="declaring-the-inkcollector"></a>Der InkCollector wird deklariert.

Die Anwendung importiert zuerst den [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) -Namespace. Anschließend deklariert die Anwendung `myInkCollector` , die das [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt für das Formular enthält.


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a>Einrichten von Aufgaben

Die-Methode des Formulars `InkCollection_Load` behandelt das [Lade](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) Ereignis des Formulars. Es erstellt ein [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt, das dem Formular zugewiesen ist, ändert die [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) -Eigenschaft des InkCollector-Objekts und aktiviert das InkCollector-Objekt.


```C++
Private Sub InkCollection_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

    ' Create an ink collector and assign it to this form's window
    myInkCollector = New InkCollector(Me.Handle)

    ' Set the pen width to be a medium width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth

    ' If you do not modify the default drawing attributes, the default 
    ' drawing attributes will use the following properties and values:
    ' ...

    ' Turn the ink collector on
    myInkCollector.Enabled = True
End Sub
```



Der [InkCollector](/previous-versions/ms836493(v=msdn.10)) wird dem Fenster des Formulars zugewiesen, indem das Fenster Handle des Formulars der [handle](/previous-versions/ms836504(v=msdn.10)) -Eigenschaft des InkCollector-Objekts zugewiesen wird. Die frei Hand Auflistung wird aktiviert, indem die [aktivierte](/previous-versions/ms836503(v=msdn.10)) Eigenschaft des InkCollector-Objekts auf **true** festgelegt wird.

Die [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) -Eigenschaft des [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekts legt die Standard Attribute fest, die einem neuen Cursor zugewiesen werden. Um unterschiedliche Attribute für einen neuen Cursor festzulegen, verwenden Sie die [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) -Eigenschaft des [Cursor](/previous-versions/ms839521(v=msdn.10)) Objekts. Verwenden Sie die [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) -Eigenschaft des [Stroke](/previous-versions/ms827842(v=msdn.10)) -Objekts, um die Zeichnungs Attribute eines einzelnen Strichs zu ändern.

## <a name="changing-the-properties"></a>Ändern der Eigenschaften

Der Rest dieser einfachen Anwendung besteht aus Handlern für die verschiedenen Menü Optionen, die der Benutzer treffen kann. Wenn der Benutzer z. b. die frei Hand Farbe in Rot ändern möchte, indem er im frei Hand Menü Rot ausgewählt wird, wird die Farbe mithilfe der [Color](/previous-versions/ms837933(v=msdn.10)) -Eigenschaft für die [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) -Eigenschaft des [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekts im Ereignishandler für das Menü geändert.


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a>Schließen des Formulars

Die [verwerfen-Methode des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt frei `myInkCollector` .

 

 
