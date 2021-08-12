---
description: 'InkCollector.CursorButtonDown-Ereignis: Tritt auf, wenn die InkCollector-Klasse eine Cursorschaltfläche erkennt, die nicht aktiv ist.'
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: InkCollector.CursorButtonDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c8a2c1a2e832d4fd18c7c84f9905d0aa1694b425f5f5e7ece91e96afc1684f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451293"
---
# <a name="inkcollectorcursorbuttondown-event"></a>InkCollector.CursorButtonDown-Ereignis

Tritt ein, wenn die [**InkCollector-Klasse**](inkcollector-class.md) eine Cursorschaltfläche erkennt, die nicht angezeigt wird.

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

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorButtonDown-Ereignis** generiert hat.

</dd> <dt>

*Schaltfläche* \[ In\]
</dt> <dd>

Die Schaltfläche, die gedrückt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Eine Schaltfläche auf einer Stiftspitze ist nach unten, wenn der Benutzer den Stift auf den Digitizer heruntersenkt und mit der Ablaufverfolgung eines Strichs beginnt. Eine Schaltfläche an einem Fass ist nach dem Drücken der Schaltfläche nicht mehr zu betätigen.

Wenn Sie die rechte Maustaste drücken, erhalten Sie tatsächlich zwei **CursorButtonDown-Ereignisse:** eines für die gedrückte rechte Schaltfläche und eines für die gedrückte linke Schaltfläche.

Diese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICECursorButtonDown definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[**CursorDown-Ereignis**](inkcollector-cursordown.md)
</dt> <dt>

[**CursorButtonUp-Ereignis**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




