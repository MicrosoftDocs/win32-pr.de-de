---
description: In diesem Thema werden die Prozess- und Threadfunktionen beschrieben.
ms.assetid: 8c8e8af0-bf50-4a4b-945c-83bae1eff7dd
title: Prozess- und Threadfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43841e86c151e7f617a702668f9de203ccb34654
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/06/2021
ms.locfileid: "111550012"
---
# <a name="process-and-thread-functions"></a>Prozess- und Threadfunktionen

In diesem Thema werden die Prozess- und Threadfunktionen beschrieben.

-   [Dispatch-Warteschlangenfunktion](#dispatch-queue-function)
-   [Prozessfunktionen](#process-functions)
-   [Prozessenumerationsfunktionen](#process-enumeration-functions)
-   [Richtlinienfunktionen](#policy-functions)
-   [Threadfunktionen](#thread-functions)
-   [Erweiterte Attributfunktionen für Prozesse und Threads](#process-and-thread-extended-attribute-functions)
-   [WOW64-Funktionen](#wow64-functions)
-   [Auftragsobjektfunktionen](#job-object-functions)
-   [Threadpoolfunktionen](#thread-pool-functions)
-   [Funktionen des Threadreihenfolgediensts](#thread-ordering-service-functions)
-   [Funktionen des Multimedia-Klassenplanerdiensts](#multimedia-class-scheduler-service-functions)
-   [Fiberfunktionen](#fiber-functions)
-   [NUMA-Unterstützungsfunktionen](#numa-support-functions)
-   [Prozessorfunktionen](#processor-functions)
-   [Zeitplanungsfunktionen im Benutzermodus](#user-mode-scheduling-functions)
-   [Veraltete Funktionen](#obsolete-functions)

## <a name="dispatch-queue-function"></a>Dispatch-Warteschlangenfunktion

Mit der folgenden Funktion wird ein [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller)erstellt.



| Funktion                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDispatcherQueueController**](/windows/desktop/api/DispatcherQueue/nf-dispatcherqueue-createdispatcherqueuecontroller) | Erstellt einen [DispatcherQueueController,](/uwp/api/windows.system.dispatcherqueuecontroller) der die Lebensdauer einer [DispatcherQueue](/uwp/api/windows.system.dispatcherqueue) verwaltet, die in der Warteschlange ausgeführte Aufgaben in der Prioritätsreihenfolge in einem anderen Thread ausführt. |



 

## <a name="process-functions"></a>Prozessfunktionen

Die folgenden Funktionen werden mit [Prozessen](child-processes.md)verwendet.



| Funktion                                                                 | BESCHREIBUNG                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)                                   | Erstellt einen neuen Prozess und seinen primären Thread.                                                                                                                                                 |
| [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)                       | Erstellt einen neuen Prozess und seinen primären Thread. Der neue Prozess wird im Sicherheitskontext des Benutzers ausgeführt, der durch das angegebene Token dargestellt wird.                                                    |
| [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw)               | Erstellt einen neuen Prozess und seinen primären Thread. Der neue Prozess führt dann die angegebene ausführbare Datei im Sicherheitskontext der angegebenen Anmeldeinformationen (Benutzer, Domäne und Kennwort) aus.      |
| [**CreateProcessWithTokenW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithtokenw)               | Erstellt einen neuen Prozess und seinen primären Thread. Der neue Prozess wird im Sicherheitskontext des angegebenen Tokens ausgeführt.                                                                            |
| [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)                                       | Beendet den aufrufenden Prozess und alle zugehörigen Threads.                                                                                                                                                 |
| [**FlushProcessWriteBuffers**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushprocesswritebuffers)             | Leert die Schreibwarteschlange jedes Prozessors, der einen Thread des aktuellen Prozesses ausführt.                                                                                                    |
| [**FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa)                 | Gibt einen Block von Umgebungszeichenfolgen frei.                                                                                                                                                         |
| [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea)                                 | Ruft die Befehlszeilenzeichenfolge für den aktuellen Prozess ab.                                                                                                                                    |
| [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess)                           | Ruft ein Pseudohandle für den aktuellen Prozess ab.                                                                                                                                            |
| [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid)                       | Ruft den Prozessbezeichner des aufrufenden Prozesses ab.                                                                                                                                      |
| [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)           | Ruft die Anzahl des Prozessors ab, auf dem der aktuelle Thread während des Aufrufs dieser Funktion ausgeführt wurde.                                                                                     |
| [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings)                   | Ruft den Umgebungsblock für den aktuellen Prozess ab.                                                                                                                                      |
| [**Getenvironmentvariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable)                 | Ruft den Wert der angegebenen Variablen aus dem Umgebungsblock des aufrufenden Prozesses ab.                                                                                              |
| [**GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess)                         | Ruft den Beendigungsstatus des angegebenen Prozesses ab.                                                                                                                                    |
| [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources)                               | Ruft die Anzahl der Handles für GUI-Objekte (Grafische Benutzeroberfläche) ab, die vom angegebenen Prozess verwendet werden.                                                                                     |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Ruft Informationen zu logischen Prozessoren und zugehöriger Hardware ab.                                                                                                                          |
| [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass)                             | Ruft die Prioritätsklasse für den angegebenen Prozess ab.                                                                                                                                       |
| [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask)                 | Ruft eine Prozessaffinitätsmaske für den angegebenen Prozess und die Systemaffinitätsmaske für das System ab.                                                                                      |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)               | Ruft die Prozessorgruppenaffinität des angegebenen Prozesses ab.                                                                                                                              |
| [**GetProcessHandleCount**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)                   | Ruft die Anzahl der offenen Handles ab, die zum angegebenen Prozess gehören.                                                                                                                    |
| [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)                                     | Ruft den Prozessbezeichner des angegebenen Prozesses ab.                                                                                                                                    |
| [**GetProcessIdOfThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread)                     | Ruft den Prozessbezeichner des Prozesses ab, der dem angegebenen Thread zugeordnet ist.                                                                                                         |
| [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters)                     | Ruft Kontoführungsinformationen für alle E/A-Vorgänge ab, die vom angegebenen Prozess ausgeführt werden.                                                                                                   |
| [**GetProcessMitigationPolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy)         | Ruft Einstellungen der Entschärfungsrichtlinie für den aufrufenden Prozess ab.                                                                                                                                 |
| [**GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost)               | Ruft den Steuerungszustand der Prioritäts boost des angegebenen Prozesses ab.                                                                                                                          |
| [**GetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessshutdownparameters)     | Ruft Parameter zum Herunterfahren für den aktuell aufrufenden Prozess ab.                                                                                                                              |
| [**GetProcessTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes)                               | Ruft Zeitsteuerungsinformationen zu für den angegebenen Prozess ab.                                                                                                                                 |
| [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion)                           | Ruft die Haupt- und Nebenversionsnummern des Systems ab, auf dem der angegebene Prozess die Ausführung erwartet.                                                                                    |
| [**GetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize)             | Ruft die minimalen und maximalen Arbeitssatzgrößen des angegebenen Prozesses ab.                                                                                                                 |
| [**GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex)         | Ruft die minimalen und maximalen Arbeitssatzgrößen des angegebenen Prozesses ab.                                                                                                                 |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)       | Ruft die Zykluszeit ab, die jeder Prozessor in der angegebenen Gruppe für die Ausführung verzögerter Prozeduraufrufe (Deferred Procedure Calls, DPCs) und Interruptdienstroutinen (ISRs) aufgewendet hat.                                         |
| [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow)                                 | Ruft den Inhalt der [**STARTUPINFO-Struktur**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) ab, die beim Erstellen des aufrufenden Prozesses angegeben wurde.                                                       |
| [**IsImmersiveProcess**](/windows/desktop/api/Winuser/nf-winuser-isimmersiveprocess)                         | Bestimmt, ob der Prozess zu einer Windows Store-App gehört.                                                                                                                                |
| [**NeedCurrentDirectoryForExePath**](/windows/win32/api/processenv/nf-processenv-needcurrentdirectoryforexepatha) | Bestimmt, ob das aktuelle Verzeichnis im Suchpfad für die angegebene ausführbare Datei enthalten sein soll.                                                                                  |
| [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)                                       | Öffnet ein vorhandenes lokales Prozessobjekt.                                                                                                                                                       |
| [**QueryFullProcessImageName**](/windows/desktop/api/WinBase/nf-winbase-queryfullprocessimagenamea)           | Ruft den vollständigen Namen des ausführbaren Images für den angegebenen Prozess ab.                                                                                                                    |
| [**QueryProcessAffinityUpdateMode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprocessaffinityupdatemode) | Ruft den Affinitätsaktualisierungsmodus des angegebenen Prozesses ab.                                                                                                                                  |
| [**QueryProcessCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryprocesscycletime)                   | Ruft die Summe der Zykluszeit aller Threads des angegebenen Prozesses ab.                                                                                                                  |
| [**Setenvironmentvariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable)                 | Legt den Wert einer Umgebungsvariablen für den aktuellen Prozess fest.                                                                                                                            |
| [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass)                             | Legt die Prioritätsklasse für den angegebenen Prozess fest.                                                                                                                                            |
| [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask)                 | Legt eine Prozessoraffinitätsmaske für die Threads eines angegebenen Prozesses fest.                                                                                                                        |
| [**SetProcessAffinityUpdateMode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessaffinityupdatemode)     | Legt den Affinitätsaktualisierungsmodus des angegebenen Prozesses fest.                                                                                                                                       |
| [**SetProcessInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessinformation)                   | Legt Informationen für den angegebenen Prozess fest.                                                                                                                                                   |
| [**SetProcessMitigationPolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy)         | Legt die Entschärfungsrichtlinie für den aufrufenden Prozess fest.                                                                                                                                           |
| [**SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost)               | Deaktiviert die Fähigkeit des Systems, die Priorität der Threads des angegebenen Prozesses vorübergehend zu erhöhen.                                                                                 |
| [**SetProcessRestrictionExemption**](/windows/desktop/api/Winuser/nf-winuser-setprocessrestrictionexemption) | Ausgenommen des aufrufenden Prozesses von Einschränkungen, die die Interaktion von Desktopprozessen mit der Windows Store-App-Umgebung verhindern. Diese Funktion wird von Entwicklungs- und Debugtools verwendet. |
| [**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)     | Legt Die Parameter für das Herunterfahren für den derzeit aufrufenden Prozess fest.                                                                                                                                   |
| [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize)             | Legt die minimale und maximale Arbeitssatzgröße für den angegebenen Prozess fest.                                                                                                                     |
| [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex)         | Legt die minimale und maximale Arbeitssatzgröße für den angegebenen Prozess fest.                                                                                                                     |
| [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)                             | Beendet den angegebenen Prozess und alle seine Threads.                                                                                                                                      |



 

## <a name="process-enumeration-functions"></a>Prozessenumerationsfunktionen

Die folgenden Funktionen werden zum Aufzählen von Prozessen verwendet.



| Funktion                                                    | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Ruft den Prozessbezeichner für jedes Prozessobjekt im System ab.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Ruft Informationen zum ersten Prozess ab, der in einer Systemmomentaufnahme gefunden wurde.    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Ruft Informationen zum nächsten Prozess ab, der in einer Systemmomentaufnahme aufgezeichnet wird.        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Ruft Informationen zu den aktiven Prozessen auf dem angegebenen Terminalserver ab. |



 

## <a name="policy-functions"></a>Richtlinienfunktionen

Die folgenden Funktionen werden mit prozessweiten Richtlinien verwendet.



|                                                      |                                                       |
|------------------------------------------------------|-------------------------------------------------------|
| Funktion                                             | BESCHREIBUNG                                           |
| [**QueryProtectedPolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprotectedpolicy) | Fragt den Wert ab, der einer geschützten Richtlinie zugeordnet ist. |
| [**SetProtectedPolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprotectedpolicy)     | Legt eine geschützte Richtlinie fest.                              |



 

## <a name="thread-functions"></a>Threadfunktionen

Die folgenden Funktionen werden mit Threads [verwendet.](multiple-threads.md)



| Funktion                                                           | BESCHREIBUNG                                                                                                                                               |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput)                     | Angefügt den Eingabeverarbeitungsmechanismus eines Threads an den eines anderen Threads.                                                                          |
| [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)                   | Erstellt einen Thread, der im virtuellen Adressraum eines anderen Prozesses ausgeführt wird.                                                                               |
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)               | Erstellt einen Thread, der im virtuellen Adressraum eines anderen Prozesses ausgeführt wird und optional erweiterte Attribute wie Prozessorgruppenaffinität angibt. |
| [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)                               | Erstellt einen Thread, der innerhalb des virtuellen Adressraums des aufrufenden Prozesses ausgeführt werden soll.                                                                      |
| [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)                                   | Beendet den aufrufenden Thread.                                                                                                                                  |
| [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread)                       | Ruft ein Pseudohand handle für den aktuellen Thread ab.                                                                                                         |
| [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid)                   | Ruft den Threadbezeichner des aufrufenden Threads ab.                                                                                                    |
| [**GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread)                     | Ruft den Beendigungsstatus des angegebenen Threads ab.                                                                                                 |
| [**GetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-getthreaddescription)               | Ruft die Beschreibung ab, die einem Thread durch Aufrufen von [**SetThreadDescription zugewiesen wurde.**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription)                                  |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)           | Ruft die Prozessorgruppenaffinität des angegebenen Threads ab.                                                                                           |
| [**GetThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadid)                                 | Ruft den Threadbezeichner des angegebenen Threads ab.                                                                                                  |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)     | Ruft die Prozessornummer des idealen Prozessors für den angegebenen Thread ab.                                                                           |
| [**GetThreadInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadinformation)               | Ruft Informationen zum angegebenen Thread ab.                                                                                                         |
| [**GetThreadIOPendingFlag**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadiopendingflag)           | Bestimmt, ob für einen angegebenen Thread E/A-Anforderungen ausstehend sind.                                                                                       |
| [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority)                     | Ruft den Prioritätswert für den angegebenen Thread ab.                                                                                                    |
| [**GetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost)           | Ruft den Steuerungszustand der Prioritätssteigerung des angegebenen Threads ab.                                                                                       |
| [**GetThreadTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadtimes)                           | Ruft Zeitsteuerungsinformationen für den angegebenen Thread ab.                                                                                                    |
| [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)                                   | Öffnet ein vorhandenes Threadobjekt.                                                                                                                          |
| [**QueryIdleProcessorCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime) | Ruft die Zykluszeit für den Leerlaufthread jedes Prozessors im System ab.                                                                             |
| [**QueryThreadCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-querythreadcycletime)               | Ruft die Zykluszeit für den angegebenen Thread ab.                                                                                                        |
| [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)                               | Dekrementiert die Anzahl der Angehaltene eines Threads.                                                                                                                      |
| [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask)             | Legt eine Prozessoraffinitätsmaske für den angegebenen Thread fest.                                                                                                  |
| [**SetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription)               | Weist einem Thread eine Beschreibung zu.                                                                                                                        |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)           | Legt die Prozessorgruppenaffinität für den angegebenen Thread fest.                                                                                               |
| [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor)         | Gibt einen bevorzugten Prozessor für einen Thread an.                                                                                                             |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)     | Legt den idealen Prozessor für den angegebenen Thread fest und ruft optional den vorherigen idealen Prozessor ab.                                                  |
| [**SetThreadInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation)               | Legt Informationen für den angegebenen Thread fest.                                                                                                                |
| [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)                     | Legt den Prioritätswert für den angegebenen Thread fest.                                                                                                         |
| [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost)           | Deaktiviert die Fähigkeit des Systems, die Priorität eines Threads vorübergehend zu erhöhen.                                                                         |
| [**SetThreadStackGuarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee)         | Legt die Stapelgarantie für den aufrufenden Thread fest.                                                                                                          |
| [**Schlafen**](/windows/win32/api/synchapi/nf-synchapi-sleep)                                             | Unterbricht die Ausführung des aktuellen Threads für ein angegebenes Intervall.                                                                                    |
| [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)                                         | Hält den aktuellen Thread an, bis die angegebene Bedingung erfüllt ist.                                                                                         |
| [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread)                             | Unterbricht den angegebenen Thread.                                                                                                                            |
| [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)                           | Bewirkt, dass der aufrufende Thread die Ausführung an einen anderen Thread übergibt, der auf dem aktuellen Prozessor ausgeführt werden kann.                                             |
| [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)                         | Beendet einen Thread.                                                                                                                                      |
| [**ThreadProc**](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))                                   | Eine anwendungsdefinierte Funktion, die als Startadresse für einen Thread dient.                                                                         |
| [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc)                                       | Ordnet einen TLS-Index (Thread Local Storage) zu.                                                                                                             |
| [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree)                                         | Gibt einen TLS-Index frei.                                                                                                                                     |
| [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue)                                 | Ruft den Wert im TLS-Slot des aufrufenden Threads für einen angegebenen TLS-Index ab.                                                                           |
| [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue)                                 | Speichert einen Wert im TLS-Slot des aufrufenden Threads für einen angegebenen TLS-Index.                                                                                |
| [**Waitforinputidle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle)                       | Wartet, bis der angegebene Prozess auf Benutzereingaben wartet, ohne dass eine Eingabe aussteht, oder bis das Time out-Intervall abgelaufen ist.                            |



 

## <a name="process-and-thread-extended-attribute-functions"></a>Erweiterte Attributfunktionen für Prozesse und Threads

Die folgenden Funktionen werden verwendet, um erweiterte Attribute für die Prozess- und Threaderstellung festzulegen.



| Funktion                                                                       | BESCHREIBUNG                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DeleteProcThreadAttributeList**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-deleteprocthreadattributelist)         | Löscht die angegebene Liste von Attributen für die Prozess- und Threaderstellung.                            |
| [**InitializeProcThreadAttributeList**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist) | Initialisiert die angegebene Liste von Attributen für die Prozess- und Threaderstellung.                        |
| [**UpdateProcThreadAttribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute)                 | Aktualisiert das angegebene Attribut in der angegebenen Attributliste für die Prozess- und Threaderstellung. |



 

## <a name="wow64-functions"></a>WOW64-Funktionen

Die folgenden Funktionen werden mit [WOW64](../winprog64/running-32-bit-applications.md)verwendet.



| Funktion                                         | BESCHREIBUNG                                                                                                                            |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**IsWow64Message**](/windows/desktop/api/Winuser/nf-winuser-iswow64message)         | Bestimmt, ob die letzte aus der Warteschlange des aktuellen Threads gelesene Nachricht von einem WOW64-Prozess stammt.                              |
| [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)         | Bestimmt, ob der angegebene Prozess unter WOW64 ausgeführt wird.                                                                       |
| [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2)       | Bestimmt, ob der angegebene Prozess unter WOW64 ausgeführt wird. gibt auch zusätzliche Informationen zum Computerprozess und zur Architektur zurück. |
| [**Wow64SuspendThread**](/windows/desktop/api/WinBase/nf-winbase-wow64suspendthread) | Unterbricht den angegebenen WOW64-Thread.                                                                                                   |



 

## <a name="job-object-functions"></a>Auftragsobjektfunktionen

Die folgenden Funktionen werden mit [Auftragsobjekten](job-objects.md)verwendet.



| Funktion                                                       | BESCHREIBUNG                                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject)   | Ordnet einen Prozess einem vorhandenen Auftragsobjekt zu.                                                    |
| [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)                     | Erstellt oder öffnet ein Auftragsobjekt.                                                                       |
| [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)                       | Bestimmt, ob der Prozess im angegebenen Auftrag ausgeführt wird.                                      |
| [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta)                         | Öffnet ein vorhandenes Auftragsobjekt.                                                                        |
| [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) | Ruft Limit- und Auftragszustandsinformationen aus dem Auftragsobjekt ab.                                       |
| [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)     | Legen Sie Grenzwerte für ein Auftragsobjekt fest.                                                                         |
| [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject)               | Beendet alle Prozesse, die dem Auftrag derzeit zugeordnet sind.                                          |
| [**UserHandleGrantAccess**](/windows/desktop/api/Winuser/nf-winuser-userhandlegrantaccess)         | Gewährt oder verweigert einem Auftrag, für den eine Benutzerschnittstelleneinschränkung gilt, Zugriff auf ein Handle für ein Benutzerobjekt. |



 

## <a name="thread-pool-functions"></a>Threadpoolfunktionen

Die folgenden Funktionen werden mit [Threadpools](thread-pools.md)verwendet.



| Funktion                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallbackMayRunLong**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-callbackmayrunlong)                                           | Gibt an, dass der Rückruf möglicherweise nicht schnell zurückgegeben wird.                                                                                                                                                                                                 |
| [**CancelThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio)                                           | Bricht die Benachrichtigung über die [**StartThreadpoolIo-Funktion**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio) ab.                                                                                                                                                          |
| [**CloseThreadpool**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool)                                                 | Schließt den angegebenen Threadpool.                                                                                                                                                                                                                   |
| [**CloseThreadpoolCleanupGroup**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup)                         | Schließt die angegebene Bereinigungsgruppe.                                                                                                                                                                                                                 |
| [**Closethreadpoolcleanupgroupmembers**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers)           | Gibt die Mitglieder der angegebenen Bereinigungsgruppe frei, wartet auf den Abschluss aller Rückruffunktionen und bricht optional alle ausstehenden Rückruffunktionen ab.                                                                                       |
| [**CloseThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolio)                                             | Gibt das angegebene E/A-Abschlussobjekt frei.                                                                                                                                                                                                       |
| [**CloseThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer)                                       | Gibt das angegebene Timerobjekt frei.                                                                                                                                                                                                                |
| [**CloseThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait)                                         | Gibt das angegebene Warteobjekt frei.                                                                                                                                                                                                                 |
| [**CloseThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork)                                         | Gibt das angegebene Arbeitsobjekt frei.                                                                                                                                                                                                                 |
| [**CreateThreadpool**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool)                                               | Ordnet einen neuen Threadpool zu, um Rückrufe auszuführen.                                                                                                                                                                                               |
| [**CreateThreadpoolCleanupGroup**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup)                       | Erstellt eine Bereinigungsgruppe, mit der Anwendungen einen oder mehrere Threadpoolrückrufe nachverfolgen können.                                                                                                                                                       |
| [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio)                                           | Erstellt ein neues E/A-Abschlussobjekt.                                                                                                                                                                                                                |
| [**CreateThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer)                                     | Erstellt ein neues Timerobjekt.                                                                                                                                                                                                                         |
| [**CreateThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait)                                       | Erstellt ein neues Warteobjekt.                                                                                                                                                                                                                          |
| [**CreateThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork)                                       | Erstellt ein neues Arbeitsobjekt.                                                                                                                                                                                                                          |
| [**DestroyThreadpoolEnvironment**](/windows/desktop/api/WinBase/nf-winbase-destroythreadpoolenvironment)                       | Löscht die angegebene Rückrufumgebung. Rufen Sie diese Funktion auf, wenn die Rückrufumgebung zum Erstellen neuer Threadpoolobjekte nicht mehr benötigt wird.                                                                                              |
| [**DisassociateCurrentThreadFromCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-disassociatecurrentthreadfromcallback)     | Entfernt die Zuordnung zwischen der derzeit ausgeführten Rückruffunktion und dem Objekt, das den Rückruf initiiert hat. Der aktuelle Thread zählt nicht mehr als Ausführen eines Rückrufs im Namen des Objekts.                                      |
| [**FreeLibraryWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns)                   | Gibt die DLL an, die der Threadpool entlädt, wenn der aktuelle Rückruf abgeschlossen ist.                                                                                                                                                             |
| [**InitializeThreadpoolEnvironment**](/windows/desktop/api/WinBase/nf-winbase-initializethreadpoolenvironment)                 | Initialisiert eine Rückrufumgebung.                                                                                                                                                                                                                 |
| [**IsThreadpoolTimerSet**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-isthreadpooltimerset)                                       | Bestimmt, ob das angegebene Timerobjekt derzeit festgelegt ist.                                                                                                                                                                                     |
| [**LeaveCriticalSectionWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-leavecriticalsectionwhencallbackreturns) | Gibt den kritischen Abschnitt an, den der Threadpool nach Abschluss des aktuellen Rückrufs freigibt.                                                                                                                                               |
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)                 | Ruft die Stapelreserve- und Commitgrößen für Threads im angegebenen Threadpool ab.                                                                                                                                                              |
| [**ReleaseMutexWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasemutexwhencallbackreturns)                 | Gibt den Mutex an, den der Threadpool nach Abschluss des aktuellen Rückrufs freigibt.                                                                                                                                                          |
| [**ReleaseSemaphoreWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasesemaphorewhencallbackreturns)         | Gibt das Semaphor an, das der Threadpool nach Abschluss des aktuellen Rückrufs freigibt.                                                                                                                                                      |
| [**SetEventWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-seteventwhencallbackreturns)                         | Gibt das Ereignis an, das vom Threadpool festgelegt wird, wenn der aktuelle Rückruf abgeschlossen ist.                                                                                                                                                              |
| [**SetThreadpoolCallbackCleanupGroup**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackcleanupgroup)             | Ordnet die angegebene Bereinigungsgruppe der angegebenen Rückrufumgebung zu.                                                                                                                                                                     |
| [**SetThreadpoolCallbackLibrary**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbacklibrary)                       | Stellt sicher, dass die angegebene DLL geladen bleibt, solange ausstehende Rückrufe bestehen.                                                                                                                                                           |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)                 | Gibt an, dass der Rückruf in einem persistenten Thread ausgeführt werden soll.                                                                                                                                                                                      |
| [**SetThreadpoolCallbackPool**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpool)                             | Legt den Threadpool fest, der beim Generieren von Rückrufen verwendet werden soll.                                                                                                                                                                                          |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)                     | Gibt die Priorität einer Rückruffunktion relativ zu anderen Arbeitselementen im selben Threadpool an.                                                                                                                                                 |
| [**SetThreadpoolCallbackRunsLong**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackrunslong)                     | Gibt an, dass Rückrufe, die dieser Rückrufumgebung zugeordnet sind, möglicherweise nicht schnell zurückgeben.                                                                                                                                                          |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)                     | Legt die Stapelreserve- und Commitgrößen für neue Threads im angegebenen Threadpool fest.                                                                                                                                                               |
| [**SetThreadpoolThreadMaximum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum)                           | Legt die maximale Anzahl von Threads fest, die der angegebene Threadpool Prozessrückrufen zuordnen kann.                                                                                                                                                |
| [**SetThreadpoolThreadMinimum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum)                           | Legt die Mindestanzahl von Threads fest, die der angegebene Threadpool für die Verarbeitung von Rückrufen zur Verfügung stellen muss.                                                                                                                                         |
| [**SetThreadpoolTimerEx**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimerex)                                       | Legt das Timerobjekt fest. Ein Arbeitsthread ruft den Rückruf des Timerobjekts auf, nachdem das angegebene Timeout abgelaufen ist.                                                                                                                                       |
| [**SetThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer)                                           | Legt das Timerobjekt fest. Ein Arbeitsthread ruft den Rückruf des Timerobjekts auf, nachdem das angegebene Timeout abgelaufen ist.                                                                                                                                       |
| [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait)                                             | Legt das Wait-Objekt fest. Ein Arbeitsthread ruft die Rückruffunktion des Wait-Objekts auf, nachdem das Handle signalisiert oder das angegebene Timeout abgelaufen ist.                                                                                           |
| [**SetThreadpoolWaitEx**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwaitex)                                         | Legt das Wait-Objekt fest. Ein Arbeitsthread ruft die Rückruffunktion des Wait-Objekts auf, nachdem das Handle signalisiert oder das angegebene Timeout abgelaufen ist.                                                                                           |
| [**StartThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio)                                             | Benachrichtigt den Threadpool, dass E/A-Vorgänge möglicherweise für das angegebene E/A-Abschlussobjekt beginnen können. Ein Arbeitsthread ruft die Rückruffunktion des E/A-Abschlussobjekts auf, nachdem der Vorgang für das an dieses Objekt gebundene Dateihandler abgeschlossen wurde. |
| [**SubmitThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork)                                       | Veröffentlicht ein Arbeitsobjekt an den Threadpool. Ein Arbeitsthread ruft die Rückruffunktion des Arbeitsobjekts auf.                                                                                                                                                  |
| [**TpInitializeCallbackEnviron**](/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron)                         | Initialisiert eine Rückrufumgebung für den Threadpool.                                                                                                                                                                                             |
| [**TpDestroyCallbackEnviron**](/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron)                               | Löscht die angegebene Rückrufumgebung. Rufen Sie diese Funktion auf, wenn die Rückrufumgebung zum Erstellen neuer Threadpoolobjekte nicht mehr benötigt wird.                                                                                              |
| [**TpSetCallbackActivationContext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext)                   | Weist der Rückrufumgebung einen Aktivierungskontext zu.                                                                                                                                                                                          |
| [**TpSetCallbackCleanupGroup**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup)                             | Ordnet die angegebene Bereinigungsgruppe der angegebenen Rückrufumgebung zu.                                                                                                                                                                     |
| [**TpSetCallbackFinalizationCallback**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback)             | Gibt eine Funktion an, die beim Abschluss der Rückrufumgebung aufruft werden soll.                                                                                                                                                                            |
| [**TpSetCallbackLongFunction**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction)                             | Gibt an, dass Rückrufe, die dieser Rückrufumgebung zugeordnet sind, möglicherweise nicht schnell zurückgeben.                                                                                                                                                          |
| [**TpSetCallbackNoActivationContext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext)               | Gibt an, dass die Rückrufumgebung über keinen Aktivierungskontext verfügt.                                                                                                                                                                                  |
| [**TpSetCallbackPersistent**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent)                                 | Gibt an, dass der Rückruf in einem persistenten Thread ausgeführt werden soll.                                                                                                                                                                                      |
| [**TpSetCallbackPriority**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority)                                     | Gibt die Priorität einer Rückruffunktion relativ zu anderen Arbeitselementen im selben Threadpool an.                                                                                                                                                 |
| [**TpSetCallbackRaceWithDll**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll)                               | Stellt sicher, dass die angegebene DLL geladen bleibt, solange ausstehende Rückrufe bestehen.                                                                                                                                                           |
| [**TpSetCallbackThreadpool**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool)                                 | Weist einer Rückrufumgebung einen Threadpool zu.                                                                                                                                                                                                    |
| [**TrySubmitThreadpoolCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-trysubmitthreadpoolcallback)                         | Fordert an, dass ein Threadthread des Threadpools die angegebene Rückruffunktion aufruft.                                                                                                                                                                     |
| [**WaitForThreadpoolIoCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooliocallbacks)                       | Wartet auf den Abschluss ausstehender E/A-Abschlussrückrufe und bricht optional ausstehende Rückrufe ab, die noch nicht ausgeführt wurden.                                                                                                           |
| [**WaitForThreadpoolTimerCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks)                 | Wartet auf den Abschluss ausstehender Timerrückrufe und bricht optional ausstehende Rückrufe ab, deren Ausführung noch nicht gestartet wurde.                                                                                                                    |
| [**WaitForThreadpoolWaitCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks)                   | Wartet auf den Abschluss ausstehender Warterückrufe und bricht optional ausstehende Rückrufe ab, die noch nicht ausgeführt wurden.                                                                                                                     |
| [**WaitForThreadpoolWorkCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolworkcallbacks)                   | Wartet auf den Abschluss ausstehender Arbeitsrückrufe und bricht optional ausstehende Rückrufe ab, die noch nicht ausgeführt wurden.                                                                                                                     |



 

