---
description: Erfahren Sie mehr über das Schreiben von MOF-Ereignissen in eine Ablaufverfolgungssitzung. Beginnen Sie mit der Registrierung Ihres Anbieters, damit er bereit ist, Ereignisse in eine Ablaufverfolgungssitzung zu schreiben.
ms.assetid: 21f62b5d-0a2d-468c-af88-2fab1512f0ec
title: Schreiben von MOF-Ereignissen (klassisch)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d081c48567851d2fb570dd7bfa5c75e687b524
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112261842"
---
# <a name="writing-mof-classic-events"></a>Schreiben von MOF-Ereignissen (klassisch)

Bevor Sie Ereignisse in eine Ablaufverfolgungssitzung schreiben können, müssen Sie Ihren Anbieter registrieren. Durch die Registrierung eines Anbieters wird ETW mitgeteilt, dass Ihr Anbieter bereit ist, Ereignisse in eine Ablaufverfolgungssitzung zu schreiben. Ein Prozess kann bis zu 1.024 Anbieter-GUIDs registrieren. Sie sollten jedoch die Anzahl der Anbieter, die ihr Prozess registriert, auf ein oder zwei beschränken.

**Vor Windows Vista:** Es gibt keine Beschränkung für die Anzahl der Anbieter, die ein Prozess registrieren kann.

Um einen klassischen Anbieter zu registrieren, rufen Sie die [**RegisterTraceGuids-Funktion**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) auf. Die Funktion registriert die GUID des Anbieters und die GUIDs der Ereignisablaufverfolgungsklasse und identifiziert den Rückruf, den ETW aufruft, wenn ein Controller den Anbieter aktiviert oder deaktiviert.

Wenn der Anbieter die [**TraceEvent-Funktion**](/windows/win32/api/evntrace/nf-evntrace-traceevent) aufruft, um Ereignisse zu protokollieren, müssen Sie beim Aufrufen der [**RegisterTraceGuids-Funktion**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) kein Array von Klassen-GUIDs (kann **NULL** sein) einschließen. Sie müssen das Array nur einschließen, wenn der Anbieter die [**TraceEventInstance-Funktion**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) aufruft, um Ereignisse zu protokollieren.

**Windows XP und Windows 2000:** Sie müssen immer das Array der Klassen-GUIDs einschließen (darf nicht **NULL** sein).

Nachdem sich ein Anbieter registriert und vom Controller aktiviert wurde, kann der Anbieter Ereignisse in der Ablaufverfolgungssitzung des Controllers protokollieren.

Rufen Sie vor dem Beenden des Anbieters die [**UnregisterTraceGuids-Funktion**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) auf, um die Registrierung des Anbieters aus ETW zu entfernen. Die [**RegisterTraceGuids-Funktion**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) gibt das Registrierungshandle zurück, das Sie an die **UnregisterTraceGuids-Funktion** übergeben.

Wenn Ihr Anbieter ereignisse nur in der Global Logger-Sitzung protokolliert, müssen Sie Ihren Anbieter nicht bei ETW registrieren, da der Globale Protokollierungscontroller anbieter nicht aktiviert oder deaktiviert. Weitere Informationen finden Sie unter [Konfigurieren und Starten der globalen Protokollierungssitzung.](configuring-and-starting-the-global-logger-session.md)

Alle [klassischen](about-event-tracing.md) Anbieter (mit Ausnahme derjenigen, die Ereignisse auf die Globale Protokollierungssitzung verfolgen) müssen die [**ControlCallback-Funktion**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) implementieren. Der Anbieter verwendet die Informationen im Rückruf, um zu bestimmen, ob er aktiviert oder deaktiviert ist und welche Ereignisse geschrieben werden sollen.

Der Anbieter gibt den Namen der Rückruffunktion an, wenn er die [**RegisterTraceGuids-Funktion**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) aufruft, um sich selbst zu registrieren. ETW ruft die Rückruffunktion auf, wenn der Controller die [**EnableTrace-Funktion aufruft,**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) um den Anbieter zu aktivieren oder zu deaktivieren.

In ihrer [**ControlCallback-Implementierung**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) müssen Sie die [**GetTraceLoggerHandle-Funktion**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) aufrufen, um das Sitzungshandle abzurufen. Sie verwenden das Sitzungshandle, wenn Sie die [**TraceEvent-Funktion**](/windows/win32/api/evntrace/nf-evntrace-traceevent) aufrufen. Sie müssen nur die [**GetTraceEnableFlags-Funktion**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) oder die [**GetTraceEnableLevel-Funktion**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) in Ihrer **ControlCallback-Implementierung** aufrufen, wenn Ihr Anbieter die Aktivierungsebene oder enable-Flags verwendet.

