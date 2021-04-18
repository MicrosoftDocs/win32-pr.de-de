---
description: Die getfrecount-Methode ruft die Anzahl von Medien Beispielen ab, die nicht verwendet werden.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: Cbasezucator. getfrecount-Methode (amfilter. h)
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
ms.openlocfilehash: a0538229053b5d47ca1bdc8f30b38a0937e36cb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371278"
---
# <a name="cbaseallocatorgetfreecount-method"></a>Cbasezucator. getfrecount-Methode

Die- `GetFreeCount` Methode ruft die Anzahl von Medien Beispielen ab, die nicht verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plbuffersfree* 
</dt> <dd>

Adresse einer Variablen, die die Anzahl von Stichproben empfängt, die nicht verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode implementiert die [**imemzuzuchanorcallbacktemp:: getfrecount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) -Methode. Die Zuweisung wird von der Zuweisung nicht verfügbar gemacht, es sei denn, das *fenablereleasecallback* -Flag ist im cbasezucator-Konstruktor auf **true** festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




