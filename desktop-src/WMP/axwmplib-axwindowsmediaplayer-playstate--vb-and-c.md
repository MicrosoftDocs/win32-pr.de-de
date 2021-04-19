---
title: AxWindowsMediaPlayer. playstate (Eigenschaft)
description: Die playstate-Eigenschaft ruft einen Enumerationswert ab, der den Zustand des Windows-Media Player Vorgangs angibt.
ms.assetid: ab9f1547-5c28-4289-beaf-9262f7f59b07
keywords:
- playstate-Eigenschaften Fenster Media Player
- playstate-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, playstate (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d397c65c1cfd7f4adb040cc94e208a66c6c42d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370310"
---
# <a name="axwindowsmediaplayerplaystate-property"></a>AxWindowsMediaPlayer. playstate (Eigenschaft)

Die playstate-Eigenschaft ruft einen Enumerationswert ab, der den Zustand des Windows-Media Player Vorgangs angibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public WMPPlayState playState {get;}
```


```VB

Public ReadOnly Property playState As WMPPlayState
```





## <a name="property-value"></a>Eigenschaftswert

Der WMPLib. WMPPlayState-Enumerationswert.

## <a name="remarks"></a>Bemerkungen

Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten. Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf. Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die playstate-Eigenschaft verwendet, um den aktuellen Wiedergabe Status des Players in einer Bezeichnung anzuzeigen. Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Test whether Windows Media Player is in the playing state. 
if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
{
    playStateLabel.Text = "Windows Media Player is playing!";
}
else
{
    playStateLabel.Text = "Windows Media Player is NOT playing!";
}
```


```VB

' Test whether Windows Media Player is in the playing state. 
If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

    playStateLabel.Text = &quot;Windows Media Player is playing!&quot;

Else

    playStateLabel.Text = &quot;Windows Media Player is NOT playing!&quot;

End If
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. PlayStateChange-Ereignis (VB und c#)**](axwmplib-axwindowsmediaplayer-playstatechange.md)
</dt> <dt>

[**WMPPlayState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





