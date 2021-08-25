---
title: IWMPControls pause-Methode
description: Die Pause-Methode hält die Wiedergabe des Medienelements an. | IWMPControls pause-Methode
ms.assetid: 1d9ebaf3-84b4-458d-a393-2b685cd0dbfb
keywords:
- pause-Methode Windows Media Player
- pause-Methode Windows Media Player , IWMPControls-Schnittstelle
- IWMPControls-Schnittstelle Windows Media Player , pause-Methode
topic_type:
- apiref
api_name:
- IWMPControls.pause
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49950b5d2c5588e27755f3845e65f0a79ce0aae6ccc4a05dd4e5af3186b879de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861880"
---
# <a name="iwmpcontrolspause-method"></a>IWMPControls::p ause-Methode

Die **Pause-Methode** hält die Wiedergabe des Medienelements an.

## <a name="syntax"></a>Syntax


```CSharp
public void pause();
```


```VB

Public Sub pause()
Implements IWMPControls.pause
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn eine Datei angehalten wird, gibt Windows Media Player keine Systemressourcen auf, z. B. das Audiogerät.

Um zu bestimmen, ob ein bestimmter Medientyp angehalten werden kann, übergeben Sie den **System.String-Wert** "pause" an die **IWMPControls.isAvailable-Eigenschaft** (die **IWMPControls.get \_ isAvailable-Methode** in C#).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **pause** verwendet, um die Wiedergabe des aktuellen Medienelements als Reaktion auf das Click-Ereignis einer Schaltfläche anzuhalten. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
private void pauseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("pause"))
    {
        controls.pause();
    }
}
```


```VB

Public Sub pauseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles pauseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;pause&quot;)) Then

        controls.pause()

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

[**IWMPControls.isAvailable (VB und C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> </dl>

 

 





