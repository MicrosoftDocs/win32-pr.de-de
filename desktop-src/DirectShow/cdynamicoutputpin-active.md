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
ms.openlocfilehash: 1d9544c0fd125146b10f008565fcfbe330d18de1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099328"
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

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                            | Beschreibung                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                                                                                             |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Fehler. [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) wurde nicht aufgerufen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBaseOutputPin::Active-Methode.**](cbaseoutputpin-active.md) Das Ereignis [**CDynamicOutputPin::m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) wird zurückgesetzt. Wenn der besitzende Filter **SetConfigInfo** nicht aufgerufen hat, gibt diese Methode E \_ FAIL zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




