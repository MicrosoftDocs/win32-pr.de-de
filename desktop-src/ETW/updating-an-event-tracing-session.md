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
# <a name="updating-an-event-tracing-session"></a><span data-ttu-id="256d6-103">Aktualisieren einer Ereignis Ablauf Verfolgungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="256d6-103">Updating an Event Tracing Session</span></span>

<span data-ttu-id="256d6-104">Um die Eigenschaften einer Ereignis Ablauf Verfolgungs Sitzung zu aktualisieren, müssen Sie die [**controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) -Funktion mit dem **\_ \_ \_ Aktualisierungs** Steuerungs Code des Ereignis Ablauf Verfolgungs Steuer Elements abrufen.</span><span class="sxs-lookup"><span data-stu-id="256d6-104">To update the properties of an event tracing session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function using the **EVENT\_TRACE\_CONTROL\_UPDATE** control code.</span></span> <span data-ttu-id="256d6-105">Sie können die Sitzung angeben, die aktualisiert werden soll, indem Sie ein Sitzungs Handle verwenden, das von einem früheren Aufrufen von [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)abgerufen wurde, oder einen Sitzungs Namen.</span><span class="sxs-lookup"><span data-stu-id="256d6-105">You can specify the session to update using a session handle obtained from an earlier call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), or a session name.</span></span> <span data-ttu-id="256d6-106">Die Eigenschaften der Ereignis Ablauf Verfolgungs Sitzung werden mithilfe der Werte aktualisiert, die in der Struktur der Ereignis Ablauf Verfolgungs [**\_ \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="256d6-106">The properties of the event tracing session are updated using the values specified in the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span> <span data-ttu-id="256d6-107">Sie können nur eine Teilmenge der Eigenschaften aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="256d6-107">You can update only a subset of the properties.</span></span> <span data-ttu-id="256d6-108">Eine Liste der Eigenschaften, die Sie aktualisieren können, finden Sie unter dem *Properties* -Parameter der **controltrace** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="256d6-108">For a list of the properties you can update, see the *Properties* parameter of the **ControlTrace** function.</span></span>

<span data-ttu-id="256d6-109">Wenn der [**controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) -Befehl erfolgreich ist, wird die Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) aktualisiert, um die neuen Eigenschaftswerte widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="256d6-109">If the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) call is successful, the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is updated to reflect the new property values.</span></span> <span data-ttu-id="256d6-110">Die Struktur enthält auch die neue Ausführungs Statistik für die Ereignis Ablauf Verfolgungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="256d6-110">The structure will also contain the new run statistics for the event tracing session.</span></span>

<span data-ttu-id="256d6-111">Das folgende Beispiel zeigt, wie die Kernel-Ereignis Ablauf Verfolgungs Sitzung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="256d6-111">The following example shows how to update the kernel event tracing session.</span></span> <span data-ttu-id="256d6-112">Im Beispiel werden die aktuellen Eigenschaftswerte abgefragt und die-Struktur vor dem Aktualisieren der Sitzung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="256d6-112">The example queries for the current property values and updates the structure before updating the session.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="256d6-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="256d6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="256d6-114">Konfigurieren und Starten einer Sitzung für private Logger</span><span class="sxs-lookup"><span data-stu-id="256d6-114">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="256d6-115">Konfigurieren und Starten einer systemtraceprovider-Sitzung</span><span class="sxs-lookup"><span data-stu-id="256d6-115">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="256d6-116">Konfigurieren und Starten einer autologger-Sitzung</span><span class="sxs-lookup"><span data-stu-id="256d6-116">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="256d6-117">Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="256d6-117">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="256d6-118">Konfigurieren und Starten der NT Kernel Logger-Sitzung</span><span class="sxs-lookup"><span data-stu-id="256d6-118">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