Die folgenden Funktionen sind Teil der ursprünglichen [Threadpooling-API.](thread-pooling.md)



| Funktion                                                            | BESCHREIBUNG                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)        | Ordnet den E/A-Abschlussport im Besitz des Threadpools dem angegebenen Dateihandle zu. Nach Abschluss einer E/A-Anforderung mit dieser Datei führt ein Nicht-E/A-Arbeitsthread die angegebene Rückruffunktion aus. |
| [**Queueuserworkitem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                      | Reiht ein Arbeitselement in die Warteschlange eines Arbeitsthreads im Threadpool ein.                                                                                                                                                              |
| [**Registerwaitforsingleobject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) | Weist einen Wartethread im Threadpool an, auf das Objekt zu warten.                                                                                                                                                        |
| [**UnregisterWaitEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-unregisterwaitex)                       | Wartet, bis eines oder alle angegebenen Objekte im signalisierten Zustand sind oder das Time out-Intervall verstrichen ist.                                                                                                            |



 

## <a name="thread-ordering-service-functions"></a>Funktionen des Threadreihenfolgediensts

Die folgenden Funktionen werden mit dem [Threadreihenfolgedienst](thread-ordering-service.md)verwendet.



| Funktion                                                                   | BESCHREIBUNG                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**AvQuerySystemResponsiveness**](/windows/desktop/api/Avrt/nf-avrt-avquerysystemresponsiveness)         | Ruft die Vom Multimediaklassenplanerdienst verwendete Einstellung für die Systemreaktionsfähigkeit ab. |
| [**AvRtCreateThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup)     | Erstellt eine Threadreihenfolgegruppe.                                                            |
| [**AvRtCreateThreadOrderingGroupEx**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroupexa) | Erstellt eine Threadreihenfolgegruppe und ordnet den Serverthread einer Aufgabe zu.               |
| [**AvRtDeleteThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup)     | Löscht die angegebene Threadreihenfolgegruppe, die vom Aufrufer erstellt wurde.                          |
| [**AvRtJoinThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup)         | Verbindet Clientthreads mit einer Threadreihenfolgegruppe.                                            |
| [**AvRtLeaveThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup)       | Ermöglicht Clientthreads, eine Threadreihenfolgegruppe zu verlassen.                                    |
| [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup)     | Ermöglicht Es Clientthreads einer Threadreihenfolgegruppe, zu warten, bis sie ausgeführt werden sollen.        |



 

