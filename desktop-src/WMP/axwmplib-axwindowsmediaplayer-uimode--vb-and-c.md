---
title: AxWindowsMediaPlayer.uiMode (Eigenschaft)
description: Die uiMode-Eigenschaft ruft einen Wert ab, der angibt, welche Steuerelemente in der Benutzeroberfläche angezeigt werden, oder legt einen Wert fest.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- uiMode-Windows Media Player
- uiMode-Eigenschaft Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , uiMode-Eigenschaft
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
ms.openlocfilehash: 51f1d716d36aafbd3625ae1144e0adde1abf0898bee4cbe6831d627cea97bb9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618770"
---
# <a name="axwindowsmediaplayeruimode-property"></a>AxWindowsMediaPlayer.uiMode (Eigenschaft)

Die uiMode-Eigenschaft ruft einen Wert ab, der angibt, welche Steuerelemente in der Benutzeroberfläche angezeigt werden, oder legt einen Wert fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Eine System.String, die einer der folgenden Werte ist.



| Wert     | BESCHREIBUNG                                                                                                                                                                                                     | Audiobeispiel                                                   | Videobeispiel                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| Unsichtbar | Windows Media Player ist ohne sichtbare Benutzeroberfläche (Steuerelemente, Video- oder Visualisierungsfenster) eingebettet.                                                                                                  | (Es wird nichts angezeigt.)                                         | (Es wird nichts angezeigt.)                                         |
| Keine      | Windows Media Player wird ohne Steuerelemente eingebettet, und nur das Video- oder Visualisierungsfenster wird angezeigt.                                                                                                   | ![uimode = 'none' mit Audio](images/uimode-none-audio-v11.png) | ![uimode = 'none' mit Video](images/uimode-none-video-v11.png) |
| Mini      | Windows Media Player wird zusätzlich zum Video- oder Visualisierungsfenster in das Statusfenster, wiedergabe/anhalten, beenden, stummschalten und Volumesteuerelemente eingebettet.                                                    | ![uimode = 'mini' mit Audio](images/uimode-mini-audio-v11.png) | ![uimode = 'mini' mit Video](images/uimode-mini-video-v11.png) |
| Voll      | Standard. Windows Media Player wird zusätzlich zum Video- oder Visualisierungsfenster mit den Steuerelementen Statusfenster, Suchleiste, Wiedergabe/Pause, Beenden, Stummschalten, Weiter, Zurück, Schnelles Vorwärts, Zurücksenden und Lautstärke eingebettet. | ![uimode = 'full' mit Audio](images/uimode-full-audio-v11.png) | ![uimode = 'full' with video](images/uimode-full-video-v11.png) |
| custom    | Windows Media Player ist in eine benutzerdefinierte Benutzeroberfläche eingebettet. Kann nur in C++-Programmen verwendet werden.                                                                                                                | (Benutzerdefinierte Benutzeroberfläche wird angezeigt.)                           | (Benutzerdefinierte Benutzeroberfläche wird angezeigt.)                           |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt die Darstellung des eingebetteten Windows Media Player. Wenn **uiMode** auf "none", "mini" oder "full" festgelegt ist, ist ein Fenster für die Anzeige von Videoclips und Audiovisualisierungen vorhanden. Dieses Fenster kann im Mini- oder  Vollmodus ausgeblendet werden, indem das Height-Attribut des **OBJECT-Tags** auf 40 (von unten gemessen) und der Steuerelementteil der Benutzeroberfläche sichtbar bleibt. Wenn keine eingebettete Schnittstelle gewünscht  ist, legen Sie sowohl das Breiten- als auch das **Höhenattribut** auf 0 (null) fest.

Wenn **uiMode** auf "invisible" festgelegt ist, wird keine Benutzeroberfläche angezeigt, aber der Platz auf der Seite ist weiterhin reserviert, wie durch Breite **und** **Höhe angegeben.** Dies ist nützlich, um das Seitenlayout bei einer **Änderung von uiMode** zu erhalten. Darüber hinaus ist der reservierte Speicherplatz transparent, sodass alle Hinterebenenelemente des Steuerelements sichtbar sind.

Wenn **uiMode** auf "full" oder "mini" festgelegt ist, zeigt Windows Media Player Transportsteuerelemente im Vollbildmodus an. Wenn **uiMode** auf "none" festgelegt ist, werden keine Steuerelemente im Vollbildmodus angezeigt.

Wenn das Fenster sichtbar ist und Audioinhalte abgespielt werden, wird die Visualisierung angezeigt, die zuletzt in der Windows Media Player.

Wenn **uiMode** in einem C++-Programm, das **IWMPRemoteMediaServices** implementiert, auf "custom" festgelegt ist, wird die durch **IWMPRemoteMediaServices.GetCustomUIMode** angegebene Skindatei angezeigt.

Während der Vollbildwiedergabe blendet Windows Media Player Mauscursor aus, wenn **enableContextMenu** gleich false und **uiMode** gleich "none" ist.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Listenfeld erstellt, mit dem der Benutzer den Benutzeroberflächenmodus für ein eingebettetes Windows Media Player kann. Das AxWMPLib.AxWindowsMediaPlayer-Objekt wird durch die Variable player dargestellt.


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add("invisible");
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
| Version<br/>   | Windows Media Player Version 7.0 oder höher. Windows Media Player 9-Serie oder höher für "unsichtbar" oder "benutzerdefiniert"<br/>   |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.enableContextMenu (VB und C#)**](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





