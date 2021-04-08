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
# <a name="boot-trigger-example-c"></a><span data-ttu-id="47aab-103">Beispiel für einen Start Auslösers (C++)</span><span class="sxs-lookup"><span data-stu-id="47aab-103">Boot Trigger Example (C++)</span></span>

<span data-ttu-id="47aab-104">Dieses Thema enthält ein C++-Codebeispiel, das veranschaulicht, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad.exe geplant ist, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="47aab-104">This topic contains a C++ code example that shows how to create a task that is scheduled to execute Notepad.exe when the system is started.</span></span> <span data-ttu-id="47aab-105">Der Task enthält einen Start--Vorgang, der eine Start Grenze und eine Verzögerungszeit angibt, nach der der Task gestartet wird, nachdem das System gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="47aab-105">The task contains a boot trigger that specifies a start boundary and delay time for the task to start after the system is started.</span></span> <span data-ttu-id="47aab-106">Der Task enthält auch eine Aktion, die die Task Ausführung Notepad.exe angibt.</span><span class="sxs-lookup"><span data-stu-id="47aab-106">The task also contains an action that specifies the task execute Notepad.exe.</span></span> <span data-ttu-id="47aab-107">Der Task wird mit dem lokalen Dienst Konto als Sicherheitskontext registriert, um den Task auszuführen.</span><span class="sxs-lookup"><span data-stu-id="47aab-107">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="47aab-108">Im folgenden Verfahren wird beschrieben, wie ein Task zum Starten einer ausführbaren Datei geplant wird, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="47aab-108">The following procedure describes how to schedule a task to start an executable when the system is started.</span></span>

<span data-ttu-id="47aab-109">**So planen Sie den Start von Notepad, wenn das System gestartet wird**</span><span class="sxs-lookup"><span data-stu-id="47aab-109">**To schedule Notepad to start when the system is started**</span></span>

1.  <span data-ttu-id="47aab-110">Initialisieren Sie com, und legen Sie allgemeine com-Sicherheit fest.</span><span class="sxs-lookup"><span data-stu-id="47aab-110">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="47aab-111">Erstellen Sie das [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="47aab-111">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span>

    <span data-ttu-id="47aab-112">Mit diesem Objekt können Sie Aufgaben in einem angegebenen Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="47aab-112">This object enables you to create tasks in a specified folder.</span></span>

3.  <span data-ttu-id="47aab-113">Rufen Sie einen Aufgaben Ordner ab, in dem eine Aufgabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="47aab-113">Get a task folder to create a task in.</span></span>

    <span data-ttu-id="47aab-114">Verwenden Sie die [**ITaskService:: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) -Methode, um den Ordner zu erhalten, und die [**ITaskService:: newtask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) -Methode zum Erstellen des [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="47aab-114">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder, and the [**ITaskService::NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) method to create the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object.</span></span>

4.  <span data-ttu-id="47aab-115">Definieren von Informationen über den Task mithilfe des [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Objekts, z. b. Registrierungsinformationen für den Task.</span><span class="sxs-lookup"><span data-stu-id="47aab-115">Define information about the task using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object, such as the registration information for the task.</span></span>

    <span data-ttu-id="47aab-116">Verwenden Sie die [**RegistrationInfo-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) und andere Eigenschaften der [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Schnittstelle, um die Aufgabeninformationen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="47aab-116">Use the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) and other properties of the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define the task information.</span></span>

5.  <span data-ttu-id="47aab-117">Erstellen Sie einen Start Trigger mithilfe der Triggers- [**Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) , um auf die [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) für die Aufgabe zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="47aab-117">Create a boot trigger using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) to access the [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) for the task.</span></span>

    <span data-ttu-id="47aab-118">Verwenden Sie die [**ITriggerCollection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) -Methode, um anzugeben, dass Sie einen Start Trigger erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="47aab-118">Use the [**ITriggerCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) method to specify that you want to create a boot trigger.</span></span> <span data-ttu-id="47aab-119">Sie können die Start Grenze und die Verzögerung für den-Befehl festlegen, sodass die Ausführung der Task Aktionen zu einem bestimmten Zeitpunkt geplant wird, zu dem das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="47aab-119">You can set the start boundary and delay for the trigger so that the task actions will be scheduled to execute at a specified time when the system is started.</span></span>

6.  <span data-ttu-id="47aab-120">Erstellen Sie eine Aktion für die auszuführende Aufgabe mithilfe der [**Actions-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) für den Zugriff auf die [**IAction Collection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) -Auflistung für den Task.</span><span class="sxs-lookup"><span data-stu-id="47aab-120">Create an action for the task to execute by using the [**Actions property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) to access the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) collection for the task.</span></span>

    <span data-ttu-id="47aab-121">Verwenden Sie die [**IAction Collection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="47aab-121">Use the [**IActionCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) method to specify the type of action you want to create.</span></span> <span data-ttu-id="47aab-122">In diesem Beispiel wird ein [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) -Objekt verwendet, das eine Aktion darstellt, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="47aab-122">This example uses an [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) object, which represents an action that executes a command-line operation.</span></span>

7.  <span data-ttu-id="47aab-123">Registrieren Sie die Aufgabe mit der [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) -Methode.</span><span class="sxs-lookup"><span data-stu-id="47aab-123">Register the task using the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method.</span></span>

<span data-ttu-id="47aab-124">Im folgenden C++-Codebeispiel wird gezeigt, wie eine Aufgabe geplant wird, die Notepad.exe 30 Sekunden nach dem Start des Systems ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47aab-124">The following C++ code example shows how to schedule a task to execute Notepad.exe 30 seconds after the system is started.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="47aab-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47aab-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47aab-126">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="47aab-126">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




