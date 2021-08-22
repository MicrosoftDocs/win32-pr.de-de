---
description: Die OnThreadStartPlay-Methode wird am Anfang der CSourceStream::D oBufferProcessingLoop-Methode aufgerufen.
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: CSourceStream.OnThreadStartPlay-Methode (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcd1ccf4b507570e0219854d1f5044c1d95db63d04b8f9049449beb3941e95d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073174"
---
# <a name="csourcestreamonthreadstartplay-method"></a>CSourceStream.OnThreadStartPlay-Methode

Die `OnThreadStartPlay` -Methode wird am Anfang der [**CSourceStream::D oBufferProcessingLoop-Methode**](csourcestream-dobufferprocessingloop.md) aufgerufen.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode führt in der Basisklasse nichts aus. sie ist für die abgeleitete Klasse zum Überschreiben verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




