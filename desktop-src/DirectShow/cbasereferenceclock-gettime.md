---
description: 'Die getTime-Methode ruft die aktuelle Verweis Zeit ab. Diese Methode implementiert die IReferenceClock:: getTime-Methode.'
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: Cbasereferenceclock. getTime-Methode (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a91f0015756d2ccfb545c4039d67434eb6d3c403
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361456"
---
# <a name="cbasereferenceclockgettime-method"></a>Cbasereferenceclock. getTime-Methode

Die- `GetTime` Methode ruft die aktuelle Verweis Zeit ab. Diese Methode implementiert die [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PTIME* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die aktuelle Uhrzeit in 100-Nanosecond-Einheiten empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                               | Beschreibung                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeigerargument.<br/>                       |
| <dl> <dt>**S \_ false**</dt> </dl>   | Die zurückgegebene Uhrzeit ist mit dem vorherigen Wert identisch.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>                                         |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**cbasereferenceclock:: getprivatetime**](cbasereferenceclock-getprivatetime.md) -Methode auf, um die tatsächliche Uhrzeit zu bestimmen. Wenn die Uhrzeitangabe streng größer als der vorherige Wert ist, `GetTime` verwendet die Uhrzeitangabe und gibt S \_ OK zurück. Andernfalls wird `GetTime` der vorherige Wert von verwendet und S \_ false zurückgegeben. Daher kann die interne Uhr für einen kurzen Zeitraum rückwärts ausgeführt werden, ohne dass die Bezugszeit rückwärts ausgeführt wird. Stattdessen wird die Verweis Zeit mit demselben Wert "Stall", bis die interne Uhr abfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ref. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasereferenceclock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




