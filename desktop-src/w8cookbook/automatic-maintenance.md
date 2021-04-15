---
title: Automatische Wartung (Compatibility Cookbook für Windows)
description: Automatische Wartung
ms.assetid: D3B61105-D118-42A4-8F3D-ED92EFAF597F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320625fa0ac8e56368396a7f1be88def0ac3c526
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104474501"
---
# <a name="automatic-maintenance"></a>Automatische Wartung

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Windows ist abhängig von der Ausführung von Posteingang und der Wartung von Drittanbietern für einen Großteil des Werts: Add, einschließlich Windows Update und automatischer Datenträger Defragmentierung sowie von Antivirenaktualisierungen und-Scans. Außerdem verwenden Unternehmen häufig Wartungsaktivitäten, z. b. NAP-Scans (Network Access Protection, Netzwerk Zugriffsschutz), um Sicherheitsstandards auf allen Unternehmens Arbeitsstationen zu erzwingen

Wartungsaktivitäten in Windows sind für die Ausführung im Hintergrund mit eingeschränkter Benutzerinteraktion und minimaler Auswirkung auf die Leistung und Energieeffizienz vorgesehen. In Windows 7 und früheren Versionen sind Leistung und Energieeffizienz jedoch weiterhin aufgrund des nicht deterministischen und sehr unterschiedlichen Zeitplans der verschiedenen Wartungsaktivitäten in Windows beeinträchtigt. Die Reaktionsfähigkeit für Benutzer wird verringert, wenn Wartungsaktivitäten ausgeführt werden, während Benutzer den Computer aktiv verwenden. Außerdem wird der Benutzer häufig aufgefordert, seine Software zu aktualisieren und die Hintergrund Wartung auszuführen und Benutzer an mehrere Benutzeroberflächen weiterzuleiten, einschließlich des Aktions Centers, der Systemsteuerung, der Windows Update, Taskplaner MMC-Snap-Ins und von Steuerelementen von Drittanbietern.

Das Ziel der automatischen Wartung besteht darin, alle Hintergrund Wartungsaktivitäten in Windows zu kombinieren und Entwicklern von Drittanbietern zu helfen, ihre Wartungsaktivitäten zu Windows hinzuzufügen, ohne dass sich dies negativ auf die Leistung und Energieeffizienz auswirkt. Außerdem ermöglicht die automatische Wartung Benutzern und Unternehmen die Kontrolle über die Planung und Konfiguration von Wartungsaktivitäten.

**Wichtige Probleme**

Die automatische Wartung ist so konzipiert, dass diese Probleme mit Wartungsaktivitäten in Windows behoben werden:

-   Frist Planung
-   Ressourcen Verwendungs Konflikte
-   Energieeffizienz
-   Transparenz für den Benutzer

## <a name="functionality"></a>Funktionalität

Durch die automatische Wartung wird die Effizienz im Leerlauf vereinfacht, und alle Aktivitäten können rechtzeitig und priorisiert ausgeführt werden. Außerdem ermöglicht Sie eine einheitliche Sichtbarkeit und Kontrolle über Wartungsaktivitäten und ermöglicht Entwicklern von Drittanbietern, ihre Wartungsaktivitäten zu Windows hinzuzufügen, ohne dass sich dies negativ auf die Leistung und Energieeffizienz auswirkt. Zu diesem Zweck bietet es einen vollständig automatischen Modus, den Benutzer initiierten Modus, automatische Beendigung, Termine und Benachrichtigung sowie die Kontrolle über das Unternehmen. Diese werden nachfolgend beschrieben.

**Vollständig automatischer Modus**

Dieser Standardmodus ermöglicht eine intelligente Zeitplanung während der Leerlaufzeit von PCs und zu geplanten Zeiten – das Ausführen und automatische Anhalten von Wartungsaktivitäten ohne Benutzereingriff. Der Benutzer kann einen wöchentlichen oder einen täglichen Zeitplan festlegen. Alle Wartungsaktivitäten sind nicht interaktiv und werden automatisch ausgeführt.

Wenn das System wahrscheinlich nicht in Gebrauch ist, wird der Computer automatisch wieder in den Standbymodus versetzt, und die Energie Verwaltungs Richtlinie, bei der es sich um Laptops handelt, wird standardmäßig nur aktiviert, wenn es sich um eine Stromversorgung handelt. Vollständige Systemressourcen mit hoher Leistung werden verwendet, um die Wartungs Aktivität so schnell wie möglich abzuschließen. Wenn das System für die automatische Wartung aus dem Standbymodus wieder aufgenommen wurde, wird es in den Standbymodus versetzt.

Alle erforderlichen Benutzerinteraktionen im Zusammenhang mit Aktivitäten, z. b. der Konfiguration, werden außerhalb der automatischen Wartungs Ausführung ausgeführt.

**Vom Benutzer initiierter Modus**

Wenn Benutzer sich für eine längere Zeit vorbereiten müssen und sich für eine längere Zeit mit der Akkuleistung ausarbeiten möchten, können Sie die automatische Wartung bei Bedarf initiieren. Benutzer können automatische Wartungs Attribute konfigurieren, einschließlich des automatischen Lauf Zeit Zeitplans. Sie können den aktuellen Status der automatischen Wartungs Ausführung anzeigen und die automatische Wartung bei Bedarf abbrechen.