## <a name="multimedia-class-scheduler-service-functions"></a>Funktionen des Multimedia-Klassenplanerdiensts

Die folgenden Funktionen werden mit dem [Multimediaklassenplanerdienst](multimedia-class-scheduler-service.md)verwendet.



| Funktion                                                                   | BESCHREIBUNG                                                                                           |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**AvRevertMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avrevertmmthreadcharacteristics) | Gibt an, dass ein Thread keine Der angegebenen Aufgabe zugeordneten Aufgaben mehr ausführt.              |
| [**AvSetMmMaxThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) | Ordnet den aufrufenden Thread den angegebenen Aufgaben zu.                                               |
| [**AvSetMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa)       | Ordnet den aufrufenden Thread der angegebenen Aufgabe zu.                                                |
| [**AvSetMmThreadPriority**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority)                     | Passt die Threadpriorität des aufrufenden Threads relativ zu anderen Threads an, die dieselbe Aufgabe ausführen. |



 

## <a name="fiber-functions"></a>Fiberfunktionen

Die folgenden Funktionen werden mit [Fibers](fibers.md)verwendet.



| Funktion                                                 | BESCHREIBUNG                                                                                                  |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**ConvertFiberToThread**](/windows/desktop/api/WinBase/nf-winbase-convertfibertothread)     | Konvertiert die aktuelle Fiber in einen Thread.                                                                    |
| [**ConvertThreadToFiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber)     | Konvertiert den aktuellen Thread in eine Fiber.                                                                    |
| [**ConvertThreadToFiberEx**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiberex) | Konvertiert den aktuellen Thread in eine Fiber.                                                                    |
| [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber)                       | Ordnet ein Fiberobjekt zu, weist ihm einen Stapel zu und richtet die Ausführung ein, um an der angegebenen Startadresse zu beginnen. |
| [**CreateFiberEx**](/windows/desktop/api/WinBase/nf-winbase-createfiberex)                   | Ordnet ein Fiberobjekt zu, weist ihm einen Stapel zu und richtet die Ausführung ein, um an der angegebenen Startadresse zu beginnen. |
| [**DeleteFiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber)                       | Löscht eine vorhandene Fiber.                                                                                   |
| [**FiberProc**](/windows/win32/api/winbase/nc-winbase-pfiber_start_routine)                           | Eine anwendungsdefinierte Funktion, die mit der [**CreateFiber-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfiber) verwendet wird.                   |
| [**FlsAlloc**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc)                             | Ordnet einen Fibre Local Storage-Index (FLS) zu.                                                                 |
| [**FlsFree**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree)                               | Gibt einen FLS-Index frei.                                                                                       |
| [**FlsGetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)                       | Ruft den Wert im FLS-Slot der aufrufenden Fiber für einen angegebenen FLS-Index ab.                               |
| [**FlsSetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)                       | Speichert einen Wert im FLS-Slot der aufrufenden Fiber für einen angegebenen FLS-Index.                                    |
| [**IsThreadAFiber**](/windows/win32/api/fibersapi/nf-fibersapi-isthreadafiber)                 | Bestimmt, ob der aktuelle Thread eine Fiber ist.                                                            |
| [**SwitchToFiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber)                   | Plant eine Fiber.                                                                                           |



 

