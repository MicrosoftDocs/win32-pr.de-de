---
description: 'InkOverlay.CursorButtonDown-Ereignis: Tritt auf, wenn die InkCollector-Klasse eine schaltfläche erkennt, die heruntergefahren ist.'
ms.assetid: 993b84a3-a5ac-4b00-bfb4-26ca1c9727c6
title: InkOverlay.CursorButtonDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e73edfd6c8d9901a1eab0adf13c3c5439ef5716d1489ddb30e008079304d44b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967099"
---
# <a name="inkoverlaycursorbuttondown-event"></a>InkOverlay.CursorButtonDown-Ereignis

Tritt ein, wenn [**die InkCollector-Klasse**](inkcollector-class.md) eine Cursorschaltfläche erkennt, die nicht mehr angezeigt wird.

## <a name="syntax"></a>Syntax


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**CursorButtonDown-Ereignis generiert**](inkcollector-cursorbuttondown.md) hat.

</dd> <dt>

*Schaltfläche* \[ In\]
</dt> <dd>

Die Schaltfläche, die gedrückt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Eine Schaltfläche auf einer Stiftspitze ist nach unten, wenn der Benutzer den Stift auf den Digitizer heruntersendt und mit der Ablaufverfolgung eines Strichs beginnt. Wenn die Schaltfläche gedrückt wird, ist eine Schaltfläche auf einer Knopffläche nicht mehr zu sehen.

Wenn Sie die rechte Maustaste drücken, erhalten Sie tatsächlich zwei [**CursorButtonDown-Ereignisse**](inkcollector-cursorbuttondown.md) : eines für die gedrückte rechte Schaltfläche und eines für die linke Schaltfläche.

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICECursorButtonDown definiert.

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

[**CursorDown-Ereignis**](inkcollector-cursordown.md)
</dt> <dt>

[**CursorButtonUp-Ereignis**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




