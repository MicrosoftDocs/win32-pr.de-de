---
description: 'InkPicture.CursorDown-Ereignis: Tritt auf, wenn die Cursorspitze mit der digitalisierenden Tablet-Oberfläche in Kontakt tritt.'
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: InkPicture.CursorDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a0fd7a6c077093ae7e14ab1d905398e0b75a585cf09c2a87b0da9b843844a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967079"
---
# <a name="inkpicturecursordown-event"></a>InkPicture.CursorDown-Ereignis

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

Diese Ereignismethoden werden in den **\_ Schnittstellen IInkCollectorEvents,** **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** definiert. Die **\_ Schnittstellen IInkCollectorEvents,** **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** implementieren die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ ICECursorDown.

Verwenden Sie dieses Ereignis sorgfältig, da es sich negativ auf die Ink-Leistung auswirken kann, wenn in den Ereignishandlern zu viel Code ausgeführt wird. Um die Leistung von Ink in Echtzeit zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown-**](inkpicture-mousedown.md) und [**MouseUp-Ereignishandlern**](inkpicture-mouseup.md) aus oder ein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**CursorButtonUp-Ereignis**](inkpicture-cursorbuttonup.md)
</dt> <dt>

[**CursorButtonDown-Ereignis**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