## <a name="numa-support-functions"></a>NUMA-Unterstützungsfunktionen

Die folgenden Funktionen bieten [NUMA-Unterstützung.](numa-support.md)



| Funktion                                                                 | BESCHREIBUNG                                                                                                                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)  | Reserviert oder committet einen Speicherbereich innerhalb des virtuellen Adressraums des angegebenen Prozesses und gibt den NUMA-Knoten für den physischen Speicher an. |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Ruft Informationen zu logischen Prozessoren und zugehöriger Hardware ab.                                                                                   |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)         | Ruft den im angegebenen Knoten verfügbaren Arbeitsspeicher ab.                                                                                        |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)     | Ruft die Arbeitsspeichermenge ab, die im angegebenen Knoten als USHORT-Wert verfügbar ist.                                                              |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)             | Ruft den Knoten ab, der derzeit über die höchste Zahl verfügt.                                                                                              |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)       | Ruft den NUMA-Knoten ab, der dem zugrunde liegenden Gerät für ein Dateihandle zugeordnet ist.                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)             | Ruft die Prozessormaske für den angegebenen Knoten ab.                                                                                                   |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)         | Ruft die Prozessormaske für den angegebenen NUMA-Knoten als USHORT-Wert ab.                                                                            |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                     | Ruft die Knotennummer für den angegebenen Prozessor ab.                                                                                                 |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                 | Ruft die Knotennummer des angegebenen logischen Prozessors als USHORT-Wert ab.                                                                        |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                     | Ruft die Knotennummer für den angegebenen Näherungsbezeichner ab.                                                                                      |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                 | Ruft die Knotennummer als USHORT-Wert für den angegebenen Näherungsbezeichner ab.                                                                    |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                        | Reserviert einen Speicherbereich innerhalb des virtuellen Adressraums des angegebenen Prozesses oder führt einen Commit aus und gibt den NUMA-Knoten für den physischen Speicher an. |



 

