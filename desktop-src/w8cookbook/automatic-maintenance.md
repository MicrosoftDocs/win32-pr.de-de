---
title: Automatische Wartung (Kompatibilitäts-Cookbook für Windows)
description: Automatische Wartung
ms.assetid: D3B61105-D118-42A4-8F3D-ED92EFAF597F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a839191d84f3f20fcc598b42433c888b090b2b174dd6891c0b5b9fc72f0af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028868"
---
# <a name="automatic-maintenance"></a>Automatische Wartung

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Windows hängt von der Ausführung von Posteingangs- und Drittanbieterwartungsaktivitäten für einen Großteil des Mehrwerts ab, einschließlich Windows Update, automatischer Datenträgerdefragmentierung sowie Antivirenupdates und Überprüfungen. Darüber hinaus verwenden Unternehmen häufig Wartungsaktivitäten wie nap-Überprüfung (Network Access Protection), um Sicherheitsstandards auf allen Unternehmensarbeitsstationen zu erzwingen.

Wartungsaktivitäten in Windows sind für die Ausführung im Hintergrund mit eingeschränkter Benutzerinteraktion und minimalen Auswirkungen auf Leistung und Energieeffizienz konzipiert. In Windows 7 und früheren Versionen sind Leistung und Energieeffizienz jedoch aufgrund des nicht deterministischen und stark variierenden Zeitplans für die verschiedenen Wartungsaktivitäten in Windows weiterhin beeinträchtigt. Die Reaktionsfähigkeit für Benutzer wird reduziert, wenn Wartungsaktivitäten ausgeführt werden, während Benutzer den Computer aktiv verwenden. Apps fordern den Benutzer außerdem häufig auf, seine Software zu aktualisieren und Hintergrundwartungen auszuführen und Benutzer an mehrere Benutzeroberflächen weiterzuleiten, einschließlich Action Center, Systemsteuerung, Windows Update, Taskplaner MMC-Snap-In und Steuerelemente von Drittanbietern.

Das Ziel von Automatische Wartung besteht darin, alle Hintergrundwartungsaktivitäten in Windows zu kombinieren und Entwicklern von Drittanbietern zu helfen, ihre Wartungsaktivitäten Windows hinzuzufügen, ohne die Leistung und Energieeffizienz zu beeinträchtigen. Darüber hinaus ermöglicht Automatische Wartung Es Benutzern und Unternehmen, die Planung und Konfiguration von Wartungsaktivitäten zu steuern.

**Wichtige Probleme**

Automatische Wartung wurde entwickelt, um diese Probleme mit Wartungsaktivitäten in Windows zu beheben:

-   Stichtagplanung
-   Konflikte bei der Ressourcennutzung
-   Energieeffizienz
-   Transparenz für den Benutzer

## <a name="functionality"></a>Funktionalität

Automatische Wartung ermöglicht die Effizienz im Leerlauf und ermöglicht die rechtzeitige und priorisierte Ausführung aller Aktivitäten. Außerdem ermöglicht sie einheitliche Sichtbarkeit und Kontrolle über wartungsbezogene Aktivitäten und ermöglicht es Entwicklern von Drittanbietern, ihre Wartungsaktivitäten Windows hinzuzufügen, ohne die Leistung und Energieeffizienz zu beeinträchtigen. Zu diesem Zeitpunkt werden ein automatischer Modus, ein vom Benutzer initiierter Modus, ein automatischer Stopp, Stichtage und Benachrichtigungen sowie die Unternehmenssteuerung ermöglicht. Diese werden jeweils unten beschrieben.

**Voll automatischer Modus**

Dieser Standardmodus ermöglicht eine intelligente Planung während der PC-Leerlaufzeit und zu geplanten Zeiten– die Ausführung und das automatische Anhalten von Wartungsaktivitäten ohne Benutzereingriff. Der Benutzer kann einen wöchentlichen oder täglichen Zeitplan festlegen. Alle Wartungsaktivitäten sind nicht interaktiv und werden im Hintergrund ausgeführt.

