---
description: Tritt ein, wenn auf das InkEdit-Steuerelement doppelklickt wird.
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: InkEdit.DblClick-Ereignis (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2f1cf2a7b7d7d699af5cd8a148e5c54a2879ad5eb879bd34af7531025748e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032088"
---
# <a name="inkeditdblclick-event"></a>InkEdit.DblClick-Ereignis

Tritt ein, wenn auf das [InkEdit-Steuerelement](inkedit-control-reference.md) doppelklickt wird.

## <a name="syntax"></a>Syntax


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE,** um das Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um zwischen den linken, rechten und mittleren Maustasten zu unterscheiden, verwenden Sie die [**MouseDown-**](inkedit-mousedown.md) und [**MouseUp-Ereignisse.**](inkedit-mouseup.md) Wenn das [**Click-Ereignis**](inkedit-click.md) Code enthält, wird das **DblClick-Ereignis** nie ausgelöst.

 

Diese Ereignismethode wird in der **\_ IInkEditEvents-Schnittstelle** definiert. Die **\_ IInkEditEvents-Schnittstelle** implementiert die IDispatch-Schnittstelle mit dem Bezeichner **DISPID \_ IeeDblClick**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (erfordert auch inked \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> </dl>

 

 




