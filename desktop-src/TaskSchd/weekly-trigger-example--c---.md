---
title: Beispiel für wöchentlichen Trigger (C++)
description: In diesem C++-Beispiel wird veranschaulicht, wie eine Aufgabe erstellt wird, für die die wöchentliche Ausführung Editor geplant ist.
ms.assetid: 7c70b743-aff2-4ef5-b65b-ef0b5fdacade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530ba3226668b8e743fe4ce1701e4b178f27fa5bee03b9518c23c2378ea0b5e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001878"
---
# <a name="weekly-trigger-example-c"></a>Beispiel für wöchentlichen Trigger (C++)

In diesem C++-Beispiel wird veranschaulicht, wie eine Aufgabe erstellt wird, für die die wöchentliche Ausführung Editor geplant ist. Die Aufgabe enthält einen wöchentlichen Trigger, der eine Startgrenze, ein Wochenintervall und einen Wochentag für den Start der Aufgabe angibt. Der Task enthält auch eine Aktion, die den Task angibt, der ausgeführt Editor.

Im folgenden Verfahren wird beschrieben, wie Sie einen Task planen, um eine ausführbare Datei wöchentlich zu starten.

**So planen sie Editor wöchentlichen Start**

1.  Initialisieren Sie COM, und legen Sie allgemeine COM-Sicherheit fest.
2.  Erstellen Sie das [**ITaskService-Objekt.**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)

    Mit diesem Objekt können Sie Aufgaben in einem angegebenen Ordner erstellen.

3.  Sie können einen Aufgabenordner zum Erstellen einer Aufgabe in erstellen.

    Verwenden Sie [**die ITaskService::GetFolder-Methode,**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) um den Ordner zu erhalten, und die [**ITaskService::NewTask-Methode,**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) um das [**ITaskDefinition-Objekt zu**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) erstellen.

4.  Definieren Sie Informationen zur Aufgabe mithilfe des [**ITaskDefinition-Objekts,**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) z. B. die Registrierungsinformationen für den Task.

    Verwenden Sie [**die RegistrationInfo-Eigenschaft von ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) und andere Eigenschaften der [**ITaskDefinition-Schnittstelle,**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) um die Aufgabeninformationen zu definieren.

5.  Erstellen Sie einen wöchentlichen Trigger mithilfe [**der Trigger-Eigenschaft von ITaskDefinition,**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) um auf die [**ITriggerCollection-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) für die Aufgabe zu zugreifen.

    Verwenden Sie [**die ITriggerCollection::Create-Methode,**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) um anzugeben, dass Sie einen wöchentlichen Trigger erstellen möchten. Sie können die Startgrenze, das Wochenintervall und den Wochentag für den [**IWeeklyTrigger-Trigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) festlegen, damit die Aufgabenaktionen zu einem bestimmten Zeitpunkt an einem bestimmten Wochentag ausgeführt werden.

6.  Erstellen Sie eine Aktion für die auszuführende Aufgabe, indem Sie mithilfe der Actions-Eigenschaft von [**ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) auf die [**IActionCollection-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) für die Aufgabe zugreifen.

    Verwenden Sie [**die IActionCollection::Create-Methode,**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) um den Typ der Aktion anzugeben, die Sie erstellen möchten. In diesem Beispiel wird ein [**IExecAction-Objekt**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) verwendet, das eine Aktion darstellt, die einen Befehlszeilenvorgang ausgeführt.

7.  Registrieren Sie die Aufgabe mithilfe der [**ITaskFolder::RegisterTaskDefinition-Methode.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)

Das folgende C++-Beispiel zeigt, wie sie eine Aufgabe so planen, dass Editor wöchentlich ausgeführt wird.


