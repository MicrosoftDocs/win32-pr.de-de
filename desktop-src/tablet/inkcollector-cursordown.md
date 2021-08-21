---
description: 'InkCollector.CursorDown-Ereignis: Tritt auf, wenn die Cursorspitze die digitalisierende Tablet-Oberfläche kontaktiert.'
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: InkCollector.CursorDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a98a58ce3c6576b45b4c60d47781f8de6ae9f8d5ab0cfea3222ef36890290f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032118"
---
# <a name="inkcollectorcursordown-event"></a>InkCollector.CursorDown-Ereignis

Tritt ein, wenn die Cursorspitze die digitalisierende Tablet-Oberfläche kontaktiert.

## <a name="syntax"></a>Syntax


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorDown-Ereignis generiert** hat.

</dd> <dt>

*Strich* \[ In\]
</dt> <dd>

Das [**IInkStrokeDisp-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) das gestartet wurde, als das [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das **CursorDown-Ereignis** ausgelöst hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den \_ IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents definiert. Die \_ Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und IInkPictureEvents implementieren die IDispatch-Schnittstelle mit dem Bezeichner \_ DISPID [](/windows/win32/api/oaidl/nn-oaidl-idispatch) \_ ICECursorDown.

Verwenden Sie dieses Ereignis sorgfältig, da es sich negativ auf die Ink-Leistung auswirken kann, wenn in den Ereignishandlern zu viel Code ausgeführt wird. Um die Leistung von Ink in Echtzeit zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown-**](inkcollector-mousedown.md) und [**MouseUp-Ereignishandlern**](inkcollector-mouseup.md) aus oder ein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[**CursorButtonDown-Ereignis**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**CursorButtonUp-Ereignis**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

