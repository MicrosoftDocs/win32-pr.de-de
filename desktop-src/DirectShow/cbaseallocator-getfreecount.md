---
description: Die GetFreeCount-Methode ruft die Anzahl der Medienbeispiele ab, die nicht verwendet werden.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: CBaseAllocator.GetFreeCount-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c4552829482a604b368a6710c62d0fc0b26a94aa3bb33b67ef386f2785d6c90e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057510"
---
# <a name="cbaseallocatorgetfreecount-method"></a>CBaseAllocator.GetFreeCount-Methode

Die `GetFreeCount` -Methode ruft die Anzahl der Medienbeispiele ab, die nicht verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plBuffersFree* 
</dt> <dd>

Adresse einer Variablen, die die Anzahl der nicht verwendeten Stichproben empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode implementiert die [**IMemAllocatorCallbackTemp::GetFreeCount-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) Die Zuweisung macht die IMemAllocatorCallbackTemp-Schnittstelle nur verfügbar, wenn das *Flag fEnableReleaseCallback* im CBaseAllocator-Konstruktor auf **TRUE** festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