Ein Anbieter kann Ablaufverfolgungsereignisse nur in einer Sitzung protokollieren, aber es gibt nichts, was mehrere Controller daran hindert, einen einzelnen Anbieter zu aktivieren. Um zu verhindern, dass ein anderer Controller Ihre Ablaufverfolgungsereignisse an seine Sitzung umleitet, können Sie Ihrer [**ControlCallback-Implementierung**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) Logik hinzufügen, um Sitzungshandles zu vergleichen und Aktivierungsanforderungen von anderen Controllern zu ignorieren.

Zum Protokollieren von Ereignissen rufen [klassische](about-event-tracing.md) Anbieter die [**TraceEvent-Funktion**](/windows/win32/api/evntrace/nf-evntrace-traceevent) auf. Ein Ereignis besteht aus der [**EVENT \_ TRACE \_ HEADER-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) und allen ereignisspezifischen Daten, die an den Header angefügt werden.

Der Header muss die folgenden Informationen enthalten:

-   Der **Size-Member** muss die Gesamtzahl der Bytes enthalten, die für das Ereignis aufgezeichnet werden sollen (einschließlich der Größe der [**EVENT TRACE \_ \_ HEADER-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) und aller ereignisspezifischen Daten, die an den Header angefügt werden).
-   Der **Guid-Member** muss die Klassen-GUID des Ereignisses enthalten (oder der **GuidPtr-Member** muss einen Zeiger auf die Klassen-GUID enthalten).

    **Windows XP und Windows 2000:** Die Klassen-GUID muss zuvor mit der [**RegisterTraceGuids-Funktion**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) registriert worden sein.

-   Der **Flags-Member** muss das **\_ \_ \_ GUID-Flag WNODE FLAG TRACED** enthalten. Wenn Sie die Klassen-GUID mithilfe des **GuidPtr-Members** angeben, fügen Sie auch das **FLAG WNODE \_ FLAG USE \_ \_ GUID \_ PTR** hinzu.
-   Der **Class.Type-Member** muss den Ereignistyp enthalten, wenn Sie MOF verwenden, um das Layout Ihrer Ereignisdaten zu veröffentlichen.
-   Der **Class.Version-Member** muss die Ereignisversion enthalten, wenn Sie MOF verwenden, um das Layout Ihrer Ereignisdaten zu veröffentlichen. Die Version wird verwendet, um zwischen Revisionen der Ereignisdaten zu unterscheiden. Legen Sie die anfängliche Versionsnummer auf 0 fest.

Wenn Sie sowohl den Anbieter als auch den Consumer schreiben, können Sie eine -Struktur verwenden, um die ereignisspezifischen Daten aufzufüllen, die an den Header angefügt werden. Wenn Sie jedoch MOF verwenden, um die ereignisspezifischen Daten zu veröffentlichen, sodass jeder Consumer das Ereignis verarbeiten kann, sollten Sie keine -Struktur verwenden, um die ereignisspezifischen Daten an den Header anzufügen. Dies liegt daran, dass der Compiler den ereignisspezifischen Daten zu Byteausrichtungszwecken zusätzliche Bytes hinzufügen kann. Da die MOF-Definition die zusätzlichen Bytes nicht berücksichtigt, ruft der Consumer möglicherweise ungültige Daten ab.

Sie sollten entweder einen Speicherblock für das Ereignis zuordnen und jedes Ereignisdatenelement in den Arbeitsspeicher kopieren oder eine Struktur erstellen, die ein Array von [**MOF \_ FIELD-Strukturen**](/windows/win32/api/evntrace/ns-evntrace-mof_field) enthält. Die meisten Anwendungen erstellen eine -Struktur, die ein Array von **MOF \_ FIELD-Strukturen** enthält. Stellen Sie sicher, dass **Header.Size** die tatsächliche Anzahl von **MOF \_ FIELD-Strukturen** angibt, die tatsächlich vor der Protokollierung des Ereignisses festgelegt werden. Wenn das Ereignis beispielsweise drei Datenfelder enthält, legen Sie **Header.Size** auf sizeof(EVENT \_ TRACE \_ HEADER) + (sizeof(MOF \_ FIELD) \* 3) fest.

Informationen zur Ablaufverfolgung verwandter Ereignisse finden Sie unter [Schreiben verwandter Ereignisse in einem End-to-End-Szenario.](writing-related-events-in-an-end-to-end-scenario.md)

