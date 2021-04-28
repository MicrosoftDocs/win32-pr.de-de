---
description: 'InkPicture.CursorDown-Ereignis: Tritt ein, wenn die Cursorspitze mit der digitalisierenden Tablettoberfläche in Kontakt tritt.'
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: InkPicture.CursorDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4b6128589ba2d0b87d4369e8bb58aa66eabf23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116698"
---
# <a name="inkpicturecursordown-event"></a>InkPicture.CursorDown-Ereignis

Tritt ein, wenn die Cursorspitze die digitalisierende Tablettoberfläche kontaktiert.

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

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorDown-Ereignis** generiert hat.

</dd> <dt>

*Strich* \[ In\]
</dt> <dd>

Das [**IInkStrokeDisp-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) das gestartet wurde, als das [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das **CursorDown-Ereignis** ausgelöst hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethoden werden in den Schnittstellen **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** definiert. Die Schnittstellen **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** implementieren die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ ICECursorDown.

Verwenden Sie dieses Ereignis sorgfältig, da es negative Auswirkungen auf die Ink-Leistung haben kann, wenn zu viel Code in den Ereignishandlern ausgeführt wird. Um die Leistung von Ink-Echtzeit zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown-**](inkpicture-mousedown.md) und [**MouseUp-Ereignishandlern**](inkpicture-mouseup.md) aus oder ein.

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

[**CursorButtonUp-Ereignis**](inkpicture-cursorbuttonup.md)
</dt> <dt>

[**CursorButtonDown-Ereignis**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

