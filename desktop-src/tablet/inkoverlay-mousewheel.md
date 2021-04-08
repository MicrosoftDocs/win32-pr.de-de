---
description: Tritt auf, wenn das Mausrad bewegt wird, während das InkCollector-oder InkOverlay-Objekt den Fokus besitzt.
ms.assetid: b7269e07-7001-48ca-8e20-a39cb02f3719
title: InkOverlay. mouswheel-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd919fdf02d85c32efa2a1a923d5de7ebe4f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868292"
---
# <a name="inkoverlaymousewheel-event"></a>InkOverlay. mouswheel-Ereignis

Tritt auf, wenn das Mausrad bewegt wird, während das [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt den Fokus besitzt.

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

*Schaltfläche* \[ in\]
</dt> <dd>

Die Maustaste, die gedrückt wurde.

</dd> <dt>

*UMSCHALT* \[ in\]
</dt> <dd>

Der Zustand der UMSCHALTTASTE.

</dd> <dt>

*Delta* \[ in\]
</dt> <dd>

Eine Anzahl mit Vorzeichen, die die Anzahl der Aufzählungs Zeichen des Mausrades gedreht hat. Eine Arretierung (Rastpunkt) ist eine Kerbe des Mausrades.

</dd> <dt>

*x* \[ in\]
</dt> <dd>

Die x-Koordinate eines Mausklicks in Pixel.

</dd> <dt>

*j* \[ in\]
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

 

Diese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ipemousewheel definiert.

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

 

 




