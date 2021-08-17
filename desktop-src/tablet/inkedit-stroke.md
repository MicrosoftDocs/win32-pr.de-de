---
description: Tritt ein, wenn der Benutzer ein neues IInkStrokeDisp-Objekt für ein IInkTablet-Objekt zeichnet.
ms.assetid: fac5104d-d0da-40b1-a4a6-00a34718d09f
title: InkEdit.Stroke-Ereignis (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1114f26fa17690b1651321ef15ad11d8ec4d55f11f8e7e1754d6d694fdceda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717895"
---
# <a name="inkeditstroke-event"></a>InkEdit.Stroke-Ereignis

Tritt ein, wenn der Benutzer ein neues [**IInkStrokeDisp-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) für ein [**IInkTablet-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) zeichnet.

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

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

</dd> <dt>

*Strich* \[ In\]
</dt> <dd>

Das gesammelte [**IInkStrokeDisp-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE,** um die Auflistung des [**IInkStrokeDisp-Objekts**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) abzubrechen. **VARIANT \_ FALSE,** um das **IInkStrokeDisp-Objekt** zu erfassen und den **Strich** gleichmäßig fortzusetzen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in der **\_ IInkEditEvents-Schnittstelle** definiert. Die **\_ IInkEditEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IeeStroke.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (erfordert auch inked \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

