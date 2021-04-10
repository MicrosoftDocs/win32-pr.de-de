---
description: Diese Anwendung veranschaulicht, wie Sie eine Handschrift Erkennungs Anwendung erstellen können. Das Windows Vista SDK bietet auch Versionen dieses Beispiels in C \# und Visual Basic .net.
ms.assetid: 4b3fc078-731e-4263-8e95-2c273d69a457
title: Ink-Erkennungs Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d97d9d15ef64a3d7a1fe1fc5d45b3cb0454ba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214556"
---
# <a name="ink-recognition-sample"></a><span data-ttu-id="88d3c-103">Ink-Erkennungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="88d3c-103">Ink Recognition Sample</span></span>

<span data-ttu-id="88d3c-104">Diese Anwendung veranschaulicht, wie Sie eine Handschrift Erkennungs Anwendung erstellen können. Das Windows Vista SDK bietet auch Versionen dieses Beispiels in C \# und Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="88d3c-104">This application demonstrates how you can build a handwriting recognition application.The Windows Vista SDK provides versions of this sample in C\# and Visual Basic .NET, as well.</span></span> <span data-ttu-id="88d3c-105">Dieses Thema bezieht sich auf das Visual Basic .NET-Beispiel, aber die Konzepte sind Zwischenversionen identisch.</span><span class="sxs-lookup"><span data-stu-id="88d3c-105">This topic refers to the Visual Basic .NET sample, but the concepts are the same between versions.</span></span>

## <a name="access-the-tablet-pc-interfaces"></a><span data-ttu-id="88d3c-106">Zugreifen auf die Tablet PC-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="88d3c-106">Access the Tablet PC Interfaces</span></span>

<span data-ttu-id="88d3c-107">Verweisen Sie zunächst auf die Tablet PC-API, die mit dem SDK installiert wird.</span><span class="sxs-lookup"><span data-stu-id="88d3c-107">First, reference the Tablet PC API, which are installed with the SDK.</span></span>


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a><span data-ttu-id="88d3c-108">"InkCollector" Initialisieren</span><span class="sxs-lookup"><span data-stu-id="88d3c-108">Initialize the InkCollector</span></span>

<span data-ttu-id="88d3c-109">Das Beispiel fügt dem [Lade](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) Ereignishandler des Formulars Code hinzu, mit dem der [InkCollector](/previous-versions/ms583683(v=vs.100)), myinkcollector, dem Gruppenfeld Fenster zugeordnet und der InkCollector aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="88d3c-109">The sample adds code to the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler that serves to associate the [InkCollector](/previous-versions/ms583683(v=vs.100)), myInkCollector, with the group box window and enable the InkCollector.</span></span>


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



## <a name="recognize-the-strokes"></a><span data-ttu-id="88d3c-110">Erkennen der Striche</span><span class="sxs-lookup"><span data-stu-id="88d3c-110">Recognize the Strokes</span></span>

<span data-ttu-id="88d3c-111">Der [Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) -Ereignishandler des [Schalt](/dotnet/api/system.windows.forms.button?view=netcore-3.1) Flächen Objekts prüft, ob der Benutzer mindestens eine Erkennung installiert hat, indem er die [count](/previous-versions/ms828521(v=msdn.10)) -Eigenschaft der [Erkennungs](/previous-versions/ms828520(v=msdn.10)) -Auflistung untersucht.</span><span class="sxs-lookup"><span data-stu-id="88d3c-111">The [Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) object's [Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event handler checks to ensure that the user has at least one recognizer installed by examining the [Count](/previous-versions/ms828521(v=msdn.10)) property of the [Recognizers](/previous-versions/ms828520(v=msdn.10)) collection.</span></span>

<span data-ttu-id="88d3c-112">Die [SelectedText](/previous-versions/windows/) -Eigenschaft des Textfelds wird auf die beste Entsprechung für die Striche festgelegt, indem die Methode " [destring](/previous-versions/ms827836(v=msdn.10)) " für die [Striche](/previous-versions/ms552701(v=vs.100)) -Auflistung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="88d3c-112">The [SelectedText](/previous-versions/windows/) property of the text box is set to the best match for the strokes using the [ToString](/previous-versions/ms827836(v=msdn.10)) method on the [Strokes](/previous-versions/ms552701(v=vs.100)) collection.</span></span> <span data-ttu-id="88d3c-113">Nachdem die Striche erkannt wurden, werden Sie gelöscht.</span><span class="sxs-lookup"><span data-stu-id="88d3c-113">After the strokes have been recognized, they are deleted.</span></span> <span data-ttu-id="88d3c-114">Schließlich erzwingt der Code das Neuzeichnen von Zeichnungs Flächen und löscht ihn für weitere frei Hand Eingaben.</span><span class="sxs-lookup"><span data-stu-id="88d3c-114">Finally, the code forces drawing area repaint, clearing it for further ink use.</span></span>


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



## <a name="closing-the-form"></a><span data-ttu-id="88d3c-115">Schließen des Formulars</span><span class="sxs-lookup"><span data-stu-id="88d3c-115">Closing the Form</span></span>

<span data-ttu-id="88d3c-116">Die [verwerfen-Methode des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="88d3c-116">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
