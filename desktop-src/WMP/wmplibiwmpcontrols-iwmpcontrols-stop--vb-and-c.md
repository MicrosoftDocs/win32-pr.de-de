---
title: Methode zum Abbrechen von iwmpcontrols
description: Die Methode "beenden" beendet die Wiedergabe des Medien Elements. | Methode zum Abbrechen von iwmpcontrols
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- Windows-Media Player "Methode"
- Methode "Methode Media Player", "iwmpcontrols"-Schnittstelle
- Iwmpcontrols-Schnittstelle, Windows Media Player, Methode "Ende"
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73271098340ea0cf0a645472b5ef6333ae0f4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371310"
---
# <a name="iwmpcontrolsstop-method"></a>Iwmpcontrols:: End-Methode

Die Methode " **Beenden** " beendet die Wiedergabe des Medien Elements.

## <a name="syntax"></a>Syntax


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode bewirkt, dass Windows Media Player alle verwendeten Systemressourcen, z. b. das Audiogerät, freigibt. Das aktuelle Medien Element wird jedoch nicht freigegeben.

Wenn Windows Media Player beendet wird, wird die aktuelle Wiedergabe Position im Medien Element auf den Anfang des Elements zurückgesetzt. Wenn Sie anschließend **iwmpcontrols. Play** aufrufen, wird die Wiedergabe am Anfang des Medien Elements gestartet. Verwenden Sie die **iwmpcontrols. Pause** -Methode, um einen Wiedergabe Vorgang anzuhalten, ohne die aktuelle Position zu ändern.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Option zum Abbrechen des aktuellen Medien Elements als Reaktion auf das Click-Ereignis einer Schalt **Fläche verwendet.** Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

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

[**Iwmpcontrols. Next (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Pause (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Play (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Previous (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





