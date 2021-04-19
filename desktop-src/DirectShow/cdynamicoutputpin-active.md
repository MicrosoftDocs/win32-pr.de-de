---
description: Die aktive Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist.
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Cdynamicoutputpin. Active-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f1765d0aa524c0dafd03a3fe4133af71e32fa70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362162"
---
# <a name="cdynamicoutputpinactive-method"></a>Cdynamicoutputpin. Active-Methode

Die- `Active` Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                            | Beschreibung                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                                                                                             |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Fehler. [**Cdynamicoutputpin:: setconfiginfo**](cdynamicoutputpin-setconfiginfo.md) wurde nicht aufgerufen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbaseoutputpin:: Active**](cbaseoutputpin-active.md) -Methode. Das Ereignis [**cdynamicoutputpin:: m \_ hstopevent**](cdynamicoutputpin-m-hstopevent.md) wird zurückgesetzt. Wenn der besitzende Filter nicht **setconfiginfo** aufgerufen hat, gibt diese Methode E \_ Fail zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




