---
title: Iwmpcontrols FastForward-Methode
description: Die FastForward-Methode startet die schnelle Wiedergabe des Medien Elements in Vorwärtsrichtung. | Iwmpcontrols FastForward-Methode
ms.assetid: 44609d63-1d1a-489c-ac17-60b6d3ddc588
keywords:
- FastForward-Methoden Fenster Media Player
- FastForward-Methode, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols-Schnittstelle, Windows Media Player, FastForward-Methode
topic_type:
- apiref
api_name:
- IWMPControls.fastForward
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d99307a7b188b238157af62833273b8c724eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370807"
---
# <a name="iwmpcontrolsfastforward-method"></a>Iwmpcontrols:: FastForward-Methode

Die **FastForward** -Methode startet die schnelle Wiedergabe des Medien Elements in Vorwärtsrichtung.

## <a name="syntax"></a>Syntax


```CSharp
public void fastForward();
```


```VB

Public Sub fastForward()
Implements IWMPControls.fastForward
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **FastForward** -Methode gibt den Clip um das Fünffache der normalen Geschwindigkeit wieder. Das Aufrufen von **FastForward** entspricht der Angabe von 5,0 für die Rate durch Festlegen der **iwmpsettings. Rate** -Eigenschaft. Wenn die Rate anschließend geändert wird, oder wenn **iwmpcontrols. Play** oder **iwmpcontrols. Stop** aufgerufen wird, beendet Windows Media Player die schnelle Weiterleitung.

Die **FastForward** -Methode funktioniert nicht für Live-Übertragungen und bestimmte Medientypen. Um zu ermitteln, ob Sie sich in einem Clip schnell vorwärts bewegen können, übergeben Sie den **System. String** -Wert "FastForward" an die **iwmpcontrols. IsAvailable** -Eigenschaft (die **iwmpcontrols. get \_ IsAvailable** -Methode in c#).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **FastForward** verwendet, um das aktuelle Medien Element in Reaktion auf das Click-Ereignis einer Schaltfläche schnell weiterzuleiten. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void fastForwardButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastForward"))
    {
        controls.fastForward();
    }
}
```


```VB

Public Sub fastForwardButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastForwardButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface. 
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastForward&quot;)) Then

        controls.fastForward()

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

[**Iwmpcontrols. IsAvailable (VB und c#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Play (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Stopps (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. Rate (VB und c#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





