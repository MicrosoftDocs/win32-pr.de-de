---
description: 'CMemAllocator.Alloc-Methode: Die Alloc-Methode belegt Speicher für die Puffer.'
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: CMemAllocator.Alloc-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d7de755aa3b8007a122e43529d16f5e39ca0cb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099038"
---
# <a name="cmemallocatoralloc-method"></a>CMemAllocator.Alloc-Methode

Die `Alloc` -Methode belegt Speicher für die Puffer.

## <a name="syntax"></a>Syntax


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                       | Beschreibung                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | Nicht genügend Arbeitsspeicher.<br/>              |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | Pufferanforderungen wurden nicht festgelegt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird von der [**CBaseAllocator::Commit-Methode**](cbaseallocator-commit.md) aufgerufen. Es ordnet einen zusammenhängenden Speicherblock zu, der für die Pufferanforderungen ausreicht, die in der [**CMemAllocator::SetProperties-Methode**](cmemallocator-setproperties.md) angegeben sind.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMemAllocator-Klasse**](cmemallocator.md)
</dt> </dl>

 

 




