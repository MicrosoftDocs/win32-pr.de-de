---
description: Die CSourceStream-Klasse stellt einen Ausgabepin für die CSource-Filterklasse bereit.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: CSourceStream-Klasse (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f7563cabff97626ac45a150e9a763033d9ce9261e5ae528e83d174e35d4f0d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428784"
---
# <a name="csourcestream-class"></a>CSourceStream-Klasse

![csourcestream-Klassenhierarchie](images/source02.png)

Die **CSourceStream-Klasse** stellt einen Ausgabepin für die [**CSource-Filterklasse**](csource.md) bereit.

Informationen zur Verwendung dieser Klasse finden Sie unter [**CSource**](csource.md). Diese Klasse erbt die [**KLASSE CABThread,**](camthread.md) die einen Arbeitsthread zum Streamen von Daten vom Pin bereitstellt. Die **CSourceStream-Klasse** implementiert die folgenden Hilfsmethoden, um Anforderungen an den Thread zu senden:

-   [**CSourceStream::Exit**](csourcestream-exit.md)
-   [**CSourceStream::Init**](csourcestream-init.md)
-   [**CSourceStream::P ause**](csourcestream-pause.md)
-   [**CSourceStream::Run**](csourcestream-run.md)
-   [**CSourceStream::Stop**](csourcestream-stop.md)

Die erste Anforderung an den Thread muss [**Init lauten.**](csourcestream-init.md) Die [**Exit-Anforderung**](csourcestream-exit.md) beendet den Thread. In der Praxis ist es nicht erforderlich, eine dieser Methoden direkt aufzurufen, da sie von den [**Methoden CSourceStream::Active**](csourcestream-active.md) und [**CSourceStream::Inactive**](csourcestream-inactive.md) des Pins bei Bedarf aufgerufen werden.

Die -Klasse stellt auch mehrere Handlermethoden bereit:

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

Diese tun nichts in der Basisklasse, aber die abgeleitete Klasse kann sie überschreiben.



| Geschützte Membervariablen                                             | Beschreibung                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ pFilter**](csourcestream-m-pfilter.md)                          | Zeiger auf den Filter, der diese Stecknadel enthält.                                                                                     |
| Geschützte Methoden                                                      | Beschreibung                                                                                                                       |
| [**OnThreadCreate**](csourcestream-onthreadcreate.md)                 | Wird aufgerufen, wenn der Streamingthread initialisiert wird. Virtuellen.                                                                         |
| [**OnThreadDestroy**](csourcestream-onthreaddestroy.md)               | Wird aufgerufen, wenn der Streamingthread gerade beendet wird. Virtuellen.                                                                       |
| [**OnThreadStartPlay**](csourcestream-onthreadstartplay.md)           | Wird am Anfang der [**CSourceStream::D oBufferProcessingLoop-Methode**](csourcestream-dobufferprocessingloop.md) aufgerufen. Virtuellen. |
| [**Aktiv**](csourcestream-active.md)                                 | Benachrichtigt den Pin, dass der Filter jetzt aktiv ist.                                                                                   |
| [**Inaktiv**](csourcestream-inactive.md)                             | Benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.                                                                             |
| [**GetRequest**](csourcestream-getrequest.md)                         | Wartet auf die nächste Threadanforderung.                                                                                                |
| [**CheckRequest**](csourcestream-checkrequest.md)                     | Überprüft, ob eine Threadanforderung ohne Blockierung vorhanden ist.                                                                            |
| [**ThreadProc**](csourcestream-threadproc.md)                         | Threadprozedur. Virtuellen.                                                                                                        |
| [**DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) | Generiert Mediendaten und übermittelt sie an den nachgeschalteten Eingabepin. Virtuellen.                                                        |
| [**CheckMediaType**](csourcestream-checkmediatype.md)                 | Bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert. Virtuellen.                                                                     |
| [**GetMediaType**](csourcestream-getmediatype.md)                     | Ruft einen bevorzugten Medientyp ab. Virtuellen.                                                                                        |
| Öffentliche Methoden                                                         | Beschreibung                                                                                                                       |
| [**CSourceStream**](csourcestream-csourcestream.md)                   | Konstruktormethode.                                                                                                               |
| [**~ CSourceStream**](csourcestream--csourcestream.md)                | Destruktormethode. Virtuellen.                                                                                                       |
| [**Init**](csourcestream-init.md)                                     | Initialisiert den Streamingthread.                                                                                                 |
| [**Beenden**](csourcestream-exit.md)                                     | Signalisiert dem Streamingthread das Beenden.                                                                                             |
| [**Ausführung**](csourcestream-run.md)                                       | Signalisiert dem Streamingthread die Ausführung.                                                                                              |
| [**Anhalten**](csourcestream-pause.md)                                   | Signalisiert dem Streamingthread, dass er aktiv wird.                                                                                    |
| [**Beenden**](csourcestream-stop.md)                                     | Signalisiert dem Streamingthread das Beenden.                                                                                             |
| Reine virtuelle Methoden                                                   | Beschreibung                                                                                                                       |
| [**FillBuffer**](csourcestream-fillbuffer.md)                         | Füllt ein Medienbeispiel mit Daten.                                                                                                   |
| IPin-Methoden                                                           | Beschreibung                                                                                                                       |
| [**QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | Ruft einen Bezeichner für den Stecknadel ab.                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Schreiben von Quellfiltern](writing-source-filters.md)
</dt> </dl>

 

 




