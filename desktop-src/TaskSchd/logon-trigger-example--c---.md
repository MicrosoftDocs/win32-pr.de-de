---
title: Beispiel eines LOGON-Auslösers (C++)
description: Dieses C++-Beispiel zeigt, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad geplant ist, wenn sich ein Benutzer anmeldet.
ms.assetid: 15647234-8d1f-4d75-b215-92927b300c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137155a28a84a981b6013b6651f327a8c6bb4474
ms.sourcegitcommit: f19e3b30abea739d83178cdc8f2478eb4905f1d0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2020
ms.locfileid: "104316694"
---
# <a name="logon-trigger-example-c"></a><span data-ttu-id="2e9bd-103">Beispiel eines LOGON-Auslösers (C++)</span><span class="sxs-lookup"><span data-stu-id="2e9bd-103">Logon Trigger Example (C++)</span></span>

<span data-ttu-id="2e9bd-104">Dieses C++-Beispiel zeigt, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad geplant ist, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-104">This C++ example shows how to create a task that is scheduled to execute Notepad when a user logs on.</span></span> <span data-ttu-id="2e9bd-105">Der Task enthält einen Logon-Auslösers, der eine Start Grenze für die zu startende Aufgabe und eine Benutzer-ID angibt, die den Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-105">The task contains a logon trigger that specifies a start boundary for the task to start and a user identifier that specifies the user.</span></span> <span data-ttu-id="2e9bd-106">Der Task wird mithilfe der Gruppe "Administratoren" als Sicherheitskontext zum Ausführen der Aufgabe registriert.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-106">The task is registered using the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="2e9bd-107">Im folgenden Verfahren wird beschrieben, wie ein Task zum Starten einer ausführbaren Datei geplant wird, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-107">The following procedure describes how to schedule a task to start an executable when a user logs on.</span></span>

<span data-ttu-id="2e9bd-108">**So planen Sie den Start von Notepad, wenn sich ein Benutzer anmeldet**</span><span class="sxs-lookup"><span data-stu-id="2e9bd-108">**To schedule Notepad to start when a user logs on**</span></span>

1.  <span data-ttu-id="2e9bd-109">Initialisieren Sie com, und legen Sie allgemeine com-Sicherheit fest.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-109">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="2e9bd-110">Erstellen Sie das [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-110">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span>

    <span data-ttu-id="2e9bd-111">Mit diesem Objekt können Sie Aufgaben in einem angegebenen Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-111">This object allows you to create tasks in a specified folder.</span></span>

