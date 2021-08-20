---
description: Die CSource-Klasse ist eine Basisklasse zum Implementieren von Quellfiltern. Ein von CSource abgeleiteter Filter enthält mindestens einen Ausgabepin, der von der CSourceStream-Klasse abgeleitet wurde. Jeder Ausgabepin erstellt einen Arbeitsthread, der Medienbeispiele nachgeschaltet pusht.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: CSource-Klasse (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6708ce38c826aae9ccb40d077972d267a20d5e22b4f67157000c4a62e92afa1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687514"
---
# <a name="csource-class"></a>CSource-Klasse

![csource-Klassenhierarchie](images/source01.png)

Die **CSource-Klasse** ist eine Basisklasse zum Implementieren von Quellfiltern. Ein von **CSource** abgeleiteter Filter enthält mindestens einen Ausgabepin, der von der [**CSourceStream-Klasse**](csourcestream.md) abgeleitet wurde. Jeder Ausgabepin erstellt einen Arbeitsthread, der Medienbeispiele nachgeschaltet pusht.

> [!Note]  
> Die **CSource-Klasse** wurde entwickelt, um das Pushmodell für den Datenfluss zu unterstützen. Diese Klasse wird nicht zum Erstellen von Dateilesefiltern empfohlen. Dateileser sollten das Pullmodell über die [**IAsyncReader-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) unterstützen. Weitere Informationen finden Sie unter [Data Flow for Filter Developers](data-flow-for-filter-developers.md).

 



| Geschützte Membervariablen                     | Beschreibung                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**m \_ iPins**](csource-m-ipins.md)            | Anzahl der Pins im Filter.                                |
| [**m \_ paStreams**](csource-m-pastreams.md)    | Array von Stecknadeln.                                               |
| [**m \_ cStateLock**](csource-m-cstatelock.md)  | Kritisches Abschnittsobjekt, das den Filterzustand schützt.      |
| Öffentliche Methoden                                 | Beschreibung                                                  |
| [**CSource**](csource-csource.md)             | Konstruktormethode.                                          |
| [**~CSource**](csource--csource.md)           | Destruktormethode.                                           |
| [**GetPinCount**](csource-getpincount.md)     | Ruft die Anzahl der Pins im Filter ab.                  |
| [**GetPin**](csource-getpin.md)               | Ruft eine Stecknadel ab.                                             |
| [**pStateLock**](csource--pstatelock.md)      | Ruft einen Zeiger auf das kritische Abschnittsobjekt des Filters ab. |
| [**AddPin**](csource-addpin.md)               | Fügt dem Filter einen neuen Ausgabepin hinzu.                         |
| [**RemovePin**](csource-removepin.md)         | Entfernt einen angegebenen Pin aus dem Filter.                     |
| [**FindPinNumber**](csource-findpinnumber.md) | Ruft die Nummer eines angegebenen Pins für den Filter ab.       |
| IBaseFilter-Methoden                            | Beschreibung                                                  |
| [**FindPin**](csource-findpin.md)             | Ruft die Stecknadel mit dem angegebenen Bezeichner ab.             |



 

## <a name="remarks"></a>Hinweise

Gehen Sie wie folgt vor, um einen Ausgabepin zu implementieren:

-   Leiten Sie eine Klasse von [**CSourceStream**](csourcestream.md)ab.
-   Überschreiben Sie die [**CSourceStream::GetMediaType-Methode**](csourcestream-getmediatype.md) und möglicherweise die [**CSourceStream::CheckMediaType-Methode,**](csourcestream-checkmediatype.md) die Medientypen für den Pin überprüft.
-   Implementieren Sie die [**CBaseOutputPin::D ecideBufferSize-Methode,**](cbaseoutputpin-decidebuffersize.md) die die Pufferanforderungen des Pins zurückgibt.
-   Implementieren Sie die [**CSourceStream::FillBuffer-Methode,**](csourcestream-fillbuffer.md) die einen Medienbeispielpuffer mit Daten füllt.

Gehen Sie wie folgt vor, um den Filter zu implementieren:

-   Leiten Sie eine Klasse von **CSource** ab.
-   Erstellen Sie im Konstruktor mindestens einen Ausgabepin, der von [**CSourceStream**](csourcestream.md)abgeleitet wurde. Die Pins fügen sich automatisch dem Filter in ihren Konstruktormethoden hinzu und entfernen sich selbst in ihren Destruktormethoden.

Um den Filterzustand zwischen mehreren Threads zu synchronisieren, rufen Sie die [**CSource::p StateLock-Methode**](csource--pstatelock.md) auf. Diese Methode gibt einen Zeiger auf den kritischen Filterzustandsabschnitt zurück. Verwenden Sie die [**CAutoLock-Klasse,**](cautolock.md) um den kritischen Abschnitt zu speichern. Über eine Pin können Sie wie folgt über die [**CBasePin::m \_ pFilter-Membervariable**](cbasepin-m-pfilter.md) des Pins auf **pStateLock** zugreifen:


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schreiben von Quellfiltern](writing-source-filters.md)
</dt> </dl>

 

 




