---
description: 'CSourceSeeking.GetAvailable-Methode: Die GetAvailable-Methode ruft den Zeitbereich ab, in dem Suchfunktionen effizient sind. Diese Methode implementiert die IMediaSeeking::GetAvailable-Methode.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: CSourceSeeking.GetAvailable-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24bc667eec4f5b21c90415e4721aa8cf0a0ad4c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085238"
---
# <a name="csourceseekinggetavailable-method"></a>CSourceSeeking.GetAvailable-Methode

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

Zeiger auf eine Variable, die die früheste Zeit für effiziente Suche empfängt. Die Variable ist auf 0 (null) festgelegt.

</dd> <dt>

*pLatest* 
</dt> <dd>

Zeiger auf eine Variable, die die letzte Zeit für effiziente Suche empfängt. Die Variable wird auf den Wert der [**CSourceSeeking::m \_ rtDuration-Membervariablen**](csourceseeking-m-rtduration.md) festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