Der Computer wird automatisch aus dem Standbymodus wieder aufgenommen, wenn das System wahrscheinlich nicht verwendet wird. Dabei wird die Energieverwaltungsrichtlinie beachtet, die im Fall von Laptops standardmäßig nur aktiviert ist, wenn die Stromversorgung aktiviert ist. Vollständige Systemressourcen mit hoher Leistung werden verwendet, um die Wartungsaktivität so schnell wie möglich abzuschließen. Wenn das System aus dem Standbymodus für Automatische Wartung wieder aufgenommen wurde, wird es aufgefordert, in den Standbymodus zurückzukehren.

Alle erforderlichen Benutzerinteraktionen im Zusammenhang mit Aktivitäten wie der Konfiguration werden außerhalb Automatische Wartung Ausführung ausgeführt.

**Vom Benutzer initiierter Modus**

Wenn Benutzer sich auf die Reise vorbereiten müssen, einen längeren Akkubetrieb erwarten oder die Leistung und Reaktionsfähigkeit optimieren möchten, haben sie die Möglichkeit, Automatische Wartung bei Bedarf zu initiieren. Benutzer können Automatische Wartung Attribute konfigurieren, einschließlich des Zeitplans für die automatische Ausführung. Sie können den aktuellen Status Automatische Wartung Ausführung anzeigen und bei Bedarf Automatische Wartung beenden.

**Automatisches Beenden**

Automatische Wartung beendet automatisch die derzeit ausgeführten Wartungsaktivitäten, wenn der Benutzer mit dem Computer interagiert. Die Wartungsaktivität wird fortgesetzt, wenn das System zum Leerlaufstatus zurückkehrt.

> [!Note]  
> Alle Aktivitäten in Automatische Wartung müssen das Beenden in mindestens 2 Sekunden unterstützen. Der Benutzer sollte benachrichtigt werden, dass die Aktivität beendet wurde.

 

**Stichtage und Benachrichtigungen**

Kritische Wartungsaktivitäten müssen innerhalb eines vordefinierten Zeitfensters ausgeführt werden. Wenn kritische Aufgaben nicht innerhalb der festgelegten Zeit ausgeführt werden konnten, werden Automatische Wartung automatisch bei der nächsten verfügbaren Gelegenheit im Leerlauf des Systems ausgeführt. Wenn der Taskzustand jedoch hinter dem Stichtag verbleibt, benachrichtigt Automatische Wartung den Benutzer über die Aktivität und stellt eine Option für eine manuelle Ausführung von Automatische Wartung bereit. Alle für die Wartung geplanten Aufgaben werden ausgeführt, obwohl die am meisten ausgehungerten Aufgaben Vorrang haben. Diese Aktivität kann sich auf die Reaktionsfähigkeit und Leistung des Systems auswirken. daher benachrichtigt Automatische Wartung den Benutzer, dass kritische Wartungsaktivitäten ausgeführt werden.

**Enterprise-Steuerelement**

Enterprise IT-Experten sollten in der Lage sein, zu bestimmen, wann Automatische Wartung auf ihren Windows Systemen ausgeführt wird, diesen Zeitplan über standardisierte Verwaltungsschnittstellen zu erzwingen und Ereignisdaten zum Status von Automatische Wartung Ausführungsversuchen abzurufen. Darüber hinaus sollten IT-Experten in der Lage sein, bestimmte Automatische Wartung Aktivitäten remote über Standardverwaltungsschnittstellen aufzurufen. Jedes Mal, wenn Automatische Wartung ausgeführt wird, wird die Statusberichterstattung ausgeführt, einschließlich Benachrichtigungen, wenn Automatische Wartung nicht ausgeführt werden konnten, da der Benutzer die Aktivität manuell angehalten hat. IT-Experten sollten erwägen, Anmeldeskripts in Automatische Wartung zu verschieben, um die Benutzeranmeldung schneller zu gestalten.

## <a name="creating-an-automatic-maintenance-task"></a>Erstellen einer Automatische Wartung Aufgabe

In diesem Abschnitt wird erläutert, wie Entwickler eine Aufgabe mithilfe einer Aufgabendefinition in XML oder C erstellen können. Beachten Sie, dass die Wartungsaktivität keine Benutzeroberfläche starten sollte, die eine Benutzerinteraktion erfordert, da Automatische Wartung vollständig unbeaufsichtigt ist und ausgeführt wird, wenn der Benutzer nicht vorhanden ist. Wenn der Benutzer während Automatische Wartung mit dem Computer interagiert, werden alle laufenden Aufgaben bis zum nächsten Leerlaufzeitraum beendet.

