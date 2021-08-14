---
description: Tritt ein, bevor das InkOverlay-Objekt oder InkPicture die Neuzeichnung abgeschlossen hat.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: InkOverlay.Painting-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42075f6ae8641c895611196b80a904228cc27c45e5d84bdc798b5cc9242e7c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218942"
---
# <a name="inkoverlaypainting-event"></a>InkOverlay.Painting-Ereignis

Tritt ein, bevor das [**InkOverlay-Objekt**](inkoverlay-class.md) oder [InkPicture](inkpicture-control-reference.md) die Neuzeichnung abgeschlossen hat.

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

*hDC* \[ In\]
</dt> <dd>

Der Gerätekontext, in dem das Zeichnen ausgeführt wird.

</dd> <dt>

*Rect* \[ In\]
</dt> <dd>

Das Rechteck, das neu maliert werden soll.

</dd> <dt>

*Zulassen* \[ in, out\]
</dt> <dd>

Gibt an, ob der neu strich ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IOEPainting definiert.

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
</dt> </dl>

 

 