Das folgende Beispiel zeigt, wie die [**TraceEvent-Funktion**](/windows/win32/api/evntrace/nf-evntrace-traceevent) aufgerufen wird, um Ereignisse zu protokollieren. Das Beispiel verweist auf die Ereignisse, die unter [Veröffentlichen des Ereignisschemas für einen klassischen Anbieter](publishing-your-event-schema-for-a-classic-provider.md)definiert sind.


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

// GUID that identifies the category of events that the provider can log. 
// The GUID is also used in the event MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {B49D5931-AD85-4070-B1B1-3F81F1532875}
static const GUID MyCategoryGuid = 
{ 0xb49d5931, 0xad85, 0x4070, { 0xb1, 0xb1, 0x3f, 0x81, 0xf1, 0x53, 0x28, 0x75 } };

// GUID that identifies the provider that you are registering.
// The GUID is also used in the provider MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };

// Identifies the event type within the MyCategoryGuid category 
// of events to be logged. This is the same value as the EventType 
// qualifier that is defined in the event type MOF class for one of 
// the MyCategoryGuid category of events.

#define MY_EVENT_TYPE 1

// Event passed to TraceEvent

typedef struct _event
{
    EVENT_TRACE_HEADER Header;
    MOF_FIELD Data[MAX_MOF_FIELDS];  // Event-specific data
} MY_EVENT, *PMY_EVENT;

#define MAX_INDICES            3
#define MAX_SIGNATURE_LEN      32
#define EVENT_DATA_FIELDS_CNT  6

// Application data to be traced for Version 1 of the MOF class.

typedef struct _evtdata
{
    LONG Cost;
    DWORD Indices[MAX_INDICES];
    WCHAR Signature[MAX_SIGNATURE_LEN];
    BOOL IsComplete;
    GUID ID;
    DWORD Size;
}EVENT_DATA, *PEVENT_DATA;

// GUID used as the value for EVENT_DATA.ID.

// {25BAEDA9-C81A-4889-8764-184FE56750F2}
static const GUID tempID = 
{ 0x25baeda9, 0xc81a, 0x4889, { 0x87, 0x64, 0x18, 0x4f, 0xe5, 0x67, 0x50, 0xf2 } };

// Global variables to store tracing state information.

TRACEHANDLE g_SessionHandle = 0; // The handle to the session that enabled the provider.
ULONG g_EnableFlags = 0; // Determines which class of events to log.
UCHAR g_EnableLevel = 0; // Determines the severity of events to log.
BOOL g_TraceOn = FALSE;  // Used by the provider to determine whether it should log events.

ULONG WINAPI ControlCallback(WMIDPREQUESTCODE RequestCode, PVOID Context, ULONG* Reserved, PVOID Header);

