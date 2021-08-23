---
description: Im Autorisierungs-Manager ist eine Aufgabe eine aktion auf hoher Ebene, die Benutzer einer Anwendung abschließen müssen. Aufgaben besteht aus Vorgängen, bei denen es sich um Low-Level-Funktionen und -Methoden der Anwendung handelt.
ms.assetid: a9a0202e-44c9-4192-8ff8-e22bddf26cfe
title: Gruppieren von Vorgängen in Tasks in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adfcfee2368a04fcd1b97faa6c27184371e047d0753080894c87d93c69957c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672080"
---
# <a name="grouping-operations-into-tasks-in-c"></a>Gruppieren von Vorgängen in Tasks in C++

Im Autorisierungs-Manager ist eine Aufgabe eine aktion auf hoher Ebene, die Benutzer einer Anwendung abschließen müssen. Aufgaben besteht aus Vorgängen, bei denen es sich um Low-Level-Funktionen und -Methoden der Anwendung handelt. Eine Aufgabe wird dann den Rollen zugewiesen, die diese Aufgabe ausführen müssen. Eine Aufgabe wird durch ein [**IAzTask-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iaztask) dargestellt. Weitere Informationen zu Vorgängen und Aufgaben finden Sie unter [Vorgänge und Aufgaben.](operations-and-tasks.md)

Im folgenden Beispiel wird gezeigt, wie Vorgänge zum Erstellen einer Aufgabe gegruppen werden. Im Beispiel wird davon ausgegangen, dass im Stammverzeichnis von Laufwerk C ein XML-Richtlinienspeicher namens MyStore.xml vorhanden ist, dass dieser Speicher eine Anwendung namens Expense enthält und dass diese Anwendung Vorgänge enthält, die im Thema Definieren von [Vorgängen in C++](defining-operations-in-c--.md)definiert sind.


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif
#pragma comment(lib, "duser.lib")

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzTask* pTask = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR taskName = NULL;
    BSTR opName = NULL;
    
    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    //  Create null VARIANT for parameters.
    VARIANT myVar; 
    VariantInit(&myVar);

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
  storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Create a task object.
    if (!(taskName = SysAllocString(L"Submit Expense")))
        MyHandleError("Could not allocate task name string.");
    hr = pApp->CreateTask(taskName, myVar, &pTask);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create task.");

    //  Add operations to the task.
    if (!(opName = SysAllocString(L"RetrieveForm")))
        MyHandleError("Could not allocate operation name string.");
    hr = pTask->AddOperation(opName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add 1st operation to the task.");
    SysFreeString(opName);

    if (!(opName = SysAllocString(L"EnqueRequest")))
        MyHandleError("Could not allocate operation name string.");
    hr = pTask->AddOperation(opName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add 2nd operation to the task.");
    SysFreeString(opName);

    if (!(opName = SysAllocString(L"UseFormControl")))
        MyHandleError("Could not allocate operation name string.");
    hr = pTask->AddOperation(opName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add 3rd operation to the task.");
    SysFreeString(opName);

    //  Save information to the store.
    hr = pTask->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save task data to the store.");

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pTask->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    VariantClear(&myVar);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 