## <a name="processor-functions"></a>Prozessorfunktionen

Die folgenden Funktionen werden mit logischen Prozessoren und [Prozessorgruppen verwendet.](processor-groups.md)



| Funktion                                                                     | BESCHREIBUNG                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)                   | Gibt die Anzahl der aktiven Prozessoren in einer Prozessorgruppe oder im System zurück.                                       |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)         | Gibt die Anzahl der aktiven Prozessorgruppen im System zurück.                                                         |
| [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)               | Ruft die Anzahl des Prozessors ab, auf dem der aktuelle Thread während des Aufrufs dieser Funktion ausgeführt wurde.            |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)           | Ruft die Prozessorgruppe und die Nummer des logischen Prozessors ab, in dem der aufrufende Thread ausgeführt wird.            |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Ruft Informationen zu logischen Prozessoren und zugehöriger Hardware ab.                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Ruft Informationen über die Beziehungen von logischen Prozessoren und zugehöriger Hardware ab.                            |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)                 | Gibt die maximale Anzahl logischer Prozessoren zurück, über die eine Prozessorgruppe oder das System verfügen kann.                      |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)       | Gibt die maximale Anzahl von Prozessorgruppen zurück, über die das System verfügen kann.                                             |
| [**QueryIdleProcessorCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime)           | Ruft die Zykluszeit für den Leerlaufthread jedes Prozessors im System ab.                                        |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)       | Ruft die akkumulierte Zykluszeit für den Leerlaufthread auf jedem logischen Prozessor in der angegebenen Prozessorgruppe ab. |



 

