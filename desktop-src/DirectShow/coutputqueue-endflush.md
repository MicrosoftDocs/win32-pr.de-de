---
description: Die endflush-Methode beendet einen Löschvorgang.
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Coutputqueue. endflush-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e18afec866176147c5c75a57fca522c4ebc5fcf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359663"
---
# <a name="coutputqueueendflush-method"></a>Coutputqueue. endflush-Methode

Die- `EndFlush` Methode beendet einen Löschvorgang.

## <a name="syntax"></a>Syntax


```C++
void EndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn das Objekt einen Thread verwendet, wartet diese Methode auf das [**coutputqueue:: m \_ evflushcomplete**](coutputqueue-m-evflushcomplete.md) -Ereignis. Der Thread signalisiert dieses Ereignis, nachdem alle ausstehenden Stichproben freigegeben wurden. Wenn das Objekt keinen Thread verwendet, ruft diese Methode die [**coutputqueue:: freesamples**](coutputqueue-freesamples.md) -Methode auf. Dann ruft die- `EndFlush` Methode die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode für die Eingabe-PIN auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




