---
description: Diese Anwendung veranschaulicht, wie Sie eine Handschrifterkennungsanwendung erstellen können. Das Windows Vista SDK stellt auch Versionen dieses Beispiels in C \# und Visual Basic .NET bereit.
ms.assetid: 4b3fc078-731e-4263-8e95-2c273d69a457
title: Beispiel für die Inkerkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c151c92c9f407461c34ecffb015af179e57b5c9ed4735b36f70c9a4d26c78088
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935120"
---
# <a name="ink-recognition-sample"></a>Beispiel für die Inkerkennung

Diese Anwendung veranschaulicht, wie Sie eine Handschrifterkennungsanwendung erstellen können. Das Windows Vista SDK stellt auch Versionen dieses Beispiels in C \# und Visual Basic .NET bereit. Dieses Thema bezieht sich auf die Visual Basic .NET-Beispiel, aber die Konzepte sind zwischen den Versionen identisch.

## <a name="access-the-tablet-pc-interfaces"></a>Zugreifen auf die Tablet PC-Schnittstellen

Verweisen Sie zunächst auf die Tablet PC-API, die mit dem SDK installiert wird.


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a>Initialisieren des InkCollector

Im Beispiel wird dem [Load-Ereignishandler](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) des Formulars Code hinzugefügt, der zum Zuordnen von [InkCollector](/previous-versions/ms583683(v=vs.100)), myInkCollector, zum Gruppenfeldfenster und zum Aktivieren von InkCollector dient.


```VB
Private Sub InkRecognition_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

   ' Create the recognizers collection
    myRecognizers = New Recognizers()

    ' Create an ink collector that uses the group box handle
    myInkCollector = New InkCollector(gbInkArea.Handle)

    ' Turn the ink collector on
    myInkCollector.Enabled = True

End Sub
```



## <a name="recognize-the-strokes"></a>Erkennen der Striche

Der [Click-Ereignishandler](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) des [Button-Objekts](/dotnet/api/system.windows.forms.button?view=netcore-3.1) überprüft, ob der Benutzer mindestens eine Erkennung installiert hat, indem die [Count-Eigenschaft](/previous-versions/ms828521(v=msdn.10)) der [Recognizers-Auflistung](/previous-versions/ms828520(v=msdn.10)) untersucht wird.

Die [SelectedText-Eigenschaft](/previous-versions/windows/) des Textfelds wird mithilfe der [ToString-Methode](/previous-versions/ms827836(v=msdn.10)) für die Strokes-Auflistung auf die beste Übereinstimmung für die [Striche](/previous-versions/ms552701(v=vs.100)) festgelegt. Nachdem die Striche erkannt wurden, werden sie gelöscht. Schließlich erzwingt der Code, dass der Zeichenbereich neu gezeichnet wird, und löscht ihn für die weitere Freihandverwendung.


```VB
Private Sub btnRecognize_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnRecognize.Click

    ' Check to ensure that the user has at least one recognizer installed
    ' Note that this is a preventive check - otherwise, an exception 
    ' occurs during recognition
    If 0 = myRecognizers.Count Then
        MessageBox.Show("There are no handwriting recognizers installed.  You need to have at least one in order to run this sample.")
    Else
        ' ...
        txtResults.SelectedText = myInkCollector.Ink.Strokes.ToString

        ' If the mouse is pressed, do not perform the recognition -
        ' this prevents deleting a stroke that is still being drawn
        If Not myInkCollector.CollectingInk Then

            ' Delete the ink from the ink collector
            myInkCollector.Ink.DeleteStrokes(myInkCollector.Ink.Strokes)

            ' Force the Frame to redraw (so the deleted ink goes away)
            gbInkArea.Refresh()

        End If
    End If
End Sub
```



## <a name="closing-the-form"></a>Schließen des Formulars

Die [Dispose-Methode](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) des Formulars gibt das [InkCollector-Objekt](/previous-versions/ms583683(v=vs.100)) frei.

 

 
