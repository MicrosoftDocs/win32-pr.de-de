---
description: 'Die setsyncsource-Methode legt eine Referenzuhr für das-Objekt fest. Diese Methode implementiert die imediafilter:: setsyncsource-Methode.'
ms.assetid: ae296741-e3da-4376-a88a-8470f0a414ed
title: Cbasemediafilter. setsyncsource-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01597228ddbadec6c1b0db481719fb690584b7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356342"
---
# <a name="cbasemediafiltersetsyncsource-method"></a>Cbasemediafilter. setsyncsource-Methode

Die- `SetSyncSource` Methode legt eine Referenzuhr für das-Objekt fest. Diese Methode implementiert die [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pclock* 
</dt> <dd>

Ein Zeiger auf die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle der Uhr oder **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasemediafilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