**Verwenden von XML**

Taskplaner enthält ein integriertes Befehlszeilentool, schtasks.exe, das eine Taskdefinition im XML-Format importieren kann. Das Schema für die Aufgabendefinition ist unter https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx dokumentiert. Im Folgenden finden Sie ein Beispiel für eine in XML definierte Automatische Wartung Aufgabe.


```
<?xml version="1.0" encoding="UTF-16"?>
<Task version="1.4" xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
  <RegistrationInfo>
    <Date>2011-07-01T11:34:31</Date>
    <Author>IT Deptartment</Author>
  </RegistrationInfo>
  <Principals>
    <Principal id="Author">
      <RunLevel>LeastPrivilege</RunLevel>
      <GroupId>NT AUTHORITY\SYSTEM</GroupId>
    </Principal>
  </Principals>
  <Settings>
    <MultipleInstancesPolicy>IgnoreNew</MultipleInstancesPolicy>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
    <AllowHardTerminate>true</AllowHardTerminate>
    <StartWhenAvailable>false</StartWhenAvailable>
    <RunOnlyIfNetworkAvailable>false</RunOnlyIfNetworkAvailable>
    <MaintenanceSettings>
      <Period>P2D</Period>
      <Deadline>P14D</Deadline>
    </MaintenanceSettings>
    <AllowStartOnDemand>true</AllowStartOnDemand>
    <Enabled>true</Enabled>
    <Hidden>false</Hidden>
    <RunOnlyIfIdle>false</RunOnlyIfIdle>
    <DisallowStartOnRemoteAppSession>false</DisallowStartOnRemoteAppSession>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
    <WakeToRun>false</WakeToRun>
    <ExecutionTimeLimit>P3D</ExecutionTimeLimit>
    <Priority>7</Priority>
  </Settings>
  <Actions Context="Author">
    <Exec>
      <Command>cmd</Command>
      <Arguments>/c timeout -t 60</Arguments>
    </Exec>
  </Actions>
</Task> 
```



Um die Aufgabe auf einem Windows Computer zu speichern, speichern Sie den obigen XML-Code als Textdatei, und verwenden Sie die folgende Befehlszeile:

`Schtasks.exe /create /tn <task name> /xml <text file name>`

**Verwenden von C**

Eine Automatische Wartung Aufgabe kann auch mithilfe von C-Code erstellt werden. Im Folgenden finden Sie ein Codebeispiel, das zum Konfigurieren der Automatische Wartung-Einstellungen eines Tasks verwendet werden kann:


