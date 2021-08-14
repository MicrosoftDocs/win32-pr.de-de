---
description: Tritt ein, wenn das InkOverlay-Objekt oder das InkPicture-Steuerelement die Neuzeichnung abgeschlossen hat.
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: InkOverlay.Painted-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f433f18d5e94be1163be519f4ee33fbe0b8d08a2e33feadd363a8eb3a43a6b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218934"
---
# <a name="inkoverlaypainted-event"></a>InkOverlay.Painted-Ereignis

Tritt ein, wenn das [**InkOverlay-Objekt**](inkoverlay-class.md) oder [das InkPicture-Steuerelement](inkpicture-control-reference.md) die Neuzeichnung abgeschlossen hat.

## <a name="syntax"></a>Syntax


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDC* \[ In\]
</dt> <dd>

Der Gerätekontext, in dem das Ereignis aufgetreten ist.

</dd> <dt>

*Rect* \[ In\]
</dt> <dd>

Das [**InkRectangle,**](inkrectangle-class.md) das neu maliert wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IOEPainted definiert.

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

 

 




