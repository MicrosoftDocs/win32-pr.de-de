---
description: Ein Autorisierungs Richtlinien Speicher enthält Autorisierungs Richtlinien Informationen für eine oder mehrere Anwendungen. Für jede Anwendung, die diesen Richtlinien Speicher verwendet, müssen Sie ein IAzApplication-Objekt erstellen und in einem Richtlinien Speicher speichern.
ms.assetid: 2bba1068-ae03-4388-be4d-9865e42e440e
title: Erstellen eines Anwendungs Objekts in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86885124e2fff52bc5cce2260e3d7fb727b58eb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863255"
---
# <a name="creating-an-application-object-in-c"></a><span data-ttu-id="6671c-104">Erstellen eines Anwendungs Objekts in C++</span><span class="sxs-lookup"><span data-stu-id="6671c-104">Creating an Application Object in C++</span></span>

<span data-ttu-id="6671c-105">Ein Autorisierungs Richtlinien Speicher enthält Autorisierungs Richtlinien Informationen für eine oder mehrere Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="6671c-105">An authorization policy store contains authorization policy information for one or more applications.</span></span> <span data-ttu-id="6671c-106">Für jede Anwendung, die diesen Richtlinien Speicher verwendet, müssen Sie ein [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekt erstellen und in einem Richtlinien Speicher speichern.</span><span class="sxs-lookup"><span data-stu-id="6671c-106">For each application that uses that policy store, you must create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object and save it to a policy store.</span></span>

<span data-ttu-id="6671c-107">Im folgenden Beispiel wird gezeigt, wie ein [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekt erstellt wird, das eine Anwendung darstellt, und wie das **IAzApplication** -Objekt dem Autorisierungs Richtlinien Speicher hinzugefügt wird, der von der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6671c-107">The following example shows how to create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object that represents an application and how to add the **IAzApplication** object to the authorization policy store the application uses.</span></span> <span data-ttu-id="6671c-108">Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6671c-108">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;

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
    
    //  Initialize the existing store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
         MyHandleError("Could not allocate application name string");
    hr = pStore->CreateApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application.");

    //  Save changes to the store.
    hr = pApp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save changes to store.");

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
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



 

 



