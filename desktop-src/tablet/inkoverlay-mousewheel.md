---
description: 'InkOverlay.MouseWheel-Ereignis: Tritt auf, wenn das Mausrad bewegt wird, während das InkCollector- oder InkOverlay-Objekt den Fokus besitzt.'
ms.assetid: b7269e07-7001-48ca-8e20-a39cb02f3719
title: InkOverlay.MouseWheel-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c2563ae898eff2b9541ac52d77626ddebb8259d8bb60a82b18f6460da55f7dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219204"
---
# <a name="inkoverlaymousewheel-event"></a>InkOverlay.MouseWheel-Ereignis

Tritt ein, wenn das Mausrad bewegt wird, während das [**InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) den Fokus besitzt.

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

Die maustaste, die gedrückt wurde.

</dd> <dt>

*Umschalten* \[ In\]
</dt> <dd>

Der Zustand der UMSCHALTTASTE.

</dd> <dt>

*Delta* \[ In\]
</dt> <dd>

Eine Anzahl mit Vorzeichen für die Anzahl von Detents, die das Mausrad gedreht hat. Eine Arretierung (Rastpunkt) ist eine Kerbe des Mausrades.

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

Gibt an, ob das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll. Der Standardwert ist **FALSE,** der angibt, dass das Ereignis nicht abgebrochen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Eigenschaften *pX* und *pY* sind in Pixel und nicht die HIMETRIC-Einheiten, die dem Freihandraum zugeordnet sind. Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Anwendung ohne Stift ersetzt und diese Art von Anwendung nur Pixel versteht.

 

Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEMouseWheel definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**InkMouseButton-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**InkShiftKeyModifierFlags-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




