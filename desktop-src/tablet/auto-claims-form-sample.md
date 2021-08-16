---
description: Im Beispiel für automatische Ansprüche wird ein hypothetisches Szenario für einen Versicherungsbewerter behandelt.
ms.assetid: bec4333a-62ca-4254-a39b-04bc2c556992
title: Beispiel für ein Formular für automatische Ansprüche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe22545d60ad4116e2607f3fcf01feb94dbfecaa74bc591288e4d91b6d3d465
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857118"
---
# <a name="auto-claims-form-sample"></a>Beispiel für ein Formular für automatische Ansprüche

Im Beispiel für automatische Ansprüche wird ein hypothetisches Szenario für einen Versicherungsbewerter behandelt. Die Arbeit des Bewerter erfordert, dass er zu Hause oder im Unternehmen Kunden besucht und seine Anspruchsinformationen in ein Formular eingeben muss. Um die Produktivität des Bewerters zu steigern, entwickelt seine IT-Abteilung eine Tablet-Anwendung, mit der er anspruchsinformationen schnell und genau über zwei Ink-Steuerelemente eingeben kann: [InkEdit-](/previous-versions/ms835842(v=msdn.10)) und [InkPicture-Steuerelemente.](/previous-versions/ms583740(v=vs.100))

In diesem Beispiel wird für jedes [Texteingabefeld ein InkEdit-Steuerelement](/previous-versions/ms835842(v=msdn.10)) verwendet. Ein Benutzer gibt die relevanten Informationen zu einer Versicherungsrichtlinie und einem Fahrzeug mit einem Stift in diese Felder ein. Das [InkPicture-Steuerelement](/previous-versions/ms583740(v=vs.100)) wird verwendet, um Ink über einem Automobilbild hinzuzufügen, um beschädigte Bereiche des Autos hervorzuheben. Das Beispiel für automatische Ansprüche ist für C und \# Microsoft Visual Basic .NET verfügbar. In diesem Thema wird die Visual Basic .NET beschrieben.

Die AutoClaims-Klasse wird als Unterklasse von [System.Windows. Forms.Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) und eine geschachtelte Klasse werden definiert, um Ebenen von Ink für verschiedene Arten von Schäden zu erstellen und zu verwalten. Vier Ereignishandler werden definiert, um die folgenden Aufgaben auszuführen:

-   Initialisieren der Formular- und Ink-Ebenen.
-   Neuzeichnung des [InkPicture-Steuerelements.](/previous-versions/ms583740(v=vs.100))
-   Auswählen einer Ink-Ebene über das Listenfeld.
-   Ändern der Sichtbarkeit einer Ink-Schicht.

> [!Note]  
> Versionen dieses Beispiels sind in C und \# Visual Basic .NET verfügbar. Die in diesem Abschnitt erläuterte Version ist Visual Basic .NET. Die Konzepte sind in den verschiedenen Versionen identisch.

 

## <a name="defining-the-form-and-ink-layers"></a>Definieren der Formular- und Ink-Ebenen

Sie müssen den [Microsoft.Ink-Namespace](/previous-versions/ms826516(v=msdn.10)) importieren:


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



Als Nächstes wird in der AutoClaims-Klasse eine geschachtelte Klasse definiert und ein `InkLayer` Array von vier `InkLayer` -Objekten deklariert. (InkLayer enthält ein [Microsoft.Ink.Ink-Objekt](/previous-versions/ms583670(v=vs.100)) zum Speichern von Freidruck sowie [System.Drawing.Color](/dotnet/api/system.drawing.color?view=netcore-3.1) und **boolesche** Werte zum Speichern der Farbe und des ausgeblendeten Zustands der Ebene.) Ein fünftes Ink-Objekt wird für die Verarbeitung von InkPicture deklariert, wenn alle [InkPicture-Ebenen](/previous-versions/ms583740(v=vs.100)) ausgeblendet sind.


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



Jede Ebene verfügt über ein eigenes [Ink-Objekt.](/previous-versions/ms583670(v=vs.100)) Es gibt vier diskrete Interessenbereiche in der Anspruchsform (Körper, Fenster, Reifen und Taschenlampen), sodass vier InkLayer-Objekte verwendet werden. Ein Benutzer kann eine beliebige Kombination von Ebenen gleichzeitig anzeigen.

## <a name="initializing-the-form-and-ink-layers"></a>Initialisieren der Formular- und Ink-Ebenen

