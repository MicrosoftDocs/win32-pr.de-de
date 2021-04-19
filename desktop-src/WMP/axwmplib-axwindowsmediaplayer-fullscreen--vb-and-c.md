---
title: AxWindowsMediaPlayer. FullScreen-Eigenschaft
description: Mit der FullScreen-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, ob Videoinhalte im Vollbildmodus abgespielt werden.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- Vollbild-Eigenschaften Fenster Media Player
- Vollbild-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, FullScreen-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23bfb1a2c67ecfa3ba7cced6f0ccb564bb387b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355878"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a>AxWindowsMediaPlayer. FullScreen-Eigenschaft

Mit der FullScreen-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, ob Videoinhalte im Vollbildmodus abgespielt werden.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a>Eigenschaftswert

Ein System. Boolean-Wert, der angibt, ob der Inhalt im Vollbildmodus wiedergegeben wird. Der Standardwert ist „FALSE“.

## <a name="remarks"></a>Bemerkungen

Damit der Vollbildmodus beim Einbetten des Windows Media Player-Steuer Elements ordnungsgemäß funktioniert, muss der Videoanzeige Bereich eine Höhe und Breite von mindestens einem Pixel aufweisen. Wenn **uiMode** auf "Mini" oder "Full" festgelegt ist, muss die Höhe des Steuer Elements auf 65 oder höher festgelegt sein, um zusätzlich zur Benutzeroberfläche den Videoanzeige Bereich aufzunehmen.

Wenn **uiMode** auf "unsichtbar" festgelegt ist, löst das Festlegen dieser Eigenschaft auf true einen Fehler aus und wirkt sich nicht auf das Verhalten des Steuer Elements aus.

Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn [enablecontextmenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) den Wert false hat und **uiMode** den Wert "None" hat.

Wenn **uiMode** auf "Full" oder "Mini" festgelegt ist, zeigt Windows Media Player Transport Steuerelemente im Vollbildmodus an, wenn der Mauszeiger bewegt wird. Nach einem kurzen Intervall ohne Mausbewegung werden die Transport Steuerelemente ausgeblendet. Wenn **uiMode** auf "None" festgelegt ist, werden keine Steuerelemente im Vollbildmodus angezeigt.

> [!Note]  
> Zum Anzeigen von Transport Steuerelementen im Vollbildmodus ist das Betriebssystem Windows XP erforderlich.

 

Wenn Transport Steuerelemente nicht im Vollbildmodus angezeigt werden, beendet Windows Media Player den Vollbildmodus automatisch, wenn die Wiedergabe angehalten wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Schaltfläche erstellt, die die FullScreen-Eigenschaft verwendet, um ein eingebettetes Player-Objekt in den Vollbildmodus zu wechseln. Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                  |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                            |
| Assembly<br/>  | <dl> <dt>AxInterop. WMPLib (AxInterop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. uiMode (VB und c#)**](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





