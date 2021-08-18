---
title: Anzeigen von Aufgabennamen und -zuzuständen (C++)
description: In diesen beiden C++-Beispielen wird gezeigt, wie Tasks aufzählt werden. Ein Beispiel zeigt, wie Informationen für Aufgaben in einem Aufgabenordner angezeigt werden, und die anderen Beispiele zeigen, wie Informationen für alle ausgeführten Aufgaben angezeigt werden.
ms.assetid: 32037133-d3f3-4186-b035-ab01d37ed58d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b80ec17b71ae45c951a27ca582855936d73457401d878b0f21f69bcbaa71ca23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760185"
---
# <a name="displaying-task-names-and-states-c"></a>Anzeigen von Aufgabennamen und -zuzuständen (C++)

In diesen beiden C++-Beispielen wird gezeigt, wie Tasks aufzählt werden. Ein Beispiel zeigt, wie Informationen für Aufgaben in einem Aufgabenordner angezeigt werden, und die anderen Beispiele zeigen, wie Informationen für alle ausgeführten Aufgaben angezeigt werden.

Im folgenden Verfahren wird beschrieben, wie Aufgabennamen und -status für alle Aufgaben in einem Aufgabenordner angezeigt werden.

**So zeigen Sie Aufgabennamen und -status für alle Aufgaben in einem Aufgabenordner an**

1.  Initialisieren Sie COM, und legen Sie allgemeine COM-Sicherheit fest.
2.  Erstellen Sie das [**ITaskService-Objekt.**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)

    Mit diesem Objekt können Sie eine Verbindung mit dem Taskplaner herstellen und auf einen bestimmten Aufgabenordner zugreifen.

3.  Get a task folder that holds the tasks you want information about.

    Verwenden Sie [**die ITaskService::GetFolder-Methode,**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) um den Ordner zu erhalten.

4.  Sie können die Auflistung der Aufgaben aus dem Ordner erhalten.

    Verwenden Sie [**die ITaskFolder::GetTasks-Methode,**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-gettasks) um die Auflistung von Aufgaben ([**IRegisteredTaskCollection ) zu erhalten.**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtaskcollection)

5.  Sie können die Anzahl der Aufgaben in der Auflistung erhalten und die einzelnen Aufgaben in der Auflistung aufzählen.

    Verwenden Sie [**die Item-Eigenschaft von IRegisteredTaskCollection,**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtaskcollection-get_item) um eine [**IRegisteredTask-Instanz**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) zu erhalten. Jede Instanz enthält eine Aufgabe in der Auflistung. Anschließend können Sie die Informationen (Eigenschaftswerte) der einzelnen registrierten Aufgaben anzeigen.

Das folgende C++-Beispiel zeigt, wie Der Name und Status aller Aufgaben im Stammaufgabenordner angezeigt werden.


```C++
/********************************************************************
 This sample enumerates through the tasks on the local computer and 
 displays their name and state. 
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
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
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
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    
    pService->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        CoUninitialize();
        return 1;
    }
    
    //  -------------------------------------------------------
    //  Get the registered tasks in the folder.
    IRegisteredTaskCollection* pTaskCollection = NULL;
    hr = pRootFolder->GetTasks( NULL, &pTaskCollection );

    pRootFolder->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get the registered tasks.: %x", hr);
        CoUninitialize();
        return 1;
    }

    LONG numTasks = 0;
    hr = pTaskCollection->get_Count(&numTasks);

    if( numTasks == 0 )
     {
        printf("\nNo Tasks are currently running" );
        pTaskCollection->Release();
        CoUninitialize();
        return 1;
     }

    printf("\nNumber of Tasks : %d", numTasks );

    TASK_STATE taskState;
    
    for(LONG i=0; i < numTasks; i++)
    {
        IRegisteredTask* pRegisteredTask = NULL;
        hr = pTaskCollection->get_Item( _variant_t(i+1), &pRegisteredTask );
        
        if( SUCCEEDED(hr) )
        {
            BSTR taskName = NULL;
            hr = pRegisteredTask->get_Name(&taskName);
            if( SUCCEEDED(hr) )
            {
                printf("\nTask Name: %S", taskName);
                SysFreeString(taskName);

                hr = pRegisteredTask->get_State(&taskState);
                if (SUCCEEDED (hr) )
                    printf("\n\tState: %d", taskState);
                else 
                    printf("\n\tCannot get the registered task state: %x", hr);
            }
            else
            {
                printf("\nCannot get the registered task name: %x", hr);
            }
            pRegisteredTask->Release();
        }
        else
        {
            printf("\nCannot get the registered task item at index=%d: %x", i+1, hr);
        }
    }

    pTaskCollection->Release();
    CoUninitialize();
    return 0;
}

```



