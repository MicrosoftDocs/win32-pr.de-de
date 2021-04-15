---
description: Zum Einrichten eines Client Kontexts in C++ kann eine Anwendung einen Client Kontext mit einem Handle für ein Token, einen Domänen-und Benutzernamen oder eine Zeichen folgen Darstellung der Sicherheits-ID des Clients erstellen.
ms.assetid: 765cd702-a1a8-4ff6-bea5-54de9fb62c0b
title: Einrichten eines Client Kontexts mit dem Autorisierungs-Manager in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79afa31db547b28d129c5b8e90dcf3e4ba1e91c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529387"
---
# <a name="establishing-a-client-context-with-authorization-manager-in-c"></a>Einrichten eines Client Kontexts mit dem Autorisierungs-Manager in C++

Im Autorisierungs-Manager bestimmt eine Anwendung, ob ein Client Zugriff auf einen Vorgang erhält, indem die [**Access Check**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) -Methode eines [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) -Objekts aufgerufen wird, das einen Client Kontext darstellt.

Eine Anwendung kann einen Client Kontext mit einem Handle für ein Token, einen Domänen-und Benutzernamen oder eine Zeichen folgen Darstellung der [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) des Clients erstellen.

Verwenden Sie die Methoden [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)und [**InitializeClientContextFromStringSID**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) der [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Schnittstelle, um einen Client Kontext zu erstellen.

Im folgenden Beispiel wird gezeigt, wie ein [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) -Objekt aus einem Client Token erstellt wird. Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist, dass dieser Speicher eine Anwendung mit dem Namen "Kosten" enthält und dass die Variable "hToken" ein gültiges Client Token enthält.


```C++
#include <windows.h>

void ExpenseCheck(ULONGLONG hToken)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzClientContext* pClientContext = NULL;
    BSTR storeName = NULL;
    BSTR appName = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
 
 //  Create a null VARIANT for function parameters.
    VARIANT myVar;
    VariantInit(&myVar);

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

    //  Allocate a string for the policy store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(0, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Create a client context from a token handle.
    hr = pApp->InitializeClientContextFromToken(hToken, myVar,
                &pClientContext);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create client context.");

    //  Use the client context as needed.

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pClientContext->Release();
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



 

 
