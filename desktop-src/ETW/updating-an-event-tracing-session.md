---
description: Um die Eigenschaften einer Ereignisablaufverfolgungssitzung zu aktualisieren, rufen Sie die ControlTrace-Funktion mithilfe des STEUERELEMENTcodes EVENT \_ TRACE CONTROL \_ UPDATE \_ auf.
ms.assetid: 1496bf88-a989-4fa1-888a-90385c4ca8ee
title: Aktualisieren einer Ereignisablaufverfolgungssitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa4f092211d59dda080906f01380f8751fbc099f79dc8f1cd8ea1f7a2ba36fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383340"
---
# <a name="updating-an-event-tracing-session"></a>Aktualisieren einer Ereignisablaufverfolgungssitzung

Um die Eigenschaften einer Ereignisablaufverfolgungssitzung zu aktualisieren, rufen Sie die [**ControlTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-controltracea) mithilfe des **STEUERELEMENTcodes EVENT \_ TRACE CONTROL \_ \_ UPDATE** auf. Sie können die zu aktualisierende Sitzung mithilfe eines Sitzungshandle angeben, das aus einem früheren Aufruf von [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)oder einem Sitzungsnamen abgerufen wurde. Die Eigenschaften der Ereignisablaufverfolgungssitzung werden mithilfe der in der [**EVENT \_ TRACE \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) angegebenen Werte aktualisiert. Sie können nur eine Teilmenge der Eigenschaften aktualisieren. Eine Liste der Eigenschaften, die Sie aktualisieren können, finden Sie im *Properties-Parameter* der **ControlTrace-Funktion.**

Wenn der [**ControlTrace-Aufruf**](/windows/win32/api/evntrace/nf-evntrace-controltracea) erfolgreich ist, wird die [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) aktualisiert, um die neuen Eigenschaftswerte widerzuspiegeln. Die -Struktur enthält auch die neuen Ausführungsstatistiken für die Ereignisablaufverfolgungssitzung.

Das folgende Beispiel zeigt, wie die Kernelereignisablaufverfolgungssitzung aktualisiert wird. Im Beispiel werden die aktuellen Eigenschaftswerte abgefragt und die Struktur vor dem Aktualisieren der Sitzung aktualisiert.


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

[Konfigurieren und Starten einer privaten Protokollierungssitzung](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer SystemTraceProvider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Konfigurieren und Starten einer AutoLogger-Sitzung](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Konfigurieren und Starten der NT-Kernelprotokollierungssitzung](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
