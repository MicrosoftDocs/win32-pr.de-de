---
description: Die csourcestream-Klasse stellt eine Ausgabe-PIN für die CSource-Filterklasse bereit.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: Csourcestream-Klasse (Quelle. h)
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
ms.openlocfilehash: 36b9085df8c15e765c751be8b5fcdfd4f4a02140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368644"
---
# <a name="csourcestream-class"></a>Csourcestream-Klasse

![csourcestream-Klassenhierarchie](images/source02.png)

Die **csourcestream** -Klasse stellt eine Ausgabe-PIN für die [**CSource**](csource.md) -Filterklasse bereit.

Weitere Informationen zur Verwendung dieser Klasse finden Sie unter [**CSource**](csource.md). Diese Klasse erbt die Klasse " [**camthread**](camthread.md) ", die einen Arbeits Thread zum Streamen von Daten aus der PIN bereitstellt. Die **csourcestream** -Klasse implementiert die folgenden Hilfsmethoden, um Anforderungen an den Thread zu senden:

-   [**Csourcestream:: Exit**](csourcestream-exit.md)
-   [**Csourcestream:: init**](csourcestream-init.md)
-   [**Csourcestream::P ause**](csourcestream-pause.md)
-   [**Csourcestream:: Run**](csourcestream-run.md)
-   [**Csourcestream:: Beendigung**](csourcestream-stop.md)

Die erste Anforderung an den Thread muss [**Init**](csourcestream-init.md)sein. Die [**Beendigungs Anforderung beendet den Thread**](csourcestream-exit.md) . In der Praxis ist es nicht notwendig, eine dieser Methoden direkt aufzurufen, da die [**csourcestream:: Active**](csourcestream-active.md) -und [**csourcestream:: ininaktiven**](csourcestream-inactive.md) -Methoden der PIN diese bei Bedarf aufrufen.

Die Klasse stellt auch mehrere "Handlermethoden" bereit:

-   [**Csourcestream:: onthreadcreate**](csourcestream-onthreadcreate.md)
-   [**Csourcestream:: onthreaddestroy**](csourcestream-onthreaddestroy.md)
-   [**Csourcestream:: onthreadstartplay**](csourcestream-onthreadstartplay.md)

Diese Aktionen werden in der Basisklasse nicht durchgesetzt, aber die abgeleitete Klasse kann Sie überschreiben.



| Geschützte Member-Variablen                                             | BESCHREIBUNG                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ pFilter**](csourcestream-m-pfilter.md)                          | Zeiger auf den Filter, der diese PIN enthält.                                                                                     |
| Geschützte Methoden                                                      | BESCHREIBUNG                                                                                                                       |
| [**Onthreadcreate**](csourcestream-onthreadcreate.md)                 | Wird aufgerufen, wenn der streamingindthread initialisiert wird. Virtu.                                                                         |
| [**Onthreaddestroy**](csourcestream-onthreaddestroy.md)               | Wird aufgerufen, wenn der streamingthread gerade beendet wird. Virtu.                                                                       |
| [**Onthreadstartplay**](csourcestream-onthreadstartplay.md)           | Wird am Anfang der [**csourcestream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) -Methode aufgerufen. Virtu. |
| [**Aktiv**](csourcestream-active.md)                                 | Benachrichtigt die PIN, dass der Filter jetzt aktiv ist.                                                                                   |
| [**Inaktiv**](csourcestream-inactive.md)                             | Benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.                                                                             |
| [**GetRequest**](csourcestream-getrequest.md)                         | Wartet auf die nächste Thread Anforderung.                                                                                                |
| [**Check Request**](csourcestream-checkrequest.md)                     | Überprüft, ob eine Thread Anforderung vorhanden ist, ohne zu blockieren.                                                                            |
| [**ThreadProc**](csourcestream-threadproc.md)                         | Thread Prozedur. Virtu.                                                                                                        |
| [**Dobufferprocessingloop**](csourcestream-dobufferprocessingloop.md) | Generiert Mediendaten und übergibt sie an die downstreameingabepin. Virtu.                                                        |
| [**Checkmediatype**](csourcestream-checkmediatype.md)                 | Bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert. Virtu.                                                                     |
| [**Getmediatype**](csourcestream-getmediatype.md)                     | Ruft einen bevorzugten Medientyp ab. Virtu.                                                                                        |
| Öffentliche Methoden                                                         | BESCHREIBUNG                                                                                                                       |
| [**Csourcestream**](csourcestream-csourcestream.md)                   | Konstruktormethode.                                                                                                               |
| [**~ Csourcestream**](csourcestream--csourcestream.md)                | Dekonstruktormethode. Virtu.                                                                                                       |
| [**Init**](csourcestream-init.md)                                     | Initialisiert den streamingthread.                                                                                                 |
| [**Beenden**](csourcestream-exit.md)                                     | Signalisiert dem streamingthread, den Vorgang zu beenden.                                                                                             |
| [**Ausführen**](csourcestream-run.md)                                       | Signalisiert, dass der streamingthread ausgeführt werden soll.                                                                                              |
| [**Anhalten**](csourcestream-pause.md)                                   | Signalisiert, dass der streamingingthread aktiv wird.                                                                                    |
| [**Stop**](csourcestream-stop.md)                                     | Signalisiert, dass der Streaminginhalt beendet werden soll.                                                                                             |
| Reine virtuelle Methoden                                                   | BESCHREIBUNG                                                                                                                       |
| [**FillBuffer**](csourcestream-fillbuffer.md)                         | Füllt ein Medien Beispiel mit Daten.                                                                                                   |
| IPin-Methoden                                                           | BESCHREIBUNG                                                                                                                       |
| [**QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | Ruft einen Bezeichner für die PIN ab.                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schreiben von Quell Filtern](writing-source-filters.md)
</dt> </dl>

 

 




