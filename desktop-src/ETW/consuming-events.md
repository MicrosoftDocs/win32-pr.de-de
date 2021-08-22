---
description: Ereignisverfolgungs-Consumers können Ereignisse von einem oder mehr Anbietern verarbeiten.
ms.assetid: 039a9f66-228e-4258-9967-2b2cd7d31091
title: Verwenden von Ereignissen (Ereignisablaufverfolgung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b42761bed132c5416a99888e067a1192571a527f39506e8964d5ea0209135b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119269360"
---
# <a name="consuming-events-event-tracing"></a>Verwenden von Ereignissen (Ereignisablaufverfolgung)

Ereignisverfolgungs-Consumers können Ereignisse von einem oder mehr Anbietern verarbeiten. Benutzer können Ereignisse aus einer Protokolldatei oder in Echtzeit verarbeiten. Sie können Ereignisse nur dann in Echtzeit nutzen, wenn der Controller den Echtzeitprotokollierungsmodus für die Sitzung angibt. Aus Leistungsgründen wird die Echtzeitverarbeitung vor der Verwendung Windows Vista nicht empfohlen.

Um die Ablaufverfolgungssitzung anzugeben, aus der Sie Ereignisse verarbeiten möchten, verwenden Sie die [**EVENT \_ TRACE \_ LOGFILE-Struktur.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) Sie müssen eine Kopie dieser Struktur für jede Protokolldatei oder Echtzeitsitzung initialisieren, die Sie verarbeiten möchten.

Um Ereignisse aus einer Protokolldatei zu nutzen, legen Sie das **LogFileName-Mitglied** auf den Namen der Protokolldatei fest. Um Ereignisse aus einer Echtzeitsitzung zu nutzen, legen Sie das **LoggerName-Mitglied** auf den Sitzungsnamen fest. Sie verwenden diese Struktur auch, um den [*BufferCallback-Rückruf*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) und den [*EventCallback-*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback) oder [**EventRecordCallback-Rückruf**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback) anzugeben, der zum Verarbeiten der Ereignisse verwendet wird.

-   [**EventRecordCallback :**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)Empfängt und verarbeitet alle Ereignisse (einschließlich des Headerereignisses) aus einer oder mehrere Protokolldateien und einer Echtzeitsitzung. Sie implementieren diesen Rückruf, wenn Sie die Ereignisdaten mithilfe der Hilfsfunktionen für Ablaufverfolgungsdaten analysieren oder Metadaten zum Ereignis abrufen möchten.
-   [*EventCallback :*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)Empfängt und verarbeitet alle Ereignisse (einschließlich des Headerereignisses) aus einer oder mehr Protokolldateien und einer Echtzeitsitzung.
-   [*BufferCallback:*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka)Empfängt und verarbeitet Zusammenfassende Informationen zum aktuellen Puffer, z. B. verlorene Ereignisse. ETW ruft den Rückruf nach der Bereitstellung aller Ereignisse im Puffer an den Consumer auf. Der Consumer kann diesen Rückruf auch zum Abbrechen der Ereignisverarbeitung verwenden. Wenn Sie Jedoch Ereignisse in Echtzeit verwenden, übermittelt ETW Ereignisse, bis der Controller die Sitzung beendet.

Nachdem Sie eine oder mehrere Ablaufverfolgungssitzungen definiert haben, rufen Sie die [**OpenTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-opentracea) für jede Ablaufverfolgungssitzung auf, die Sie verarbeiten möchten. Sie können Ereignisse aus einer oder mehrere Protokolldateien verarbeiten, jedoch nur aus einer Echtzeitsitzung. Anschließend übergeben Sie die Liste der Ablaufverfolgungssitzungshandles, die **OpenTrace zurückgibt,** an die [**ProcessTrace-Funktion.**](/windows/win32/api/evntrace/nf-evntrace-processtrace) Die **ProcessTrace-Funktion** kombiniert die Ereignisse, sortiert sie in chronologischer Reihenfolge und übergibt sie dann nach und nach an die Rückrufe. Die Ereignisse können mithilfe der Parameter *StartTime* und *EndTime* so gefiltert werden, dass sie nur die ereignisse enthalten, die in einen bestimmten Zeitrahmen fallen. Die **ProcessTrace-Funktion** blockiert den Thread, bis ihr Consumer alle Ereignisse in den Ablaufverfolgungssitzungen verarbeitet, [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) **FALSE** zurückgibt oder [**CloseTrace aufruft.**](/windows/win32/api/evntrace/nf-evntrace-closetrace)

**Vor der Windows Vista:** Sie können [**CloseTrace erst aufrufen,**](/windows/win32/api/evntrace/nf-evntrace-closetrace) nachdem [**ProcessTrace zurückgegeben**](/windows/win32/api/evntrace/nf-evntrace-processtrace) wurde.

Ein Beispiel, das zeigt, wie Ereignisse verwendet werden, die mit einem Manifest, MOF oder TMF-Dateien veröffentlicht wurden, finden Sie unter [Retrieving Event Data Using TDH](retrieving-event-data-using-tdh.md)(Abrufen von Ereignisdaten mit TDH). Beachten Sie, dass Sie ab Windows Vista die TDH-Funktionen (Trace Data Helper) verwenden sollten, um Ereignisse zu verarbeiten.

Ein Beispiel, das zeigt, wie Mit MOF veröffentlichte Ereignisse verwendet werden, finden Sie unter Retrieving Event Data Using MOF (Abrufen [von Ereignisdaten mit MOF).](retrieving-event-data-using-mof.md)

 

 
