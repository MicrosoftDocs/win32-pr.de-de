---
description: 'InkOverlay.CursorButtonUp-Ereignis: Tritt auf, wenn der InkCollector eine Cursorschaltfläche erkennt, die aktiv ist.'
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: InkOverlay.CursorButtonUp-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f22590362c6eb9a987da94bf3adb4e99943c12cd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086848"
---
# <a name="inkoverlaycursorbuttonup-event"></a>InkOverlay.CursorButtonUp-Ereignis

Tritt ein, wenn [**der InkCollector**](inkcollector-class.md) eine cursor-Schaltfläche erkennt, die aktiv ist.

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

## <a name="remarks"></a>Bemerkungen

Eine Schaltfläche auf einer Stiftspitze wird angezeigt, wenn der Benutzer einen Strich abschließt und den Stift aus dem Digitizer hebt. Eine Schaltfläche an einem Fass ist hoch, wenn die Schaltfläche nicht gedrückt wird.

Wenn Sie die rechte Maustaste loslassen, erhalten Sie tatsächlich zwei [**CursorButtonUp-Ereignisse:**](inkcollector-cursorbuttonup.md) eines für die rechte Schaltfläche nach oben und eines für die linke Schaltfläche nach oben.

Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICECursorButtonUp definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]<br/>                                                       |
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

 

 




