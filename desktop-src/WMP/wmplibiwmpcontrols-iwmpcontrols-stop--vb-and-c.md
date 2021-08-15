---
title: IWMPControls stop-Methode
description: Die stop-Methode beendet die Wiedergabe des Medienelements. | IWMPControls stop-Methode
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- stop-Methode Windows Media Player
- stop-Methode Windows Media Player , IWMPControls-Schnittstelle
- IWMPControls-Schnittstelle Windows Media Player , stop-Methode
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
ms.openlocfilehash: 6f941ac90fa86cdd16dedf5349c0a6d614c57f49bc91009f5d62c56bb83144bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332075"
---
# <a name="iwmpcontrolsstop-method"></a>IWMPControls::stop-Methode

Die **stop-Methode** beendet die Wiedergabe des Medienelements.

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

## <a name="remarks"></a>Hinweise

Diese Methode bewirkt, dass Windows Media Player alle verwendeten Systemressourcen freigibt, z. B. das Audiogerät. Das aktuelle Medienelement wird jedoch nicht freigegeben.

Wenn Windows Media Player beendet wird, wird die aktuelle Wiedergabeposition im Medienelement auf den Anfang des Elements zurückgesetzt. Anschließend startet der Aufruf von **IWMPControls.play** die Wiedergabe vom Anfang des Medienelements aus. Um einen Wiedergabevorgang anzuhalten, ohne die aktuelle Position zu ändern, verwenden Sie die **IWMPControls.pause-Methode.**

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **stop** verwendet, um das aktuelle Medienelement als Reaktion auf das Click-Ereignis einer Schaltfläche zu beenden. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPControls-Schnittstelle (VB und C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.next (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[**IWMPControls.pause (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls.previous (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





