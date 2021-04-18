---
description: Ereignis Ablauf Verfolgung in DirectShow
ms.assetid: e78c4514-25f4-441d-bfd0-6dac4f7567fd
title: Ereignis Ablauf Verfolgung in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c567d8a2e75d838570323d8ad6be04f11502c9c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345605"
---
# <a name="event-tracing-in-directshow"></a>Ereignis Ablauf Verfolgung in DirectShow

DirectShow unterstützt die Ereignis Ablauf Verfolgung für Windows (ETW), die zum Erstellen von Ereignisprotokollen für die Instrumentation oder das Debuggen verwendet werden kann. Weitere Informationen zu etw finden Sie in der Windows SDK-Dokumentation. Um etw-Ereignisse in einer DirectShow-Anwendung zu nutzen, müssen Sie die Ablauf Verfolgung aktivieren und dann die Ablauf Verfolgungs Ereignisse verarbeiten. Führen Sie die folgenden Schritte aus.

**Festlegen der erforderlichen Registrierungsschlüssel**

Um die Ablauf Verfolgung auf dem Computer des Benutzers zu aktivieren, legen Sie zunächst die folgenden Registrierungsschlüssel fest:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DirectX
    GlitchInstrumentation = 0x00000001 (REG_DWORD)
HKEY_LOCAL_MACHINE\SOFTWARE\DEBUG\Quartz.dll
    PERFLOG = 0x00000001 (REG_DWORD) 
```



Diese Schlüssel gelten sowohl für Release-als auch für Debug-Binärdateien.

**Aktivieren der Ablauf Verfolgung in der Anwendung**

Führen Sie die folgenden Schritte aus, um die Ablauf Verfolgung in der Anwendung zu aktivieren:

1.  Aufrufen von **starttrace** , um eine neue Ablauf Verfolgungs Sitzung zu starten.
2.  Ruft **EnableTrace** zum Aktivieren der Ablauf Verfolgung auf. Die Anbieter-GUID für DirectShow ist GUID \_ DShow \_ CTL.
3.  Bevor die Anwendung beendet wird, wird **stoptrace** aufgerufen, um die Ablauf Verfolgungs Sitzung zu schließen.

**Verarbeiten der Ereignisse**

Um die Ereignisse zu verarbeiten, führen Sie die folgenden Schritte aus:

1.  Ruft **opentrace** auf, um die Ablauf Verfolgung für die Verarbeitung zu öffnen.
2.  Aufrufen von **processtrace** , um die Ereignisse zu verarbeiten.
3.  Verwenden Sie im **processtrace** -Rückruf die Ereignis-GUID, um den Ereignistyp zu suchen. Die Ereignis-GUID gibt die Struktur an, die für die Ereignisdaten verwendet wird. Siehe [Trace-Ereignis-GUIDs](trace-guids.md).
4.  Beenden Sie **closetrace** , um das Ablauf Verfolgungs Handle zu schließen.

**Beispiel Code**

Der folgende Code zeigt eine Hilfsklasse, die die Ablauf Verfolgung aktiviert. Dieser Code zeigt, wie Ereignisse in eine Protokolldatei geschrieben werden, die nach Abschluss der Sitzung verarbeitet werden kann. Sie können Ereignisse auch in Echtzeit verarbeiten. Weitere Informationen finden Sie in der etw-Dokumentation in der Windows SDK.


```C++
#include <wmistr.h>
#include <evntrace.h>
#include <perfstruct.h>

// Event classes. These are defined in dxmperf.h.
#ifndef DXMPERF_VIDEOREND
#define DXMPERF_VIDEOREND   0x00000001
#endif

#ifndef AUDIOBREAK_BIT
#define AUDIOBREAK_BIT      0x00000010
#endif

// This structure extends the EVENT_TRACE_PROPERTIES by adding fields
// for the name of the WMI session name and the log file.
struct PERFMON_LOGGERINFO
{
    EVENT_TRACE_PROPERTIES TraceProperties;
    WCHAR wcSessionName[ MAX_PATH ];    // Session name.
    WCHAR wcLogFileName[ MAX_PATH ];    // Log file.
};

// Helper class for DirectShow event tracing.
class CTrace
{
public:
    CTrace() : m_SessionLogger((TRACEHANDLE) INVALID_HANDLE_VALUE)
    {
        ZeroMemory(&m_LogInfo, sizeof(&m_LogInfo));
    }

