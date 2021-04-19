---
description: Tritt ein, wenn der Benutzer die Maus bewegt, während sich der Mauszeiger über dem InkEdit-Steuerelement befindet.
ms.assetid: 6ccaf2eb-acec-4dfd-9ec7-c78aca043900
title: InkEdit. mousermove-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0d3e98827a1f0ebcdc80f5d44765ebe768f65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350301"
---
# <a name="inkeditmousemove-event"></a>InkEdit. mousermove-Ereignis

Tritt ein, wenn der Benutzer die Maus bewegt, während sich der Mauszeiger über dem [InkEdit](inkedit-control-reference.md) -Steuerelement befindet.

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

Ein Member der [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) -Enumeration, der angibt, welche Maustasten gedrückt sind.



| Wert                                                                                                                                                            | Bedeutung                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <dt>**Nein \_ Schaltfläche**</dt> </dl>             | Standard. Es wurde keine Maustaste gedrückt. <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <dt>**Links \_ Schaltfläche**</dt> </dl>       | Die linke Maustaste wurde gedrückt. <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <dt>**Rechts \_ Schaltfläche**</dt> </dl>    | Die rechte Maustaste wurde gedrückt. <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <dt>**Mittel \_ Schaltfläche**</dt> </dl> | Die mittlere Maustaste wurde gedrückt. <br/>  |



 

</dd> <dt>

*ShiftKey* 
</dt> <dd>

Ein Member der [**inkshiftkeymodifierflags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) -Enumeration, der angibt, welche modifiziererschlüssel zum Zeitpunkt des Ereignisses gedrückt werden.



| Wert                                                                                                                                                                                     | Bedeutung                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**IKM- \_ Schicht**</dt> </dl>             | Gibt an, dass die Umschalttaste als Modifizierer verwendet wurde. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Steuer** Element</dt> </dl> | Gibt an, dass die STRG-Taste als Modifizierer verwendet wurde. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ Alt**</dt> </dl>                 | Gibt an, dass die Alt-Taste als Modifizierer verwendet wurde. <br/>   |



 

</dd> <dt>

*xmaus* 
</dt> <dd>

Die aktuelle x-Koordinate des Mauszeigers in Pixel.

</dd> <dt>

*ymouse* 
</dt> <dd>

Die aktuelle y-Koordinate des Mauszeigers in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn eine Maustaste gedrückt wird, während sich der Mauszeiger über einem [InkEdit](inkedit-control-reference.md) -Steuerelement befindet, erfasst das Steuerelement die Maus und empfängt alle Mausereignisse bis einschließlich des letzten [**MouseUp**](inkedit-mouseup.md) -Ereignisses. Dies impliziert, dass die (x, y)-Mauszeiger Koordinaten, die von einem Maus Ereignis zurückgegeben werden, sich nicht immer im internen Bereich des Objekts befinden, das Sie empfängt.

Wenn die Maustasten nacheinander gedrückt werden, empfängt das Objekt, das die Maus nach dem ersten drücken aufzeichnet, alle Mausereignisse, bis alle Schaltflächen losgelassen werden.

Das **MouseMove** -Ereignis wird fortlaufend generiert, wenn der Mauszeiger über Objekte bewegt wird. Wenn die Maus von keinem anderen Objekt erfasst wird, erkennt ein [InkEdit](inkedit-control-reference.md) -Steuerelement immer dann ein **MouseMove** -Ereignis, wenn sich die Mausposition innerhalb seines Rahmens befindet.

Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert. Die **\_ iinkeditevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ieemouabmove.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Inkmouerbutton-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Inkshiftkeymodifierflags-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Mousdown-Ereignis, \[ InkEdit-Steuerelement\]**](inkedit-mousedown.md)
</dt> <dt>

[**Mousup-Ereignis \[ InkEdit-Steuerelement\]**](inkedit-mouseup.md)
</dt> </dl>

 

