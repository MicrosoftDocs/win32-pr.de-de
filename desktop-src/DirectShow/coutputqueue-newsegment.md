---
description: Die NewSegment-Methode übergibt ein neues Segment an den Eingabepin.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: COutputQueue.NewSegment-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4057cafa3962c85fbca9342debbf7bb0e92355fc083e693889df298e53509259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768140"
---
# <a name="coutputqueuenewsegment-method"></a>COutputQueue.NewSegment-Methode

Die `NewSegment` -Methode übergibt ein neues Segment an den Eingabepin.

## <a name="syntax"></a>Syntax


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tStart* 
</dt> <dd>

Startmedienposition des Segments in Einheiten von 100 Nanosekunden.

</dd> <dt>

*tStop* 
</dt> <dd>

Endmedienposition des Segments in Einheiten von 100 Nanosekunden.

</dd> <dt>

*dRate* 
</dt> <dd>

Rate, mit der dieses Segment verarbeitet werden soll, als Prozentsatz der ursprünglichen Rate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Wenn das Objekt einen Thread verwendet, werden die folgenden Elemente in der Reihenfolge in die Warteschlange gestellt:

-   Eine NEUE \_ SEGMENT-Steuermeldung.
-   Die Segmentdaten.

Die Meldung NEW SEGMENT benachrichtigt den Thread, dass das nächste Element in der Warteschlange \_ Segmentdaten enthält. Die Segmentdaten werden in einer -Struktur gebündelt, die wie folgt deklariert wird:


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



Der Thread ruft die [**IPin::NewSegment-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) auf dem Eingabepin unter Verwendung der in der -Struktur angegebenen Daten auf.

Wenn das Objekt keinen Thread verwendet, ruft es die [**COutputQueue::SendAnyway-Methode**](coutputqueue-sendanyway.md) auf, um ausstehende Stichproben zu übermitteln. Anschließend ruft sie **IPin::NewSegment auf** dem Eingabepin auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




