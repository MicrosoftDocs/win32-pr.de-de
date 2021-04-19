---
title: Wiedergabemethode von iwmpcontrols
description: Die Play-Methode beginnt mit der Wiedergabe des aktuellen Medien Elements oder nimmt die Wiedergabe eines angehaltenen Elements wieder auf.
ms.assetid: 02e00df6-4dc1-44bb-9826-e69e8298ccaa
keywords:
- Wiedergabemethode Windows Media Player
- Wiedergabemethode, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, Play-Methode
topic_type:
- apiref
api_name:
- IWMPControls.play
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd87a2e2ba3d53b119df328fa68668c91c78d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369246"
---
# <a name="iwmpcontrolsplay-method"></a>Iwmpcontrols::p Lay-Methode

Die **Play** -Methode beginnt mit der Wiedergabe des aktuellen Medien Elements oder nimmt die Wiedergabe eines angehaltenen Elements wieder auf.

## <a name="syntax"></a>Syntax


```CSharp
public void play();
```


```VB

Public Sub play()
Implements IWMPControls.play
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode während der schnellen Weiterleitung oder rebuggen aufgerufen wird, wird die Wiederholungsrate (der Wert von **iwmpsettings. Rate**) auf 1,0 festgelegt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **Play** verwendet, um das aktuelle Medien Element als Reaktion auf das Click-Ereignis einer Schaltfläche wiederzugeben. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void playButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("play"))
    {
        controls.play();
    }
}
```


```VB

Public Sub playButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;play&quot;)) Then

        controls.play()

    End If

End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcontrols-Schnittstelle (VB und c#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. PlayItem (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. Rate (VB und c#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





