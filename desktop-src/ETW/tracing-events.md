---
description: Bevor Sie Ereignisse in eine Ablauf Verfolgungs Sitzung schreiben können, müssen Sie den Anbieter registrieren.
ms.assetid: 21f62b5d-0a2d-468c-af88-2fab1512f0ec
title: Schreiben von MOF-Ereignissen (klassisch)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3d041e2792540d4a05637bcffdb67e1164a95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980905"
---
# <a name="writing-mof-classic-events"></a>Schreiben von MOF-Ereignissen (klassisch)

Bevor Sie Ereignisse in eine Ablauf Verfolgungs Sitzung schreiben können, müssen Sie den Anbieter registrieren. Wenn Sie einen Anbieter registrieren, wird etw mitgeteilt, dass der Anbieter zum Schreiben von Ereignissen in eine Ablauf Verfolgungs Sitzung bereit ist. Ein Prozess kann bis zu 1.024 Anbieter-GUIDs registrieren. Sie sollten jedoch die Anzahl der Anbieter, die Ihr Prozess registriert, auf einen oder zwei beschränken.

**Vor Windows Vista:** Es gibt keine Beschränkung für die Anzahl der Anbieter, die ein Prozess registrieren kann.

Um einen klassischen Anbieter zu registrieren, müssen Sie die Funktion [**registertraceguids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) aufrufen. Die-Funktion registriert die GUID des Anbieters, Ereignis Ablauf Verfolgungs Klasse-GUIDs und identifiziert den Rückruf, der von etw aufgerufen wird, wenn ein Controller den Anbieter aktiviert oder deaktiviert.

Wenn der Anbieter die [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) -Funktion aufruft, um Ereignisse zu protokollieren, müssen Sie beim Aufrufen der [**registertraceguids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) -Funktion nicht das Array der Klassen-GUIDs (kann **null** sein) einschließen. Sie müssen das Array nur einschließen, wenn der Anbieter die [**traceeventinstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) -Funktion aufruft, um Ereignisse zu protokollieren.

**Windows XP und Windows 2000:** Sie müssen immer das Array der Klassen-GUIDs einschließen (darf nicht **null** sein).

Nachdem sich ein Anbieter selbst registriert und durch den Controller aktiviert wurde, kann der Anbieter Ereignisse in der Ablauf Verfolgungs Sitzung des Controllers protokollieren.

Bevor der Anbieter beendet wird, müssen Sie die [**unregistertraceguids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) -Funktion aufrufen, um die Registrierung des Anbieters von etw zu entfernen. Die [**registertraceguids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) -Funktion gibt das Registrierungs Handle zurück, das Sie an die **unregistertraceguids** -Funktion übergeben.

Wenn Ihr Anbieter Ereignisse nur in der globalen Protokollierungs Sitzung protokolliert, müssen Sie den Anbieter nicht bei etw registrieren, da der globale Protokollierungs Controller Anbieter nicht aktiviert oder deaktiviert. Weitere Informationen finden Sie unter [Konfigurieren und Starten der globalen](configuring-and-starting-the-global-logger-session.md)Protokollierungs Sitzung.

Alle [klassischen](about-event-tracing.md) Anbieter (mit Ausnahme derjenigen, die Ereignisse in der globalen Protokollierungs Sitzung verfolgen) müssen die [**controlcallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) -Funktion implementieren. Der Anbieter verwendet die Informationen im Rückruf, um zu bestimmen, ob er aktiviert oder deaktiviert ist und welche Ereignisse er schreiben soll.

Der Anbieter gibt den Namen der Rückruffunktion an, wenn die [**registertraceguids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) -Funktion aufgerufen wird, um sich selbst zu registrieren. Etw Ruft die Rückruffunktion auf, wenn der Controller die Funktion [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) aufruft, um den Anbieter zu aktivieren oder zu deaktivieren.

In Ihrer [**controlcallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) -Implementierung müssen Sie die [**gettraceloggerhandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) -Funktion aufrufen, um das Sitzungs Handle abzurufen. Sie verwenden das Sitzungs handle, wenn Sie die [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) -Funktion aufrufen. Sie müssen nur die [**gettraceenableflags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) -Funktion oder die [**gettraceenablelevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) -Funktion in der **controlcallback** -Implementierung aufrufen, wenn Ihr Anbieter die Aktivierungsstufe enable oder Enable Flags verwendet.

