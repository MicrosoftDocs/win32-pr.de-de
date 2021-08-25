---
title: IWMPControls-Wiedergabemethode
description: Die Wiedergabemethode beginnt mit der Wiedergabe des aktuellen Medienelements oder setzt die Wiedergabe eines angehaltenen Elements wieder auf.
ms.assetid: 02e00df6-4dc1-44bb-9826-e69e8298ccaa
keywords:
- Play-Windows Media Player
- play-Windows Media Player , IWMPControls-Schnittstelle
- IWMPControls-Schnittstelle Windows Media Player , Play-Methode
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
ms.openlocfilehash: 2823c5f9846ec2569da0ede6629a4b7e8c04c7b61e14060451c8d0cf3a02f71d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761020"
---
# <a name="iwmpcontrolsplay-method"></a>IWMPControls::p lay-Methode

Die **Wiedergabemethode** beginnt mit der Wiedergabe des aktuellen Medienelements oder setzt die Wiedergabe eines angehaltenen Elements wieder auf.

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

## <a name="remarks"></a>Hinweise

Wenn diese Methode während der schnellen Weiterleitung oder Zurückladung aufgerufen wird, wird die Wiedergaberate (der Wert **von IWMPSettings.rate**) auf 1,0 festgelegt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **play verwendet,** um das aktuelle Medienelement als Reaktion auf das Click-Ereignis einer Schaltfläche wieder zu spielen. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPControls-Schnittstelle (VB und C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.playItem (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.rate (VB und C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





