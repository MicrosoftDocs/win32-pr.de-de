---
description: Die deliverendofstream-Methode übergibt eine streamingbenachrichtigung an die verbundene Eingabe-PIN.
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: Cbaseoutputpin. deliverendof-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 334101c9b61631a35c5da91bd398cb7742d39235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373954"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a>Cbaseoutputpin. deliverendosstream-Methode

Die- `DeliverEndOfStream` Methode übermittelt eine Streamende-Benachrichtigung an die verbundene Eingabe-PIN.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DeliverEndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                           | Beschreibung                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die PIN ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode für die Eingabe-PIN auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