```
/********************************************************************
This sample creates a maintenance task to start cmd window during maintenance opportunities with periodicity of 2 days and deadline 0f 14 days.
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
//  Include the task header file.
#include <taskschd.h>
//#pragma comment(lib, "taskschd.lib")
//#pragma comment(lib, "comsupp.lib")

int __cdecl 
MainteanceTask( )
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr;

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"MaintenanceTask";

    ITaskService *pService = NULL;
    ITaskFolder *pRootFolder = NULL;
    ITaskDefinition *pTask = NULL;
    ITaskSettings *pSettings = NULL;
    IRegistrationInfo *pRegInfo= NULL;
    IPrincipal *pPrincipal = NULL;
    ITaskSettings3 *pSettings3 = NULL;
    IMaintenanceSettings* pMaintenanceSettings = NULL;
    IActionCollection *pActionCollection = NULL;
    IAction *pAction = NULL;
    IExecAction *pExecAction = NULL;
    IRegisteredTask *pRegisteredTask = NULL;

    wprintf(L"\nCreate Maintenance Task %ws", wszTaskName );

    hr = CoInitializeEx( NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity( NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL,
        0,
        NULL);

    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeSecurity failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to create an instance of ITaskService: %x", hr);
        goto CleanUp;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(), _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        wprintf(L"\nITaskService::Connect failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Root folder pointer: %x", hr );
        goto CleanUp;
    }
    
    //  If the same task exists, remove it.
    ( void ) pRootFolder->DeleteTask( _bstr_t(wszTaskName), 0  );
    
    //  Create the task definition object to create the task.
    hr = pService->NewTask( 0, &pTask );
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to CoCreate an instance of the TaskService class: %x", hr);
        goto CleanUp;
    }
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get identification pointer: %x", hr );
        goto CleanUp;
    }
    
    hr = pRegInfo->put_Author( _bstr_t(L"Author Name") );    
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put identification info: %x", hr );
        goto CleanUp;
    }

    // The task needs to grant explicit FRFX to LOCAL SERVICE (A;;FRFX;;;LS)
    hr = pRegInfo->put_SecurityDescriptor( _variant_t(L"D:P(A;;FA;;;BA)(A;;FA;;;SY)(A;;FRFX;;;LS)") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put security descriptor: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create the principal for the task - these credentials
    //  are overwritten with the credentials passed to RegisterTaskDefinition
    hr = pTask->get_Principal( &pPrincipal );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get principal pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Set up principal logon type to interactive logon
    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put principal info: %x", hr );
        goto CleanUp;
    }  

    //  ------------------------------------------------------
    //  Create the settings for the task
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get settings pointer: %x", hr );
        goto CleanUp;
    }

    hr = pSettings->QueryInterface( __uuidof(ITaskSettings3), (void**) &pSettings3 );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot query ITaskSettings3 interface: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->put_UseUnifiedSchedulingEngine( VARIANT_TRUE );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_UseUnifiedSchedulingEngine: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->CreateMaintenanceSettings( &pMaintenanceSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot CreateMaintenanceSettings: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Period ( _bstr_t(L"P2D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Deadline ( _bstr_t(L"P14D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Add an action to the task. This task will execute notepad.exe.     
    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Task collection pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Create the action, specifying that it is an executable action.
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot create the action: %x", hr );
        goto CleanUp;
    }

    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( IID_IExecAction, (void**) &pExecAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nQueryInterface call failed for IExecAction: %x", hr );
        goto CleanUp;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t(L"cmd") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put action path: %x", hr );
        goto CleanUp;
    }  
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t(wszTaskName),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(), 
            _variant_t(), 
            TASK_LOGON_INTERACTIVE_TOKEN,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        wprintf(L"\nError saving the Task : %x", hr );
        goto CleanUp;
    }
    
    wprintf(L"\nSuccess!\n----------------------------------" );

CleanUp:

    if ( pService != NULL ) pService->Release();
    if ( pRootFolder != NULL ) pRootFolder->Release();
    if ( pTask != NULL ) pTask->Release();
    if ( pSettings != NULL ) pSettings->Release();
    if ( pRegInfo != NULL ) pRegInfo->Release();
    if ( pPrincipal != NULL ) pPrincipal->Release();
    if ( pSettings3 != NULL ) pSettings3->Release();
    if ( pMaintenanceSettings != NULL ) pMaintenanceSettings->Release();
    if ( pActionCollection != NULL ) pActionCollection->Release();
    if ( pAction != NULL ) pAction->Release();
    if ( pExecAction != NULL ) pExecAction->Release();
    if ( pRegisteredTask != NULL ) pRegisteredTask->Release();

    CoUninitialize();
    return SUCCEEDED ( hr ) ? 0 : 1;
}
```



## <a name="validating-tasks"></a>Überprüfen von Aufgaben

Überprüfen Sie, ob der Task erfolgreich erstellt wurde und im Rahmen der Wartung ausgeführt wird.

**Überprüfen der Taskerstellung**

Verwenden Sie diese Befehlszeile, um die Taskdefinition in eine Datei zu exportieren und sicherzustellen, dass die Taskdefinition wie erwartet ist:

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

**Überprüfen der Taskausführung**

Führen Sie diese Befehlszeile aus, um den Task zu starten und zu überprüfen, ob die Taskplaner UI (taskschd.msc) anzeigt, dass der Task ausgeführt wurde:

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a>Ressourcen

-   [Taskzeitplan 2.0](/previous-versions/bb756979(v=msdn.10))

 

 