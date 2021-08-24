---
description: 'InkCollector.MouseWheel-Ereignis: Tritt auf, wenn das Mausrad bewegt wird, während das InkCollector- oder InkOverlay-Objekt den Fokus besitzt.'
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: InkCollector.MouseWheel-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6c66d5b8698131f3dce422e404f7ce33a25472a0c1e28211f5f90b5616f9f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713020"
---
# <a name="inkcollectormousewheel-event"></a>InkCollector.MouseWheel-Ereignis

Tritt ein, wenn sich das Mausrad bewegt, während [**das InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) den Fokus besitzt.

## <a name="syntax"></a>Syntax


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schaltfläche* \[ In\]
</dt> <dd>

Die gedrückte Maustaste.

</dd> <dt>

*Umschalten* \[ In\]
</dt> <dd>

Der Zustand der UMSCHALTTASTE.

</dd> <dt>

*Delta* \[ In\]
</dt> <dd>

Eine Anzahl mit Vorzeichen für die Anzahl der Detenten, die das Mausrad gedreht hat. Eine Arretierung (Rastpunkt) ist eine Kerbe des Mausrades.

</dd> <dt>

*x* \[ in\]
</dt> <dd>

Die x-Koordinate eines Mausklicks in Pixel.

</dd> <dt>

*y* \[ in\]
</dt> <dd>

Die y-Koordinate eines Mausklicks in Pixel.

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE,** um das Ereignis für das übergeordnete Steuerelement abzubricht; andernfalls **VARIANT \_ FALSE**. Der Standardwert ist **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Eigenschaften *pX* und *pY* befinden sich in Pixeln und nicht in den HIMETRIC-Einheiten, die dem Freiraum zugeordnet sind. Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Nicht-Stiftanwendung ersetzt und diese Art von Anwendung nur Pixel versteht.

 

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEMouseWheel definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[**InkMouseButton-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**InkShiftKeyModifierFlags-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




