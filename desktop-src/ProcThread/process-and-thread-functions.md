---
description: In diesem Thema werden die Prozess-und Thread Funktionen beschrieben.
ms.assetid: 8c8e8af0-bf50-4a4b-945c-83bae1eff7dd
title: Prozess- und Threadfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97d871c7fc3635734ce79ba5cbf231e6955e59d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216013"
---
# <a name="process-and-thread-functions"></a>Prozess- und Threadfunktionen

In diesem Thema werden die Prozess-und Thread Funktionen beschrieben.

-   [Dispatchqueue-Funktion](#dispatch-queue-function)
-   [Prozessfunktionen](#process-functions)
-   [Verarbeiten von Enumerationsfunktionen](#process-enumeration-functions)
-   [Richtlinien Funktionen](#policy-functions)
-   [Thread Funktionen](#thread-functions)
-   [Prozess-und Thread Funktionen für erweiterte Attribute](#process-and-thread-extended-attribute-functions)
-   [WOW64-Funktionen](#wow64-functions)
-   [Auftrags Objektfunktionen](#job-object-functions)
-   [Thread Pool Funktionen](#thread-pool-functions)
-   [Dienstfunktionen für die Thread Bestellung](#thread-ordering-service-functions)
-   [Dienstfunktionen für Multimedia-Klassen Planer](#multimedia-class-scheduler-service-functions)
-   [Fiber-Funktionen](#fiber-functions)
-   [NUMA-Unterstützungsfunktionen](#numa-support-functions)
-   [Prozessor Funktionen](#processor-functions)
-   [Zeit Planungsfunktionen im Benutzermodus](#user-mode-scheduling-functions)
-   [Veraltete Funktionen](#obsolete-functions)

## <a name="dispatch-queue-function"></a>Dispatchqueue-Funktion

Die folgende Funktion erstellt einen [dispatcherqueuecontroller](/uwp/api/windows.system.dispatcherqueuecontroller).



| Funktion                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreatedispatcherqueuecontroller"**](/windows/desktop/api/DispatcherQueue/nf-dispatcherqueue-createdispatcherqueuecontroller) | Erstellt einen [dispatcherqueuecontroller](/uwp/api/windows.system.dispatcherqueuecontroller) , der die Lebensdauer einer [DispatcherQueue](/uwp/api/windows.system.dispatcherqueue) verwaltet, die in der Reihenfolge der Priorität in einem anderen Thread Aufgaben in der Warteschlange ausführt. |



 

## <a name="process-functions"></a>Prozessfunktionen

Die folgenden Funktionen werden für- [Prozesse](child-processes.md)verwendet.



| Funktion                                                                 | BESCHREIBUNG                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)                                   | Erstellt einen neuen Prozess und seinen primären Thread.                                                                                                                                                 |
| [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)                       | Erstellt einen neuen Prozess und seinen primären Thread. Der neue Prozess wird im Sicherheitskontext des Benutzers ausgeführt, der durch das angegebene Token dargestellt wird.                                                    |
| [**"Kreateprocesswithlogonw"**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw)               | Erstellt einen neuen Prozess und seinen primären Thread. Der neue Prozess führt dann die angegebene ausführbare Datei im Sicherheitskontext der angegebenen Anmelde Informationen (Benutzer, Domäne und Kennwort) aus.      |
| [**"Kreateprocesswithper kenw"**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithtokenw)               | Erstellt einen neuen Prozess und seinen primären Thread. Der neue Prozess wird im Sicherheitskontext des angegebenen Tokens ausgeführt.                                                                            |
| [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)                                       | Beendet den aufrufenden Prozess und alle zugehörigen Threads.                                                                                                                                                 |
| [**Flushprocessbeschreib tebuffers**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushprocesswritebuffers)             | Leert die Schreib Warteschlange jedes Prozessors, der einen Thread des aktuellen Prozesses ausgeführt hat.                                                                                                    |
| [**Frei Handzeichen folgen**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa)                 | Gibt einen Block von Umgebungs Zeichenfolgen frei.                                                                                                                                                         |
| [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea)                                 | Ruft die Befehlszeilenzeichenfolge für den aktuellen Prozess ab.                                                                                                                                    |
| [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess)                           | Ruft ein Pseudo Handle für den aktuellen Prozess ab.                                                                                                                                            |
| [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid)                       | Ruft den Prozess Bezeichner des aufrufenden Prozesses ab.                                                                                                                                      |
| [**Getcurrentprocessornumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)           | Ruft die Nummer des Prozessors ab, auf dem der aktuelle Thread während des Aufrufens dieser Funktion ausgeführt wurde.                                                                                     |
| [**Getenvironmentstrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings)                   | Ruft den Umgebungsblock für den aktuellen Prozess ab.                                                                                                                                      |
| [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable)                 | Ruft den Wert der angegebenen Variablen aus dem Umgebungsblock des aufrufenden Prozesses ab.                                                                                              |
| [**GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess)                         | Ruft den Beendigungs Status des angegebenen Prozesses ab.                                                                                                                                    |
| [**Getguiresources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources)                               | Ruft die Anzahl von Handles für grafische Benutzeroberflächen Objekte (GUI) ab, die vom angegebenen Prozess verwendet werden.                                                                                     |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Ruft Informationen über logische Prozessoren und zugehörige Hardware ab.                                                                                                                          |
| [**Getpriorityclass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass)                             | Ruft die Prioritäts Klasse für den angegebenen Prozess ab.                                                                                                                                       |
| [**Getprocessaffinitymask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask)                 | Ruft eine prozessaffinitäts Maske für den angegebenen Prozess und die systemaffinitäts Maske für das System ab.                                                                                      |
| [**Getprocessgroupaffität**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)               | Ruft die Prozessor Gruppen Affinität des angegebenen Prozesses ab.                                                                                                                              |
| [**Getprocesshandlecount**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)                   | Ruft die Anzahl der geöffneten Handles ab, die zum angegebenen Prozess gehören.                                                                                                                    |
| [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)                                     | Ruft den Prozess Bezeichner des angegebenen Prozesses ab.                                                                                                                                    |
| [**Getprocessidofthread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread)                     | Ruft den Prozess Bezeichner des Prozesses ab, der dem angegebenen Thread zugeordnet ist.                                                                                                         |
| [**Getprocessiocounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters)                     | Ruft Buchhaltungsinformationen für alle e/a-Vorgänge ab, die vom angegebenen Prozess ausgeführt werden.                                                                                                   |
| [**Getprocessentschärationpolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy)         | Ruft Einstellungen für die Entschärfungs Richtlinie für den aufrufenden Prozess ab.                                                                                                                                 |
| [**Getprocesspriorityboost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost)               | Ruft den Prioritäts Steuerungs Zustand des angegebenen Prozesses ab.                                                                                                                          |
| [**Getprocessshutdownparameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessshutdownparameters)     | Ruft das Herunterfahren von Parametern für den aktuell aufrufenden Prozess ab.                                                                                                                              |
| [**GetProcessTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes)                               | Ruft Informationen zur zeitlichen Steuerung für den angegebenen Prozess ab.                                                                                                                                 |
| [**Getprocessversion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion)                           | Ruft die Haupt-und neben Versionsnummern des Systems ab, auf dem der angegebene Prozess die Ausführung erwartet.                                                                                    |
| [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize)             | Ruft die minimalen und maximalen workingsetgrößen des angegebenen Prozesses ab.                                                                                                                 |
| [**Getprocessworkingsetsizeex**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex)         | Ruft die minimalen und maximalen workingsetgrößen des angegebenen Prozesses ab.                                                                                                                 |
| [**Getprocessorsystemcycletime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)       | Ruft die Schleifen Zeit ab, die jeder Prozessor in der angegebenen Gruppe für das Ausführen von verzögerten Prozedur aufrufen (DPCs) und Interrupt-Dienst Routinen (ISRs) aufgewendet hat.                                         |
| [**Getstartupinfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow)                                 | Ruft den Inhalt der [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) -Struktur ab, die beim Erstellen des aufrufenden Prozesses angegeben wurde.                                                       |
| [**Isimmersiveprocess**](/windows/desktop/api/Winuser/nf-winuser-isimmersiveprocess)                         | Bestimmt, ob der Prozess zu einer Windows Store-App gehört.                                                                                                                                |
| [**Needcurrentdirectoriyforexepath**](/windows/win32/api/processenv/nf-processenv-needcurrentdirectoryforexepatha) | Bestimmt, ob das aktuelle Verzeichnis in den Suchpfad für die angegebene ausführbare Datei aufgenommen werden soll.                                                                                  |
| [**Bei OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)                                       | Öffnet ein vorhandenes lokales Prozess Objekt.                                                                                                                                                       |
| [**Queryfullprocessimagename**](/windows/desktop/api/WinBase/nf-winbase-queryfullprocessimagenamea)           | Ruft den vollständigen Namen des ausführbaren Images für den angegebenen Prozess ab.                                                                                                                    |
| [**Queryprocessaffinityupdatemode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprocessaffinityupdatemode) | Ruft den Affinitäts Aktualisierungs Modus für den angegebenen Prozess ab.                                                                                                                                  |
| [**Queryprocesskycletime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryprocesscycletime)                   | Ruft die Summe der Umlaufzeit aller Threads des angegebenen Prozesses ab.                                                                                                                  |
| [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable)                 | Legt den Wert einer Umgebungsvariablen für den aktuellen Prozess fest.                                                                                                                            |
| [**Setpriorityclass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass)                             | Legt die Prioritäts Klasse für den angegebenen Prozess fest.                                                                                                                                            |
| [**Setprocessaffinitymask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask)                 | Legt eine Prozessor Affinitäts Maske für die Threads eines angegebenen Prozesses fest.                                                                                                                        |
| [**Setprocessaffinityupdatemode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessaffinityupdatemode)     | Legt den Affinitäts Aktualisierungs Modus für den angegebenen Prozess fest.                                                                                                                                       |
| [**Setprocessinformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessinformation)                   | Legt Informationen für den angegebenen Prozess fest.                                                                                                                                                   |
| [**Setprocessentschärationpolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy)         | Legt die Entschärfungs Richtlinie für den aufrufenden Prozess fest.                                                                                                                                           |
| [**Setprocesspriorityboost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost)               | Deaktiviert die Fähigkeit des Systems, die Priorität der Threads des angegebenen Prozesses vorübergehend zu erhöhen.                                                                                 |
| [**Setprocessrestrictionbefreiung**](/windows/desktop/api/Winuser/nf-winuser-setprocessrestrictionexemption) | Gibt den aufrufenden Prozess von Einschränkungen aus, die verhindern, dass Desktop Prozesse mit der Windows Store-App-Umgebung interagieren. Diese Funktion wird von Entwicklungs-und Debugtools verwendet. |
| [**Setprocessshutdownparameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)     | Legt Parameter für das Herunterfahren für den aktuell aufrufenden Prozess fest.                                                                                                                                   |
| [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize)             | Legt die minimalen und maximalen workingsetgrößen für den angegebenen Prozess fest.                                                                                                                     |
| [**Setprocessworkingsetsizeex**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex)         | Legt die minimalen und maximalen workingsetgrößen für den angegebenen Prozess fest.                                                                                                                     |
| [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)                             | Beendet den angegebenen Prozess und alle zugehörigen Threads.                                                                                                                                      |



 

## <a name="process-enumeration-functions"></a>Verarbeiten von Enumerationsfunktionen

Die folgenden Funktionen werden zum Auflisten von Prozessen verwendet.



| Funktion                                                    | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Ruft den Prozess Bezeichner für jedes Prozess Objekt im System ab.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Ruft Informationen zum ersten Prozess ab, der in einer System Momentaufnahme aufgetreten ist.    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Ruft Informationen zum nächsten Prozess ab, der in einer System Momentaufnahme aufgezeichnet wurde.        |
| [**Wtsenum erateprocesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Ruft Informationen zu den aktiven Prozessen auf dem angegebenen Terminal Server ab. |



 

## <a name="policy-functions"></a>Richtlinien Funktionen

Die folgenden Funktionen werden mit der Prozess weiten Richtlinie verwendet.



|                                                      |                                                       |
|------------------------------------------------------|-------------------------------------------------------|
| Funktion                                             | BESCHREIBUNG                                           |
| [**Queryprotectedpolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprotectedpolicy) | Fragt den Wert ab, der einer geschützten Richtlinie zugeordnet ist. |
| [**Setprotectedpolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprotectedpolicy)     | Legt eine geschützte Richtlinie fest.                              |



 

## <a name="thread-functions"></a>Thread Funktionen

Die folgenden Funktionen werden mit [Threads](multiple-threads.md)verwendet.



| Funktion                                                           | BESCHREIBUNG                                                                                                                                               |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attachthreadinput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput)                     | Fügt den Eingabe Verarbeitungs Mechanismus eines Threads an die eines anderen Threads an.                                                                          |
| [**"Kreateremotethread"**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)                   | Erstellt einen Thread, der im virtuellen Adressraum eines anderen Prozesses ausgeführt wird.                                                                               |
| [**"Kreateremotethreadex"**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)               | Erstellt einen Thread, der im virtuellen Adressraum eines anderen Prozesses ausgeführt wird, und gibt optional Erweiterte Attribute an, wie z. b. Prozessor Gruppen Affinität. |
| [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)                               | Erstellt einen Thread, der innerhalb des virtuellen Adressraums des aufrufenden Prozesses ausgeführt werden soll.                                                                      |
| [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)                                   | Beendet den aufrufenden Thread.                                                                                                                                  |
| [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread)                       | Ruft ein Pseudo Handle für den aktuellen Thread ab.                                                                                                         |
| [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid)                   | Ruft den Thread Bezeichner des aufrufenden Threads ab.                                                                                                    |
| [**GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread)                     | Ruft den Beendigungs Status des angegebenen Threads ab.                                                                                                 |
| [**Getthreaddescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-getthreaddescription)               | Ruft die Beschreibung ab, die einem Thread durch Aufrufen von [**setthreaddescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription)zugewiesen wurde.                                  |
| [**Getthreadgroupaffität**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)           | Ruft die Prozessor Gruppen Affinität des angegebenen Threads ab.                                                                                           |
| [**GetThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadid)                                 | Ruft den Thread Bezeichner des angegebenen Threads ab.                                                                                                  |
| [**Getthreadidealprocessorex**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)     | Ruft die Prozessornummer des idealen Prozessors für den angegebenen Thread ab.                                                                           |
| [**Getthreadinformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadinformation)               | Ruft Informationen über den angegebenen Thread ab.                                                                                                         |
| [**Getthreadiopendingflag**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadiopendingflag)           | Bestimmt, ob ein angegebener Thread über ausstehende e/a-Anforderungen verfügt.                                                                                       |
| [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority)                     | Ruft den Prioritätswert für den angegebenen Thread ab.                                                                                                    |
| [**Getthreadpriorityboost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost)           | Ruft den Prioritäts Erhöhung-Steuerungs Zustand des angegebenen Threads ab.                                                                                       |
| [**Getthreadtimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadtimes)                           | Ruft Zeit Steuerungsinformationen für den angegebenen Thread ab.                                                                                                    |
| [**Openthread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)                                   | Öffnet ein vorhandenes Thread Objekt.                                                                                                                          |
| [**Queryidleprocessorcycletime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime) | Ruft die Umlaufzeit für den Leerlauf Thread jedes Prozessors im System ab.                                                                             |
| [**Querythreadcycletime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-querythreadcycletime)               | Ruft die Umlaufzeit für den angegebenen Thread ab.                                                                                                        |
| [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)                               | Dekrementierungen den anhaltezähler eines Threads.                                                                                                                      |
| [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask)             | Legt eine Prozessor Affinitäts Maske für den angegebenen Thread fest.                                                                                                  |
| [**SetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription)               | Weist einem Thread eine Beschreibung zu.                                                                                                                        |
| [**Setthreadgroupaffität**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)           | Legt die Prozessor Gruppen Affinität für den angegebenen Thread fest.                                                                                               |
| [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor)         | Gibt einen bevorzugten Prozessor für einen Thread an.                                                                                                             |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)     | Legt den idealen Prozessor für den angegebenen Thread fest und ruft optional den vorherigen idealen Prozessor ab.                                                  |
| [**Setthreadinformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation)               | Legt Informationen für den angegebenen Thread fest.                                                                                                                |
| [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)                     | Legt den Prioritätswert für den angegebenen Thread fest.                                                                                                         |
| [**Setthreadpriorityboost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost)           | Deaktiviert die Fähigkeit des Systems, die Priorität eines Threads vorübergehend zu erhöhen.                                                                         |
| [**Setthreadstackgarantie**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee)         | Legt die Stapel Garantie für den aufrufenden Thread fest.                                                                                                          |
| [**Standby**](/windows/win32/api/synchapi/nf-synchapi-sleep)                                             | Hält die Ausführung des aktuellen Threads für ein angegebenes Intervall an.                                                                                    |
| [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)                                         | Hält den aktuellen Thread an, bis die angegebene Bedingung erfüllt ist.                                                                                         |
| [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread)                             | Hält den angegebenen Thread an.                                                                                                                            |
| [**Switchthread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)                           | Bewirkt, dass der aufrufende Thread die Ausführung an einen anderen Thread übergibt, der auf dem aktuellen Prozessor ausgeführt werden kann.                                             |
| [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)                         | Beendet einen Thread.                                                                                                                                      |
| [**ThreadProc**](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))                                   | Eine Anwendungs definierte Funktion, die als Startadresse für einen Thread fungiert.                                                                         |
| [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc)                                       | Weist einen TLS-Index (Thread Local Storage) zu.                                                                                                             |
| [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree)                                         | Gibt einen TLS-Index frei.                                                                                                                                     |
| [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue)                                 | Ruft den Wert im TLS-Slot des aufrufenden Threads für einen angegebenen TLS-Index ab.                                                                           |
| [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue)                                 | Speichert einen Wert im TLS-Slot des aufrufenden Threads für einen angegebenen TLS-Index.                                                                                |
| [**WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle)                       | Wartet, bis der angegebene Prozess auf eine Benutzereingabe wartet, ohne dass eine Eingabe aussteht, oder bis das Timeout Intervall abgelaufen ist.                            |



 

## <a name="process-and-thread-extended-attribute-functions"></a>Prozess-und Thread Funktionen für erweiterte Attribute

Die folgenden Funktionen werden verwendet, um erweiterte Attribute für die Prozess-und Thread Erstellung festzulegen.



| Funktion                                                                       | BESCHREIBUNG                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Deleteprocthreadattributelist**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-deleteprocthreadattributelist)         | Löscht die angegebene Liste von Attributen für die Prozess-und Thread Erstellung.                            |
| [**Initializeprocthreadattributelist**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist) | Initialisiert die angegebene Liste der Attribute für die Prozess-und Thread Erstellung.                        |
| [**Updateprocthreadattribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute)                 | Aktualisiert das angegebene Attribut in der angegebenen Liste von Attributen für die Prozess-und Thread Erstellung. |



 

## <a name="wow64-functions"></a>WOW64-Funktionen

Die folgenden Funktionen werden mit [WOW64](../winprog64/running-32-bit-applications.md)verwendet.



| Funktion                                         | BESCHREIBUNG                                                                                                                            |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**IsWow64Message**](/windows/desktop/api/Winuser/nf-winuser-iswow64message)         | Bestimmt, ob die letzte aus der Warteschlange des aktuellen Threads gelesene Nachricht aus einem WOW64-Prozess stammt.                              |
| [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)         | Bestimmt, ob der angegebene Prozess unter WOW64 ausgeführt wird.                                                                       |
| [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2)       | Bestimmt, ob der angegebene Prozess unter WOW64 ausgeführt wird. gibt auch zusätzliche Informationen zum Computer Prozess und zur Architektur zurück. |
| [**Wow64SuspendThread**](/windows/desktop/api/WinBase/nf-winbase-wow64suspendthread) | Hält den angegebenen WOW64-Thread an.                                                                                                   |



 

## <a name="job-object-functions"></a>Auftrags Objektfunktionen

Die folgenden Funktionen werden mit [Auftrags Objekten](job-objects.md)verwendet.



| Funktion                                                       | BESCHREIBUNG                                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Zutragprozesstojobobject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject)   | Ordnet einem vorhandenen Auftrags Objekt einen Prozess zu.                                                    |
| [**"Kreatejobobject"**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)                     | Erstellt oder öffnet ein Auftrags Objekt.                                                                       |
| [**Isprocessinjob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)                       | Bestimmt, ob der Prozess im angegebenen Auftrag ausgeführt wird.                                      |
| [**Openjobobject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta)                         | Öffnet ein vorhandenes Auftrags Objekt.                                                                        |
| [**Queryinformationjobobject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) | Ruft Limit-und Auftrags Zustandsinformationen aus dem Auftrags Objekt ab.                                       |
| [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)     | Festlegen von Grenzwerten für ein Auftrags Objekt.                                                                         |
| [**Terminatejobobject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject)               | Beendet alle Prozesse, die momentan dem Auftrag zugeordnet sind.                                          |
| [**Userlenker grantaccess**](/windows/desktop/api/Winuser/nf-winuser-userhandlegrantaccess)         | Gewährt oder verweigert dem Benutzerobjekt den Zugriff auf ein Handle für einen Auftrag, der über eine Benutzeroberflächen Einschränkung verfügt. |



 

## <a name="thread-pool-functions"></a>Thread Pool Funktionen

Die folgenden Funktionen werden mit [Thread Pools](thread-pools.md)verwendet.



| Funktion                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallbackMayRunLong**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-callbackmayrunlong)                                           | Gibt an, dass der Rückruf möglicherweise nicht schnell zurückgegeben wird.                                                                                                                                                                                                 |
| [**CancelThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio)                                           | Bricht die Benachrichtigung von der [**StartThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio) -Funktion ab.                                                                                                                                                          |
| [**CloseThreadpool**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool)                                                 | Schließt den angegebenen Thread Pool.                                                                                                                                                                                                                   |
| [**CloseThreadpoolCleanupGroup**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup)                         | Schließt die angegebene Bereinigungs Gruppe.                                                                                                                                                                                                                 |
| [**CloseThreadpoolCleanupGroupMembers**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers)           | Gibt die Mitglieder der angegebenen Bereinigungs Gruppe frei, wartet, bis alle Rückruf Funktionen vollständig sind, und bricht optional alle ausstehenden Rückruf Funktionen ab.                                                                                       |
| [**CloseThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolio)                                             | Gibt das angegebene e/a-Abschluss Objekt frei.                                                                                                                                                                                                       |
| [**CloseThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer)                                       | Gibt das angegebene Zeit Geber Objekt frei.                                                                                                                                                                                                                |
| [**CloseThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait)                                         | Gibt das angegebene warte Objekt frei.                                                                                                                                                                                                                 |
| [**CloseThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork)                                         | Gibt das angegebene Arbeits Objekt frei.                                                                                                                                                                                                                 |
| [**"Kreatethread Pool"**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool)                                               | Ordnet einen neuen Thread Pool zu, um Rückrufe auszuführen.                                                                                                                                                                                               |
| [**"Kreatethlespoolcleanupgroup"**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup)                       | Erstellt eine Bereinigungs Gruppe, die Anwendungen verwenden können, um einen oder mehrere Thread Pool Rückrufe zu verfolgen.                                                                                                                                                       |
| [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio)                                           | Erstellt ein neues e/a-Abschluss Objekt.                                                                                                                                                                                                                |
| [**"Kreatethread PoolTimer"**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer)                                     | Erstellt ein neues Timer-Objekt.                                                                                                                                                                                                                         |
| [**"Kreatethread poolwait"**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait)                                       | Erstellt ein neues Wait-Objekt.                                                                                                                                                                                                                          |
| [**CreateThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork)                                       | Erstellt ein neues Arbeits Objekt.                                                                                                                                                                                                                          |
| [**DestroyThreadpoolEnvironment**](/windows/desktop/api/WinBase/nf-winbase-destroythreadpoolenvironment)                       | Löscht die angegebene Rückruf Umgebung. Rufen Sie diese Funktion auf, wenn die Rückruf Umgebung zum Erstellen neuer Thread Pool Objekte nicht mehr benötigt wird.                                                                                              |
| [**DisassociateCurrentThreadFromCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-disassociatecurrentthreadfromcallback)     | Entfernt die Zuordnung zwischen der aktuell ausgeführten Rückruffunktion und dem Objekt, das den Rückruf initiiert hat. Der aktuelle Thread zählt nicht mehr als das Ausführen eines Rückrufs für das-Objekt.                                      |
| [**Freelibrary\callbackreturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns)                   | Gibt die dll an, die der Thread Pool entladen wird, wenn der aktuelle Rückruf abgeschlossen ist.                                                                                                                                                             |
| [**Initializethreadpoolenvironment**](/windows/desktop/api/WinBase/nf-winbase-initializethreadpoolenvironment)                 | Initialisiert eine Rückruf Umgebung.                                                                                                                                                                                                                 |
| [**IsThreadpoolTimerSet**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-isthreadpooltimerset)                                       | Bestimmt, ob das angegebene Zeit Geber Objekt aktuell festgelegt ist.                                                                                                                                                                                     |
| [**Leavecriticalsection\callbackreturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-leavecriticalsectionwhencallbackreturns) | Gibt den kritischen Abschnitt an, den der Thread Pool nach Abschluss des aktuellen Rückrufs freigibt.                                                                                                                                               |
| [**Querythreadpoolstackinformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)                 | Ruft die Stapel Reserve-und-Commit-Größen für Threads im angegebenen Thread Pool ab.                                                                                                                                                              |
| [**Releasemutex\callbackreturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasemutexwhencallbackreturns)                 | Gibt den Mutex an, den der Thread Pool nach Abschluss des aktuellen Rückrufs freigibt.                                                                                                                                                          |
| [**Releasesemaphore\callbackreturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasesemaphorewhencallbackreturns)         | Gibt das Semaphor an, das der Thread Pool nach Abschluss des aktuellen Rückrufs freigibt.                                                                                                                                                      |
| [**"*"**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-seteventwhencallbackreturns)                         | Gibt das Ereignis an, das vom Thread Pool festgelegt wird, wenn der aktuelle Rückruf abgeschlossen ist.                                                                                                                                                              |
| [**SetThreadpoolCallbackCleanupGroup**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackcleanupgroup)             | Ordnet die angegebene Bereinigungs Gruppe der angegebenen Rückruf Umgebung zu.                                                                                                                                                                     |
| [**SetThreadpoolCallbackLibrary**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbacklibrary)                       | Stellt sicher, dass die angegebene DLL weiterhin geladen wird, solange ausstehende Rückrufe vorhanden sind.                                                                                                                                                           |
| [**Setthreadpoolcallbackpersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)                 | Gibt an, dass der Rückruf in einem permanenten Thread ausgeführt werden soll.                                                                                                                                                                                      |
| [**SetThreadpoolCallbackPool**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpool)                             | Legt den Thread Pool fest, der verwendet werden soll, wenn Rückrufe erzeugt werden.                                                                                                                                                                                          |
| [**Setthreadpoolcallbackpriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)                     | Gibt die Priorität einer Rückruffunktion in Relation zu anderen Arbeits Elementen im gleichen Thread Pool an.                                                                                                                                                 |
| [**SetThreadpoolCallbackRunsLong**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackrunslong)                     | Gibt an, dass Rückrufe, die dieser Rückruf Umgebung zugeordnet sind, möglicherweise nicht schnell zurückgeben                                                                                                                                                          |
| [**Setthreadpoolstackinformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)                     | Legt die Stapel Reserve-und-Commit-Größen für neue Threads im angegebenen Thread Pool fest.                                                                                                                                                               |
| [**SetThreadpoolThreadMaximum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum)                           | Legt die maximale Anzahl von Threads fest, die der angegebene Thread Pool zuordnen kann, um Rückrufe zu verarbeiten.                                                                                                                                                |
| [**SetThreadpoolThreadMinimum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum)                           | Legt die Mindestanzahl von Threads fest, die der angegebene Thread Pool für die Verarbeitung von Rückrufen verfügbar machen muss.                                                                                                                                         |
| [**Setthreadpooltimerex**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimerex)                                       | Legt das Timer-Objekt fest. Ein Arbeits Thread ruft den Rückruf des Zeit Geber Objekts auf, nachdem das angegebene Timeout abgelaufen ist.                                                                                                                                       |
| [**SetThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer)                                           | Legt das Timer-Objekt fest. Ein Arbeits Thread ruft den Rückruf des Zeit Geber Objekts auf, nachdem das angegebene Timeout abgelaufen ist.                                                                                                                                       |
| [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait)                                             | Legt das Wait-Objekt fest. Ein Arbeits Thread ruft die Rückruffunktion des wait-Objekts auf, nachdem das Handle signalisiert wurde oder nachdem das angegebene Timeout abgelaufen ist.                                                                                           |
| [**Setthreadpoolwaitex**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwaitex)                                         | Legt das Wait-Objekt fest. Ein Arbeits Thread ruft die Rückruffunktion des wait-Objekts auf, nachdem das Handle signalisiert wurde oder nachdem das angegebene Timeout abgelaufen ist.                                                                                           |
| [**StartThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio)                                             | Benachrichtigt den Thread Pool, dass e/a-Vorgänge möglicherweise mit dem angegebenen e/a-Abschluss Objekt beginnen. Ein Arbeits Thread ruft die Rückruffunktion des e/a-Abschluss Objekts auf, nachdem der Vorgang für das an dieses Objekt gebundene Datei Handle abgeschlossen wurde. |
| [**SubmitThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork)                                       | Sendet ein Arbeits Objekt an den Thread Pool. Ein Arbeits Thread ruft die Rückruffunktion des Arbeits Objekts auf.                                                                                                                                                  |
| [**Tpinitializecallbackenviron**](/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron)                         | Initialisiert eine Rückruf Umgebung für den Thread Pool.                                                                                                                                                                                             |
| [**Tpdestroycallbackenviron**](/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron)                               | Löscht die angegebene Rückruf Umgebung. Rufen Sie diese Funktion auf, wenn die Rückruf Umgebung zum Erstellen neuer Thread Pool Objekte nicht mehr benötigt wird.                                                                                              |
| [**Tpsetcallbackactivationcontext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext)                   | Weist der Rückruf Umgebung einen Aktivierungs Kontext zu.                                                                                                                                                                                          |
| [**Tpsetcallbackcleanupgroup**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup)                             | Ordnet die angegebene Bereinigungs Gruppe der angegebenen Rückruf Umgebung zu.                                                                                                                                                                     |
| [**Tpsetcallbackfinalizationcallback**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback)             | Gibt eine Funktion an, die aufgerufen werden soll, wenn die Rückruf Umgebung abgeschlossen ist.                                                                                                                                                                            |
| [**Tpsetcallbacklongfunction**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction)                             | Gibt an, dass Rückrufe, die dieser Rückruf Umgebung zugeordnet sind, möglicherweise nicht schnell zurückgeben                                                                                                                                                          |
| [**Tpsetcallbacknoactivationcontext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext)               | Gibt an, dass die Rückruf Umgebung über keinen Aktivierungs Kontext verfügt.                                                                                                                                                                                  |
| [**Tpsetcallbackpersistent**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent)                                 | Gibt an, dass der Rückruf in einem permanenten Thread ausgeführt werden soll.                                                                                                                                                                                      |
| [**Tpsetcallbackpriority**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority)                                     | Gibt die Priorität einer Rückruffunktion in Relation zu anderen Arbeits Elementen im gleichen Thread Pool an.                                                                                                                                                 |
| [**Tpsetcallbackracewithdll**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll)                               | Stellt sicher, dass die angegebene DLL weiterhin geladen wird, solange ausstehende Rückrufe vorhanden sind.                                                                                                                                                           |
| [**Tpsetcallbackthreadpool**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool)                                 | Weist einer Rückruf Umgebung einen Thread Pool zu.                                                                                                                                                                                                    |
| [**TrySubmitThreadpoolCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-trysubmitthreadpoolcallback)                         | Fordert an, dass ein Thread Pool-Arbeits Thread die angegebene Rückruffunktion aufruft.                                                                                                                                                                     |
| [**Waitöffumpooliocallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooliocallbacks)                       | Wartet auf den Abschluss ausstehender e/a-Abschluss Rückrufe und bricht optional ausstehende Rückrufe ab, deren Ausführung noch nicht gestartet wurde.                                                                                                           |
| [**Waitoffener pooltimercallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks)                 | Wartet auf den Abschluss ausstehender Zeit Geber Rückrufe und bricht optional ausstehende Rückrufe ab, deren Ausführung noch nicht gestartet wurde.                                                                                                                    |
| [**Waitoffener poolwaitcallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks)                   | Wartet darauf, dass ausstehende warte Rückrufe abgeschlossen werden, und bricht optional ausstehende Rückrufe ab, deren Ausführung noch nicht gestartet wurde.                                                                                                                     |
| [**WaitForThreadpoolWorkCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolworkcallbacks)                   | Wartet darauf, dass ausstehende Arbeits Rückrufe abgeschlossen werden, und bricht optional ausstehende Rückrufe ab, deren Ausführung noch nicht gestartet wurde.                                                                                                                     |



 

Die folgenden Funktionen sind Teil der ursprünglichen [Thread Pooling](thread-pooling.md) -API.



| Funktion                                                            | BESCHREIBUNG                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**' Bindiocompletioncallback '**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)        | Ordnet den e/a-Abschlussport, der dem Thread Pool gehört, dem angegebenen Datei Handle zu. Beim Abschluss einer e/a-Anforderung, die diese Datei umfasst, führt ein nicht-e/a-Arbeits Thread die angegebene Rückruffunktion aus. |
| [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                      | Fügt eine Arbeitsaufgabe einem Arbeits Thread im Thread Pool in die Warteschlange.                                                                                                                                                              |
| [**Von RegisterWaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) | Weist einen Warte Thread im Thread Pool an, auf das Objekt zu warten.                                                                                                                                                        |
| [**' Unregisterwaitex '**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-unregisterwaitex)                       | Wartet, bis ein oder alle der angegebenen Objekte im signalisierten Zustand sind oder das Timeout Intervall abläuft.                                                                                                            |



 

## <a name="thread-ordering-service-functions"></a>Dienstfunktionen für die Thread Bestellung

Die folgenden Funktionen werden mit dem [Thread Reihen folgen Dienst](thread-ordering-service.md)verwendet.



| Funktion                                                                   | BESCHREIBUNG                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**Avquerysystemreaktionsfähigkeit**](/windows/desktop/api/Avrt/nf-avrt-avquerysystemresponsiveness)         | Ruft die systemreaktionseinstellung ab, die vom Multimedia Class Scheduler-Dienst verwendet wird. |
| [**Avrtkreatethumorderinggroup**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup)     | Erstellt eine Thread Reihenfolge Gruppe.                                                            |
| [**Avrtkreatethumorderinggroupex**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroupexa) | Erstellt eine Thread Reihenfolge Gruppe und ordnet den Server Thread einer Aufgabe zu.               |
| [**Avrtdeletethreadorderinggroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup)     | Löscht die angegebene Thread Reihenfolge Gruppe, die vom Aufrufer erstellt wurde.                          |
| [**Avrtjointhreadorderinggroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup)         | Verknüpft Clientthreads mit einer Thread Reihenfolge Gruppe.                                            |
| [**Avrtleavethreadorderinggroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup)       | Ermöglicht Clientthreads das Verlassen einer Thread Reihenfolge Gruppe.                                    |
| [**Avrtwaitonthreadorderinggroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup)     | Aktiviert Clientthreads einer Thread Reihenfolge Gruppe, um zu warten, bis Sie ausgeführt werden.        |



 

## <a name="multimedia-class-scheduler-service-functions"></a>Dienstfunktionen für Multimedia-Klassen Planer

Die folgenden Funktionen werden mit dem [Multimedia Class Scheduler-Dienst](multimedia-class-scheduler-service.md)verwendet.



| Funktion                                                                   | BESCHREIBUNG                                                                                           |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Avrevertmmthreadcharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avrevertmmthreadcharacteristics) | Gibt an, dass ein Thread keine Arbeit mehr durchführt, die mit der angegebenen Aufgabe verknüpft ist.              |
| [**Avsetmmmaxthreadcharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) | Verknüpft den aufrufenden Thread mit den angegebenen Tasks.                                               |
| [**Avsetmmthreadcharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa)       | Ordnet den aufrufenden Thread der angegebenen Aufgabe zu.                                                |
| [**Avsetmmthreadpriority**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority)                     | Passt die Thread Priorität des aufrufenden Threads relativ zu anderen Threads an, die dieselbe Aufgabe ausführen. |



 

## <a name="fiber-functions"></a>Fiber-Funktionen

Die folgenden Funktionen werden mit [Fibers](fibers.md)verwendet.



| Funktion                                                 | BESCHREIBUNG                                                                                                  |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Convertfiberto Thread**](/windows/desktop/api/WinBase/nf-winbase-convertfibertothread)     | Konvertiert die aktuelle Fiber in einen Thread.                                                                    |
| [**Convertthreadumfiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber)     | Konvertiert den aktuellen Thread in eine Fiber.                                                                    |
| [**Convertthreadthfiberex**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiberex) | Konvertiert den aktuellen Thread in eine Fiber.                                                                    |
| [**"Kreatefiber"**](/windows/desktop/api/WinBase/nf-winbase-createfiber)                       | Ordnet ein Fiber Objekt zu, weist ihm einen Stapel zu und richtet die Ausführung so ein, dass die Ausführung an der angegebenen Startadresse beginnt. |
| [**"Kreatefiberex"**](/windows/desktop/api/WinBase/nf-winbase-createfiberex)                   | Ordnet ein Fiber Objekt zu, weist ihm einen Stapel zu und richtet die Ausführung so ein, dass die Ausführung an der angegebenen Startadresse beginnt. |
| [**Deletefiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber)                       | Löscht eine vorhandene Fiber.                                                                                   |
| [**Fiberproc**](/windows/win32/api/winbase/nc-winbase-pfiber_start_routine)                           | Eine Anwendungs definierte Funktion, die mit der Funktion " [**kreatefiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) " verwendet wird.                   |
| [**Flsalloc**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc)                             | Ordnet einen FLS-Index (Fiber Local Storage) zu.                                                                 |
| [**Flsfree**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree)                               | Gibt einen FLS-Index frei.                                                                                       |
| [**Flsgetvalue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)                       | Ruft den Wert im FLS-Slot der aufrufenden Fiber für einen angegebenen FLS-Index ab.                               |
| [**Flssetvalue**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)                       | Speichert einen Wert im FLS-Slot der aufrufenden Fiber für einen angegebenen FLS-Index.                                    |
| [**Isthreadafiber**](/windows/win32/api/fibersapi/nf-fibersapi-isthreadafiber)                 | Bestimmt, ob der aktuelle Thread eine Fiber ist.                                                            |
| [**Switchumfiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber)                   | Plant eine Fiber.                                                                                           |



 

## <a name="numa-support-functions"></a>NUMA-Unterstützungsfunktionen

Die folgenden Funktionen bieten [NUMA-Unterstützung](numa-support.md).



| Funktion                                                                 | BESCHREIBUNG                                                                                                                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zuordnung von "Zuweisung"**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)  | Reserviert einen Arbeitsspeicher Bereich innerhalb des virtuellen Adressraums des angegebenen Prozesses oder führt einen Commit aus und gibt den NUMA-Knoten für den physischen Speicher an. |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Ruft Informationen über logische Prozessoren und zugehörige Hardware ab.                                                                                   |
| [**Getnumaavailablememorynode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)         | Ruft die Menge des Arbeitsspeichers ab, der im angegebenen Knoten verfügbar ist.                                                                                        |
| [**Getnumaavailablememorynode Ex**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)     | Ruft die Menge des Arbeitsspeichers ab, der im angegebenen Knoten als ushort-Wert verfügbar ist.                                                              |
| [**Getnumahighestnodenzuber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)             | Ruft den Knoten ab, der derzeit die höchste Anzahl aufweist.                                                                                              |
| [**Getnumanodenumschlag**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)       | Ruft den NUMA-Knoten ab, der dem zugrunde liegenden Gerät für ein Datei Handle zugeordnet ist.                                                                       |
| [**Getnumanodeprocessormask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)             | Ruft die Prozessor Maske für den angegebenen Knoten ab.                                                                                                   |
| [**Getnumanodeprocessormaskex**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)         | Ruft die Prozessor Maske für den angegebenen NUMA-Knoten als ushort-Wert ab.                                                                            |
| [**Getnumaprocessornode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                     | Ruft die Knotennummer für den angegebenen Prozessor ab.                                                                                                 |
| [**Getnumaprocessornode Ex**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                 | Ruft die Knotennummer des angegebenen logischen Prozessors als ushort-Wert ab.                                                                        |
| [**Getnumaproximitynode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                     | Ruft die Knotennummer für den angegebenen Näherungs Bezeichner ab.                                                                                      |
| [**Getnumaproximitynode Ex**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                 | Ruft die Knotennummer als ushort-Wert für den angegebenen Näherungs Bezeichner ab.                                                                    |
| [**Virtualzuweisung-exnuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                        | Reserviert einen Arbeitsspeicher Bereich innerhalb des virtuellen Adressraums des angegebenen Prozesses oder führt einen Commit aus und gibt den NUMA-Knoten für den physischen Speicher an. |



 

## <a name="processor-functions"></a>Prozessor Funktionen

Die folgenden Funktionen werden für logische Prozessoren und [Prozessor Gruppen](processor-groups.md)verwendet.



| Funktion                                                                     | BESCHREIBUNG                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**Getactiveprocessorcount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)                   | Gibt die Anzahl aktiver Prozessoren in einer Prozessor Gruppe oder im System zurück.                                       |
| [**Getactiveprocessorgroupcount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)         | Gibt die Anzahl aktiver Prozessor Gruppen im System zurück.                                                         |
| [**Getcurrentprocessornumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)               | Ruft die Nummer des Prozessors ab, auf dem der aktuelle Thread während des Aufrufens dieser Funktion ausgeführt wurde.            |
| [**Getcurrentprocessornumex**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)           | Ruft die Prozessor Gruppe und die Anzahl der logischen Prozessoren ab, in denen der aufrufenden Thread ausgeführt wird.            |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Ruft Informationen über logische Prozessoren und zugehörige Hardware ab.                                                 |
| [**Getlogicalprocessorinformationex**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Ruft Informationen über die Beziehungen von logischen Prozessoren und zugehöriger Hardware ab.                            |
| [**Getmaximumprocessorcount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)                 | Gibt die maximale Anzahl logischer Prozessoren zurück, die eine Prozessor Gruppe oder das System aufweisen kann.                      |
| [**Getmaximumprocessorgroupcount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)       | Gibt die maximale Anzahl von Prozessor Gruppen zurück, die das System aufweisen kann.                                             |
| [**Queryidleprocessorcycletime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime)           | Ruft die Umlaufzeit für den Leerlauf Thread jedes Prozessors im System ab.                                        |
| [**Queryidleprocessorcycletimeex**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)       | Ruft die akkumulierte Zeit für den Leerlauf Thread für jeden logischen Prozessor in der angegebenen Prozessor Gruppe ab. |



 

## <a name="user-mode-scheduling-functions"></a>User-Mode Zeit Planungsfunktionen

Die folgenden Funktionen werden bei der Benutzermodus-Zeitplanung (ums) verwendet.



| Funktion                                                               | BESCHREIBUNG                                                                                               |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**"Kreateumscompletionlist"**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)             | Erstellt eine ums-Vervollständigungsliste.                                                                            |
| [**"Kreateumsthread Context"**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)               | Erstellt einen ums-Thread Kontext zur Darstellung eines ums-Arbeitsthreads.                                            |
| [**Deleteumscompletionlist**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)             | Löscht die angegebene ums-Vervollständigungsliste. Die Liste muss leer sein.                                        |
| [**Deleteumsthread Context**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)               | Löscht den angegebenen ums-Thread Kontext. Der Thread muss beendet werden.                                  |
| [**"Abqueueumscompletionlistitems"**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) | Ruft ums-Arbeitsthreads aus der angegebenen ums-Vervollständigungsliste ab.                                      |
| [**Enterumsschedulingmode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)               | Konvertiert den aufrufenden Thread in einen ums-Scheduler-Thread.                                                  |
| [**Executeumsthread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)                           | Führt den angegebenen ums-Workerthread aus.                                                                     |
| [**Getcurrentumsthread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)                     | Gibt den ums-Thread Kontext des aufrufenden UMS-Threads zurück.                                                 |
| [**Getnextumslistitem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)                       | Gibt den nächsten ums-Thread Kontext in einer Liste von ums-Thread Kontexten zurück.                                     |
| [**Getumscompletionlistevent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)         | Ruft ein Handle für das-Ereignis ab, das der angegebenen ums-Vervollständigungsliste zugeordnet ist.                        |
| [**Getgetssystemthreadinformation**](/windows/desktop/api/WinBase/nf-winbase-getumssystemthreadinformation) | Fragt ab, ob der angegebene Thread ein ums-Scheduler-Thread, ein ums-Arbeits Thread oder ein nicht-ums-Thread ist. |
| [**Queryumsthumeinformationen**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)         | Ruft Informationen über den angegebenen ums-Arbeitsthreads ab.                                              |
| [**Informationen zu "abtumsthinfo"**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)             | Legt anwendungsspezifische Kontextinformationen für den angegebenen ums-Arbeits Thread fest.                        |
| [*Umsschedulerproc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)                             | Die Anwendungs definierte ums-Scheduler-Einstiegspunkt Funktion, die mit einer ums-Vervollständigungsliste verknüpft ist.         |
| [**Umsthumyield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)                               | Übergibt die Steuerung an den ums-planerthread, in dem der aufrufenden ums-Arbeits Thread ausgeführt wird.             |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

-   [**Ntgetcurrentprocessornumber**](ntgetcurrentprocessornumber.md)
-   [**Ntqueryinformationprocess**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationprocess)
-   [**Ntqueryinformationthread**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationthread)
-   [**Winexec**](/windows/desktop/api/WinBase/nf-winbase-winexec)
-   [**Zwqueryinformationprocess**](zwqueryinformationprocess.md)

 

 
