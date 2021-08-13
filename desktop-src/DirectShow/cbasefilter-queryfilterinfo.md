---
description: Die QueryFilterInfo-Methode ruft Informationen zum Filter ab. Diese Methode implementiert die IBaseFilter::QueryFilterInfo-Methode.
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: CBaseFilter.QueryFilterInfo-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31eb135a29a6e8e1c4f27c28d24b5cbf50eba3bb87b99ba9a1d3a5868c2fbc49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341740"
---
# <a name="cbasefilterqueryfilterinfo-method"></a>CBaseFilter.QueryFilterInfo-Methode

Die `QueryFilterInfo` -Methode ruft Informationen zum Filter ab. Diese Methode implementiert die [**IBaseFilter::QueryFilterInfo-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo)

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pinfo* 
</dt> <dd>

Zeiger auf eine [**FILTER \_ INFO-Struktur.**](/windows/win32/api/strmif/ns-strmif-filter_info)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E \_ POINTER zurück.

## <a name="remarks"></a>Hinweise

Diese Methode kopiert den Namen des Filters aus der [**CBaseFilter::m pName-Membervariablen \_**](cbasefilter-m-pname.md) in den **member des filtersName** der FILTER \_ INFO-Struktur. Wenn **\_ "m pName"** **NULL ist,** legt die Methode **"namename"** auf "L' \\ 0" fest.

Die -Methode legt das **pGraph-Member** der FILTER INFO-Struktur auf die \_ [**CBaseFilter::m \_ pGraph-Membervariable**](cbasefilter-m-pgraph.md) fest und erhöht die Verweisanzahl. Der Aufrufer muss die Schnittstelle frei geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




