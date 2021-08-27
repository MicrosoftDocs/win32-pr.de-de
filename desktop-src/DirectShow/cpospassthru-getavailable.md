---
description: 'CPosPassThru.GetAvailable-Methode: Die GetAvailable-Methode ruft den Zeitbereich ab, in dem Suchfunktionen effizient sind. Diese Methode implementiert die IMediaSeeking::GetAvailable-Methode.'
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: CPosPassThru.GetAvailable-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1db45b20264f192b2ade7d8863f9da86d5fc02159567611eff86e9cdfff1b10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084250"
---
# <a name="cpospassthrugetavailable-method"></a>CPosPassThru.GetAvailable-Methode

Die `GetAvailable` -Methode ruft den Zeitbereich ab, in dem Suchfunktionen effizient sind. Diese Methode implementiert die [**IMediaSeeking::GetAvailable-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pEarliest* 
</dt> <dd>

Zeiger auf eine Variable, die die früheste Zeit für effiziente Suche erhält.

</dd> <dt>

*pLatest* 
</dt> <dd>

Zeiger auf eine Variable, die die letzte Zeit für effiziente Suche empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




