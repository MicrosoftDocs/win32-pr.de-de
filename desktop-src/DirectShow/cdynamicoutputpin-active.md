---
description: 'CDynamicOutputPin.Active-Methode: Die Active-Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist.'
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: CDynamicOutputPin.Active-Methode (Amfilter.h)
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
ms.openlocfilehash: 12e59b434562e84c42228c16282620efe10866ea9dad85a4d62beb46f5a59e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688980"
---
# <a name="cdynamicoutputpinactive-method"></a>CDynamicOutputPin.Active-Methode

Die `Active` -Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                            | Beschreibung                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                                                                                             |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Fehler. [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) wurde nicht aufgerufen.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBaseOutputPin::Active-Methode.**](cbaseoutputpin-active.md) Das Ereignis [**CDynamicOutputPin::m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) wird zurückgesetzt. Wenn der besitzende Filter **setConfigInfo** nicht aufgerufen hat, gibt diese Methode E \_ FAIL zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




