---
description: Die newsegment-Methode übergibt ein neues Segment an die eingabepin.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: Coutputqueue. newsegment-Methode (outputq. h)
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
ms.openlocfilehash: e682211a98f4409fda35687160c88b121fa93898
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373828"
---
# <a name="coutputqueuenewsegment-method"></a>Coutputqueue. newsegment-Methode

Die- `NewSegment` Methode übergibt ein neues Segment an die eingabepin.

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

*tSTART* 
</dt> <dd>

Start Medien Position des Segments in 100-Nanosecond-Einheiten.

</dd> <dt>

*tstopps* 
</dt> <dd>

Die endmedien Position des Segments in 100-Nanosecond-Einheiten.

</dd> <dt>

*drate* 
</dt> <dd>

Die Rate, mit der dieses Segment verarbeitet werden soll, als Prozentsatz der ursprünglichen Rate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn das Objekt einen Thread verwendet, werden die folgenden Elemente in der angegebenen Reihenfolge in die Warteschlange eingereiht:

-   Eine neue \_ Segment Steuerungs Meldung.
-   Die Segment Daten.

Die neue \_ Segment Nachricht benachrichtigt den Thread, dass das nächste Element in der Warteschlange Segment Daten enthält. Die Segment Daten werden in einer Struktur gebündelt, die wie folgt deklariert wird:


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



Der Thread ruft die [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) -Methode für die Eingabe-PIN auf, wobei die in der Struktur angegebenen Daten verwendet werden.

Wenn das Objekt keinen Thread verwendet, ruft es die [**coutputqueue:: sendanyway**](coutputqueue-sendanyway.md) -Methode auf, um alle ausstehenden Beispiele bereitzustellen. Anschließend wird **IPin:: newsegment** für die Eingabe-PIN aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




