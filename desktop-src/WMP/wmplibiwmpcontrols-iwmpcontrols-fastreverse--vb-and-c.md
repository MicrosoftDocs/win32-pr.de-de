---
title: IWMPControls fastReverse-Methode
description: Die fastReverse-Methode startet die schnelle Wiedergabe des Medienelements in umgekehrter Richtung.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- fastReverse-Methode Windows Media Player
- fastReverse-Methode Windows Media Player , IWMPControls-Schnittstelle
- IWMPControls-Schnittstelle Windows Media Player , fastReverse-Methode
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bbc1442ca223765b498560d078879c9a7033011117b7f663d4d40ff26bdd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761080"
---
# <a name="iwmpcontrolsfastreverse-method"></a>IWMPControls::fastReverse-Methode

Die **fastReverse-Methode** startet die schnelle Wiedergabe des Medienelements in umgekehrter Richtung.

## <a name="syntax"></a>Syntax


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **fastReverse-Methode** scannt den Clip um das Fünffache der Normalgeschwindigkeit in umgekehrter Richtung und zeigt nur die Keyframes an, wenn es sich um eine Videodatei handelt. Das Aufrufen von **fastReverse** entspricht der Angabe von -5.0 für die Rate durch Festlegen der **IWMPSettings.rate-Eigenschaft.** Wenn die Rate anschließend geändert wird oder **"IWMPControls.play"** oder **"IWMPControls.stop"** aufgerufen wird, wird Windows Media Player die schnelle Umkehrung beendet.

Wenn das Element Teil einer Wiedergabeliste ist, wird **fastReverse** am Anfang der aktuellen Spur angehalten. Wenn z. B. Track 3 sich in **fastReverse** befindet, wenn der Anfang von Track 3 erreicht wird, wird Windows Media Player nicht zu Track 2 wechseln. Die Wiedergabeanzahl wird beim Aufrufen von **fastReverse** nicht erhöht.

Wenn Sie **IWMPControls.fastForward** aufrufen, während **fastReverse** ausgeführt wird, wird **fastReverse** beendet, und **IWMPControls.fastForward** beginnt.

Diese Methode funktioniert nicht für Liveübertragungen und bestimmte digitale Medientypen. Übergeben Sie den **System.String-Wert** "FastReverse" an die **IWMPControls.isAvailable-Eigenschaft** (die **IWMPControls.get \_ isAvailable-Methode** in C#), um zu bestimmen, ob Sie schnelles Umgekehrtes in einem Clip verwenden können.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **fastReverse** verwendet, um das aktuelle Medienelement als Reaktion auf das Click-Ereignis einer Schaltfläche umzukehren. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

    End If

End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPControls-Schnittstelle (VB und C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.fastForward (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls.isAvailable (VB und C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls.stop (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.rate (VB und C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





