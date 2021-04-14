---
description: Tritt auf, wenn ein oder mehrere Striche aus der inkstrokes-Auflistung gelöscht werden.
ms.assetid: 58d78143-c733-45dc-ae5f-fe13136010db
title: Inkstrokes. StrokesRemoved-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86448f9676e07a11effe683ecd883874791ff3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349889"
---
# <a name="inkstrokesstrokesremoved-event"></a>Inkstrokes. StrokesRemoved-Ereignis

Tritt auf, wenn ein oder mehrere Striche aus der [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung gelöscht werden.

## <a name="syntax"></a>Syntax


```C++
void StrokesRemoved(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StrokeIds* \[ in\]
</dt> <dd>

Das ganzzahlige Array von bezeichgern für jedes [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt, das bei Auftreten dieses Ereignisses gelöscht wird.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in der \_ iinkevents-Schnittstelle definiert. Die \_ iinkevents-Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID" \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Inkstrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Methode "inkstrokes" der Methode entfernen \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)
</dt> <dt>

[**InkDisp-Klasse**](inkdisp-class.md)
</dt> </dl>

 

