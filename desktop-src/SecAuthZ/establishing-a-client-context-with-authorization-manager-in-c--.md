---
description: Um einen Clientkontext in C++ zu erstellen, kann eine Anwendung einen Clientkontext mit einem Handle für ein Token, eine Domäne und einen Benutzernamen oder eine Zeichenfolgendarstellung der Sicherheits-ID des Clients erstellen.
ms.assetid: 765cd702-a1a8-4ff6-bea5-54de9fb62c0b
title: Einrichten eines Clientkontexts mit dem Autorisierungs-Manager in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1b74cab7d6c113f5120a682250f85dca772e1764acf432317049da27ec091d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672120"
---
# <a name="establishing-a-client-context-with-authorization-manager-in-c"></a>Einrichten eines Clientkontexts mit dem Autorisierungs-Manager in C++

Im Autorisierungs-Manager bestimmt eine Anwendung, ob einem Client Zugriff auf einen Vorgang erteilt wird, indem die [**AccessCheck-Methode**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) eines [**IAzClientContext-Objekts**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) aufgerufen wird, das einen Clientkontext darstellt.

Eine Anwendung kann einen Clientkontext mit einem Handle für ein Token, eine [](/windows/desktop/SecGloss/s-gly) Domäne und einen Benutzernamen oder eine Zeichenfolgendarstellung der Sicherheits-ID (SID) des Clients erstellen.

Verwenden Sie [**die Methoden InitializeClientContextFromToken,**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken) [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)und [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) der [**IAzApplication-Schnittstelle,**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) um einen Clientkontext zu erstellen.

Das folgende Beispiel zeigt, wie sie ein [**IAzClientContext-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) aus einem Clienttoken erstellen. Im Beispiel wird davon ausgegangen, dass im Stammverzeichnis von Laufwerk C ein XML-Richtlinienspeicher namens MyStore.xml vorhanden ist, dass dieser Speicher eine Anwendung namens Expense enthält und dass die Variable hToken ein gültiges Clienttoken enthält.


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



 

 