3.  <span data-ttu-id="2e9bd-112">Rufen Sie einen Aufgaben Ordner ab, in dem eine Aufgabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-112">Get a task folder to create a task in.</span></span>

    <span data-ttu-id="2e9bd-113">Verwenden Sie die [**ITaskService:: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) -Methode, um den Ordner zu erhalten, und die [**ITaskService:: newtask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) -Methode zum Erstellen des [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-113">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder, and the [**ITaskService::NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) method to create the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object.</span></span>

4.  <span data-ttu-id="2e9bd-114">Definieren von Informationen über den Task mithilfe des [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Objekts, z. b. Registrierungsinformationen für den Task.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-114">Define information about the task using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object, such as the registration information for the task.</span></span>

    <span data-ttu-id="2e9bd-115">Verwenden Sie die [**RegistrationInfo-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) und andere Eigenschaften der [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Schnittstelle, um die Aufgabeninformationen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-115">Use the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) and other properties of the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define the task information.</span></span>

5.  <span data-ttu-id="2e9bd-116">Erstellen Sie einen Logon-Trigger mithilfe der Triggers- [**Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) für den Zugriff auf die [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) -Schnittstelle für den Task.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-116">Create a logon trigger using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) to access the [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) interface for the task.</span></span>

    <span data-ttu-id="2e9bd-117">Verwenden Sie die [**ITriggerCollection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) -Methode, um anzugeben, dass Sie einen Logon-Trigger erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-117">Use the [**ITriggerCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) method to specify that you want to create a logon trigger.</span></span> <span data-ttu-id="2e9bd-118">Sie können die Start Grenze und die [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) -Eigenschaft für den-Befehl festlegen, sodass die Aktionen der Aufgabe für die Ausführung geplant werden, wenn sich der Benutzer nach der Start Grenze anmeldet.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-118">You can set the start boundary and the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property for the trigger so that the task's actions will be scheduled to execute when the user logs on after the start boundary.</span></span>

6.  <span data-ttu-id="2e9bd-119">Erstellen Sie eine Aktion für die Ausführung der Aufgabe mithilfe der [**Actions-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) , um auf die [**IAction Collection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) -Schnittstelle für den Task zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-119">Create an action for the task to execute by using the [**Actions property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) to access the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface for the task.</span></span> <span data-ttu-id="2e9bd-120">Verwenden Sie die [**IAction Collection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-120">Use the [**IActionCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="2e9bd-121">In diesem Beispiel wird ein [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) -Objekt verwendet, das eine Aktion darstellt, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-121">This example uses an [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) object, which represents an action that executes a command-line operation.</span></span>
7.  <span data-ttu-id="2e9bd-122">Registrieren Sie die Aufgabe mit der [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-122">Register the task using the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method.</span></span>

<span data-ttu-id="2e9bd-123">Im folgenden Beispiel wird gezeigt, wie eine Aufgabe für die Ausführung von Notepad geplant wird, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="2e9bd-123">The following C++ example shows how to schedule a task to execute Notepad when a user logs on.</span></span>


```C++
/**********************************************************************
 This sample schedules a task to start notepad.exe when a user logs on. 
**********************************************************************/

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
    LPCWSTR wszTaskName = L"Logon Trigger Test Task";

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
    //  Get the trigger collection to insert the logon trigger.
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

    //  Add the logon trigger to the task.
    ITrigger *pTrigger = NULL;
    hr = pTriggerCollection->Create( TASK_TRIGGER_LOGON, &pTrigger );
    pTriggerCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create the trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    ILogonTrigger *pLogonTrigger = NULL;       
    hr = pTrigger->QueryInterface( 
            IID_ILogonTrigger, (void**) &pLogonTrigger );
    pTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for ILogonTrigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    hr = pLogonTrigger->put_Id( _bstr_t( L"Trigger1" ) );
    if( FAILED(hr) )
       printf("\nCannot put the trigger ID: %x", hr);
    
    //  Set the task to start at a certain time. The time 
    //  format should be YYYY-MM-DDTHH:MM:SS(+-)(timezone).
    //  For example, the start boundary below
    //  is January 1st 2005 at 12:05
    hr = pLogonTrigger->put_StartBoundary( _bstr_t(L"2005-01-01T12:05:00") );
    if( FAILED(hr) )
       printf("\nCannot put the start boundary: %x", hr);
    
    hr = pLogonTrigger->put_EndBoundary( _bstr_t(L"2015-05-02T08:00:00") );
    if( FAILED(hr) )
       printf("\nCannot put the end boundary: %x", hr);    
    
    //  Define the user.  The task will execute when the user logs on.
    //  The specified user must be a user on this computer.  
    hr = pLogonTrigger->put_UserId( _bstr_t( L"DOMAIN\\UserName" ) );  
    pLogonTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot add user ID to logon trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Add an Action to the task. This task will execute notepad.exe.     
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
        printf("\nCannot set path of executable: %x", hr );
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
            _variant_t(L"S-1-5-32-544"),
            _variant_t(), 
            TASK_LOGON_GROUP,
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

    // Clean up
    pRootFolder->Release();
    pTask->Release();
    pRegisteredTask->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="2e9bd-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2e9bd-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e9bd-125">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="2e9bd-125">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




