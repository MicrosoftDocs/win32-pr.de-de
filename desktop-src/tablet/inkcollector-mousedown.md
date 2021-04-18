---
description: Tritt auf, wenn sich der Mauszeiger über dem InkCollector-oder InkOverlay-Objekt befindet und eine Maustaste gedrückt wird.
ms.assetid: db9ec396-b2a7-4f4f-99f2-95aad46eea28
title: InkCollector. mouabdown-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760801fb5c578ddbdd67b15a4201c21c4981b097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525271"
---
# <a name="inkcollectormousedown-event"></a>InkCollector. mousegdown-Ereignis

Tritt auf, wenn sich der Mauszeiger über dem [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt befindet und eine Maustaste gedrückt wird.

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

Die X-Koordinate eines Mausklicks in Pixel.

</dd> <dt>

*pY* \[ in\]
</dt> <dd>

Die Y-Koordinate eines Mausklicks in Pixel.

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

**Variant \_ TRUE** , um das Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um die Echtzeitleistung zu verbessern, blenden Sie den Mauszeiger in den **MouseDown** -und [**MouseUp**](inkcollector-mouseup.md) -Ereignis Handlern aus, oder zeigen Sie ihn an.

> [!Note]  
> Die Eigenschaften *px* und *pY* befinden sich in Pixel und nicht in den HIMETRIC-Einheiten, die dem frei Handbereich zugeordnet sind. Dies liegt daran, dass dieses Ereignis das verknüpfte Maus Ereignis einer Anwendung, für die ein Stift nicht gilt, ersetzt und dieser Anwendungstyp nur Pixel versteht.

 

> [!Note]  
> Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen **mouledown**-, [**mousermove**](inkcollector-mousemove.md)-und [**mouberup**](inkcollector-mouseup.md) -Ereignissen. Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.

 

Diese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ipemousedown definiert.

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
</dt> <dt>

[**Mouberup-Ereignis**](inkcollector-mouseup.md)
</dt> </dl>

 

 