## <a name="user-mode-scheduling-functions"></a>User-Mode Planungsfunktionen

Die folgenden Funktionen werden bei der Benutzermodusplanung (UMS) verwendet.



| Funktion                                                               | BESCHREIBUNG                                                                                               |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)             | Erstellt eine UMS-Vervollständigungsliste.                                                                            |
| [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)               | Erstellt einen UMS-Threadkontext zur Darstellung eines UMS-Arbeitsthreads.                                            |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)             | Löscht die angegebene UMS-Vervollständigungsliste. Die Liste muss leer sein.                                        |
| [**DeleteUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)               | Löscht den angegebenen UMS-Threadkontext. Der Thread muss beendet werden.                                  |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) | Ruft UMS-Arbeitsthreads aus der angegebenen UMS-Vervollständigungsliste ab.                                      |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)               | Konvertiert den aufrufenden Thread in einen UMS-Planerthread.                                                  |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)                           | Führt den angegebenen UMS-Arbeitsthread aus.                                                                     |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)                     | Gibt den UMS-Threadkontext des aufrufenden UMS-Threads zurück.                                                 |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)                       | Gibt den nächsten UMS-Threadkontext in einer Liste von UMS-Threadkontexten zurück.                                     |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)         | Ruft ein Handle für das Ereignis ab, das der angegebenen UMS-Vervollständigungsliste zugeordnet ist.                        |
| [**GetUmsSystemThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-getumssystemthreadinformation) | Fragt ab, ob der angegebene Thread ein UMS-Planerthread, ein UMS-Arbeitsthread oder ein Nicht-UMS-Thread ist. |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)         | Ruft Informationen zum angegebenen UMS-Arbeitsthread ab.                                              |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)             | Legt anwendungsspezifische Kontextinformationen für den angegebenen UMS-Arbeitsthread fest.                        |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)                             | Die anwendungsdefinierte UMS-Planereinstiegspunktfunktion, die einer UMS-Vervollständigungsliste zugeordnet ist.         |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)                               | Gibt die Steuerung an den UMS-Planerthread zurück, in dem der aufrufende UMS-Arbeitsthread ausgeführt wird.             |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

-   [**NtGetCurrentProcessorNumber**](ntgetcurrentprocessornumber.md)
-   [**NtQueryInformationProcess**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationprocess)
-   [**NtQueryInformationThread**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationthread)
-   [**WinExec**](/windows/desktop/api/WinBase/nf-winbase-winexec)
-   [**ZwQueryInformationProcess**](zwqueryinformationprocess.md)

 

 
