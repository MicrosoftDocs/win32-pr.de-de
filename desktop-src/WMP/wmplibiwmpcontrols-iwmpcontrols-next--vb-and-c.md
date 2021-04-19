---
title: Iwmpcontrols Next-Methode
description: Die Next-Methode legt das nächste Element in der Wiedergabeliste als Aktuelles Element fest.
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- nächste Methode, Windows Media Player
- nächste Methode, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, nächste Methode
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8444ba7d9209759cb64c4b582e1af9d074332ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373971"
---
# <a name="iwmpcontrolsnext-method"></a>Iwmpcontrols:: Next-Methode

Die **Next** -Methode legt das nächste Element in der Wiedergabeliste als Aktuelles Element fest.

## <a name="syntax"></a>Syntax


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn sich die Wiedergabeliste auf dem letzten Eintrag befindet, wenn **Next** aufgerufen wird, wird der erste Eintrag in der Wiedergabeliste zum aktuellen Eintrag.

Bei serverseitigen Wiedergabelisten springt diese Methode zum nächsten Element in der serverseitigen Wiedergabeliste, nicht zur Client Wiedergabeliste.

Beim Abspielen einer DVD überspringt diese Methode das nächste logische Kapitel in der Wiedergabe Sequenz, das möglicherweise nicht das nächste Kapitel in der Wiedergabeliste ist. Bei der Wiedergabe von DVD-Bildern wird diese Methode zum nächsten Bild überspringt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird als Reaktion auf das Click-Ereignis einer Schaltfläche **als nächstes** verwendet, um zum nächsten Element in der aktuellen Wiedergabeliste zu wechseln. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

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

[**Iwmpcontrols. Previous (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Stopps (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