Im folgenden Verfahren wird beschrieben, wie Aufgabennamen und -status für alle ausgeführten Aufgaben angezeigt werden.

**So zeigen Sie Aufgabennamen und -status für alle ausgeführten Aufgaben an**

1.  Initialisieren Sie COM, und legen Sie allgemeine COM-Sicherheit fest.
2.  Erstellen Sie das [**ITaskService-Objekt.**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)

    Mit diesem Objekt können Sie eine Verbindung mit dem Taskplaner herstellen und auf einen bestimmten Aufgabenordner zugreifen.

3.  Verwenden Sie [**die ITaskService::GetRunningTasks-Methode,**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getrunningtasks) um eine Auflistung aller ausgeführten Aufgaben [**(IRunningTaskCollection) zu erhalten.**](/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection) Sie können angeben, dass Instanzen der ausgeführten Aufgabe entweder ausgeblendete Aufgaben ein- oder ausschließen.
4.  Sie können die Anzahl der Aufgaben in der Auflistung erhalten und die einzelnen Aufgaben in der Auflistung aufzählen.

    Verwenden Sie [**die Item-Eigenschaft von IRunningTaskCollection,**](/windows/desktop/api/taskschd/nf-taskschd-irunningtaskcollection-get_item) um eine [**IRunningTask-Instanz**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) zu erhalten. Jede Instanz enthält eine Aufgabe in der Auflistung. Anschließend können Sie die Informationen (Eigenschaftswerte) der einzelnen registrierten Aufgaben anzeigen.

Das folgende C++-Beispiel zeigt, wie Der Name und Status aller ausgeführten Aufgaben, einschließlich ausgeblendeter Aufgaben, angezeigt werden.


```C++
/********************************************************************
 This sample enumerates through all running tasks on the local computer and 
 displays their name and state. 
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
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
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

       // Get the running tasks.
       IRunningTaskCollection* pRunningTasks = NULL;
       hr = pService->GetRunningTasks(TASK_ENUM_HIDDEN, &pRunningTasks);

    pService->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        CoUninitialize();
        return 1;
    }
        
    LONG numTasks = 0;
    hr = pRunningTasks->get_Count(&numTasks);

    if( numTasks == 0 )
     {
        printf("\nNo Tasks are currently running" );
        pRunningTasks->Release();
        CoUninitialize();
        return 1;
     }

    printf("\nNumber of running tasks : %d", numTasks );

    TASK_STATE taskState;
    
    for(LONG i=0; i < numTasks; i++)
    {
        IRunningTask* pRunningTask = NULL;
        hr = pRunningTasks->get_Item( _variant_t(i+1), &pRunningTask );
        
        if( SUCCEEDED(hr) )
        {
            BSTR taskName = NULL;
            hr = pRunningTask->get_Name(&taskName);
            if( SUCCEEDED(hr) )
            {
                printf("\nTask Name: %S", taskName);
                SysFreeString(taskName);

                hr = pRunningTask->get_State(&taskState);
                if (SUCCEEDED (hr) )
                    printf("\n\tState: %d", taskState);
                else 
                    printf("\n\tCannot get the registered task state: %x", hr);
            }
            else
            {
                printf("\nCannot get the registered task name: %x", hr);
            }
            pRunningTask->Release();
        }
        else
        {
            printf("\nCannot get the registered task item at index=%d: %x", i+1, hr);
        }
    }

    pRunningTasks->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




