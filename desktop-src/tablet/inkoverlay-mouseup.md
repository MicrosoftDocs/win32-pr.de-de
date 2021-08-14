---
description: 'InkOverlay.MouseUp-Ereignis: Tritt auf, wenn sich der Mauszeiger über dem InkCollector- oder InkOverlay-Objekt befindet und eine Maustaste losgelassen wird.'
ms.assetid: 049e1560-d4b2-4d34-9d54-2b45217001b2
title: InkOverlay.MouseUp-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 675c588d12976a506afec02e1bec58d97a99fd13ec897250f0e472dfbc519490
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219786"
---
# <a name="inkoverlaymouseup-event"></a>InkOverlay.MouseUp-Ereignis

Tritt ein, wenn sich der Mauszeiger über dem [**InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) befindet und eine Maustaste losgelassen wird.

## <a name="syntax"></a>Syntax


```C++
void MouseUp(
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

Die Maustaste, die losgelassen wurde.

</dd> <dt>

*Umschalten* \[ In\]
</dt> <dd>

Der Zustand der UMSCHALTTASTE.

</dd> <dt>

*pX* \[ In\]
</dt> <dd>

Die x-Koordinate eines Mausklicks in Pixel.

</dd> <dt>

*pY* \[ In\]
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

Um die Leistung von Ink in Echtzeit zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown-**](inkcollector-mousedown.md) und [**MouseUp-Ereignishandlern**](inkcollector-mouseup.md) aus oder ein.

> [!Note]  
> Die Eigenschaften *pX* und *pY* sind in Pixeln und nicht in den HIMETRIC-Einheiten angegeben, die dem Freiraum zugeordnet sind. Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Nicht-Stiftanwendung ersetzt und diese Art von Anwendung nur Pixel versteht.

 

> [!Note]  
> Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**MouseDown-,**](inkcollector-mousedown.md) [**MouseMove-**](inkcollector-mousemove.md)und [**MouseUp-Ereignissen.**](inkcollector-mouseup.md) Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.

 

Diese Ereignismethode wird in den \_ Dispatchschnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEMouseUp definiert.

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

 

 




