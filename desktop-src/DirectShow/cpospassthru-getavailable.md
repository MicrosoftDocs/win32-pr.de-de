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
ms.openlocfilehash: 0d56827a68f4c287e5808f0d8f64b8142c31b1f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095288"
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

Zeiger auf eine Variable, die die früheste Zeit für effiziente Suche empfängt.

</dd> <dt>

*pLatest* 
</dt> <dd>

Zeiger auf eine Variable, die die letzte Zeit für effiziente Suche empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




