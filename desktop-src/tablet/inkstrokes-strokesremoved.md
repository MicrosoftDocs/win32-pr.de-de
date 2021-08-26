---
description: Tritt ein, wenn ein oder mehrere Striche aus der Sammlung InkStrokes gelöscht werden.
ms.assetid: 58d78143-c733-45dc-ae5f-fe13136010db
title: InkStrokes.StrokesRemoved-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69a5c4f7d53f88c50efd77e537cfa311f08ab168abdb4a05392286fb6c0b6b4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934860"
---
# <a name="inkstrokesstrokesremoved-event"></a>InkStrokes.StrokesRemoved-Ereignis

Tritt ein, wenn ein oder mehrere Striche aus der [Sammlung InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) gelöscht werden.

## <a name="syntax"></a>Syntax


```C++
void StrokesRemoved(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StrokeIds* \[ In\]
</dt> <dd>

Das ganzzahlige Array von Bezeichnern für jedes [**IInkStrokeDisp-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) das gelöscht wird, wenn dieses Ereignis eintritt.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in der \_ IInkEvents-Schnittstelle definiert. Die \_ IInkEvents-Schnittstelle implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ SEStrokesRemoved.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkStrokes-Sammlung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Remove Method \[ InkStrokes Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)
</dt> <dt>

[**InkDisp-Klasse**](inkdisp-class.md)
</dt> </dl>

 

