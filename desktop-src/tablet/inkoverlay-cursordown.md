---
description: Tritt auf, wenn die Cursor-QuickInfo die digitalisierende Tablet-Oberfläche kontaktiert
ms.assetid: 753aa733-8d62-4983-b76d-d58844b79c35
title: InkOverlay. currsordown-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea0bd76d8836ae31c6e17877ddc4870dafaaa93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360632"
---
# <a name="inkoverlaycursordown-event"></a>InkOverlay. currsordown-Ereignis

Tritt auf, wenn die Cursor-QuickInfo die digitalisierende Tablet-Oberfläche kontaktiert

## <a name="syntax"></a>Syntax


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ in\]
</dt> <dd>

Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das [**CursorDown**](inkcollector-cursordown.md) -Ereignis generiert hat.

</dd> <dt>

*Strich* \[ in\]
</dt> <dd>

Das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt, das gestartet wurde, [**als das "**](inkcollector-cursordown.md) [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) "-Objekt ausgelöst wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode ist in den \_ iinkcollectorevents-, \_ iinkoverlayevents-und \_ iinkpictureevents-Ereignissen definiert. die \_ iinkcollector Events \_ -, iinkoverlayevents-und \_ iinkpictureevents-Schnittstelle implementieren die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ icecursordown.

Verwenden Sie dieses Ereignis sorgfältig, da dies eine negative Auswirkung auf die Handschrift Leistung haben kann, wenn zu viel Code in den Ereignis Handlern ausgeführt wird. Um die Echtzeitleistung zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown**](inkcollector-mousedown.md) -und [**MouseUp**](inkcollector-mouseup.md) -Ereignis Handlern aus, oder zeigen Sie ihn an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**Currsorbuttondown-Ereignis**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Currsorbuttonup-Ereignis**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

