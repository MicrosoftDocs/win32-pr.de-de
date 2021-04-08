---
description: Tritt auf, wenn der Benutzer ein neues IInkStrokeDisp-Objekt für ein beliebiges iinktablet-Objekt zeichnet.
ms.assetid: fac5104d-d0da-40b1-a4a6-00a34718d09f
title: InkEdit. Stroke-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d21abde9deb565f207a44ddd44b51681f1bfa6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759540"
---
# <a name="inkeditstroke-event"></a>InkEdit. Stroke-Ereignis

Tritt auf, wenn der Benutzer ein neues [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt für ein beliebiges [**iinktablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekt zeichnet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ in\]
</dt> <dd>

Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt.

</dd> <dt>

*Strich* \[ in\]
</dt> <dd>

Das gesammelte [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt.

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

**Variant \_ TRUE** , wenn die Auflistung des [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekts abgebrochen werden soll. **Variant \_ FALSE** , um das **IInkStrokeDisp** -Objekt zu erfassen und auch mit dem **Strich** fortzufahren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert. Die **\_ iinkeditevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ieestroke.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

