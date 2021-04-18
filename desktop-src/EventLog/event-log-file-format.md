---
description: Jedes Ereignisprotokoll enthält einen Header (dargestellt durch die elf- \_ logfile- \_ Header Struktur) mit fester Größe, gefolgt von einer Variablen Anzahl von Ereignisdaten Sätzen (dargestellt durch EventLogRecord-Strukturen) und einem dateiendedatensatz (dargestellt durch die elf \_ EOF- \_ Daten Satzstruktur).
ms.assetid: 2b62b807-4ffd-4a8f-afe4-34e109d01856
title: Format der Ereignisprotokoll Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4ba5c8bc0114e319107272e706801544e3effa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528751"
---
# <a name="event-log-file-format"></a>Format der Ereignisprotokoll Datei

Jedes Ereignisprotokoll enthält einen Header (dargestellt durch die [**elf- \_ logfile- \_ Header**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) Struktur) mit fester Größe, gefolgt von einer Variablen Anzahl von Ereignisdaten Sätzen (dargestellt durch [**EventLogRecord**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) -Strukturen) und einem dateiendedatensatz (dargestellt durch die [**elf \_ EOF- \_ Daten Satz**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) Struktur).

Die **elf \_ logfile- \_ Header** Struktur und die **elf \_ EOF- \_ Daten Satz** Struktur werden im Ereignisprotokoll geschrieben, wenn das Ereignisprotokoll erstellt wird, und werden jedes Mal aktualisiert, wenn ein Ereignis in das Protokoll geschrieben wird.

Wenn eine Anwendung die [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) -Funktion aufruft, um einen Eintrag in das Ereignisprotokoll zu schreiben, übergibt das System die Parameter an den Ereignis Protokollierungs Dienst. Der Ereignis Protokollierungs Dienst verwendet die Informationen, um eine **EventLogRecord** -Struktur in das Ereignisprotokoll zu schreiben. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Schreiben einer Protokolldatei](images/evreport.png)

Die Ereignisdaten Sätze sind auf eine der folgenden Arten organisiert:

-   Nicht Umbrüchen. Der älteste Datensatz liegt unmittelbar nach dem Ereignisprotokoll Header und neuen Datensätzen nach dem letzten hinzugefügten Datensatz (vor dem **elf- \_ EOF- \_ Datensatz**). Das folgende Beispiel zeigt die nicht Wrapping Methode:

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    Eine nicht-Wrapping kann auftreten, wenn das Ereignisprotokoll erstellt wird oder wenn das Ereignisprotokoll gelöscht wird. Das Ereignisprotokoll wird weiterhin nicht umwickelt, bis die Größenbeschränkung für das Ereignisprotokoll erreicht ist. Die Größe des Ereignis Protokolls wird entweder durch den **MaxSize** -Konfigurations Wert oder durch die Menge der Systemressourcen beschränkt.

    Wenn das Größenlimit für das Ereignisprotokoll erreicht wird, beginnt es möglicherweise mit der Umbrüchen. Das umwickeln wird durch den Wert für die **Beibehaltungs** Konfiguration gesteuert. Weitere Informationen zu den Konfigurations Werten für das Ereignisprotokoll finden Sie unter [EventLog Key](eventlog-key.md).

-   Wrapping. Die Datensätze werden als Zirkel Puffer organisiert. Wenn neue Datensätze hinzugefügt werden, werden die ältesten Datensätze ersetzt. Der Speicherort der ältesten und neuesten Datensätze variiert. Das folgende Beispiel zeigt die Wrapping Methode.

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

    Zwischen dem **elf \_ EOF- \_ Datensatz** und dem ältesten Datensatz liegt ein Speicherplatz vor, da das System eine ganzzahlige Anzahl von Datensätzen löscht, um Speicherplatz für den neuesten Datensatz freizugeben. Wenn der neueste Datensatz z. b. 100 Byte lang ist und die zwei ältesten Datensätze 75 Bytes lang sind, entfernt das System die beiden ältesten Datensätze. Die zusätzlichen 50 Bytes werden später verwendet, wenn neue Datensätze geschrieben werden.

    Eine Ereignisprotokoll Datei hat eine festgelegte Größe, und wenn die Datensätze in der Datei wrappen, wird der Datensatz am Ende der Datei in der Regel in zwei Datensätze aufgeteilt. Wenn die Position für den nächsten Schreibvorgang z. b. 100 Bytes vom Dateiende und die Größe des Datensatzes 300 Bytes beträgt, werden die ersten 100 Bytes am Ende der Datei geschrieben, und die nächsten 200 Bytes werden am Anfang der Datei unmittelbar nach dem **elf- \_ logfile- \_ Header** geschrieben. Wenn der verfügbare Speicherplatz am Ende der Datei kleiner ist als der festgelegte Teil von **EventLogRecord** (0x38 Bytes), werden alle neuen Datensätze am Anfang der Datei unmittelbar nach dem **elf- \_ logfile- \_ Header** geschrieben. Die nicht verwendeten Bytes am Ende der Datei werden mit dem Muster 0x00000027 aufgefüllt.

Weitere Informationen und ein Codebeispiel finden Sie unter [Berichterstellung für ein Ereignis](reporting-an-event.md).

 

 
