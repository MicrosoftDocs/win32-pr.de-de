---
description: Tritt ein, bevor das InkOverlay-Objekt oder InkPicture das erneute Zeichnen von sich selbst abgeschlossen hat.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: InkOverlay. Paint-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc056667f88c0631e84a76767fc97f90ca05a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529903"
---
# <a name="inkoverlaypainting-event"></a>InkOverlay. Paint-Ereignis

Tritt ein, bevor das [**InkOverlay**](inkoverlay-class.md) -Objekt oder [InkPicture](inkpicture-control-reference.md) das erneute Zeichnen von sich selbst abgeschlossen hat.

## <a name="syntax"></a>Syntax


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdc* \[ in\]
</dt> <dd>

Der Gerätekontext, auf dem gezeichnet werden soll.

</dd> <dt>

*Rect* \[ in\]
</dt> <dd>

Das Rechteck, das neu gezeichnet werden soll.

</dd> <dt>

*Zulassen* \[ in, out\]
</dt> <dd>

Gibt an, ob der Repaint-Vorgang ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ioepaint definiert.

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
</dt> </dl>

 

 




