---
description: Tritt auf, wenn die Cursor-QuickInfo die digitalisierende Tablet-Oberfläche kontaktiert
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: InkPicture. currsordown-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15724f0a71e801393ca8e93100ba2105da9ff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529897"
---
# <a name="inkpicturecursordown-event"></a>InkPicture. currsordown-Ereignis

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

Diese Ereignis Methoden werden in den Schnittstellen **\_ iinkcollectorevents**, **\_ iinkoverlayevents** und **\_ iinkpictureevents** definiert. Die **\_ iinkcollector Events**-, **\_ iinkoverlayevents**-und **\_ iinkpictureevents** -Schnittstelle implementieren die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ icecursordown.

Verwenden Sie dieses Ereignis sorgfältig, da dies eine negative Auswirkung auf die Handschrift Leistung haben kann, wenn zu viel Code in den Ereignis Handlern ausgeführt wird. Um die Echtzeitleistung zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown**](inkpicture-mousedown.md) -und [**MouseUp**](inkpicture-mouseup.md) -Ereignis Handlern aus, oder zeigen Sie ihn an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Currsorbuttonup-Ereignis**](inkpicture-cursorbuttonup.md)
</dt> <dt>

[**Currsorbuttondown-Ereignis**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

