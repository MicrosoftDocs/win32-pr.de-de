---
title: Methode zum Anhalten von iwmpcontrols
description: Die Pause-Methode hält die Wiedergabe des Medien Elements an. | Methode zum Anhalten von iwmpcontrols
ms.assetid: 1d9ebaf3-84b4-458d-a393-2b685cd0dbfb
keywords:
- Windows-Media Player für die Methoden Pause
- Pause-Methode, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, anhaltemethode
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
ms.openlocfilehash: 5cf89cfef66c84be76a529d9c0cef6ec3ae6ac40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365647"
---
# <a name="iwmpcontrolspause-method"></a>Iwmpcontrols::p ause-Methode

Die **Pause** -Methode hält die Wiedergabe des Medien Elements an.

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

## <a name="remarks"></a>Bemerkungen

Wenn eine Datei angehalten wird, gibt Windows Media Player keine Systemressourcen, z. b. das Audiogerät, aus.

Um zu ermitteln, ob ein bestimmter Medientyp angehalten werden kann, übergeben Sie den **System. String** -Wert "Pause" an die **iwmpcontrols. IsAvailable** -Eigenschaft (die **iwmpcontrols. get \_ IsAvailable** -Methode in c#).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **Pause** verwendet, um die Wiedergabe des aktuellen Medien Elements als Reaktion auf das Click-Ereignis einer Schaltfläche anzuhalten. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcontrols-Schnittstelle (VB und c#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. IsAvailable (VB und c#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> </dl>

 

 





