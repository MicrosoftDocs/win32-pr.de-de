---
title: Beispiel für einen Start Auslösers (C++)
description: Dieses Thema enthält ein C++-Codebeispiel, das veranschaulicht, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad.exe geplant ist, wenn das System gestartet wird.
ms.assetid: d4dbbfe5-bde9-4a1c-8e11-24cd1e14646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdbd5a5a73d100394b90e91f8b9c30c1bd495ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856451"
---
# <a name="boot-trigger-example-c"></a>Beispiel für einen Start Auslösers (C++)

Dieses Thema enthält ein C++-Codebeispiel, das veranschaulicht, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad.exe geplant ist, wenn das System gestartet wird. Der Task enthält einen Start--Vorgang, der eine Start Grenze und eine Verzögerungszeit angibt, nach der der Task gestartet wird, nachdem das System gestartet wurde. Der Task enthält auch eine Aktion, die die Task Ausführung Notepad.exe angibt. Der Task wird mit dem lokalen Dienst Konto als Sicherheitskontext registriert, um den Task auszuführen.

Im folgenden Verfahren wird beschrieben, wie ein Task zum Starten einer ausführbaren Datei geplant wird, wenn das System gestartet wird.

**So planen Sie den Start von Notepad, wenn das System gestartet wird**

1.  Initialisieren Sie com, und legen Sie allgemeine com-Sicherheit fest.
2.  Erstellen Sie das [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) -Objekt.

    Mit diesem Objekt können Sie Aufgaben in einem angegebenen Ordner erstellen.

