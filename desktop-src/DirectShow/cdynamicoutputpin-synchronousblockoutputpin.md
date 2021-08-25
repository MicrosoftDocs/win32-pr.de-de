---
description: Die SynchronousBlockOutputPin-Methode blockiert den Pin. gibt erst dann zurück, wenn die Stecknadel blockiert ist.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: CDynamicOutputPin.SynchronousBlockOutputPin-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8613a27d8af2dc2b69a93a1f324db17b054cf2dd312fdb0c9d6cd63e6c89ca8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916310"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a>CDynamicOutputPin.SynchronousBlockOutputPin-Methode

Die `SynchronousBlockOutputPin` -Methode blockiert die Stecknadel; gibt erst dann zurück, wenn die Stecknadel blockiert ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                                                    | Beschreibung                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Erfolg.<br/>                                      |
| <dl> <dt>**VFW \_ \_ E-PIN \_ BEREITS \_ BLOCKIERT**</dt> </dl>                   | Das Anheften ist bereits in einem anderen Thread blockiert.<br/>     |
| <dl> <dt>**VFW \_ \_ E-PIN \_ FÜR \_ DIESEN \_ \_ \_ THREAD BEREITS BLOCKIERT**</dt> </dl> | Pin ist im aufrufenden Thread bereits blockiert.<br/> |



 

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode nicht aus dem Streamingthread auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




