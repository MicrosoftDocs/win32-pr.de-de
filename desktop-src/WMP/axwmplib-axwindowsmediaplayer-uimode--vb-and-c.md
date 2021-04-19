---
title: AxWindowsMediaPlayer. uiMode (Eigenschaft)
description: Mit der uiMode-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, welche Steuerelemente in der Benutzeroberfläche angezeigt werden.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- uiMode-Eigenschaften Fenster Media Player
- uiMode-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, uiMode-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.uiMode
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33edcf6bdff9e1587269df9eb49c3729099d091e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361390"
---
# <a name="axwindowsmediaplayeruimode-property"></a>AxWindowsMediaPlayer. uiMode (Eigenschaft)

Mit der uiMode-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, welche Steuerelemente in der Benutzeroberfläche angezeigt werden.

## <a name="syntax"></a>Syntax


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Ein System. String-Wert, der einem der folgenden Werte entspricht.



| Wert     | BESCHREIBUNG                                                                                                                                                                                                     | Audiobeispiel                                                   | Video Beispiel                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| Unsichtbar | Windows Media Player ist ohne sichtbare Benutzeroberfläche eingebettet (Steuerelemente, Video-oder Visualisierungs Fenster).                                                                                                  | (Nichts wird angezeigt.)                                         | (Nichts wird angezeigt.)                                         |
| none      | Windows Media Player ist ohne Steuerelemente eingebettet, und nur das Video-oder Visualisierungs Fenster wird angezeigt.                                                                                                   | ![uiMode = ' none ' with Audiodatei](images/uimode-none-audio-v11.png) | ![uiMode = ' none ' mit Video](images/uimode-none-video-v11.png) |
| Minibar      | Windows Media Player ist in das Fenster "Status", "Wiedergabe", "anhalten", "anhalten", "stumm" und "Lautstärke" neben dem Video-oder Visualisierungs Fenster eingebettet                                                    | ![uiMode = ' Mini ' mit Audiodatei](images/uimode-mini-audio-v11.png) | ![uiMode = ' Mini ' mit Video](images/uimode-mini-video-v11.png) |
| Voll      | Standard. Windows Media Player ist neben dem Video-oder Visualisierungs Fenster in die Steuerelemente "Status", "suchen", "Wiedergabe", "anhalten", "stumm Schaltung", "weiter", "zurück", "Zurückspulen" und "Volume" eingebettet | ![uiMode = ' Full ' mit Audiodatei](images/uimode-full-audio-v11.png) | ![uiMode = ' Full ' mit Video](images/uimode-full-video-v11.png) |
| custom    | Windows Media Player ist mit einer benutzerdefinierten Benutzeroberfläche eingebettet. Kann nur in C++-Programmen verwendet werden.                                                                                                                | (Benutzerdefinierte Benutzeroberfläche wird angezeigt.)                           | (Benutzerdefinierte Benutzeroberfläche wird angezeigt.)                           |



 

## <a name="remarks&quot;></a>Bemerkungen

Diese Eigenschaft gibt die Darstellung der eingebetteten Windows-Media Player an. Wenn **uiMode** auf &quot;None&quot;, &quot;Mini&quot; oder &quot;Full&quot; festgelegt ist, ist ein Fenster für die Anzeige von Videoclips und Audiovisualisierungen vorhanden. Dieses Fenster kann im Mini-oder vollständigen Modus ausgeblendet werden, indem das **height** -Attribut des **Object** -Tags auf 40 festgelegt wird. dieses Fenster wird von unten gemessen und lässt den Steuerelement Teil der Benutzeroberfläche sichtbar. Wenn keine eingebettete Schnittstelle gewünscht ist, legen Sie die Attribute &quot; **Width** &quot; und &quot; **height** &quot; auf NULL fest.

Wenn **uiMode** auf &quot;unsichtbar&quot; festgelegt ist, wird keine Benutzeroberfläche angezeigt, aber der Leerraum ist nach wie vor durch **Breite** und **Höhe** angegeben. Dies ist nützlich, um das Seitenlayout beizubehalten, wenn **uiMode** geändert werden kann. Außerdem ist der reservierte Speicherplatz transparent, sodass alle Elemente hinter dem Steuerelement sichtbar sind.

Wenn **uiMode** auf &quot;Full&quot; oder &quot;Mini&quot; festgelegt ist, zeigt Windows Media Player Transport Steuerelemente im Vollbildmodus an. Wenn **uiMode** auf &quot;None&quot; festgelegt ist, werden keine Steuerelemente im Vollbildmodus angezeigt.

Wenn das Fenster sichtbar ist und Audioinhalt wiedergegeben wird, wird die Visualisierung angezeigt, die zuletzt in Windows Media Player verwendet wurde.

Wenn **uiMode** in einem C++-Programm, das **iwmpremotemediaservices** implementiert, auf &quot;Custom&quot; festgelegt ist, wird die von **iwmpremotemediaservices. getcustomuimode** angezeigte Skin-Datei angezeigt.

Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn **enablecontextmenu** den Wert false hat und **uiMode** den Wert &quot;None&quot; hat.

## <a name=&quot;examples&quot;></a>Beispiele

Im folgenden Beispiel wird ein Listenfeld erstellt, das es dem Benutzer ermöglicht, den Benutzeroberflächen Modus für ein eingebettetes Windows-Media Player Objekt zu ändern. Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen &quot;Player&quot; dargestellt.


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible");
uiModeOptions.Items.Add("none");
uiModeOptions.Items.Add("mini");
uiModeOptions.Items.Add("full");


private void uiModeOptions_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Get the selected UI mode in the list box as a string.
    string newMode = (string)(((System.Windows.Forms.ListBox)sender).SelectedItem);
     
    // Set the UI mode that the user selected.
    player.uiMode = newMode;            
}
```


```VB

' Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible&quot;)
uiModeOptions.Items.Add(&quot;none&quot;)
uiModeOptions.Items.Add(&quot;mini&quot;)
uiModeOptions.Items.Add(&quot;full&quot;)


Public Sub uiModeOptions_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles uiModeOptions.SelectedIndexChanged

    &#39; Get the selected UI mode in the list box as a string.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim newMode As String = lb.SelectedItem

    &#39; Set the UI mode that the user selected.
    player.uiMode = newMode

End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player Version 7,0 oder höher. Windows Media Player 9 oder höher für "unsichtbar" oder "Benutzer definiert"<br/>   |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. enablecontextmenu (VB und c#)**](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





