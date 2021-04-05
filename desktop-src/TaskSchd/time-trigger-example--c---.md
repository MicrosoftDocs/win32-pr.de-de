---
title: Beispiel für Zeit Auslösung (C++)
description: Dieses C++-Beispiel zeigt, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad zu einem bestimmten Zeitpunkt geplant ist.
ms.assetid: e45b18b0-5a7f-4283-b42f-15e9ffcfaff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f7f8d3c8bd1f179b0def9be069d710a2e126a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708909"
---
# <a name="time-trigger-example-c"></a><span data-ttu-id="f4e5a-103">Beispiel für Zeit Auslösung (C++)</span><span class="sxs-lookup"><span data-stu-id="f4e5a-103">Time Trigger Example (C++)</span></span>

<span data-ttu-id="f4e5a-104">Dieses C++-Beispiel zeigt, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad zu einem bestimmten Zeitpunkt geplant ist.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-104">This C++ example shows how to create a task that is scheduled to execute Notepad at a specified time.</span></span> <span data-ttu-id="f4e5a-105">Der Task enthält einen zeitbasierten-Auslösers, der eine Start Grenze und eine Endgrenze für den Task angibt.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-105">The task contains a time-based trigger that specifies a start boundary and an end boundary for the task.</span></span> <span data-ttu-id="f4e5a-106">Der Task enthält auch eine Aktion, die den Task zum Ausführen von Notepad angibt.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-106">The task also contains an action that specifies the task to execute Notepad.</span></span> <span data-ttu-id="f4e5a-107">Der Task wird mit einem interaktiven Anmeldetyp registriert. Dies bedeutet, dass der Task im Sicherheitskontext des Benutzers ausgeführt wird, der die Anwendung ausführt.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-107">The task is registered using an interactive logon type, which means the task runs under the security context of the user who runs the application.</span></span> <span data-ttu-id="f4e5a-108">Der Task enthält auch Einstellungen im Leerlauf, die angeben, wie Taskplaner Tasks ausführt, wenn sich der Computer im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-108">The task also contains idle settings, which specifies how Task Scheduler performs tasks when the computer is in an idle condition.</span></span>

<span data-ttu-id="f4e5a-109">Im folgenden Verfahren wird beschrieben, wie eine Aufgabe zum Starten einer ausführbaren Datei zu einem bestimmten Zeitpunkt geplant wird.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-109">The following procedure describes how to schedule a task to start an executable at a certain time.</span></span>

<span data-ttu-id="f4e5a-110">**So planen Sie den Start von Notepad zu einem bestimmten Zeitpunkt**</span><span class="sxs-lookup"><span data-stu-id="f4e5a-110">**To schedule Notepad to start at a specific time**</span></span>

1.  <span data-ttu-id="f4e5a-111">Initialisieren Sie com, und legen Sie allgemeine com-Sicherheit fest.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-111">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="f4e5a-112">Erstellen Sie das [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-112">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span>

    <span data-ttu-id="f4e5a-113">Mit diesem Objekt können Sie Aufgaben in einem angegebenen Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-113">This object allows you to create tasks in a specified folder.</span></span>

3.  <span data-ttu-id="f4e5a-114">Rufen Sie einen Aufgaben Ordner ab, in dem eine Aufgabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-114">Get a task folder to create a task in.</span></span>

    <span data-ttu-id="f4e5a-115">Verwenden Sie die [**ITaskService:: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) -Methode, um den Ordner zu erhalten, und die [**ITaskService:: newtask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) -Methode zum Erstellen des [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-115">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder, and the [**ITaskService::NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) method to create the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object.</span></span>

4.  <span data-ttu-id="f4e5a-116">Definieren von Informationen über den Task mithilfe des [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Objekts, z. b. Registrierungsinformationen für den Task.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-116">Define information about the task using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object, such as the registration information for the task.</span></span>

    <span data-ttu-id="f4e5a-117">Verwenden Sie die [**RegistrationInfo-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) und andere Eigenschaften der [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Schnittstelle, um die Aufgabeninformationen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-117">Use the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) and other properties of the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define the task information.</span></span>

5.  <span data-ttu-id="f4e5a-118">Erstellen Sie einen zeitbasierten Trigger mithilfe der Triggers- [**Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) , um auf die [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) für die Aufgabe zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-118">Create a time-based trigger using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) to access the [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) for the task.</span></span>

    <span data-ttu-id="f4e5a-119">Verwenden Sie die [**ITriggerCollection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) -Methode (geben Sie den Typ des zu erstellenden Triggers an), um einen zeitbasierten Trigger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-119">Use the [**ITriggerCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) method (specifying the type of trigger you want to create) to create a time-based trigger.</span></span> <span data-ttu-id="f4e5a-120">Auf diese Weise können Sie die Anfangs Grenze und die Endgrenze für den-Befehl festlegen, sodass die Aktionen der Aufgabe zur Ausführung zu einem bestimmten Zeitpunkt geplant werden.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-120">This allows you to set the start boundary and the end boundary for the trigger so that the task's actions will be scheduled to execute at a specified time.</span></span>

6.  <span data-ttu-id="f4e5a-121">Erstellen Sie eine Aktion für die Ausführung der Aufgabe mithilfe der [**Actions-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) , um auf die [**IAction Collection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) -Schnittstelle für den Task zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-121">Create an action for the task to execute by using the [**Actions property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) to access the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface for the task.</span></span>

    <span data-ttu-id="f4e5a-122">Verwenden Sie die [**IAction Collection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-122">Use the [**IActionCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="f4e5a-123">In diesem Beispiel wird ein [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) -Objekt verwendet, das eine Aktion darstellt, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-123">This example uses an [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) object, which represents an action that executes a command-line operation.</span></span>

7.  <span data-ttu-id="f4e5a-124">Registrieren Sie die Aufgabe mit der [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-124">Register the task using the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method.</span></span>

<span data-ttu-id="f4e5a-125">Im folgenden Beispiel wird gezeigt, wie Sie einen Task so planen, dass der Editor eine Minute nach der Registrierung der Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4e5a-125">The following C++ example shows how to schedule a task to execute Notepad one minute after the task is registered.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f4e5a-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f4e5a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4e5a-127">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="f4e5a-127">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