3.  Rufen Sie einen Aufgaben Ordner ab, in dem eine Aufgabe erstellt werden soll.

    Verwenden Sie die [**ITaskService:: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) -Methode, um den Ordner zu erhalten, und die [**ITaskService:: newtask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) -Methode zum Erstellen des [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Objekts.

4.  Definieren von Informationen über den Task mithilfe des [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Objekts, z. b. Registrierungsinformationen für den Task.

    Verwenden Sie die [**RegistrationInfo-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) und andere Eigenschaften der [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Schnittstelle, um die Aufgabeninformationen zu definieren.

5.  Erstellen Sie einen Start Trigger mithilfe der Triggers- [**Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) , um auf die [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) für die Aufgabe zuzugreifen.

    Verwenden Sie die [**ITriggerCollection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) -Methode, um anzugeben, dass Sie einen Start Trigger erstellen möchten. Sie können die Start Grenze und die Verzögerung für den-Befehl festlegen, sodass die Ausführung der Task Aktionen zu einem bestimmten Zeitpunkt geplant wird, zu dem das System gestartet wird.

6.  Erstellen Sie eine Aktion für die auszuführende Aufgabe mithilfe der [**Actions-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) für den Zugriff auf die [**IAction Collection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) -Auflistung für den Task.

    Verwenden Sie die [**IAction Collection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten. In diesem Beispiel wird ein [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) -Objekt verwendet, das eine Aktion darstellt, die einen Befehlszeilen Vorgang ausführt.

7.  Registrieren Sie die Aufgabe mit der [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) -Methode.

Im folgenden C++-Codebeispiel wird gezeigt, wie eine Aufgabe geplant wird, die Notepad.exe 30 Sekunden nach dem Start des Systems ausgeführt wird.


```C++
/********************************************************************
 This sample schedules a task to start Notepad.exe 30 seconds after
 the system is started. 
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")


using namespace std;

int __cdecl wmain()
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        printf("\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity(
        NULL,
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
        printf("\nCoInitializeSecurity failed: %x", hr );
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"Boot Trigger Test Task";

    //  Get the Windows directory and set the path to Notepad.exe.
    wstring wstrExecutablePath = _wgetenv( L"WINDIR");
    wstrExecutablePath += L"\\SYSTEM32\\NOTEPAD.EXE";


    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to create an instance of ITaskService: %x", hr);
          CoUninitialize();
          return 1;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(),
        _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        printf("ITaskService::Connect failed: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  
    //  This folder will hold the new task that is registered.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }
    
    //  If the same task exists, remove it.
    pRootFolder->DeleteTask( _bstr_t( wszTaskName), 0  );
    
    //  Create the task builder object to create the task.
    ITaskDefinition *pTask = NULL;
    hr = pService->NewTask( 0, &pTask );

    pService->Release();  // COM clean up.  Pointer is no longer used.
    if (FAILED(hr))
    {
          printf("Failed to create a task definition: %x", hr);
          pRootFolder->Release();
          CoUninitialize();
          return 1;
    }
    
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    IRegistrationInfo *pRegInfo= NULL;
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        printf("\nCannot get identification pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    hr = pRegInfo->put_Author(L"Author Name");
    pRegInfo->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put identification info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create the settings for the task
    ITaskSettings *pSettings = NULL;
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        printf("\nCannot get settings pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  Set setting values for the task. 
    hr = pSettings->put_StartWhenAvailable(VARIANT_TRUE);
    pSettings->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put setting info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
       

    //  ------------------------------------------------------
    //  Get the trigger collection to insert the boot trigger.
    ITriggerCollection *pTriggerCollection = NULL;
    hr = pTask->get_Triggers( &pTriggerCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get trigger collection: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  Add the boot trigger to the task.
    ITrigger *pTrigger = NULL;
    hr = pTriggerCollection->Create( TASK_TRIGGER_BOOT, &pTrigger ); 
    pTriggerCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create the trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    IBootTrigger *pBootTrigger = NULL;
    hr = pTrigger->QueryInterface( 
        IID_IBootTrigger, (void**) &pBootTrigger );
    pTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for IBootTrigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    hr = pBootTrigger->put_Id( _bstr_t( L"Trigger1" ) );
    if( FAILED(hr) )
       printf("\nCannot put the trigger ID: %x", hr);
    
    //  Set the task to start at a certain time. The time 
    //  format should be YYYY-MM-DDTHH:MM:SS(+-)(timezone).
    //  For example, the start boundary below
    //  is January 1st 2005 at 12:05
    hr = pBootTrigger->put_StartBoundary( _bstr_t(L"2005-01-01T12:05:00") );
    if( FAILED(hr) )
       printf("\nCannot put the start boundary: %x", hr);
  
    hr = pBootTrigger->put_EndBoundary( _bstr_t(L"2015-05-02T08:00:00") );
    if( FAILED(hr) )
       printf("\nCannot put the end boundary: %x", hr);

    // Delay the task to start 30 seconds after system start. 
    hr = pBootTrigger->put_Delay( L"PT30S" );
    pBootTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put delay for boot trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    } 
       

    //  ------------------------------------------------------
    //  Add an Action to the task. This task will execute Notepad.exe.     
    IActionCollection *pActionCollection = NULL;

    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get Task collection pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
        
    //  Create the action, specifying it as an executable action.
    IAction *pAction = NULL;
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    pActionCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create the action: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    IExecAction *pExecAction = NULL;
    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( 
        IID_IExecAction, (void**) &pExecAction );
    pAction->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for IExecAction: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  Set the path of the executable to Notepad.exe.
    hr = pExecAction->put_Path( _bstr_t( wstrExecutablePath.c_str() ) ); 
    pExecAction->Release(); 
    if( FAILED(hr) )
    {
        printf("\nCannot set path of executable: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
      
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    IRegisteredTask *pRegisteredTask = NULL;
    VARIANT varPassword;
    varPassword.vt = VT_EMPTY;
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t( wszTaskName ),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(L"Local Service"), 
            varPassword, 
            TASK_LOGON_SERVICE_ACCOUNT,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        printf("\nError saving the Task : %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    printf("\n Success! Task successfully registered. " );

    //  Clean up.
    pRootFolder->Release();
    pTask->Release();
    pRegisteredTask->Release();
    CoUninitialize();
    return 0;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




