---
description: Um die Eigenschaften einer Ereignis Ablauf Verfolgungs Sitzung zu aktualisieren, müssen Sie die controltrace-Funktion mit dem \_ \_ \_ Aktualisierungs Steuerungs Code des Ereignis Ablauf Verfolgungs Steuer Elements abrufen.
ms.assetid: 1496bf88-a989-4fa1-888a-90385c4ca8ee
title: Aktualisieren einer Ereignis Ablauf Verfolgungs Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e580c2e84dec6682e5fad323fe0cad427300a21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959120"
---
# <a name="updating-an-event-tracing-session"></a>Aktualisieren einer Ereignis Ablauf Verfolgungs Sitzung

Um die Eigenschaften einer Ereignis Ablauf Verfolgungs Sitzung zu aktualisieren, müssen Sie die [**controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) -Funktion mit dem **\_ \_ \_ Aktualisierungs** Steuerungs Code des Ereignis Ablauf Verfolgungs Steuer Elements abrufen. Sie können die Sitzung angeben, die aktualisiert werden soll, indem Sie ein Sitzungs Handle verwenden, das von einem früheren Aufrufen von [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)abgerufen wurde, oder einen Sitzungs Namen. Die Eigenschaften der Ereignis Ablauf Verfolgungs Sitzung werden mithilfe der Werte aktualisiert, die in der Struktur der Ereignis Ablauf Verfolgungs [**\_ \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) angegeben sind. Sie können nur eine Teilmenge der Eigenschaften aktualisieren. Eine Liste der Eigenschaften, die Sie aktualisieren können, finden Sie unter dem *Properties* -Parameter der **controltrace** -Funktion.

Wenn der [**controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) -Befehl erfolgreich ist, wird die Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) aktualisiert, um die neuen Eigenschaftswerte widerzuspiegeln. Die Struktur enthält auch die neue Ausführungs Statistik für die Ereignis Ablauf Verfolgungs Sitzung.

Das folgende Beispiel zeigt, wie die Kernel-Ereignis Ablauf Verfolgungs Sitzung aktualisiert wird. Im Beispiel werden die aktuellen Eigenschaftswerte abgefragt und die-Struktur vor dem Aktualisieren der Sitzung aktualisiert.


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

#define MAX_SESSION_NAME_LEN 1024
#define MAX_LOGFILE_PATH_LEN 1024

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name.
    // This example specifies the maximum size for the session name 
    // and log file name.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + 
        (MAX_SESSION_NAME_LEN * sizeof(WCHAR)) + 
        (MAX_LOGFILE_PATH_LEN * sizeof(WCHAR));

    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;

    // Query for the kernel trace session's current property values.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_QUERY);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_WMI_INSTANCE_NOT_FOUND == status)
        {
            wprintf(L"The Kernel Logger is not running.\n");
        }
        else
        {
            wprintf(L"ControlTrace(query) failed with %lu\n", status);
        }

        goto cleanup;
    }

    // Update the enable flags to also enable the Process and Thread providers.

    pSessionProperties->LogFileNameOffset = 0;  // Zero tells ETW not to update the file name
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->EnableFlags |= EVENT_TRACE_FLAG_PROCESS | EVENT_TRACE_FLAG_THREAD;

    // Update the session's properties.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_UPDATE);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"ControlTrace(update) failed with %lu.\n", status);
        goto cleanup;
    }

    wprintf(L"\nUpdated session");

cleanup:

    if (pSessionProperties)
    {
        free(pSessionProperties);
        pSessionProperties = NULL;
    }
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

[Konfigurieren und Starten der NT Kernel Logger-Sitzung](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