    // Start: Starts a trace session.
    HRESULT Start(WCHAR *wszLogFile)
    {
        const WCHAR* wszSessionName = L"PerfMon_DirectShow"; 
        HRESULT hr = S_OK;
        ULONG result; 

        ZeroMemory(&m_LogInfo, sizeof(m_LogInfo));
        
        EVENT_TRACE_PROPERTIES& prop = m_LogInfo.TraceProperties;

        prop.Wnode.BufferSize = sizeof(m_LogInfo);  // Size of the structure.
        prop.Wnode.Flags = WNODE_FLAG_TRACED_GUID;  // Must be this value.

        // Use the QPC (high resolution timer).
        prop.Wnode.ClientContext = 1;        

        prop.Wnode.Guid = GUID_DSHOW_CTL;           // Event provider GUID.
        prop.LogFileMode = 
            EVENT_TRACE_FILE_MODE_CIRCULAR | EVENT_TRACE_USE_PAGED_MEMORY; 
        prop.EnableFlags = 
            EVENT_TRACE_FLAG_PROCESS;   // Process events.

        // Set the offset from the start of the structure to the log file name.
        prop.LogFileNameOffset = 
            sizeof(m_LogInfo.TraceProperties) + sizeof(m_LogInfo.wcSessionName);  

        // Set the offset from the start of the structure to the session name.
        prop.LoggerNameOffset = sizeof(m_LogInfo.TraceProperties); 

        // Copy the names into the structure.
        StringCchCopy(m_LogInfo.wcSessionName, MAX_PATH, wszSessionName);
        StringCchCopy(m_LogInfo.wcLogFileName, MAX_PATH, wszLogFile);

        // Start the trace.
        result = StartTrace(
            &m_SessionLogger, 
            m_LogInfo.wcSessionName, 
            &m_LogInfo.TraceProperties
            );

        if (result == ERROR_SUCCESS)
        {
            result = EnableTrace(
                TRUE,                                   // Enable.
                AUDIOBREAK_BIT | DXMPERF_VIDEOREND,     // Event classes.
                TRACE_LEVEL_VERBOSE,                    // Trace level.
                &GUID_DSHOW_CTL,                        // Event provider.
                m_SessionLogger                         // Session handle.
                );
        }
        if (result != ERROR_SUCCESS)
        { 
            hr = __HRESULT_FROM_WIN32(result);
        }
        return hr;
    }

    HRESULT Stop()
    {
        HRESULT hr = S_OK;

        // Stop the trace.
        if (m_SessionLogger != (TRACEHANDLE)INVALID_HANDLE_VALUE)
        {
            LONG result = 0;

            result = EnableTrace(FALSE, 0, 0, &GUID_DSHOW_CTL, m_SessionLogger);
            if (result == ERROR_SUCCESS)
            {
                result = StopTrace(
                    m_SessionLogger, 
                    m_LogInfo.wcSessionName, 
                    &m_LogInfo.TraceProperties);
            }

            m_SessionLogger = (TRACEHANDLE)INVALID_HANDLE_VALUE;
            if (result != ERROR_SUCCESS)
            { 
                hr = __HRESULT_FROM_WIN32(result);
            }
        }
        return hr;
    }

protected:
    TRACEHANDLE         m_SessionLogger;
    PERFMON_LOGGERINFO  m_LogInfo;
};
```



Der folgende Code zeigt, wie das Ereignisprotokoll verarbeitet wird:


```C++
// Callback for event processing.
VOID WINAPI EventCallback(PEVENT_TRACE pEvent)
{
    PERFINFO_DSHOW_STREAMTRACE  *pStreamTrace = NULL;
    PERFINFO_DSHOW_AVREND       *pVideoRender = NULL;
    PERFINFO_DSHOW_AUDIOBREAK   *pAudioBreak = NULL;

    if (pEvent->Header.Guid == GUID_STREAMTRACE) 
    {
        pStreamTrace = (PPERFINFO_DSHOW_STREAMTRACE)pEvent->MofData;

        switch (pStreamTrace->id)
        {
            // TODO: Handle the event.
        }
    }
    else if(pEvent->Header.Guid == GUID_VIDEOREND)
    {      
        pVideoRender = (PPERFINFO_DSHOW_AVREND)pEvent->MofData;
        // TODO: Handle the event.
    }
    else if(pEvent->Header.Guid == GUID_AUDIOBREAK)
    {
        pAudioBreak = (PPERFINFO_DSHOW_AUDIOBREAK)pEvent->MofData;
        // TODO: Handle the event.
    }
}

void ProcessTraceEvents(WCHAR *wszLogFile)
{
    ULONG result = 0;        
    EVENT_TRACE_LOGFILE logfile;

    ZeroMemory(&logfile, sizeof(logfile));
    logfile.LogFileName = wszLogFile;
    logfile.EventCallback  = EventCallback;   

    TRACEHANDLE handle = OpenTrace(&logfile);
    if (handle != (TRACEHANDLE)INVALID_HANDLE_VALUE)
    {
        result = ProcessTrace(&handle, 1, NULL, NULL);
        CloseTrace(handle);
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen in DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



