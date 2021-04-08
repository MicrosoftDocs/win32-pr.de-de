---
title: Anzeigen von Aufgaben Namen und-Zuständen (C++)
description: In diesen beiden C++-Beispielen wird veranschaulicht, wie Aufgaben aufgezählt werden. In einem Beispiel wird gezeigt, wie Informationen zu Aufgaben in einem Aufgaben Ordner angezeigt werden. in den anderen Beispielen wird gezeigt, wie Informationen für alle ausgelaufenden Aufgaben angezeigt werden.
ms.assetid: 32037133-d3f3-4186-b035-ab01d37ed58d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6189960ef5b6e4ad78e75f156a482481f347b4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714285"
---
# <a name="displaying-task-names-and-states-c"></a>Anzeigen von Aufgaben Namen und-Zuständen (C++)

In diesen beiden C++-Beispielen wird veranschaulicht, wie Aufgaben aufgezählt werden. In einem Beispiel wird gezeigt, wie Informationen zu Aufgaben in einem Aufgaben Ordner angezeigt werden. in den anderen Beispielen wird gezeigt, wie Informationen für alle ausgelaufenden Aufgaben angezeigt werden.

Im folgenden Verfahren wird beschrieben, wie Aufgaben Namen und Status für alle Aufgaben in einem Aufgaben Ordner angezeigt werden.

**So zeigen Sie Aufgaben Namen und den Status für alle Aufgaben in einem Aufgaben Ordner an**

1.  Initialisieren Sie com, und legen Sie allgemeine com-Sicherheit fest.
2.  Erstellen Sie das [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) -Objekt.

    Mit diesem Objekt können Sie eine Verbindung mit dem Taskplaner-Dienst herstellen und auf einen bestimmten Aufgaben Ordner zugreifen.

3.  Sie erhalten einen Aufgaben Ordner, der die Aufgaben enthält, über die Sie Informationen erhalten möchten.

    Verwenden Sie die [**ITaskService:: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) -Methode, um den Ordner zu erhalten.

4.  Die Auflistung von Tasks aus dem Ordner erhalten.

    Verwenden Sie die [**ITaskFolder:: GetTasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-gettasks) -Methode, um die Sammlung von Aufgaben ([**iregisteredtaskcollection**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtaskcollection)) zu erhalten.

5.  Holen Sie sich die Anzahl der Aufgaben in der Auflistung, und durchlaufen Sie die einzelnen Aufgaben in der Sammlung.

    Verwenden Sie die [**Item-Eigenschaft von iregisteredtaskcollection**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtaskcollection-get_item) , um eine [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) -Instanz zu erhalten. Jede Instanz enthält eine Aufgabe in der Auflistung. Anschließend können Sie die Informationen (Eigenschaftswerte) für jede registrierte Aufgabe anzeigen.

Im folgenden Beispiel wird gezeigt, wie der Name und der Zustand aller Aufgaben im Stamm Aufgaben Ordner angezeigt werden.


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



Im folgenden Verfahren wird beschrieben, wie Aufgaben Namen und Status für alle ausgelaufenden Tasks angezeigt werden.

**So zeigen Sie Aufgaben Namen und den Status für alle ausgelaufenden Tasks an**

1.  Initialisieren Sie com, und legen Sie allgemeine com-Sicherheit fest.
2.  Erstellen Sie das [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) -Objekt.

    Mit diesem Objekt können Sie eine Verbindung mit dem Taskplaner-Dienst herstellen und auf einen bestimmten Aufgaben Ordner zugreifen.

3.  Verwenden Sie die [**ITaskService:: getrunningtasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getrunningtasks) -Methode, um eine Sammlung aller ausgelaufenden Tasks ("[**ununningtaskcollection**](/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection)") zu erhalten. Sie können angeben, um Instanzen der laufenden Aufgabe zu erhalten, indem Sie ausgeblendete Tasks einschließen oder ausschließen.
4.  Holen Sie sich die Anzahl der Aufgaben in der Auflistung, und durchlaufen Sie die einzelnen Aufgaben in der Sammlung.

    Verwenden Sie die [**Item-Eigenschaft von "ununningtaskcollection**](/windows/desktop/api/taskschd/nf-taskschd-irunningtaskcollection-get_item) ", um eine [**ununningtask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) -Instanz zu erhalten. Jede Instanz enthält eine Aufgabe in der Auflistung. Anschließend können Sie die Informationen (Eigenschaftswerte) für jede registrierte Aufgabe anzeigen.

Im folgenden Beispiel wird gezeigt, wie der Name und der Zustand aller ausgelaufenden Tasks, einschließlich ausgeblendeter Tasks, angezeigt werden.


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

 

 




