---
description: Die SetSyncSource-Methode legt eine Referenzuhr für den Filter fest. Diese Methode implementiert die IMediaFilter::SetSyncSource-Methode.
ms.assetid: 298039fc-dd38-4063-8752-2669b134b8ef
title: CBaseFilter.SetSyncSource-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95e1f1b3578fa88d4616fc9e0b7d0af9fe89ab80c2e93ee32eef305b93d45478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659586"
---
# <a name="cbasefiltersetsyncsource-method"></a>CBaseFilter.SetSyncSource-Methode

Die **SetSyncSource-Methode** legt eine Referenzuhr für den Filter fest. Diese Methode implementiert die [**IMediaFilter::SetSyncSource-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pclock* 
</dt> <dd>

Zeiger auf die [**IReferenceClock-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) der Uhr oder **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




