---
description: 'InkOverlay.CursorButtonUp-Ereignis: Tritt auf, wenn der InkCollector eine Cursorschaltfläche erkennt, die aktiv ist.'
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: InkOverlay.CursorButtonUp-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e94fb9c1727e0c8fce13f3696397462fdf590c076627df869dcafd177190c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220845"
---
# <a name="inkoverlaycursorbuttonup-event"></a>InkOverlay.CursorButtonUp-Ereignis

Tritt ein, wenn [**der InkCollector**](inkcollector-class.md) eine Cursorschaltfläche erkennt, die aktiv ist.

## <a name="syntax"></a>Syntax


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Schnittstellenobjekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**CursorButtonUp-Ereignis**](inkcollector-cursorbuttonup.md) generiert hat.

</dd> <dt>

*Schaltfläche* \[ In\]
</dt> <dd>

Die Schaltfläche, die freigegeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Eine Schaltfläche auf einer Stiftspitze wird angezeigt, wenn der Benutzer einen Strich abschließt und den Stift aus dem Digitizer hebt. Eine Schaltfläche an einem Fass ist hoch, wenn die Schaltfläche nicht gedrückt wird.

Wenn Sie die rechte Maustaste loslassen, erhalten Sie tatsächlich zwei [**CursorButtonUp-Ereignisse:**](inkcollector-cursorbuttonup.md) eines für die rechte Schaltfläche nach oben und eines für die linke Schaltfläche nach oben.

Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICECursorButtonUp definiert.

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

[**CursorButtonDown-Ereignis**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**CursorDown-Ereignis**](inkcollector-cursordown.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




