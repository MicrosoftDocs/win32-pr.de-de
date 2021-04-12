---
description: Tritt auf, wenn der Mauszeiger über das InkCollector-oder InkOverlay-Objekt bewegt wird.
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: InkOverlay. moutarmove-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ddefd5f3b3f75b03488f74bdbd4aee222a89d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218050"
---
# <a name="inkoverlaymousemove-event"></a>InkOverlay. moutarmove-Ereignis

Tritt auf, wenn der Mauszeiger über das [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt bewegt wird.

## <a name="syntax"></a>Syntax


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schaltfläche* \[ in\]
</dt> <dd>

Die Maustaste, die gedrückt wurde.

</dd> <dt>

*UMSCHALT* \[ in\]
</dt> <dd>

Der Zustand der UMSCHALTTASTE.

</dd> <dt>

*px* \[ in\]
</dt> <dd>

Die x-Koordinate eines Mausklicks in Pixel.

</dd> <dt>

*pY* \[ in\]
</dt> <dd>

Die y-Koordinate eines Mausklicks in Pixel.

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

Ob das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll. Der Standardwert ist **false**. er gibt an, dass das Ereignis nicht abgebrochen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Eigenschaften *px* und *pY* befinden sich in Pixel und nicht in den HIMETRIC-Einheiten, die dem frei Handbereich zugeordnet sind. Dies liegt daran, dass dieses Ereignis das verknüpfte Maus Ereignis einer Anwendung, für die ein Stift nicht gilt, ersetzt und dieser Anwendungstyp nur Pixel versteht.

 

> [!Note]  
> Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**mouledown**](inkcollector-mousedown.md)-, [**mousermove**](inkcollector-mousemove.md)-und [**mouberup**](inkcollector-mouseup.md) -Ereignissen. Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.

 

Diese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ipemousemove definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**Inkmouerbutton-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Inkshiftkeymodifierflags-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




