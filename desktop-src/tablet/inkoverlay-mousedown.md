---
description: 'InkOverlay.MouseDown-Ereignis: Tritt auf, wenn sich der Mauszeiger über dem InkCollector- oder InkOverlay-Objekt befindet und eine Maustaste gedrückt wird.'
ms.assetid: 95c3b1ae-0e77-4ca2-ab73-a0e97ab115b5
title: InkOverlay.MouseDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b0d605dd36f4cae410de2514542aa15818d4604e4484352c68dac54b40b1d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219266"
---
# <a name="inkoverlaymousedown-event"></a>InkOverlay.MouseDown-Ereignis

Tritt ein, wenn sich der Mauszeiger über dem [**InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) befindet und eine Maustaste gedrückt wird.

## <a name="syntax"></a>Syntax


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
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

*pX* \[ In\]
</dt> <dd>

Die X-Koordinate eines Mausklicks in Pixel.

</dd> <dt>

*pY* \[ In\]
</dt> <dd>

Die Y-Koordinate eines Mausklicks in Pixel.

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE,** um das Ereignis für das übergeordnete Steuerelement abzubricht; andernfalls **VARIANT \_ FALSE**. Der Standardwert ist **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um die Leistung von Ink in Echtzeit zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown-**](inkcollector-mousedown.md) und [**MouseUp-Ereignishandlern**](inkcollector-mouseup.md) aus oder ein.

> [!Note]  
> Die Eigenschaften pX und pY befinden sich in Pixeln und nicht in den HIMETRIC-Einheiten, die dem Freiraum zugeordnet sind. Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Nicht-Stiftanwendung ersetzt und diese Art von Anwendung nur Pixel versteht.

 

> [!Note]  
> Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**MouseDown-,**](inkcollector-mousedown.md) [**MouseMove-**](inkcollector-mousemove.md)und [**MouseUp-Ereignissen.**](inkcollector-mouseup.md) Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.

 

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEMouseDown definiert.

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
</dt> <dt>

[**MouseUp-Ereignis**](inkcollector-mouseup.md)
</dt> </dl>

 

 




