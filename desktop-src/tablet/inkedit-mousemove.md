---
description: Tritt ein, wenn der Benutzer die Maus bewegt, während sich der Mauszeiger über dem InkEdit-Steuerelement befindet.
ms.assetid: 6ccaf2eb-acec-4dfd-9ec7-c78aca043900
title: InkEdit.MouseMove-Ereignis (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 601bcaa4c5bc3379c207302c28e5eb17d44b2b184ce42452d5b78b6079d88ead
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939110"
---
# <a name="inkeditmousemove-event"></a>InkEdit.MouseMove-Ereignis

Tritt ein, wenn der Benutzer die Maus bewegt, während sich der Mauszeiger über dem [InkEdit-Steuerelement](inkedit-control-reference.md) befindet.

## <a name="syntax"></a>Syntax


```C++
HRESULT MouseMove(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schaltfläche* 
</dt> <dd>

Ein Member der [**MouseButton-Enumeration,**](/windows/desktop/api/inked/ne-inked-mousebutton) der angibt, welche Maustasten gedrückt sind.



| Wert                                                                                                                                                            | Bedeutung                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <dt>**NEIN \_ SCHALTFLÄCHE**</dt> </dl>             | Standard. Es wurde keine Maustaste gedrückt. <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <dt>**LEFT \_ SCHALTFLÄCHE**</dt> </dl>       | Die linke Maustaste wurde gedrückt. <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <dt>**RIGHT \_ SCHALTFLÄCHE**</dt> </dl>    | Die rechte Maustaste wurde gedrückt. <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <dt>**MIDDLE \_ SCHALTFLÄCHE**</dt> </dl> | Die mittlere Maustaste wurde gedrückt. <br/>  |



 

</dd> <dt>

*SHIFTKey* 
</dt> <dd>

Ein Member der [**InkShiftKeyModifierFlags-Enumeration,**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) der angibt, welche Modifiziererschlüssel zum Zeitpunkt des Ereignisses geschwenken werden.



| Wert                                                                                                                                                                                     | Bedeutung                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**IKM \_ Shift**</dt> </dl>             | Gibt an, dass die UMSCHALTTASTE als Modifizierer verwendet wurde. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Steuerelement**</dt> </dl> | Gibt an, dass die STRG-Taste als Modifizierer verwendet wurde. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ ALT**</dt> </dl>                 | Gibt an, dass die ALT-TASTE als Modifizierer verwendet wurde. <br/>   |



 

</dd> <dt>

*xMouse* 
</dt> <dd>

Die aktuelle x-Koordinate des Mauszeigers in Pixel.

</dd> <dt>

*yMouse* 
</dt> <dd>

Die aktuelle y-Koordinate des Mauszeigers in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn eine Maustaste gedrückt wird, während sich der Mauszeiger über einem [InkEdit-Steuerelement](inkedit-control-reference.md) befindet, erfasst dieses Steuerelement die Maus und empfängt alle Mausereignisse bis einschließlich des letzten [**MouseUp-Ereignisses.**](inkedit-mouseup.md) Dies bedeutet, dass sich die (x, y)-Mauszeigerkoordinaten, die von einem Mausereignis zurückgegeben werden, möglicherweise nicht immer im internen Bereich des Objekts, das sie empfängt, bewegen.

Wenn die Maustasten nacheinander gedrückt werden, empfängt das Objekt, das die Maus nach dem ersten Drücken erfasst, alle Mausereignisse, bis alle Schaltflächen losgelassen werden.

Das **MouseMove-Ereignis** wird kontinuierlich generiert, wenn sich der Mauszeiger über Objekte bewegt. Sofern die Maus nicht von einem anderen Objekt erfasst wurde, erkennt ein [InkEdit-Steuerelement](inkedit-control-reference.md) ein **MouseMove-Ereignis,** wenn sich die Mausposition innerhalb der Rahmen befindet.

Diese Ereignismethode wird in der **\_ IInkEditEvents-Schnittstelle** definiert. Die **\_ IInkEditEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IeeMouseMove.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (erfordert auch inked \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> <dt>

[**InkMouseButton-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**InkShiftKeyModifierFlags-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**MouseDown-Ereignis \[ inkEdit-Steuerelement\]**](inkedit-mousedown.md)
</dt> <dt>

[**MouseUp-Ereignis \[ - InkEdit-Steuerelement\]**](inkedit-mouseup.md)
</dt> </dl>

 

