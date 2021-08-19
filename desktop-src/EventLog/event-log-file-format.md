---
description: Jedes Ereignisprotokoll enthält einen Header (dargestellt durch die ELF \_ LOGFILE \_ HEADER-Struktur), der eine feste Größe aufweist, gefolgt von einer variablen Anzahl von Ereignisdatensätzen (dargestellt durch EVENTLOGRECORD-Strukturen) und einem Dateiendedatensatz (dargestellt durch die ELF \_ EOF \_ RECORD-Struktur).
ms.assetid: 2b62b807-4ffd-4a8f-afe4-34e109d01856
title: Ereignisprotokolldateiformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ed6df35ac1fcd641a9a895b2c32eb34d6a4c1cb472ab03f16417f55900c767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814292"
---
# <a name="event-log-file-format"></a>Ereignisprotokolldateiformat

Jedes Ereignisprotokoll enthält einen Header (dargestellt durch die [**ELF \_ LOGFILE \_ HEADER-Struktur),**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) der eine feste Größe aufweist, gefolgt von einer variablen Anzahl von Ereignisdatensätzen (dargestellt durch [**EVENTLOGRECORD-Strukturen)**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) und einem Dateiendedatensatz (dargestellt durch die [**ELF \_ EOF \_ RECORD-Struktur).**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85))

Die **ELF \_ LOGFILE \_ HEADER-Struktur** und die **ELF \_ EOF \_ RECORD-Struktur** werden beim Erstellen des Ereignisprotokolls in das Ereignisprotokoll geschrieben und jedes Mal aktualisiert, wenn ein Ereignis in das Protokoll geschrieben wird.

Wenn eine Anwendung die [**ReportEvent-Funktion**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) aufruft, um einen Eintrag in das Ereignisprotokoll zu schreiben, übergibt das System die Parameter an den Ereignisprotokollierungsdienst. Der Ereignisprotokollierungsdienst verwendet die Informationen, um eine **EVENTLOGRECORD-Struktur** in das Ereignisprotokoll zu schreiben. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Schreiben einer Protokolldatei](images/evreport.png)

Die Ereignisdatensätze sind auf eine der folgenden Arten organisiert:

-   Nicht umschließend. Der älteste Datensatz befindet sich unmittelbar nach dem Ereignisprotokollheader, und neue Datensätze werden nach dem letzten hinzugefügten Datensatz (vor **ELF \_ EOF \_ RECORD)** hinzugefügt. Das folgende Beispiel zeigt die nicht umschließende Methode:

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    Ein Nichtumbruch kann auftreten, wenn das Ereignisprotokoll erstellt oder das Ereignisprotokoll gelöscht wird. Das Ereignisprotokoll ist weiterhin nicht umschließend, bis das Größenlimit des Ereignisprotokolls erreicht ist. Die Größe des Ereignisprotokolls wird entweder durch den **MaxSize-Konfigurationswert** oder die Menge der Systemressourcen beschränkt.

    Wenn das Größenlimit des Ereignisprotokolls erreicht ist, beginnt es möglicherweise mit dem Umschließen. Das Umschließen wird durch den Konfigurationswert **Aufbewahrung** gesteuert. Weitere Informationen zu den Konfigurationswerten des Ereignisprotokolls finden Sie unter [Eventlog Key](eventlog-key.md).

-   Verpackung. Die Datensätze sind als Kreispuffer organisiert. Wenn neue Datensätze hinzugefügt werden, werden die ältesten Datensätze ersetzt. Der Speicherort der ältesten und neuesten Datensätze variiert. Das folgende Beispiel zeigt die Wrapping-Methode.

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    EVENT RECORD 301         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 400         (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    Wasted space
    EVENT RECORD 102         (EVENTLOGRECORD)
    EVENT RECORD 103         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 299         (EVENTLOGRECORD)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    ```

    Im Beispiel ist der älteste Datensatz nicht mehr 1, sondern 102, da der Speicherplatz für die Datensätze 1 bis 101 überschrieben wurde.

    Zwischen **ELF \_ EOF \_ RECORD** und dem ältesten Datensatz ist etwas Platz vorhanden, da das System eine ganzzahlige Anzahl von Datensätzen löscht, um Speicherplatz für den neuesten Datensatz frei zu machen. Wenn der neueste Datensatz beispielsweise 100 Bytes lang ist und die beiden ältesten Datensätze 75 Bytes lang sind, entfernt das System die beiden ältesten Datensätze. Die zusätzlichen 50 Bytes werden später verwendet, wenn neue Datensätze geschrieben werden.

    Eine Ereignisprotokolldatei hat eine feste Größe, und wenn die Datensätze in der Datei umbrochen werden, wird der Datensatz am Ende der Datei in der Regel in zwei Datensätze aufgeteilt. Wenn die Position für den nächsten Schreibvorgang beispielsweise 100 Bytes vom Ende der Datei entfernt ist und die Größe des Datensatzes 300 Bytes beträgt, werden die ersten 100 Bytes am Ende der Datei geschrieben, und die nächsten 200 Bytes werden am Anfang der Datei unmittelbar nach dem **ELF \_ LOGFILE \_ HEADER** geschrieben. Wenn der verfügbare Speicherplatz am Ende der Datei kleiner als der feste Teil von **EVENTLOGRECORD** (0x38 Bytes) ist, wird der gesamte neue Datensatz unmittelbar nach dem **ELF LOGFILE \_ \_ HEADER** am Anfang der Datei geschrieben. Die nicht verwendeten Bytes am Ende der Datei werden mit dem Muster 0x00000027 gefüllt.

Weitere Informationen und ein Codebeispiel finden Sie unter [Reporting an Event](reporting-an-event.md).

 

 
