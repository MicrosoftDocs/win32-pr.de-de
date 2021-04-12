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
# <a name="auto-claims-form-sample"></a>Beispiel für automatisches Anspruchsformular

Das Beispiel für automatische Ansprüche adressiert ein hypothetisches Szenario für einen Versicherungs Prüfer. Die Arbeit des assors erfordert, dass er mit den Clients zu Hause oder Unternehmen besucht und seine Anspruchs Informationen in ein Formular eingegeben hat. Zur Steigerung der Produktivität des assors entwickelt seine IT-Abteilung eine Tablet-Anwendung, die es Ihnen oder Ihnen ermöglicht, Anspruchs Informationen schnell und genau über zwei Ink-Steuerelemente einzugeben: [InkEdit](/previous-versions/ms835842(v=msdn.10)) -und [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelemente.

In diesem Beispiel wird ein [InkEdit](/previous-versions/ms835842(v=msdn.10)) -Steuerelement für jedes Texteingabefeld verwendet. Ein Benutzer gibt die relevanten Informationen über eine Versicherungsrichtlinie und ein Fahrzeug in diese Felder mit einem Stift ein. Das [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelement wird zum Hinzufügen von frei Hand Eingaben über ein Auto Mobil Bild verwendet, um beschädigte Bereiche des Autos hervorzuheben. Das Beispiel für automatische Ansprüche ist für C \# und Microsoft Visual Basic .net verfügbar. In diesem Thema wird das Visual Basic .net beschrieben.

Die autoclaims-Klasse ist als eine Unterklasse von [System. Windows. Forms. Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) definiert, und eine-Klasse, die für die Erstellung und Verwaltung von Freihand Ebenen für unterschiedliche Arten von Beschädigungen definiert ist. Vier Ereignishandler werden definiert, um die folgenden Aufgaben auszuführen:

-   Die Formular-und Freihand Ebenen werden initialisiert.
-   Das [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelement wird neu gezeichnet.
-   Auswählen einer Freihand Schicht durch das Listenfeld.
-   Ändern der Sichtbarkeit einer Freihand Schicht.

> [!Note]  
> Versionen dieses Beispiels sind in C \# und Visual Basic .net verfügbar. Die in diesem Abschnitt erörterte Version ist Visual Basic .net. Die Konzepte sind Zwischenversionen identisch.

 

## <a name="defining-the-form-and-ink-layers"></a>Definieren von Formular-und Freihand Ebenen

Sie müssen den [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) -Namespace importieren:


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



Im nächsten Schritt wird in der autoclaims-Klasse eine `InkLayer` -Klasse definiert und ein Array aus vier- `InkLayer` Objekten deklariert. (Inklayer enthält ein [Microsoft. Ink.](/previous-versions/ms583670(v=vs.100)) Ink-Objekt zum Speichern von "Ink" und " [System. Drawing. Color](/dotnet/api/system.drawing.color?view=netcore-3.1) " und **boolesche** Werte zum Speichern der Farbe und des verborgenen Zustands der Ebene.) Ein fünftes Ink-Objekt wird deklariert, um frei Hand Eingaben für das [InkPicture](/previous-versions/ms583740(v=vs.100)) zu behandeln, wenn alle frei Hand Ebenen ausgeblendet sind.


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



Jede Ebene verfügt über ein eigenes [Ink](/previous-versions/ms583670(v=vs.100)) -Objekt. Das Anspruchsformular (Body, Windows, Tiers und Scheinwerfer) enthält vier diskrete Bereiche, sodass vier inklayer-Objekte verwendet werden. Ein Benutzer kann eine beliebige Kombination von Ebenen gleichzeitig anzeigen.

## <a name="initializing-the-form-and-ink-layers"></a>Initialisieren von Formular-und Freihand Ebenen

Der `Load` Ereignishandler initialisiert das [](/previous-versions/ms583670(v=vs.100)) frei Hand Objekt und die vier `InkLayer` Objekte.


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



Legen Sie abschließend die frei Hand Farbe für das [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelement auf den aktuell ausgewählten Listenfeld Eintrag fest.


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a>Umzeichnen des InkPicture-Steuer Elements

Im geerbten [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) -Ereignishandler des [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuer Elements werden die frei Hand Ebenen geprüft, um zu bestimmen, welche ausgeblendet sind. Wenn eine Ebene nicht ausgeblendet ist, wird Sie von der Ereignis Prozedur mithilfe der [Draw](/previous-versions/ms828488(v=msdn.10)) -Methode der [Renderer](/previous-versions/ms582196(v=vs.100)) -Eigenschaft angezeigt. Wenn Sie die Objektkatalog betrachten, sehen Sie, dass die Microsoft. Ink. InkPicture. Renderer-Eigenschaft als [Microsoft. Ink. Renderer](/previous-versions/ms828481(v=msdn.10)) -Objekt definiert ist:


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



## <a name="selecting-an-ink-layer-through-the-list-box"></a>Auswählen einer Freihand Schicht über das Listenfeld

Wenn der Benutzer ein Element im Listenfeld auswählt, prüft der [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) -Ereignishandler zunächst, ob die Auswahl geändert wurde und das [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelement momentan keine Freihand sammelt. Anschließend wird die frei Hand Farbe des InkPicture-Steuer Elements auf die entsprechende Farbe für die ausgewählte Freihand-Ebene festgelegt. Außerdem wird das Kontrollkästchen Ebene ausblenden so aktualisiert, dass der verborgene Status der ausgewählten Freihand Schicht angezeigt wird. Schließlich wird die geerbte [Aktualisierungs](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) Methode des InkPicture-Steuer Elements verwendet, um nur die gewünschten Ebenen innerhalb des Steuer Elements anzuzeigen.


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



## <a name="changing-the-visibility-of-an-ink-layer"></a>Ändern der Sichtbarkeit einer Freihand Schicht

Der `CheckedChanged` Ereignishandler prüft zunächst, ob die Auswahl geändert wurde und dass das [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelement zurzeit keine Freihand sammelt. Anschließend wird der verborgene Status der ausgewählten Freihand Schicht aktualisiert, und die InkEnabled des InkPicture-Steuer Elements wird auf **false** festgelegt.

Als nächstes wird die InkEnabled-Eigenschaft des InkPicture-Steuer Elements vor dem Aktualisieren der Ink-Eigenschaft auf **false** festgelegt.

Zum Schluss ist das [InkPicture](/previous-versions/ms583740(v=vs.100)) -Steuerelement für den jeweiligen Fahrzeugteil entweder aktiviert oder deaktiviert, je nachdem, ob das Kontrollkästchen Ebene ausblenden aktiviert ist, und die [Aktualisierungs](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) Methode des InkPicture-Steuer Elements wird verwendet, um nur die gewünschten Ebenen innerhalb des Steuer Elements anzuzeigen.


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

Im vom Windows Form-Designer generierten Code werden die Steuerelemente [InkEdit](/previous-versions/ms835842(v=msdn.10)) und [InkPicture](/previous-versions/ms583740(v=vs.100)) der Komponentenliste des Formulars hinzugefügt, wenn das Formular initialisiert wird. Wenn das Formular geschlossen wird, werden die InkEdit-und InkPicture-Steuerelemente sowie die anderen Komponenten des Formulars von der [verwerfen-Methode](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) des Formulars entfernt. Die verwerfen-Methode des Formulars gibt auch die frei [Hand Objekte frei, die für](/previous-versions/ms583670(v=vs.100)) das Formular erstellt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100))
</dt> <dt>

[InkPicture-Steuerelement](inkpicture-control.md)
</dt> <dt>

[InkEdit-Steuerelement](inkedit-control.md)
</dt> </dl>

 

 
