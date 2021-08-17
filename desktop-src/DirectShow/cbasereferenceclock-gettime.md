---
description: Die GetTime-Methode ruft die aktuelle Verweiszeit ab. Diese Methode implementiert die IReferenceClock::GetTime-Methode.
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: CBaseReferenceClock.GetTime-Methode (Refclock.h)
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
ms.openlocfilehash: 5a1ffd021ac917a7aa1e12f3d3dc9c4a62ea1f883f126bca1d9c1300d335bdae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954979"
---
# <a name="cbasereferenceclockgettime-method"></a>CBaseReferenceClock.GetTime-Methode

Die `GetTime` -Methode ruft die aktuelle Verweiszeit ab. Diese Methode implementiert die [**IReferenceClock::GetTime-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTime* 
</dt> <dd>

Zeiger auf eine Variable, die die aktuelle Zeit in Einheiten von 100 Nanosekunden empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                               | Beschreibung                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> |  NULL-Zeigerargument.<br/>                       |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Die zurückgegebene Zeit ist mit dem vorherigen Wert identisch.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>                                         |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**CBaseReferenceClock::GetPrivateTime-Methode**](cbasereferenceclock-getprivatetime.md) auf, um die Echtzeituhrzeit zu bestimmen. Wenn die Uhrzeit strikt größer als der vorherige Wert ist, verwendet die Uhrzeit und `GetTime` gibt S \_ OK zurück. Andernfalls `GetTime` verwendet den vorherigen Wert und gibt S \_ FALSE zurück. Daher kann die interne Uhr für einen kurzen Zeitraum rückwärts ausgeführt werden, ohne dass die Verweiszeit rückwärts ausgeführt wird. Stattdessen wird die Referenzzeit bei demselben Wert "stocken", bis die interne Uhr aufholt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Refclock.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseReferenceClock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




