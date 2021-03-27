---
description: Die NT Kernel Logger-Sitzung ist eine Ereignis Ablauf Verfolgungs Sitzung, die einen vordefinierten Satz von Kernel Ereignissen aufzeichnet.
ms.assetid: 3c4258d8-8073-4cc5-a29d-ce485a3fdc14
title: Konfigurieren und Starten der NT Kernel Logger-Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d13cb0d429bc4b0e01e02c33e2686040f0b7454b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980945"
---
# <a name="configuring-and-starting-the-nt-kernel-logger-session"></a>Konfigurieren und Starten der NT Kernel Logger-Sitzung

Die NT Kernel Logger-Sitzung ist eine Ereignis Ablauf Verfolgungs Sitzung, die einen vordefinierten Satz von Kernel Ereignissen aufzeichnet. Die Funktion [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) wird nicht zum Aktivieren der Kernel Anbieter aufgerufen. Stattdessen verwenden Sie den **enableflags** -Member der [**\_ \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) Struktur der Ereignis Ablauf Verfolgung, um die Kernel Ereignisse anzugeben, die Sie empfangen möchten. Die Funktion [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) verwendet die Aktivierungsflags, die Sie angeben, um die Kernel Anbieter zu aktivieren.

Es ist nur eine NT Kernel Logger-Sitzung vorhanden. Wenn die Sitzung bereits verwendet wird, gibt die [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion einen Fehler zurück, der \_ bereits \_ vorhanden ist.

Weitere Informationen zum Starten einer Ereignis Ablauf Verfolgungs Sitzung finden Sie unter [Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md).

Weitere Informationen zum Starten einer privaten Protokollierungs Sitzung finden Sie unter [Konfigurieren und Starten einer Sitzung für private](configuring-and-starting-a-private-logger-session.md)Protokollierung.

Weitere Informationen zum Starten einer globalen Protokollierungs Sitzung finden Sie unter [Konfigurieren und Starten der globalen](configuring-and-starting-the-global-logger-session.md)Protokollierungs Sitzung.

Weitere Informationen zum Starten einer autologger-Sitzung finden Sie unter [Konfigurieren und Starten einer autologger-Sitzung](configuring-and-starting-an-autologger-session.md).

Im folgenden Beispiel wird gezeigt, wie eine NT-Kernel Protokollierungs Sitzung konfiguriert und gestartet wird, die Netzwerk-TCP/IP-Kernel Ereignisse sammelt und Sie in eine 5-MB-zirkuläre Datei schreibt.


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

[Konfigurieren und Starten einer Sitzung für private Logger](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer systemtraceprovider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Konfigurieren und Starten einer autologger-Sitzung](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Aktualisieren einer Ereignis Ablauf Verfolgungs Sitzung](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
