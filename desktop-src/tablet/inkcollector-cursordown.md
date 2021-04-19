---
description: Tritt auf, wenn die Cursor-QuickInfo die digitalisierende Tablet-Oberfläche kontaktiert
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: InkCollector. currsordown-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fd009c5f42e6a26cdaf493e97532be7716381c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353058"
---
# <a name="inkcollectorcursordown-event"></a>InkCollector. currsordown-Ereignis

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

Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das **CursorDown** -Ereignis generiert hat.

</dd> <dt>

*Strich* \[ in\]
</dt> <dd>

Das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt, das gestartet wurde, **als das "** [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) "-Objekt ausgelöst wurde.

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

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[**Currsorbuttondown-Ereignis**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Currsorbuttonup-Ereignis**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