```C++
/********************************************************************
 This sample schedules a task to start on a weekly basis. 
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


void main(void)
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        printf("\nCoInitializeEx failed: %x", hr );
        return;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_PKT,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL,
        0,
        NULL);

    if( FAILED(hr) )
    {
        printf("\nCoInitializeSecurity failed: %x", hr );
        CoUninitialize();
        return;
    }

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"Weekly Trigger Task";

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
          return;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(),
        _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        printf("ITaskService::Connect failed: %x", hr );
        pService->Release();
        CoUninitialize();
        return;
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
        return;
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
          return;
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
        return;
    }
    
    hr = pRegInfo->put_Author( L"Author Name" );
    pRegInfo->Release();  // COM clean up.  Pointer is no longer used.
    if( FAILED(hr) )
    {
        printf("\nCannot put identification info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }
    
    //  ------------------------------------------------------
    //  Get the trigger collection to insert the weekly trigger.
    ITriggerCollection *pTriggerCollection = NULL;
    hr = pTask->get_Triggers( &pTriggerCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get trigger collection: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }
        
    ITrigger *pTrigger = NULL;
    hr = pTriggerCollection->Create( TASK_TRIGGER_WEEKLY, &pTrigger );     
    pTriggerCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create the trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }

    IWeeklyTrigger *pWeeklyTrigger = NULL;
    hr = pTrigger->QueryInterface( 
            IID_IWeeklyTrigger, (void**) &pWeeklyTrigger );
    pTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call for IWeeklyTrigger failed: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }
    
    hr = pWeeklyTrigger->put_Id( _bstr_t( L"Trigger1" ) );
    if( FAILED(hr) )
        printf("\nCannot put trigger ID: %x", hr);

    //  Set the task to start weekly at a certain time. The time 
    //  format should be YYYY-MM-DDTHH:MM:SS(+-)(timezone).
    //  For example, the start boundary below is January 1st 2005 at
    //  12:05
    hr = pWeeklyTrigger->put_StartBoundary( _bstr_t(L"2005-01-01T12:05:00") );
    if( FAILED(hr) )
        printf("\nCannot put the start boundary: %x", hr);

    //  Set the time when the trigger is deactivated.
    hr = pWeeklyTrigger->put_EndBoundary( _bstr_t(L"2007-01-01T12:05:00") );
    if( FAILED(hr) )
        printf("\nCannot put the end boundary: %x", hr);
    
    
    //  Define the interval for the weekly trigger. 
    //  An interval of 2 produces an
    //  every other week schedule
    hr = pWeeklyTrigger->put_WeeksInterval( (short)2 );
    if( FAILED(hr) )
    {
        printf("\nCannot put weeks interval: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }
    
    hr = pWeeklyTrigger->put_DaysOfWeek( (short)2 );    // Runs on Monday
    pWeeklyTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put days of week interval: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
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
        return;
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
        return;
    }

    IExecAction *pExecAction = NULL;
    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( 
        IID_IExecAction, (void**) &pExecAction );
    pAction->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed on IExecAction: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t( wstrExecutablePath.c_str() ) );
    pExecAction->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot add path for executable action: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }

    //  ------------------------------------------------------
    //  Securely get the user name and password. The task will
    //  be created to run with the credentials from the supplied 
    //  user name and password.
    CREDUI_INFO cui;
    TCHAR pszName[CREDUI_MAX_USERNAME_LENGTH] = "";
    TCHAR pszPwd[CREDUI_MAX_PASSWORD_LENGTH] = "";
    BOOL fSave;
    DWORD dwErr;

    cui.cbSize = sizeof(CREDUI_INFO);
    cui.hwndParent = NULL;
    //  Ensure that MessageText and CaptionText identify
    //  what credentials to use and which application requires them.
    cui.pszMessageText = TEXT("Account information for task registration:");
    cui.pszCaptionText = TEXT("Enter Account Information for Task Registration");
    cui.hbmBanner = NULL;
    fSave = FALSE;

    //  Create the UI asking for the credentials.
    dwErr = CredUIPromptForCredentials(
        &cui,                             //  CREDUI_INFO structure
        TEXT(""),                         //  Target for credentials
        NULL,                             //  Reserved
        0,                                //  Reason
        pszName,                          //  User name
        CREDUI_MAX_USERNAME_LENGTH,       //  Max number for user name
        pszPwd,                           //  Password
        CREDUI_MAX_PASSWORD_LENGTH,       //  Max number for password
        &fSave,                           //  State of save check box
        CREDUI_FLAGS_GENERIC_CREDENTIALS |  //  Flags
        CREDUI_FLAGS_ALWAYS_SHOW_UI |
        CREDUI_FLAGS_DO_NOT_PERSIST);  

    if(dwErr)
    {
        cout << "Did not get credentials." << endl;    
        CoUninitialize();
        return;      
    }

    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    IRegisteredTask *pRegisteredTask = NULL;
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t( wszTaskName ),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(_bstr_t(pszName)), 
            _variant_t(_bstr_t(pszPwd)), 
            TASK_LOGON_PASSWORD,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        printf("\nError saving the Task : %x", hr );
        pRootFolder->Release();
        pTask->Release();
        SecureZeroMemory(pszName, sizeof(pszName));
        SecureZeroMemory(pszPwd, sizeof(pszPwd));
        CoUninitialize();
        return;
    }

    printf("\n Success! Task succesfully registered. " );

    //  Clean up
    pRootFolder->Release();
    pTask->Release();
    pRegisteredTask->Release();
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
    CoUninitialize();
    return;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




