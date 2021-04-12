---
description: Das Beispiel für automatische Ansprüche adressiert ein hypothetisches Szenario für einen Versicherungs Prüfer.
ms.assetid: bec4333a-62ca-4254-a39b-04bc2c556992
title: Beispiel für automatisches Anspruchsformular
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5ff78a3c38036ef9352660b4d7959e2ad87e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346889"
---
# <a name="auto-claims-form-sample"></a><span data-ttu-id="c4e7a-103">Beispiel für automatisches Anspruchsformular</span><span class="sxs-lookup"><span data-stu-id="c4e7a-103">Auto Claims Form Sample</span></span>

<span data-ttu-id="c4e7a-104">Das Beispiel für automatische Ansprüche adressiert ein hypothetisches Szenario für einen Versicherungs Prüfer.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-104">The Auto Claims sample addresses a hypothetical scenario for an insurance assessor.</span></span> <span data-ttu-id="c4e7a-105">Die Arbeit des assors erfordert, dass er mit den Clients zu Hause oder Unternehmen besucht und seine Anspruchs Informationen in ein Formular eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-105">The assessor's work requires him or her to visit with clients at their home or business and to enter their claim information into a form.</span></span> <span data-ttu-id="c4e7a-106">Zur Steigerung der Produktivität des assors entwickelt seine IT-Abteilung eine Tablet-Anwendung, die es Ihnen oder Ihnen ermöglicht, Anspruchs Informationen schnell und genau über zwei Ink-Steuerelemente einzugeben: [InkEdit](/previous-versions/ms835842(v=msdn.10)) -und [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-106">To increase the assessor's productivity, his IT department develops a tablet application that enables him or her to quickly and accurately enter claim information through two ink controls: [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls.</span></span>

<span data-ttu-id="c4e7a-107">In diesem Beispiel wird ein [InkEdit](/previous-versions/ms835842(v=msdn.10)) -Steuerelement für jedes Texteingabefeld verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-107">In this sample, a [InkEdit](/previous-versions/ms835842(v=msdn.10)) control is used for each text input field.</span></span> <span data-ttu-id="c4e7a-108">Ein Benutzer gibt die relevanten Informationen über eine Versicherungsrichtlinie und ein Fahrzeug in diese Felder mit einem Stift ein.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-108">A user enters the relevant information about an insurance policy and vehicle into these fields with a pen.</span></span> <span data-ttu-id="c4e7a-109">Das [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelement wird zum Hinzufügen von frei Hand Eingaben über ein Auto Mobil Bild verwendet, um beschädigte Bereiche des Autos hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-109">The [InkPicture](/previous-versions/ms583740(v=vs.100)) control is used to add ink over an automobile image to highlight damaged areas of the automobile.</span></span> <span data-ttu-id="c4e7a-110">Das Beispiel für automatische Ansprüche ist für C \# und Microsoft Visual Basic .net verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-110">The Auto Claims sample is available for C\# and Microsoft Visual Basic .NET.</span></span> <span data-ttu-id="c4e7a-111">In diesem Thema wird das Visual Basic .net beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-111">This topic describes the Visual Basic .NET.</span></span>

<span data-ttu-id="c4e7a-112">Die autoclaims-Klasse ist als eine Unterklasse von [System. Windows. Forms. Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) definiert, und eine-Klasse, die für die Erstellung und Verwaltung von Freihand Ebenen für unterschiedliche Arten von Beschädigungen definiert ist.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-112">The AutoClaims Class is defined as a subclass of [System.Windows.Forms.Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , and a nested class is defined for creating and managing layers of ink for different types of damage.</span></span> <span data-ttu-id="c4e7a-113">Vier Ereignishandler werden definiert, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-113">Four event handlers are defined to perform the following tasks:</span></span>

-   <span data-ttu-id="c4e7a-114">Die Formular-und Freihand Ebenen werden initialisiert.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-114">Initializing the form and ink layers.</span></span>
-   <span data-ttu-id="c4e7a-115">Das [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelement wird neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-115">Redrawing the [InkPicture](/previous-versions/ms583740(v=vs.100)) control.</span></span>
-   <span data-ttu-id="c4e7a-116">Auswählen einer Freihand Schicht durch das Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-116">Selecting an ink layer through the list box.</span></span>
-   <span data-ttu-id="c4e7a-117">Ändern der Sichtbarkeit einer Freihand Schicht.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-117">Changing the visibility of an ink layer.</span></span>

> [!Note]  
> <span data-ttu-id="c4e7a-118">Versionen dieses Beispiels sind in C \# und Visual Basic .net verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-118">Versions of this sample are available in C\# and Visual Basic .NET.</span></span> <span data-ttu-id="c4e7a-119">Die in diesem Abschnitt erörterte Version ist Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-119">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="c4e7a-120">Die Konzepte sind Zwischenversionen identisch.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-120">The concepts are the same between versions.</span></span>

 

## <a name="defining-the-form-and-ink-layers"></a><span data-ttu-id="c4e7a-121">Definieren von Formular-und Freihand Ebenen</span><span class="sxs-lookup"><span data-stu-id="c4e7a-121">Defining the Form and Ink Layers</span></span>

<span data-ttu-id="c4e7a-122">Sie müssen den [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) -Namespace importieren:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-122">You need to import the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace:</span></span>


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



<span data-ttu-id="c4e7a-123">Im nächsten Schritt wird in der autoclaims-Klasse eine `InkLayer` -Klasse definiert und ein Array aus vier- `InkLayer` Objekten deklariert.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-123">Next, in the AutoClaims Class, a nested `InkLayer` class is defined and an array of four `InkLayer` objects is declared.</span></span> <span data-ttu-id="c4e7a-124">(Inklayer enthält ein [Microsoft. Ink.](/previous-versions/ms583670(v=vs.100)) Ink-Objekt zum Speichern von "Ink" und " [System. Drawing. Color](/dotnet/api/system.drawing.color?view=netcore-3.1) " und **boolesche** Werte zum Speichern der Farbe und des verborgenen Zustands der Ebene.) Ein fünftes Ink-Objekt wird deklariert, um frei Hand Eingaben für das [InkPicture](/previous-versions/ms583740(v=vs.100)) zu behandeln, wenn alle frei Hand Ebenen ausgeblendet sind.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-124">(InkLayer contains an [Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100)) object for storing ink, and [System.Drawing.Color](/dotnet/api/system.drawing.color?view=netcore-3.1) and **Boolean** values for storing the color and hidden state of the layer.) A fifth Ink object is declared to handle ink for the [InkPicture](/previous-versions/ms583740(v=vs.100)) when all of the ink layers are hidden.</span></span>


```VB
' Declare the array of ink layers used the vehicle illustration.
Dim inkLayers(3) As InkLayer

' Declare an empty ink object (used when we don't want to draw
' any ink).
Dim emptyInk As Ink

' Declare a value to hold the index of selected ink
Dim selectedIndex As Integer

' Declare a value to hold whether the selected ink is hidden
Dim selectedHidden As Boolean 
```




```VB
// Declare the array of ink layers used the vehicle illustration.
InkLayer[] inkLayers;

// Declare an empty ink object (used when we don't want to draw
// any ink).
Ink emptyInk;

// Declare a value to hold the index of selected ink
int selectedIndex = -1;

// Declare a value to hold whether the selected ink is hidden
bool selectedHidden = false;
```



<span data-ttu-id="c4e7a-125">Jede Ebene verfügt über ein eigenes [Ink](/previous-versions/ms583670(v=vs.100)) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-125">Each layer has its own [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span> <span data-ttu-id="c4e7a-126">Das Anspruchsformular (Body, Windows, Tiers und Scheinwerfer) enthält vier diskrete Bereiche, sodass vier inklayer-Objekte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-126">There are four discrete areas of interest in the claim form (body, windows, tires, and headlights), so four InkLayer objects are used.</span></span> <span data-ttu-id="c4e7a-127">Ein Benutzer kann eine beliebige Kombination von Ebenen gleichzeitig anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-127">A user can view any combination of layers at once.</span></span>

## <a name="initializing-the-form-and-ink-layers"></a><span data-ttu-id="c4e7a-128">Initialisieren von Formular-und Freihand Ebenen</span><span class="sxs-lookup"><span data-stu-id="c4e7a-128">Initializing the Form and Ink Layers</span></span>

<span data-ttu-id="c4e7a-129">Der `Load` Ereignishandler initialisiert das [](/previous-versions/ms583670(v=vs.100)) frei Hand Objekt und die vier `InkLayer` Objekte.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-129">The `Load` event handler initializes the [Ink](/previous-versions/ms583670(v=vs.100)) object and the four `InkLayer` objects.</span></span>


```VB
' Initialize the empty ink
emptyInk = New Ink()

' Initialize the four different layers of ink on the vehicle diagram:  
' vehicle body, windows, tires, and headlights.
inkLayers(0) = New InkLayer(New Ink(), Color.Red, False)
inkLayers(1) = New InkLayer(New Ink(), Color.Violet, False)
inkLayers(2) = New InkLayer(New Ink(), Color.LightGreen, False)
inkLayers(3) = New InkLayer(New Ink(), Color.Aqua, False)
```




```VB
// Initialize the empty ink
emptyInk = new Ink();

// Initialize the four different layers of ink on the vehicle diagram:  
// vehicle body, windows, tires, and headlights.
inkLayers = new InkLayer[4];
inkLayers[0] = new InkLayer(new Ink(), Color.Red, false);
inkLayers[1] = new InkLayer(new Ink(), Color.Violet, false);
inkLayers[2] = new InkLayer(new Ink(), Color.LightGreen, false);
inkLayers[3] = new InkLayer(new Ink(), Color.Aqua, false);
```



<span data-ttu-id="c4e7a-130">Wählen Sie dann den ersten Eintrag (Text) im Listenfeld aus.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-130">Then, select the first entry (Body) in the list box.</span></span>


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



<span data-ttu-id="c4e7a-131">Legen Sie abschließend die frei Hand Farbe für das [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelement auf den aktuell ausgewählten Listenfeld Eintrag fest.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-131">Finally, set the ink color for the [InkPicture](/previous-versions/ms583740(v=vs.100)) control to the currently selected list box entry.</span></span>


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a><span data-ttu-id="c4e7a-132">Umzeichnen des InkPicture-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="c4e7a-132">Redrawing the InkPicture Control</span></span>

<span data-ttu-id="c4e7a-133">Im geerbten [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) -Ereignishandler des [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuer Elements werden die frei Hand Ebenen geprüft, um zu bestimmen, welche ausgeblendet sind.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-133">In the [InkPicture](/previous-versions/ms583740(v=vs.100)) Control's inherited [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event handler, the ink layers are checked to determine which are hidden.</span></span> <span data-ttu-id="c4e7a-134">Wenn eine Ebene nicht ausgeblendet ist, wird Sie von der Ereignis Prozedur mithilfe der [Draw](/previous-versions/ms828488(v=msdn.10)) -Methode der [Renderer](/previous-versions/ms582196(v=vs.100)) -Eigenschaft angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-134">If a layer is not hidden, the event procedure displays it by using the [Renderer](/previous-versions/ms582196(v=vs.100)) property's [Draw](/previous-versions/ms828488(v=msdn.10)) method.</span></span> <span data-ttu-id="c4e7a-135">Wenn Sie die Objektkatalog betrachten, sehen Sie, dass die Microsoft. Ink. InkPicture. Renderer-Eigenschaft als [Microsoft. Ink. Renderer](/previous-versions/ms828481(v=msdn.10)) -Objekt definiert ist:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-135">If you look in the Object Browser, you'll see that the Microsoft.Ink.InkPicture.Renderer property is defined as a [Microsoft.Ink.Renderer](/previous-versions/ms828481(v=msdn.10)) object:</span></span>


```VB
Private Sub inkPictVehicle_Paint(ByVal sender As System.Object, ByVal e As System.Windows.Forms.PaintEventArgs) Handles inkPictVehicle.Paint
    Dim layer As InkLayer

    ' Cycle through each ink layer.  If it is visible, paint it.
    ' Note that it is necessary to customize the paint
    ' behavior, since we want to hide/show different ink layers.
    For Each layer In inkLayers
        If (Not layer.Hidden) Then
            inkPictVehicle.Renderer.Draw(e.Graphics, layer.ActiveInk.Strokes)
        End If
    Next
End Sub
```




```VB
private void inkPictVehicle_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    // Cycle through each ink layer.  If it is visible, paint it.
    // Note that it is necessary to customize the paint
    // behavior, since we want to hide/show different ink layers.
    foreach (InkLayer layer in inkLayers)
    {
        if (!layer.Hidden)
        {
             inkPictVehicle.Renderer.Draw(e.Graphics,layer.ActiveInk.Strokes);
        }
    }          
}
```



## <a name="selecting-an-ink-layer-through-the-list-box"></a><span data-ttu-id="c4e7a-136">Auswählen einer Freihand Schicht über das Listenfeld</span><span class="sxs-lookup"><span data-stu-id="c4e7a-136">Selecting an Ink Layer through the List Box</span></span>

<span data-ttu-id="c4e7a-137">Wenn der Benutzer ein Element im Listenfeld auswählt, prüft der [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) -Ereignishandler zunächst, ob die Auswahl geändert wurde und das [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelement momentan keine Freihand sammelt.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-137">When the user selects an item in the list box, the [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="c4e7a-138">Anschließend wird die frei Hand Farbe des InkPicture-Steuer Elements auf die entsprechende Farbe für die ausgewählte Freihand-Ebene festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-138">It then sets the ink color of the InkPicture control to the appropriate color for the selected ink layer.</span></span> <span data-ttu-id="c4e7a-139">Außerdem wird das Kontrollkästchen Ebene ausblenden so aktualisiert, dass der verborgene Status der ausgewählten Freihand Schicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-139">Also, it updates the Hide Layer check box to reflect the selected ink layer's hidden status.</span></span> <span data-ttu-id="c4e7a-140">Schließlich wird die geerbte [Aktualisierungs](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) Methode des InkPicture-Steuer Elements verwendet, um nur die gewünschten Ebenen innerhalb des Steuer Elements anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-140">Finally, the InkPicture control's inherited [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
       Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
       End If
   End If
End Sub
```




```VB
private void lstAnnotationLayer_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Provided that the new selected index value is different than
    // the previous value...
    if (lstAnnotationLayer.SelectedIndex != selectedIndex) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Set the ink and visiblity of the current ink layer
            inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
            chHideLayer.Checked = inkLayers[lstAnnotationLayer.SelectedIndex].Hidden;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;
    
            selectedIndex = lstAnnotationLayer.SelectedIndex;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the selection to its previous value.
            lstAnnotationLayer.SelectedIndex = selectedIndex;
            MessageBox.Show("Cannot change active ink while collecting ink.");
        }
    }
}
```



## <a name="changing-the-visibility-of-an-ink-layer"></a><span data-ttu-id="c4e7a-141">Ändern der Sichtbarkeit einer Freihand Schicht</span><span class="sxs-lookup"><span data-stu-id="c4e7a-141">Changing the Visibility of an Ink Layer</span></span>

<span data-ttu-id="c4e7a-142">Der `CheckedChanged` Ereignishandler prüft zunächst, ob die Auswahl geändert wurde und dass das [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelement zurzeit keine Freihand sammelt.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-142">The `CheckedChanged` event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="c4e7a-143">Anschließend wird der verborgene Status der ausgewählten Freihand Schicht aktualisiert, und die InkEnabled des InkPicture-Steuer Elements wird auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-143">It then updates the selected ink layer's hidden status, sets the InkPicture control's InkEnabled to **FALSE**, .</span></span>

<span data-ttu-id="c4e7a-144">Als nächstes wird die InkEnabled-Eigenschaft des InkPicture-Steuer Elements vor dem Aktualisieren der Ink-Eigenschaft auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-144">Next, the InkPicture control's InkEnabled property is set to **FALSE** before updating its Ink property.</span></span>

<span data-ttu-id="c4e7a-145">Zum Schluss ist das [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelement für den jeweiligen Fahrzeugteil entweder aktiviert oder deaktiviert, je nachdem, ob das Kontrollkästchen Ebene ausblenden aktiviert ist, und die [Aktualisierungs](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) Methode des InkPicture-Steuer Elements wird verwendet, um nur die gewünschten Ebenen innerhalb des Steuer Elements anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-145">Finally, the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is either enabled or disabled for the particular vehicle part based on whether the Hide Layer check box is selected, and the InkPicture control's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
        Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
        End If
    End If
End Sub
```




```VB
private void chHideLayer_CheckedChanged(object sender, System.EventArgs e)
{
    // Provided that the new checked hidden value is different than
    // the previous value...
    if (chHideLayer.Checked != selectedHidden) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Update the array indicating the visibility of each ink layer
            inkLayers[lstAnnotationLayer.SelectedIndex].Hidden = chHideLayer.Checked;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
 
            // If the layer is marked hidden, disable ink collections
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;

            // Update the previous checkbox value to reflect the current
            selectedHidden = chHideLayer.Checked;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden;
            MessageBox.Show("Cannot change visiblity while collecting ink.");
        }
    }
}
```



## <a name="closing-the-form"></a><span data-ttu-id="c4e7a-146">Schließen des Formulars</span><span class="sxs-lookup"><span data-stu-id="c4e7a-146">Closing the Form</span></span>

<span data-ttu-id="c4e7a-147">Im vom Windows Form-Designer generierten Code werden die Steuerelemente [InkEdit](/previous-versions/ms835842(v=msdn.10)) und [InkPicture](/previous-versions/ms583740(v=vs.100)) der Komponentenliste des Formulars hinzugefügt, wenn das Formular initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-147">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="c4e7a-148">Wenn das Formular geschlossen wird, werden die InkEdit-und InkPicture-Steuerelemente sowie die anderen Komponenten des Formulars von der [verwerfen-Methode](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) des Formulars entfernt.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-148">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) method.</span></span> <span data-ttu-id="c4e7a-149">Die verwerfen-Methode des Formulars gibt auch die frei [Hand Objekte frei, die für](/previous-versions/ms583670(v=vs.100)) das Formular erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-149">The form's Dispose method also disposes the [Ink](/previous-versions/ms583670(v=vs.100)) objects that are created for the form.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4e7a-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4e7a-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c4e7a-151">[Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="c4e7a-151">[Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="c4e7a-152">InkPicture-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c4e7a-152">InkPicture Control</span></span>](inkpicture-control.md)
</dt> <dt>

[<span data-ttu-id="c4e7a-153">InkEdit-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c4e7a-153">InkEdit Control</span></span>](inkedit-control.md)
</dt> </dl>

 

 
