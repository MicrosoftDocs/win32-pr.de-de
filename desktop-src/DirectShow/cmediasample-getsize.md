---
description: Die GetSize-Methode ruft die Größe des Puffers ab. Diese Methode implementiert die IMediaSample::GetSize-Methode.
ms.assetid: 14562ef4-f554-4d5a-83d3-1a29abae08a4
title: CMediaSample.GetSize-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3559f972f35a01738c60f32414ab0b42a079032ac5bc6b3ab0e5b7212900d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156751"
---
# <a name="cmediasamplegetsize-method"></a>CMediaSample.GetSize-Methode

Die `GetSize` -Methode ruft die Größe des Puffers ab. Diese Methode implementiert die [**IMediaSample::GetSize-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize)

## <a name="syntax"></a>Syntax


```C++
LONG GetSize();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die Größe des Puffers in Bytes zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




