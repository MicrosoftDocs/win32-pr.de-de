---
description: Konstruktormethode.
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Camevent. camevent-Konstruktor (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a01d9d1f592675f58d19e81b800c966dddaca1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369934"
---
# <a name="cameventcamevent-constructor"></a>Camevent. camevent-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nicht verfügbar* 
</dt> <dd>

Boolescher Wert, der angibt, ob das Objekt ein manuelles Zurücksetzungs Ereignis oder ein Auto-Reset-Ereignis ist. **True** gibt an, dass das Objekt ein manuelles Zurücksetzungs Ereignis ist. Andernfalls handelt es sich um ein Auto Reset-Ereignis.

</dd> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen **HRESULT** -Wert. Wenn der Konstruktor ausfällt, empfängt dieser Parameter einen Fehlercode. Wenn dies auftritt, befindet sich das Objekt nicht in einem gültigen Zustand.

Aus Gründen der Abwärtskompatibilität mit früheren Versionen von "straumbase. lib" ist dieser Parameter standardmäßig **null**. Die Übergabe eines Werts ungleich **null** wird jedoch bevorzugt, sodass der Aufrufer den Status des Objekts überprüfen kann.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Ereignis beginnt in einem nicht signalisierten Zustand.

Bei einem Auto-Reset-Ereignis setzt die Methode " [**camevent:: Wait**](camevent-wait.md) " das Ereignis auf "nicht signalisiert" zurück, wenn die Methode zurückgegeben wird. Bei einem manuellen Reset-Ereignis bleibt das Ereignis signalisiert, bis Sie die Methode " [**camevent:: Reset**](camevent-reset.md) " aufgerufen haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camevent-Klasse**](camevent.md)
</dt> </dl>

 

 




