---
description: 'CSourceSeeking.GetAvailable-Methode: Die GetAvailable-Methode ruft den Zeitbereich ab, in dem suchvorgang effizient ist. Diese Methode implementiert die IMediaSeeking::GetAvailable-Methode.'
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
ms.openlocfilehash: ae42efad42bf9f1e0df0f4f791f1e4e8abb76fe8252818a8e35eda4dd6e6b87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953749"
---
# <a name="csourceseekinggetavailable-method"></a>CSourceSeeking.GetAvailable-Methode

Die `GetAvailable` -Methode ruft den Zeitbereich ab, in dem suchweise effizient ist. Diese Methode implementiert die [**IMediaSeeking::GetAvailable-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable)

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

Zeiger auf eine Variable, die die früheste Zeit für eine effiziente Suche empfängt. Die Variable ist auf 0 (null) festgelegt.

</dd> <dt>

*pLatest* 
</dt> <dd>

Zeiger auf eine Variable, die die letzte Zeit für effiziente Such suchte. Die Variable wird auf den Wert der [**CSourceSeeking::m \_ rtDuration-Membervariable**](csourceseeking-m-rtduration.md) festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




