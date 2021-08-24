---
description: Die NT-Kernelprotokollierungssitzung ist eine Ereignisablaufverfolgungssitzung, die einen vordefinierten Satz von Kernelereignissen auf zeichnet.
ms.assetid: 3c4258d8-8073-4cc5-a29d-ce485a3fdc14
title: Konfigurieren und Starten der NT-Kernelprotokollierungssitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41398c9caac3ecd090af68a18bfb148095632d96b8c75eaaee7f04a551360fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901220"
---
# <a name="configuring-and-starting-the-nt-kernel-logger-session"></a>Konfigurieren und Starten der NT-Kernelprotokollierungssitzung

Die NT-Kernelprotokollierungssitzung ist eine Ereignisablaufverfolgungssitzung, die einen vordefinierten Satz von Kernelereignissen auf zeichnet. Sie rufen die [**EnableTrace-Funktion nicht auf,**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) um die Kernelanbieter zu aktivieren. Stattdessen verwenden Sie den **EnableFlags-Member** der [**EVENT TRACE \_ \_ PROPERTIES-Struktur,**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) um die Kernelereignisse anzugeben, die Sie empfangen möchten. Die [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) verwendet die Aktivierungsflags, die Sie angeben, um die Kernelanbieter zu aktivieren.

Es gibt nur eine NT-Kernelprotokollierungssitzung. Wenn die Sitzung bereits verwendet wird, gibt die [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) ERROR \_ ALREADY EXISTS \_ zurück.

Weitere Informationen zum Starten einer Ereignisablaufverfolgungssitzung finden Sie unter Konfigurieren und [Starten einer Ereignisablaufverfolgungssitzung.](configuring-and-starting-an-event-tracing-session.md)

Weitere Informationen zum Starten einer privaten Protokollierungssitzung finden Sie unter Konfigurieren und [Starten einer privaten Protokollierungssitzung.](configuring-and-starting-a-private-logger-session.md)

Weitere Informationen zum Starten einer globalen Protokollierungssitzung finden Sie unter Konfigurieren und [Starten der globalen Protokollierungssitzung.](configuring-and-starting-the-global-logger-session.md)

Weitere Informationen zum Starten einer AutoLogger-Sitzung finden Sie unter Konfigurieren und [Starten einer AutoLogger-Sitzung.](configuring-and-starting-an-autologger-session.md)

Das folgende Beispiel zeigt, wie Sie eine NT-Kernelprotokollierungssitzung konfigurieren und starten, die TCP/IP-Kernelereignisse des Netzwerks sammelt und in eine zirkuläre 5-MB-Datei schreibt.


```C++
#define INITGUID  // Include this #define to use SystemTraceControlGuid in Evntrace.h.

#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <strsafe.h>
#include <wmistr.h>
#include <evntrace.h>

#define LOGFILE_PATH L"<FULLPATHTOTHELOGFILE.etl>"

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE SessionHandle = 0;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name,
    // which get appended to the end of the session properties structure.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(LOGFILE_PATH) + sizeof(KERNEL_LOGGER_NAME);
    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    // Set the session properties. You only append the log file name
    // to the properties structure; the StartTrace function appends
    // the session name for you.

    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->Wnode.ClientContext = 1; //QPC clock resolution
    pSessionProperties->Wnode.Guid = SystemTraceControlGuid; 
    pSessionProperties->EnableFlags = EVENT_TRACE_FLAG_NETWORK_TCPIP;
    pSessionProperties->LogFileMode = EVENT_TRACE_FILE_MODE_CIRCULAR;
    pSessionProperties->MaximumFileSize = 5;  // 5 MB
    pSessionProperties->LoggerNameOffset = sizeof(EVENT_TRACE_PROPERTIES);
    pSessionProperties->LogFileNameOffset = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(KERNEL_LOGGER_NAME); 
    StringCbCopy((LPWSTR)((char*)pSessionProperties + pSessionProperties->LogFileNameOffset), sizeof(LOGFILE_PATH), LOGFILE_PATH);

    // Create the trace session.

    status = StartTrace((PTRACEHANDLE)&SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_ALREADY_EXISTS == status)
        {
            wprintf(L"The NT Kernel Logger session is already in use.\n");
        }
        else
        {
            wprintf(L"EnableTrace() failed with %lu\n", status);
        }

        goto cleanup;
    }

    wprintf(L"Press any key to end trace session ");
    _getch();

cleanup:

    if (SessionHandle)
    {
        status = ControlTrace(SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_STOP);

        if (ERROR_SUCCESS != status)
        {
            wprintf(L"ControlTrace(stop) failed with %lu\n", status);
        }
    }

    if (pSessionProperties)
        free(pSessionProperties);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren und Starten einer privaten Protokollierungssitzung](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer SystemTraceProvider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Konfigurieren und Starten einer AutoLogger-Sitzung](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Aktualisieren einer Ereignisablaufverfolgungssitzung](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
