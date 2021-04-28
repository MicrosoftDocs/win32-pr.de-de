---
description: 'CABEvent.CABEvent-Konstruktor : Konstruktormethode.'
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: CABEvent.CABEvent-Konstruktor (Wxutil.h)
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
ms.openlocfilehash: cdd37ba72d9467c16d46b2aec3ec40c206466eaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096531"
---
# <a name="cameventcamevent-constructor"></a>CABEvent.CABEvent-Konstruktor

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

Ein boolescher Wert, der angibt, ob es sich bei dem Objekt um ein Ereignis mit manueller oder automatischer Zurücksetzung handelt. True gibt an, dass das Objekt ein Ereignis für die manuelle Zurücksetzung ist. Andernfalls handelt es sich um ein Ereignis für die automatische Zurücksetzung.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Wenn der Konstruktor fehlschlägt, empfängt dieser Parameter einen Fehlercode. In diesem Fall befindet sich das Objekt nicht in einem gültigen Zustand.

Aus Gründen der Abwärtskompatibilität mit früheren Versionen von strmbase.lib wird dieser Parameter standardmäßig auf **NULL** gesetzt. Die Übergabe eines Werts ungleich **NULL** wird jedoch bevorzugt, damit der Aufrufer den Status des Objekts überprüfen kann.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Ereignis beginnt in einem nicht signalisierten Zustand.

Bei einem Ereignis für die automatische Zurücksetzung setzt die [**RESETEvent::Wait-Methode**](camevent-wait.md) das Ereignis auf nicht signalisiert zurück, wenn die Methode zurückgegeben wird. Bei einem Ereignis für die manuelle Zurücksetzung bleibt das Ereignis signalisiert, bis Sie die [**METHODE RESETEvent::Reset**](camevent-reset.md) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WEBCAMEvent-Klasse**](camevent.md)
</dt> </dl>

 

 