Der `Load` Ereignishandler initialisiert das [Ink-Objekt](/previous-versions/ms583670(v=vs.100)) und die vier `InkLayer` -Objekte.


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



Wählen Sie dann den ersten Eintrag (Text) im Listenfeld aus.


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



Legen Sie abschließend die Freidruckfarbe für das [InkPicture-Steuerelement](/previous-versions/ms583740(v=vs.100)) auf den aktuell ausgewählten Listenfeldeintrag fest.


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a>Neuzeichnung des InkPicture-Steuerelements

Im geerbten Paint des InkPicture-Steuerelements werden die [InkPicture-Ebenen](/previous-versions/ms583740(v=vs.100)) überprüft, um zu bestimmen, welche ausgeblendet sind. [](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) Wenn eine Ebene nicht ausgeblendet ist, zeigt die Ereignisprozedur sie mithilfe der Draw-Methode der [Renderer-Eigenschaft](/previous-versions/ms582196(v=vs.100)) an. [](/previous-versions/ms828488(v=msdn.10)) Wenn Sie im Objektbrowser nachschauen, sehen Sie, dass die Microsoft.Ink.InkPicture.Renderer-Eigenschaft als [Microsoft.Ink.Renderer-Objekt definiert](/previous-versions/ms828481(v=msdn.10)) ist:


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



## <a name="selecting-an-ink-layer-through-the-list-box"></a>Auswählen einer Ink-Schicht über das Listenfeld

Wenn der Benutzer ein Element im Listenfeld auswählt, überprüft der [SelectedIndexChanged-Ereignishandler](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) zunächst, ob die Auswahl geändert wurde und dass das InkPicture-Steuerelement derzeit keine [InkPicture-Funktion](/previous-versions/ms583740(v=vs.100)) sammelt. Anschließend wird die InkPicture-Farbe des InkPicture-Steuerelements auf die entsprechende Farbe für die ausgewählte Ink-Schicht legt. Außerdem wird das Kontrollkästchen Ebene ausblenden aktualisiert, um den ausgeblendeten Status der ausgewählten Ink-Ebene widerzubilden. Schließlich wird die geerbte [Refresh-Methode](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) des InkPicture-Steuerelements verwendet, um nur die gewünschten Ebenen innerhalb des Steuerelements anzuzeigen.


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



## <a name="changing-the-visibility-of-an-ink-layer"></a>Ändern der Sichtbarkeit einer Ink-Schicht

Der Ereignishandler überprüft zunächst, ob sich die Auswahl geändert hat und ob das `CheckedChanged` InkPicture-Steuerelement derzeit keine [InkPicture-Daten](/previous-versions/ms583740(v=vs.100)) sammelt. Anschließend wird der ausgeblendete Status der ausgewählten InkPicture-Ebene aktualisiert, und das InkEnabled-Steuerelement des InkPicture-Steuerelements wird auf **FALSE**, festgelegt.

Als Nächstes wird die InkEnabled-Eigenschaft des InkPicture-Steuerelements auf **FALSE** festgelegt, bevor die Ink-Eigenschaft aktualisiert wird.

Schließlich wird das [InkPicture-Steuerelement](/previous-versions/ms583740(v=vs.100)) entweder für das bestimmte Fahrzeugteil aktiviert oder deaktiviert, je nach Aktivierter Kontrollkästchen Ebene ausblenden, und die [Refresh-Methode](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) des InkPicture-Steuerelements wird verwendet, um nur die gewünschten Ebenen innerhalb des Steuerelements anzuzeigen.


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



## <a name="closing-the-form"></a>Schließen des Formulars

Im Windows des Formular-Designers werden die Steuerelemente [InkEdit](/previous-versions/ms835842(v=msdn.10)) und [InkPicture](/previous-versions/ms583740(v=vs.100)) der Komponentenliste des Formulars hinzugefügt, wenn das Formular initialisiert wird. Wenn das Formular geschlossen wird, werden die Steuerelemente InkEdit und InkPicture sowie die anderen Komponenten des Formulars durch die [Dispose-Methode](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) des Formulars verworfen. Die Dispose-Methode des Formulars [](/previous-versions/ms583670(v=vs.100)) gibt auch die Fürk-Objekte zurück, die für das Formular erstellt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100))
</dt> <dt>

[InkPicture-Steuerelement](inkpicture-control.md)
</dt> <dt>

[InkEdit-Steuerelement](inkedit-control.md)
</dt> </dl>

 

 
