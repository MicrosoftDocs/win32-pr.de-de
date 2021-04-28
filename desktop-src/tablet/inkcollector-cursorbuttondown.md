---
description: 'InkCollector.CursorButtonDown-Ereignis: Tritt auf, wenn die InkCollector-Klasse eine schaltfläche erkennt, die heruntergefahren ist.'
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: InkCollector.CursorButtonDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd1a820445a1ba3ed07dad8a22a11ad86e8da96f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110328"
---
# <a name="inkcollectorcursorbuttondown-event"></a>InkCollector.CursorButtonDown-Ereignis

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

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorButtonDown-Ereignis generiert** hat.

</dd> <dt>

*Schaltfläche* \[ In\]
</dt> <dd>

Die Schaltfläche, die gedrückt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine Schaltfläche auf einer Stiftspitze ist nach unten, wenn der Benutzer den Stift auf den Digitizer heruntersendt und mit der Ablaufverfolgung eines Strichs beginnt. Wenn die Schaltfläche gedrückt wird, ist eine Schaltfläche auf einer Knopffläche nicht mehr zu sehen.

Wenn Sie die rechte Maustaste drücken, erhalten Sie tatsächlich zwei **CursorButtonDown-Ereignisse** : eines für die gedrückte rechte Schaltfläche und eines für die linke Schaltfläche.

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICECursorButtonDown definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

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

 

 




