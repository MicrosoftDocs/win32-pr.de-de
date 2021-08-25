---
description: Rufen Sie die AccessCheck-Methode der IAzClientContext-Schnittstelle auf, um zu überprüfen, ob der Client Zugriff auf einen oder mehrere Vorgänge hat.
ms.assetid: 7c8a63c5-2eab-4414-9a3d-c99a92b67a62
title: Überprüfen des Clientzugriffs auf eine angeforderte Ressource in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363490e3636f5ad5229dd4234eba3bf38b9dfc54a4564bda775b143a249fe640
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906730"
---
# <a name="verifying-client-access-to-a-requested-resource-in-c"></a>Überprüfen des Clientzugriffs auf eine angeforderte Ressource in C++

Rufen Sie die [**AccessCheck-Methode**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) der [**IAzClientContext-Schnittstelle**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) auf, um zu überprüfen, ob der Client Zugriff auf einen oder mehrere Vorgänge hat. Ein Client kann mitglied in mehr als einer Rolle sein, und ein Vorgang kann mehreren Aufgaben zugewiesen sein, sodass der Autorisierungs-Manager alle Rollen und Aufgaben überprüft. Wenn eine Rolle, zu der der Client gehört, eine Aufgabe enthält, die einen Vorgang enthält, wird der Zugriff auf diesen Vorgang gewährt.

Um den Zugriff nur auf eine einzelne Rolle zu überprüfen, zu der der Client gehört, legen Sie die [**RoleForAccessCheck-Eigenschaft**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) der [**IAzClientContext-Schnittstelle**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) fest.

Beim Initialisieren des Autorisierungsrichtlinienspeichers für die Zugriffsüberprüfung müssen Sie 0 (null) als Wert des *lFlags-Parameters* der [**IAzAuthorizationStore::Initialize-Methode**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) übergeben.

Das folgende Beispiel zeigt, wie der Zugriff eines Clients auf einen Vorgang überprüft wird. Im Beispiel wird davon ausgegangen, dass im Stammverzeichnis von Laufwerk C ein vorhandener XML-Richtlinienspeicher mit dem Namen MyStore.xml vorhanden ist, dass dieser Speicher eine Anwendung mit dem Namen Expense und einen Vorgang namens UseFormControl enthält und dass die Variable hToken ein gültiges Clienttoken enthält.


```C++
#include <windows.h>
#include <stdio.h>
#include <azroles.h>

void CheckAccess(ULONGLONG hToken)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzClientContext* pClientContext = NULL;
    IAzOperation* pOperation = NULL;
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR operationName = NULL;
    BSTR objectName = NULL;
    LONG operationID;
    HRESULT hr;
    VARIANT varOperationIdArray;
    VARIANT varOperationId;
    VARIANT varResultsArray;
    VARIANT varResult;
    void MyHandleError(char *s);

    VARIANT myVar;
    VariantInit(&myVar);//.vt) = VT_NULL;

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

    //  Allocate a string for the  policy store.
    if(!(storeName = SysAllocString(L"msxml://c:\\myStore.xml")))
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

    //  Set up parameters for access check.

    //  Set up the object name.
    if (!(operationName = SysAllocString(L"UseFormControl")))
        MyHandleError("Could not allocate operation name string.");

    //  Get the ID of the operation to check.
    hr = pApp->OpenOperation(operationName, myVar, &pOperation);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open operation.");

    hr = pOperation->get_OperationID(&operationID);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not get operation ID.");

    //  Create a SAFEARRAY for the operation ID.
    varOperationIdArray.parray = SafeArrayCreateVector(VT_VARIANT, 0, 1);

    //  Set SAFEARRAY type.
    varOperationIdArray.vt = VT_ARRAY | VT_VARIANT;

    //  Create an array of indexes.
    LONG* index = new LONG[1];
    index[0] = 0;

    //  Populate a SAFEARRAY with the operation ID.
    varOperationId.vt = VT_I4;
    varOperationId.lVal = operationID;

    hr = SafeArrayPutElement(varOperationIdArray.parray, index,
   &varOperationId);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not put operation ID in array.");

    if(!(objectName = SysAllocString(L"UseFormControl")))//used for audit
        MyHandleError("Could not allocate object name string.");

    //  Check access.
    hr = pClientContext->AccessCheck(
        objectName,
        myVar,
        varOperationIdArray,
        myVar,               // use default application scope
        myVar,
        myVar,
        myVar,
        myVar,
        &varResultsArray);

    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not complete access check.");

    hr = SafeArrayGetElement(varResultsArray.parray, index, &varResult);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not get result from array.");

    if (varResult.lVal == 0)
        printf("Access granted.\n");
    else
        printf("Access denied.\n");
    

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pClientContext->Release();
    pOperation->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(operationName);
    SysFreeString(objectName);
    VariantClear(&myVar);
    VariantClear(&varOperationIdArray);
    VariantClear(&varOperationId);
    VariantClear(&varResultsArray);
    VariantClear(&varResult); 
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



 

 



