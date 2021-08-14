---
description: Tritt ein, wenn der Benutzer eine Taste drückt, während das InkEdit-Steuerelement den Fokus besitzt.
ms.assetid: 14b05b72-ae5d-416a-8ea5-9d9716c0967f
title: InkEdit.KeyDown-Ereignis (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ab1c1b54f9f60d4bd0868f6e093505e21255991502653712a540728394664c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967138"
---
# <a name="inkeditkeydown-event"></a>InkEdit.KeyDown-Ereignis

Tritt ein, wenn der Benutzer eine Taste drückt, während das [InkEdit-Steuerelement](inkedit-control-reference.md) den Fokus besitzt.

## <a name="syntax"></a>Syntax


```C++
HRESULT KeyDown(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pKey* 
</dt> <dd>

Der Code der virtuellen Taste, die vom Benutzer gedrückt wird.

</dd> <dt>

*UMSCHALTTASTE* 
</dt> <dd>

Ein Member der [**InkShiftKeyModifierFlags-Enumeration,**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) der angibt, welche Modifiziererschlüssel zum Zeitpunkt des Ereignisses abgetastet werden.



| Wert                                                                                                                                                                                     | Bedeutung                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**\_IKM-Umschalt**</dt> </dl>             | Gibt an, dass die UMSCHALTTASTE als Modifizierer verwendet wurde. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Steuerelement**</dt> </dl> | Gibt an, dass die STRG-Taste als Modifizierer verwendet wurde. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ ALT**</dt> </dl>                 | Gibt an, dass der ALT-Schlüssel als Modifizierer verwendet wurde. <br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in der **\_ IInkEditEvents-Schnittstelle** definiert. Die **\_ IInkEditEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IeeKeyDown.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (erfordert auch inked \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> <dt>

[**InkShiftKeyModifierFlags-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**KeyPress-Ereignis \[ inkEdit-Steuerelement\]**](inkedit-keypress.md)
</dt> <dt>

[**KeyUp-Ereignis \[ inkEdit-Steuerelement\]**](inkedit-keyup.md)
</dt> </dl>

 

