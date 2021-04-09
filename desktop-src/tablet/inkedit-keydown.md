---
description: Tritt ein, wenn der Benutzer eine Taste drückt, während das InkEdit-Steuerelement den Fokus besitzt.
ms.assetid: 14b05b72-ae5d-416a-8ea5-9d9716c0967f
title: InkEdit. KeyDown-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cee260d4c902534b9b234e0e30d0b60645c579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960672"
---
# <a name="inkeditkeydown-event"></a>InkEdit. KeyDown-Ereignis

Tritt ein, wenn der Benutzer eine Taste drückt, während das [InkEdit](inkedit-control-reference.md) -Steuerelement den Fokus besitzt.

## <a name="syntax"></a>Syntax


```C++
HRESULT KeyDown(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pkey* 
</dt> <dd>

Der Code des virtuellen Schlüssels, der vom Benutzer gedrückt wurde.

</dd> <dt>

*ShiftKey* 
</dt> <dd>

Ein Member der [**inkshiftkeymodifierflags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) -Enumeration, der angibt, welche modifiziererschlüssel zum Zeitpunkt des Ereignisses gedrückt werden.



| Wert                                                                                                                                                                                     | Bedeutung                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**IKM- \_ Schicht**</dt> </dl>             | Gibt an, dass die Umschalttaste als Modifizierer verwendet wurde. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Steuer** Element</dt> </dl> | Gibt an, dass die STRG-Taste als Modifizierer verwendet wurde. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ Alt**</dt> </dl>                 | Gibt an, dass die Alt-Taste als Modifizierer verwendet wurde. <br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert. Die **\_ iinkeditevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ieekeydown.

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

[**Inkshiftkeymodifierflags-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**KeyPress-Ereignis, \[ InkEdit-Steuerelement\]**](inkedit-keypress.md)
</dt> <dt>

[**KeyUp-Ereignis \[ InkEdit-Steuerelement\]**](inkedit-keyup.md)
</dt> </dl>

 

