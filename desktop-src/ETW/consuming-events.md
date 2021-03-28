---
description: Ereignisablaufverfolgungs-Consumer können Ereignisse von einem oder mehreren Anbietern verarbeiten.
ms.assetid: 039a9f66-228e-4258-9967-2b2cd7d31091
title: Verarbeiten von Ereignissen (Ereignis Ablauf Verfolgung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad8234cc66d07b5a52c10ab39c7d7b3c8aa029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980856"
---
# <a name="consuming-events-event-tracing"></a>Verarbeiten von Ereignissen (Ereignis Ablauf Verfolgung)

Ereignisablaufverfolgungs-Consumer können Ereignisse von einem oder mehreren Anbietern verarbeiten. Consumer können Ereignisse aus einer Protokolldatei oder in Echtzeit verarbeiten. Ereignisse können nur in Echtzeit verwendet werden, wenn der Controller den Echt Zeit Protokollierungs Modus für die Sitzung angibt. Aus Leistungsgründen wird die Echtzeitverarbeitung vor Windows Vista nicht empfohlen.

Wenn Sie die Ablauf Verfolgungs Sitzung angeben möchten, von der Ereignisse verarbeitet werden sollen, verwenden Sie die [**\_ \_ logfile**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) -Struktur der Ereignis Ablauf Verfolgung. Sie müssen eine Kopie dieser Struktur für jede Protokolldatei oder Echt Zeit Sitzung initialisieren, die Sie verarbeiten möchten.

Wenn Sie Ereignisse aus einer Protokolldatei nutzen möchten, legen Sie den **LogFileName** -Member auf den Namen der Protokolldatei fest. Um Ereignisse aus der Echt Zeit Sitzung zu nutzen, legen Sie den **Loggername** -Member auf den Sitzungs Namen fest. Außerdem verwenden Sie diese Struktur, um den [*buffercallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) -Rückruf und den [*EventCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback) -oder [**eventrecordcallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback) -Rückruf anzugeben, der zum Verarbeiten der Ereignisse verwendet wird.

-   [**Eventrecordcallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)– empfängt und verarbeitet alle Ereignisse (einschließlich des Header Ereignisses) aus einer oder mehreren Protokolldateien und einer echt Zeit Sitzung. Sie implementieren diesen Rückruf, wenn Sie die Daten der Ablauf Verfolgungs Daten verwenden, um die Ereignisdaten zu analysieren, oder Sie Metadaten zu dem Ereignis abrufen möchten.
-   [*EventCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)– empfängt und verarbeitet alle Ereignisse (einschließlich des Header Ereignisses) aus einer oder mehreren Protokolldateien und einer echt Zeit Sitzung.
-   [*Buffercallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka)– empfängt und verarbeitet Zusammenfassungs Informationen zum aktuellen Puffer, z. b. verlorene Ereignisse. Etw Ruft den Rückruf auf, nachdem alle Ereignisse im Puffer an den Consumer über gestellt wurden. Der Consumer kann diesen Rückruf auch zum Abbrechen der Ereignisverarbeitung verwenden. Wenn Sie jedoch Ereignisse in Echtzeit verarbeiten, liefert ETW Ereignisse, bis der Controller die Sitzung beendet.

Nachdem eine oder mehrere Ablauf Verfolgungs Sitzungen definiert wurden, wird die [**opentrace**](/windows/win32/api/evntrace/nf-evntrace-opentracea) -Funktion für jede Ablauf Verfolgungs Sitzung aufgerufen, die Sie verarbeiten möchten. Sie können Ereignisse aus einer oder mehreren Protokolldateien, aber nur aus einer echt Zeit Sitzung verarbeiten. Anschließend übergeben Sie die Liste der Ablauf Verfolgungs Sitzungs Handles, die **opentrace** an die [**processtrace**](/windows/win32/api/evntrace/nf-evntrace-processtrace) -Funktion zurückgibt. Die **processtrace** -Funktion kombiniert die Ereignisse, sortiert sie in chronologischer Reihenfolge und übergibt Sie dann nacheinander an die Rückrufe. Die Ereignisse können so gefiltert werden, dass Sie nur diejenigen enthalten, die in einem bestimmten Zeitrahmen unter Verwendung der Parameter *StartTime* und *EndTime* liegen. Die **processtrace** -Funktion blockiert den Thread, bis der Consumer alle Ereignisse in den Ablauf Verfolgungs Sitzungen verarbeitet, der [*buffercallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) **false** zurückgibt oder [**closetrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace)aufgerufen wird.

**Vor Windows Vista:** [**Closetrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace) kann nur aufgerufen werden, nachdem [**processtrace**](/windows/win32/api/evntrace/nf-evntrace-processtrace) zurückgegeben wurde.

Ein Beispiel, das zeigt, wie Ereignisse verwendet werden, die mithilfe von Manifest-, MOF-oder TMF-Dateien veröffentlicht werden, finden Sie unter [Abrufen von Ereignisdaten mit TDH](retrieving-event-data-using-tdh.md). Beachten Sie, dass Sie ab Windows Vista die TDH-Funktionen (Trace Data Helper) verwenden sollten, um Ereignisse zu verarbeiten.

Ein Beispiel für die Verwendung von Ereignissen, die mit MOF veröffentlicht werden, finden Sie unter [Abrufen von Ereignisdaten mithilfe von MOF](retrieving-event-data-using-mof.md).

 

 