**Automatisches Abbrechen**

Durch die automatische Wartung werden die derzeit laufenden Wartungsaktivitäten automatisch beendet, wenn der Benutzer mit der Interaktion mit dem Computer beginnt. Wartungsaktivitäten werden fortgesetzt, wenn das System in den Leerlauf Status zurückkehrt.

> [!Note]  
> Alle Aktivitäten bei der automatischen Wartung müssen das Beenden in zwei Sekunden oder weniger unterstützen. Der Benutzer sollte benachrichtigt werden, dass die Aktivität beendet wurde.

 

**Termine und Benachrichtigungen**

Eine kritische Wartungs Aktivität muss innerhalb eines vordefinierten Zeitfensters ausgeführt werden. Wenn wichtige Tasks nicht innerhalb der vorgesehenen Zeit ausgeführt werden konnten, wird die automatische Wartung automatisch mit der nächsten verfügbaren System Leerlauf Chance gestartet. Wenn sich der Task Status jedoch hinter dem Stichtag befindet, benachrichtigt die automatische Wartung den Benutzer über die Aktivität und stellt eine Option für die manuelle Durchführung der automatischen Wartung bereit. Alle Tasks, die für die Wartung geplant sind, werden ausgeführt, obwohl die am meisten gestarteten Tasks Vorrang haben. Diese Aktivität kann sich auf die Reaktionsfähigkeit und Leistung des Systems auswirken. Daher wird der Benutzer durch die automatische Wartung benachrichtigt, dass eine kritische Wartungs Aktivität ausgeführt wird.

**Unternehmenssteuerung**

IT-Experten in Unternehmen sollten ermitteln können, wann die automatische Wartung auf Ihren Windows-Systemen ausgeführt wird, diesen Zeitplan über standardisierte Verwaltungs Schnittstellen erzwingen und Ereignisdaten zum Status der automatischen Wartungs Ausführung abrufen. Außerdem sollten IT-Experten in der Lage sein, bestimmte automatische Wartungsaktivitäten Remote über Standard Verwaltungs Schnittstellen aufzurufen. Jedes Mal, wenn die automatische Wartung ausgeführt wird, wird die Status Berichterstattung, einschließlich Benachrichtigungen, wenn die automatische Wartung nicht ausgeführt werden konnte, da der Benutzer die Aktivität manuell angehalten hat, ausgeführt. IT-Experten sollten erwägen, Anmelde Skripts in die automatische Wartung zu verschieben, um die Anmeldung des Benutzers zu beschleunigen.

## <a name="creating-an-automatic-maintenance-task"></a>Erstellen eines automatischen Wartungs Tasks

In diesem Abschnitt wird erläutert, wie Entwickler eine Aufgabe mit einer Aufgabendefinition in XML-oder C-Sprache erstellen können. Beachten Sie, dass die Wartungs Aktivität keine Benutzeroberfläche starten sollte, die eine Benutzerinteraktion erfordert, da die automatische Wartung vollständig abläuft und ausgeführt wird, wenn der Benutzer nicht vorhanden ist. Wenn der Benutzer während der automatischen Wartung mit dem Computer interagiert, werden alle Aufgaben, die in Bearbeitung sind, bis zum nächsten Leerlauf Zeitraum beendet.

**Verwenden von XML**

Taskplaner enthält ein integriertes Befehlszeilen Tool schtasks.exe, mit dem eine Aufgabendefinition im XML-Format importiert werden kann. Das Schema für die Aufgabendefinition ist unter dokumentiert https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx . Im folgenden finden Sie ein Beispiel für einen automatischen Wartungs Task, der in XML definiert ist.


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



Speichern Sie den obigen XML-Code als Textdatei, und verwenden Sie die folgende Befehlszeile, um die Aufgabe auf einem Windows-Computer zu speichern:

`Schtasks.exe /create /tn <task name> /xml <text file name>`

**Verwenden von C**

Eine automatische Wartungs Aufgabe kann auch mithilfe von C-Code erstellt werden. Im folgenden finden Sie ein Codebeispiel, das zum Konfigurieren der automatischen Wartungs Einstellungen eines Tasks verwendet werden kann:


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



## <a name="validating-tasks"></a>Validieren von Aufgaben

Überprüfen Sie, ob die Aufgabe erfolgreich erstellt wurde und im Rahmen der Wartung ausgeführt wird.

**Die Task Erstellung wird überprüft.**

Verwenden Sie diese Befehlszeile, um die Aufgabendefinition in eine Datei zu exportieren und sicherzustellen, dass die Aufgabendefinition erwartungsgemäß lautet:

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

**Validieren der Task Ausführung**

Führen Sie diese Befehlszeile aus, um die Aufgabe zu starten und zu überprüfen, ob die Taskplaner Benutzeroberfläche (taskschd. msc) anzeigt, dass die Aufgabe ausgeführt wurde

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a>Ressourcen

-   [Aufgaben Zeitplan 2,0](/previous-versions/bb756979(v=msdn.10))

 

 