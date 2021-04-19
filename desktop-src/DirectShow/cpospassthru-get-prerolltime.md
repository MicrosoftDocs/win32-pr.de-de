---
description: 'Die get \_ prerolltime-Methode ruft die Menge der Daten ab, die vor der Startposition in die Warteschlange eingereiht werden. Diese Methode implementiert die Methode imediaposition:: get \_ prerolltime.'
ms.assetid: 37c12798-eb0d-4859-8b2e-52d6ae147863
title: CPosPassThru.get_PrerollTime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55cb2cc37a18c9ea00b4eb7115590f472b8d467e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370079"
---
# <a name="cpospassthruget_prerolltime-method"></a>Cpospassthru. get \_ prerolltime-Methode

Die- `get_PrerollTime` Methode ruft die Menge der Daten ab, die vor der Startposition in die Warteschlange eingereiht werden. Diese Methode implementiert die Methode [**imediaposition:: get \_ prerolltime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) .

## <a name="syntax"></a>Syntax


```C++
HRESULT get_PrerollTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plltime* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die vorab-Zeit (in Sekunden) empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