Ein Anbieter kann Ablauf Verfolgungs Ereignisse nur an eine Sitzung protokollieren, es gibt jedoch nichts, um zu verhindern, dass mehrere Controller einen einzelnen Anbieter aktivieren. Um zu verhindern, dass ein anderer Controller die Ablauf Verfolgungs Ereignisse an seine Sitzung umleitet, empfiehlt es sich, der [**controlcallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) -Implementierung Logik hinzuzufügen, um Sitzungs Handles zu vergleichen und die Aktivierung von Anforderungen von anderen Controllern zu ignorieren.

Zum Protokollieren von Ereignissen wird von [klassischen](about-event-tracing.md) Anbietern die [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) -Funktion aufgerufen. Ein Ereignis besteht aus der [**Ereignis Ablauf \_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Struktur und allen ereignisspezifischen Daten, die an den Header angehängt werden.

Der Header muss die folgenden Informationen enthalten:

-   Der **size** -Member muss die Gesamtzahl der Bytes enthalten, die für das Ereignis aufgezeichnet werden sollen (einschließlich der Größe der Ereignis-Ablauf [**\_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Struktur und von ereignisspezifischen Daten, die an den Header angefügt werden).
-   Der **GUID** -Member muss die Klassen-GUID des Ereignisses enthalten (oder der **guidptr** -Member muss einen Zeiger auf die Klassen-GUID enthalten).

    **Windows XP und Windows 2000:** Die Klassen-GUID muss zuvor mithilfe der [**registertraceguids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) -Funktion registriert worden sein.

-   Der **Flags** -Member muss das Flag für die nach **\_ \_ verfolgte \_ GUID des wnode** -Flags enthalten. Wenn Sie die Klassen-GUID mit dem **guidptr** -Member angeben, fügen Sie auch das **wnode- \_ Flag \_ use \_ GUID \_ ptr** -Flag hinzu.
-   Der **Class. Type** -Member muss den Ereignistyp enthalten, wenn Sie das Layout der Ereignisdaten mit MOF veröffentlichen.
-   Der Member **Class. Version** muss die Ereignis Version enthalten, wenn Sie das Layout der Ereignisdaten mit MOF veröffentlichen. Die-Version wird verwendet, um zwischen Revisionen der Ereignisdaten zu unterscheiden. Legen Sie die anfängliche Versionsnummer auf 0 fest.

Wenn Sie sowohl den Anbieter als auch den Consumer schreiben, können Sie eine-Struktur verwenden, um die ereignisspezifischen Daten aufzufüllen, die an den-Header angefügt werden. Wenn Sie jedoch MOF zum Veröffentlichen der ereignisspezifischen Daten verwenden, sodass alle Consumer das Ereignis verarbeiten können, sollten Sie keine-Struktur verwenden, um die ereignisspezifischen Daten an den-Header anzuhängen. Dies liegt daran, dass der Compiler den ereignisspezifischen Daten für Byte-Ausrichtungs Zwecke zusätzliche Bytes hinzufügen kann. Da in der MOF-Definition die zusätzlichen Bytes nicht berücksichtigt werden, kann der Consumer Daten abrufen, die nicht gültig sind.

Sie sollten entweder einen Speicherblock für das Ereignis zuordnen und jedes Ereignisdaten Element in den Speicher kopieren oder eine Struktur erstellen, die ein Array von [**MOF- \_ Feld**](/windows/win32/api/evntrace/ns-evntrace-mof_field) Strukturen enthält. die meisten Anwendungen erstellen eine Struktur, die ein Array von **MOF- \_ Feld** Strukturen enthält. Stellen Sie sicher, dass **Header. Size** die tatsächliche Anzahl der **MOF- \_ Feld** Strukturen angibt, die vor dem Protokollieren des Ereignisses tatsächlich festgelegt sind. Wenn das Ereignis z. b. drei Datenfelder enthält, legen Sie **Header. Size** auf sizeof (Ereignis Ablauf \_ Verfolgungs \_ Header) + (sizeof (MOF- \_ Feld) \* 3) fest.

Weitere Informationen zur Ablauf Verfolgung für verwandte Ereignisse finden [Sie unterschreiben von verknüpften Ereignissen in einem End-to-End-Szenario](writing-related-events-in-an-end-to-end-scenario.md).

Im folgenden Beispiel wird gezeigt, wie die [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) -Funktion zum Protokollieren von Ereignissen aufgerufen wird. Das Beispiel verweist auf die in [Veröffentlichen Ihres Ereignis Schemas für einen klassischen Anbieter](publishing-your-event-schema-for-a-classic-provider.md)definierten Ereignisse.


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



 

 
