---
description: Tritt auf, wenn das Mausrad bewegt wird, während das InkCollector-oder InkOverlay-Objekt den Fokus besitzt.
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: InkCollector. mouswheel-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e6a6728bfcbe058ff5eab56499f6c8e885351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346304"
---
# <a name="inkcollectormousewheel-event"></a>InkCollector. mouswheel-Ereignis

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

**Variant \_ TRUE** , um das Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls ist der Wert **\_ false**. Der Standardwert ist **Variant \_ false**.

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

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[**Inkmouerbutton-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Inkshiftkeymodifierflags-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




