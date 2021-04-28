---
description: 'InkPicture.CursorButtonDown-Ereignis: Tritt auf, wenn die InkCollector-Klasse eine Cursorschaltfläche erkennt, die nicht aktiv ist.'
ms.assetid: 9ee2c19e-8a44-428b-a4c1-3c7250dcdeda
title: InkPicture.CursorButtonDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2017cd7dc2291bdb29aa01df3d94f20211b7cf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116778"
---
# <a name="inkpicturecursorbuttondown-event"></a>InkPicture.CursorButtonDown-Ereignis

Tritt ein, wenn die [**InkCollector-Klasse**](inkcollector-class.md) eine Cursorschaltfläche erkennt, die nicht aktiv ist.

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

## <a name="remarks"></a>Bemerkungen

Eine Schaltfläche auf einer Stiftspitze ist nach unten geschaltet, wenn der Benutzer den Stift auf den Digitizer heruntersenkt und mit der Ablaufverfolgung eines Strichs beginnt. Eine Schaltfläche an einem Fass ist nach dem Drücken der Schaltfläche nicht mehr zu haben.

Wenn Sie die rechte Maustaste drücken, erhalten Sie tatsächlich zwei **CursorButtonDown-Ereignisse:** eines für die gedrückte rechte Schaltfläche und eines für die gedrückte linke Schaltfläche.

Diese Ereignismethode wird in der **\_ IInkCollectorEvents-,** **\_ IInkOverlayEvents-** und **\_ IInkPictureEvents-Dispatch-Only-Schnittstelle** (dispinterfaces) mit der ID DISPID \_ ICECursorButtonDown definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**CursorDown-Ereignis**](inkpicture-cursordown.md)
</dt> <dt>

[**CursorButtonUp-Ereignis**](inkpicture-cursorbuttonup.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