// For this example to log the event, run the session example
// to enable the provider before running this example.

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_DATA EventData;
    MY_EVENT MyEvent; 
    TRACEHANDLE RegistrationHandle = 0; 
    TRACE_GUID_REGISTRATION EventClassGuids[] = {
        (LPGUID)&MyCategoryGuid, NULL
        };

    // Register the provider and specify the control callback function
    // that receives the enable/disable notifications.

    status = RegisterTraceGuids(
        (WMIDPREQUEST)ControlCallback,
        NULL,
        (LPGUID)&ProviderGuid,
        sizeof(EventClassGuids)/sizeof(TRACE_GUID_REGISTRATION),
        EventClassGuids,
        NULL,
        NULL,
        &RegistrationHandle
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegisterTraceGuids failed with %lu\n", status);
        goto cleanup;
    }

    // Set the event-specific data.

    EventData.Cost = 32;
    EventData.ID = tempID;
    EventData.Indices[0] = 4;
    EventData.Indices[1] = 5;
    EventData.Indices[2] = 6;
    EventData.IsComplete = TRUE;
    wcscpy_s(EventData.Signature, MAX_SIGNATURE_LEN, L"Signature");
    EventData.Size = 1024;

    // Log the event if the provider is enabled and the session
    // passed a severity level value >= TRACE_LEVEL_ERROR (or zero).
    // If your provider generates more than one class of events, you
    // would also need to check g_EnableFlags.

    if (g_TraceOn && (0 == g_EnableLevel || TRACE_LEVEL_ERROR <= g_EnableLevel))
    {
        // Initialize the event data structure.

        ZeroMemory(&MyEvent, sizeof(MY_EVENT));
        MyEvent.Header.Size = sizeof(EVENT_TRACE_HEADER) + (sizeof(MOF_FIELD) * EVENT_DATA_FIELDS_CNT);
        MyEvent.Header.Flags = WNODE_FLAG_TRACED_GUID | WNODE_FLAG_USE_MOF_PTR;
        MyEvent.Header.Guid = MyCategoryGuid;
        MyEvent.Header.Class.Type = MY_EVENT_TYPE;
        MyEvent.Header.Class.Version = 1;
        MyEvent.Header.Class.Level = g_EnableLevel;

        // Load the event data. You can also use the DEFINE_TRACE_MOF_FIELD
        // macro defined in evntrace.h to set the MOF_FIELD members. For example,
        // DEFINE_TRACE_MOF_FIELD(&EventData.Data[0], &EventData.Cost, sizeof(EventData.Cost), 0);

        MyEvent.Data[0].DataPtr = (ULONG64) &(EventData.Cost);
        MyEvent.Data[0].Length = sizeof(EventData.Cost);
        MyEvent.Data[1].DataPtr = (ULONG64) &(EventData.Indices);
        MyEvent.Data[1].Length = sizeof(EventData.Indices);
        MyEvent.Data[2].DataPtr = (ULONG64) &(EventData.Signature);
        MyEvent.Data[2].Length = (ULONG)(wcslen(EventData.Signature) + 1) * sizeof(WCHAR);
        MyEvent.Data[3].DataPtr = (ULONG64) &(EventData.IsComplete);
        MyEvent.Data[3].Length = sizeof(EventData.IsComplete);
        MyEvent.Data[4].DataPtr = (ULONG64) &(EventData.ID);
        MyEvent.Data[4].Length = sizeof(EventData.ID);
        MyEvent.Data[5].DataPtr = (ULONG64) &(EventData.Size);
        MyEvent.Data[5].Length = sizeof(EventData.Size);

        // Write the event.

        status = TraceEvent(g_SessionHandle, &(MyEvent.Header));

        if (ERROR_SUCCESS != status)
        {
            // Decide how you want to handle failures. Typically, you do not
            // want to terminate the application because you failed to
            // log an event. If the error is a memory failure, you may
            // may want to log a message to the system event log or turn
            // off logging.

            wprintf(L"TraceEvent() event failed with %lu\n", status);
            g_TraceOn = FALSE;
        }
    }

cleanup:

    if (RegistrationHandle)
    {
        UnregisterTraceGuids(RegistrationHandle);
    }
}


// The callback function that receives enable/disable notifications
// from one or more ETW sessions. Because more than one session
// can enable the provider, this example ignores requests from other 
// sessions if it is already enabled.

ULONG WINAPI ControlCallback(
    WMIDPREQUESTCODE RequestCode,
    PVOID Context,
    ULONG* Reserved, 
    PVOID Header
    )
{
    UNREFERENCED_PARAMETER(Context);
    UNREFERENCED_PARAMETER(Reserved);

    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE TempSessionHandle = 0; 

    switch (RequestCode)
    {
        case WMI_ENABLE_EVENTS:  // Enable the provider.
        {
            SetLastError(0);

            // If the provider is already enabled to a provider, ignore 
            // the request. Get the session handle of the enabling session.
            // You need the session handle to call the TraceEvent function.
            // The session could be enabling the provider or it could be
            // updating the level and enable flags.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (0 == g_SessionHandle)
            {
                g_SessionHandle = TempSessionHandle;
            }
            else if (g_SessionHandle != TempSessionHandle)
            {
                break;
            }

            // Get the severity level of the events that the
            // session wants you to log.

            g_EnableLevel = GetTraceEnableLevel(g_SessionHandle); 
            if (0 == g_EnableLevel)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable level means to your provider.
                    // For this example, it means log all events.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableLevel failed with, %lu.\n", status);
                    break;
                } 
            }

            // Get the enable flags that indicate the events that the
            // session wants you to log. The provider determines the
            // flags values. How it articulates the flag values and 
            // meanings to perspective sessions is up to it.

            g_EnableFlags = GetTraceEnableFlags(g_SessionHandle);
            if (0 == g_EnableFlags)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable flags value means to your provider.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableFlags failed with, %lu.\n", status);
                    break;
                }
            }

            g_TraceOn = TRUE;
            break;
        }
 
        case WMI_DISABLE_EVENTS:  // Disable the provider.
        {
            // Disable the provider only if the request is coming from the
            // session that enabled the provider.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (g_SessionHandle == TempSessionHandle)
            {
                g_TraceOn = FALSE;
                g_SessionHandle = 0;
            }
            break;
        }

        default:
        {
            status = ERROR_INVALID_PARAMETER;
            break;
        }
    }

    return status;
}
```



 

 
