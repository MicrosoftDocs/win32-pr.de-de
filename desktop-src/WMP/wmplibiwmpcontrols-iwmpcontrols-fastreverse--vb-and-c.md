---
title: Iwmpcontrols fastreverse-Methode
description: Die fastreverse-Methode startet die schnelle Wiedergabe des Medien Elements in umgekehrter Richtung.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- fastreverse-Methode, Windows-Media Player
- fastreverse-Methode, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, fastreverse-Methode
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
ms.openlocfilehash: 7061481aea13b0ed83c3a3d0eb47ca24b940358b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361472"
---
# <a name="iwmpcontrolsfastreverse-method"></a>Iwmpcontrols:: fastreverse-Methode

Die **fastreverse** -Methode startet die schnelle Wiedergabe des Medien Elements in umgekehrter Richtung.

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

## <a name="remarks"></a>Bemerkungen

Die **fastreverse** -Methode scannt den Clip in umgekehrter Reihenfolge mit dem fünfmal normalen Tempo und zeigt nur die Keyframes an, wenn es sich um eine Videodatei handelt. Das Aufrufen von **fastreverse** entspricht der Angabe von-5,0 für die Rate durch Festlegen der **iwmpsettings. Rate** -Eigenschaft. Wenn die Rate anschließend geändert wird, oder wenn **iwmpcontrols. Play** oder **iwmpcontrols. Stop** aufgerufen wird, wird Windows Media Player schnell umkehren.

Wenn das Element Teil einer Wiedergabeliste ist, wird **fastreverse** am Anfang der aktuellen Spur angehalten. Wenn sich beispielsweise Track 3 in **fastreverse** befindet und der Anfang von Track 3 erreicht wird, wechselt Windows Media Player nicht mehr zu Track 2. Die Wiedergabe Anzahl wird beim Aufrufen von **fastreverse** nicht inkrementiert.

Wenn Sie beim Ausführen von **fastreverse** **iwmpcontrols. FastForward** aufzurufen, wird **fastreverse** angehalten, und **iwmpcontrols. FastForward** wird gestartet.

Diese Methode funktioniert nicht für Live Übertragungen und bestimmte digitale Medientypen. Um zu ermitteln, ob Sie in einem Clip fast Reverse verwenden können, übergeben Sie den **System. String** -Wert "fastreverse" an die **iwmpcontrols. IsAvailable** -Eigenschaft (die **iwmpcontrols. get \_ IsAvailable** -Methode in c#).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **fastreverse** verwendet, um das aktuelle Medien Element als Reaktion auf das Click-Ereignis einer Schaltfläche umzukehren. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcontrols-Schnittstelle (VB und c#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. FastForward (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. IsAvailable (VB und c#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Play (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Stopps (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. Rate (VB und c#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





