---
title: AxWindowsMediaPlayer.fullScreen-Eigenschaft
description: Die fullScreen-Eigenschaft ruft einen Wert ab, der angibt, ob Videoinhalte im Vollbildmodus wiedergegeben werden, oder legt einen Wert fest.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- fullScreen-Eigenschaft Windows Media Player
- fullScreen-Eigenschaft Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , fullScreen-Eigenschaft
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
ms.openlocfilehash: e128d8c7e0cf49d3feaae723a7fb5a51740cda47e5016df6290b4852c20ec27b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902620"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a>AxWindowsMediaPlayer.fullScreen-Eigenschaft

Die fullScreen-Eigenschaft ruft einen Wert ab, der angibt, ob Videoinhalte im Vollbildmodus wiedergegeben werden, oder legt einen Wert fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a>Eigenschaftswert

Ein System.Boolean-Wert, der angibt, ob Inhalt im Vollbildmodus wiedergegeben wird. Der Standardwert ist „FALSE“.

## <a name="remarks"></a>Hinweise

Damit der Vollbildmodus beim Einbetten des Windows Media Player-Steuerelements ordnungsgemäß funktioniert, muss der Videoanzeigebereich eine Höhe und Breite von mindestens einem Pixel aufweisen. Wenn **uiMode** auf "mini" oder "full" festgelegt ist, muss die Höhe des Steuerelements selbst mindestens 65 sein, um den Videoanzeigebereich zusätzlich zur Benutzeroberfläche aufnehmen zu können.

Wenn **uiMode** auf "invisible" festgelegt ist, löst das Festlegen dieser Eigenschaft auf TRUE einen Fehler aus und wirkt sich nicht auf das Verhalten des Steuerelements aus.

Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) false und **uiMode** gleich "none" ist.

Wenn **uiMode** auf "full" oder "mini" festgelegt ist, zeigt Windows Media Player Transportsteuerelemente im Vollbildmodus an, wenn der Mauszeiger bewegt wird. Nach einem kurzen Intervall ohne Mausbewegung werden die Transportsteuerelemente ausgeblendet. Wenn **uiMode** auf "none" festgelegt ist, werden keine Steuerelemente im Vollbildmodus angezeigt.

> [!Note]  
> Das Anzeigen von Transportsteuerelementen im Vollbildmodus erfordert das Windows XP-Betriebssystem.

 

Wenn Transportsteuerelemente nicht im Vollbildmodus angezeigt werden, beendet Windows Media Player automatisch den Vollbildmodus, wenn die Wiedergabe beendet wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Schaltfläche erstellt, die die fullScreen-Eigenschaft verwendet, um ein eingebettetes Playerobjekt in den Vollbildmodus zu wechseln. Das AxWMPLib.AxWindowsMediaPlayer-Objekt wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                  |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                            |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib (AxInterop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.uiMode (VB und C#)**](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





