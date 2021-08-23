---
title: Zeittriggerbeispiel (C++)
description: In diesem C++-Beispiel wird gezeigt, wie Sie eine Aufgabe erstellen, für die die Ausführung Editor zu einem bestimmten Zeitpunkt geplant ist.
ms.assetid: e45b18b0-5a7f-4283-b42f-15e9ffcfaff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 227d6fe24aa63b430376a7ce50d23b4b8ecd282f807315384b42175b9903d1b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059649"
---
# <a name="time-trigger-example-c"></a>Zeittriggerbeispiel (C++)

In diesem C++-Beispiel wird gezeigt, wie Sie eine Aufgabe erstellen, für die die Ausführung Editor zu einem bestimmten Zeitpunkt geplant ist. Die Aufgabe enthält einen zeitbasierten Trigger, der eine Startgrenze und eine Endgrenze für den Task angibt. Die Aufgabe enthält auch eine Aktion, die den Task angibt, der Editor ausgeführt werden soll. Die Aufgabe wird mit einem interaktiven Anmeldetyp registriert. Dies bedeutet, dass die Aufgabe im Sicherheitskontext des Benutzers ausgeführt wird, der die Anwendung ausführt. Die Aufgabe enthält auch Leerlaufeinstellungen, die angeben, wie Taskplaner Aufgaben ausführt, wenn sich der Computer in einem Leerlaufzustand befindet.

Im folgenden Verfahren wird beschrieben, wie eine Aufgabe so geplant wird, dass eine ausführbare Datei zu einem bestimmten Zeitpunkt gestartet wird.

**So planen Sie Editor, um zu einem bestimmten Zeitpunkt zu starten**

1.  Initialisieren Sie COM, und legen Sie die allgemeine COM-Sicherheit fest.
2.  Erstellen Sie das [**ITaskService-Objekt.**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)

    Mit diesem Objekt können Sie Aufgaben in einem angegebenen Ordner erstellen.

3.  Abrufen eines Aufgabenordners zum Erstellen einer Aufgabe.

    Verwenden Sie die [**ITaskService::GetFolder-Methode,**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) um den Ordner abzurufen, und die [**ITaskService::NewTask-Methode,**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) um das [**ITaskDefinition-Objekt**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) zu erstellen.

4.  Definieren Sie Informationen zur Aufgabe mithilfe des [**ITaskDefinition-Objekts,**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) z. B. die Registrierungsinformationen für die Aufgabe.

    Verwenden Sie die [**RegistrationInfo-Eigenschaft von ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) und andere Eigenschaften der [**ITaskDefinition-Schnittstelle,**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) um die Taskinformationen zu definieren.

5.  Erstellen Sie mithilfe der [**Trigger-Eigenschaft von ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) einen zeitbasierten Trigger, um auf die [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) für die Aufgabe zuzugreifen.

    Verwenden Sie die [**ITriggerCollection::Create-Methode**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) (die den Typ des Triggers angibt, den Sie erstellen möchten), um einen zeitbasierten Trigger zu erstellen. Dadurch können Sie die Startgrenze und die Endgrenze für den Trigger festlegen, sodass die Ausführung der Aufgabenaktionen zu einem bestimmten Zeitpunkt geplant wird.

6.  Erstellen Sie eine Aktion für die auszuführende Aufgabe, indem Sie die [**Actions-Eigenschaft von ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) verwenden, um auf die [**IActionCollection-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) für die Aufgabe zuzugreifen.

    Verwenden Sie die [**IActionCollection::Create-Methode,**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) um den Typ der Aktion anzugeben, die Sie erstellen möchten. In diesem Beispiel wird ein [**IExecAction-Objekt**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) verwendet, das eine Aktion darstellt, die einen Befehlszeilenvorgang ausführt.

7.  Registrieren Sie die Aufgabe mithilfe der [**ITaskFolder::RegisterTaskDefinition-Methode.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)

Das folgende C++-Beispiel zeigt, wie Sie eine Aufgabe so planen, dass sie Editor eine Minute nach der Registrierung des Tasks ausgeführt wird.


```C++
/********************************************************************
 This sample schedules a task to start notepad.exe 1 minute from the
 time the task is registered. 
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")
#pragma comment(lib, "credui.lib")

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
    LPCWSTR wszTaskName = L"Time Trigger Test Task";

    //  Get the windows directory and set the path to notepad.exe.
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
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        printf("Cannot get Root folder pointer: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }
    
    //  If the same task exists, remove it.
    pRootFolder->DeleteTask( _bstr_t( wszTaskName), 0  );
    
    //  Create the task definition object to create the task.
    ITaskDefinition *pTask = NULL;
    hr = pService->NewTask( 0, &pTask );

    pService->Release();  // COM clean up.  Pointer is no longer used.
    if (FAILED(hr))
    {
        printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
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
    
    hr = pRegInfo->put_Author( L"Author Name" );    
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
    //  Create the principal for the task - these credentials
    //  are overwritten with the credentials passed to RegisterTaskDefinition
    IPrincipal *pPrincipal = NULL;
    hr = pTask->get_Principal( &pPrincipal );
    if( FAILED(hr) )
    {
        printf("\nCannot get principal pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  Set up principal logon type to interactive logon
    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    pPrincipal->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put principal info: %x", hr );
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
        printf("\nCannot put setting information: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    // Set the idle settings for the task.
    IIdleSettings *pIdleSettings = NULL;
    hr = pSettings->get_IdleSettings( &pIdleSettings );
    if( FAILED(hr) )
    {
        printf("\nCannot get idle setting information: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    hr = pIdleSettings->put_WaitTimeout(L"PT5M");
    pIdleSettings->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put idle setting information: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    

    //  ------------------------------------------------------
    //  Get the trigger collection to insert the time trigger.
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

    //  Add the time trigger to the task.
    ITrigger *pTrigger = NULL;    
    hr = pTriggerCollection->Create( TASK_TRIGGER_TIME, &pTrigger );     
    pTriggerCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    ITimeTrigger *pTimeTrigger = NULL;
    hr = pTrigger->QueryInterface( 
        IID_ITimeTrigger, (void**) &pTimeTrigger );
    pTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for ITimeTrigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    hr = pTimeTrigger->put_Id( _bstr_t( L"Trigger1" ) );
    if( FAILED(hr) )
        printf("\nCannot put trigger ID: %x", hr);

    hr = pTimeTrigger->put_EndBoundary( _bstr_t(L"2015-05-02T08:00:00") );
    if( FAILED(hr) )
        printf("\nCannot put end boundary on trigger: %x", hr);

    //  Set the task to start at a certain time. The time 
    //  format should be YYYY-MM-DDTHH:MM:SS(+-)(timezone).
    //  For example, the start boundary below
    //  is January 1st 2005 at 12:05
    hr = pTimeTrigger->put_StartBoundary( _bstr_t(L"2005-01-01T12:05:00") );
    pTimeTrigger->Release();    
    if( FAILED(hr) )
    {
        printf("\nCannot add start boundary to trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    

    //  ------------------------------------------------------
    //  Add an action to the task. This task will execute notepad.exe.     
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
    
    //  Create the action, specifying that it is an executable action.
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

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t( wstrExecutablePath.c_str() ) );
    pExecAction->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put action path: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }  
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    IRegisteredTask *pRegisteredTask = NULL;
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t( wszTaskName ),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(), 
            _variant_t(), 
            TASK_LOGON_INTERACTIVE_TOKEN,
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

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




