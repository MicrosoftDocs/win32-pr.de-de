---
description: 'TAREvent.CAMEvent-Konstruktor: Konstruktormethode.'
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: TAREvent.CAMEvent-Konstruktor (Wxutil.h)
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
ms.openlocfilehash: f0fd5895ada4bbbd1bf4ad24710f7782fdfb9c932f2d9446ff0d992335437da9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540554"
---
# <a name="cameventcamevent-constructor"></a>KONSTRUKTOR "TAREVENT.TAREVENT"

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

*fManualReset* 
</dt> <dd>

Ein boolescher Wert, der angibt, ob es sich bei dem Objekt um ein Ereignis mit manueller oder automatischer Zurücksetzung handelt. True **gibt an,** dass das -Objekt ein Ereignis mit manueller Zurücksetzung ist. Andernfalls handelt es sich um ein Ereignis zur automatischen Zurücksetzung.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Wenn der Konstruktor fehlschlägt, empfängt dieser Parameter einen Fehlercode. In diesem Fall befindet sich das Objekt nicht in einem gültigen Zustand.

Aus Gründen der Abwärtskompatibilität mit früheren Versionen von strmbase.lib wird dieser Parameter standardmäßig auf **NULL festgelegt.** Die Übergabe eines Werts, der nicht **NULL** ist, wird jedoch bevorzugt, damit der Aufrufer den Status des Objekts überprüfen kann.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das Ereignis beginnt in einem nicht signalisiertem Zustand.

Bei einem Ereignis für die automatische Zurücksetzung setzt die [**METHODE WEBCAMEvent::Wait**](camevent-wait.md) das Ereignis auf nicht signalisiert zurück, wenn die Methode zurückgegeben wird. Bei einem Manuellzurücksetzungsereignis bleibt das Ereignis signalisiert, bis Sie die [**METHODECAMEvent::Reset**](camevent-reset.md) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CAMEvent-Klasse**](camevent.md)
</dt> </dl>

 

 




