---
description: Diese Anwendung basiert auf dem InkCollector-Objekt und veranschaulicht die Auflistung von Ink.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Beispiel für die Ink-Sammlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5f568abf38abfa31d9374a7a1874f9f73481a799a740c402f3e8f168963c3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718259"
---
# <a name="ink-collection-sample"></a>Beispiel für die Ink-Sammlung

Diese Anwendung basiert auf dem [InkCollector-Objekt](/previous-versions/ms836493(v=msdn.10)) und veranschaulicht die Auflistung von Ink. Die Anwendung erstellt ein Fenster, angefügt ein InkCollector-Objekt und stellt dem Benutzer Menüoptionen zur Verfügung, die zum Ändern der Farbe der Ink-Farbe, der Breite der Ink-Objekte und zum Aktivieren und Deaktivieren der Ink-Sammlung verwendet werden können.

> [!Note]  
> Die in diesem Abschnitt erläuterte Version ist Visual Basic .NET. Die Konzepte sind bei anderen Sprachversionen in der Beispielbibliothek identisch.

 

## <a name="declaring-the-inkcollector"></a>Deklarieren des InkCollector

Die Anwendung importiert zunächst den [Microsoft.Ink-Namespace.](/previous-versions/ms826516(v=msdn.10)) Anschließend deklariert die Anwendung , die `myInkCollector` das [InkCollector-Objekt](/previous-versions/ms836493(v=msdn.10)) für das Formular enthält.


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a>Einrichten der Dinge

Die -Methode des `InkCollection_Load` Formulars behandelt das [Load-Ereignis des Formulars.](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) Er erstellt ein [InkCollector-Objekt,](/previous-versions/ms836493(v=msdn.10)) das dem Formular zugewiesen ist, ändert die [DefaultDrawingAttributes-Eigenschaft](/previous-versions/ms836500(v=msdn.10)) des InkCollector-Objekts und aktiviert das InkCollector-Objekt.


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



Der [InkCollector](/previous-versions/ms836493(v=msdn.10)) wird dem Fenster des Formulars zugewiesen, indem der Handle-Eigenschaft des InkCollector-Objekts das Fensterhandle des [Formulars zugewiesen](/previous-versions/ms836504(v=msdn.10)) wird. Die Ink-Sammlung wird aktiviert, indem die [Enabled-Eigenschaft](/previous-versions/ms836503(v=msdn.10)) des InkCollector-Objekts auf **TRUEfestgeschaltet wird.**

Die [DefaultDrawingAttributes-Eigenschaft](/previous-versions/ms836500(v=msdn.10)) des [InkCollector-Objekts](/previous-versions/ms836493(v=msdn.10)) legt die Standardattribute fest, die einem neuen Cursor zugewiesen sind. Verwenden Sie zum Festlegen verschiedener Attribute für einen neuen Cursor die [DrawingAttributes-Eigenschaft](/previous-versions/ms839523(v=msdn.10)) des [Cursorobjekts.](/previous-versions/ms839521(v=msdn.10)) Um die Zeichnungsattribute eines einzelnen Strichs zu ändern, verwenden Sie die [DrawingAttributes-Eigenschaft](/previous-versions/ms827846(v=msdn.10)) des [Stroke-Objekts.](/previous-versions/ms827842(v=msdn.10))

## <a name="changing-the-properties"></a>Ändern der Eigenschaften

Der Rest dieser einfachen Anwendung besteht aus Handlern für die verschiedenen Menüauswahlen, die der Benutzer treffen kann. Wenn der Benutzer beispielsweise die Freidruckfarbe durch Auswahl von Rot im Freidruckmenü in Rot ändert, wird die Farbe mithilfe der [Color-Eigenschaft](/previous-versions/ms837933(v=msdn.10)) der [DefaultDrawingAttributes-Eigenschaft](/previous-versions/ms836500(v=msdn.10)) des [InkCollector-Objekts](/previous-versions/ms836493(v=msdn.10)) im Ereignishandler für das Menü geändert.


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a>Schließen des Formulars

Die Dispose-Methode [des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector-Objekt](/previous-versions/ms836493(v=msdn.10)) `myInkCollector` zurück.

 

 
