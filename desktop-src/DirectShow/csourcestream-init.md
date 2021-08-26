---
description: Die Init-Methode initialisiert den Streamingthread.
ms.assetid: c746e595-de97-478c-8b22-5c4dd5594a8f
title: CSourceStream.Init-Methode (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e656ba46b25045406fb794653078b72e2c47155635cf24ae4a99b35238aa51df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871314"
---
# <a name="csourcestreaminit-method"></a>CSourceStream.Init-Methode

Die `Init` -Methode initialisiert den Streamingthread.

## <a name="syntax"></a>Syntax


```C++
HRESULT Init();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Methode muss die erste Threadanforderung sein, die an die [**CSourceStream::ThreadProc-Methode**](csourcestream-threadproc.md) gesendet wird. Die [**CSourceStream::Active-Methode**](csourcestream-active.md) ruft diese Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




