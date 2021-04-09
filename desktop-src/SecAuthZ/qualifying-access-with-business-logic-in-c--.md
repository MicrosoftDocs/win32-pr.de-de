---
description: Verwenden von Geschäftsregel Skripts in C++, um Lauf Zeit Logik zum Überprüfen des Zugriffs zu bieten.
ms.assetid: 058086ab-8ebd-4ff6-b552-8d3c19ae5d38
title: Qualifizieren des Zugriffs mit Geschäftslogik in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e176fb9cbb221fb52404e22c7ba61d272897082c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129913"
---
# <a name="qualifying-access-with-business-logic-in-c"></a>Qualifizieren des Zugriffs mit Geschäftslogik in C++

Verwenden Sie Geschäftsregel Skripts, um Lauf Zeit Logik zum Überprüfen des Zugriffs bereitzustellen. Weitere Informationen zu Geschäftsregeln finden Sie unter [Geschäftsregeln](business-rules.md).

Um einer Aufgabe eine Geschäftsregel zuzuweisen, legen Sie zunächst die Eigenschaft [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) des [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekts fest, das die Aufgabe darstellt. Das Skript muss sich in Visual Basic Scripting Edition oder JScript befinden. Nachdem Sie die Skriptsprache angegeben haben, legen Sie die Eigenschaft [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) des **iaztask** -Objekts auf eine Zeichen folgen Darstellung des Skripts fest.

Beim Überprüfen des Zugriffs für einen Vorgang, der in einem Task enthalten ist, dem eine Geschäftsregel zugeordnet ist, muss die Anwendung zwei Arrays derselben Größe erstellen, die als Parameter des Typs " *varParameterNames* " und " *varParameterValues* " der [**IAzClientContext:: AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) -Methode übermittelt werden. Weitere Informationen zum Erstellen eines Client Kontexts finden Sie unter [Einrichten eines Client Kontexts mit dem Autorisierungs-Manager in C++](establishing-a-client-context-with-authorization-manager-in-c--.md).

Die [**IAzClientContext:: AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) -Methode erstellt ein [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) -Objekt, das an das Geschäftsregel Skript übergeben wird. Das Skript legt dann die Eigenschaft [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) des **AzBizRuleContext** -Objekts fest. Der Wert **true** gibt an, dass der Zugriff gewährt wird, und der Wert **false** gibt an, dass der Zugriff verweigert wird.

Einem [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt, das in einem Delegierten [**iazscope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) -Objekt enthalten ist, kann kein Geschäftsregel Skript zugewiesen werden.

Im folgenden Beispiel wird gezeigt, wie ein Geschäftsregel Skript verwendet wird, um den Zugriff eines Clients auf einen Vorgang zu überprüfen. Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis von Laufwerk C vorhanden ist, dass dieser Speicher eine Anwendung mit dem Namen "Kosten", eine Aufgabe mit dem Namen "Kosten senden" und einen Vorgang mit dem Namen "useformcontrol" enthält und dass die Variable "hToken" ein gültiges Client Token


```C++
#include <windows.h>
#include <stdio.h>
#include <azroles.h>

void CheckAccess(ULONGLONG hToken)
//  Void CheckAccess().
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzClientContext* pClientContext = NULL;
    IAzOperation* pOperation = NULL;
    IAzTask* pTask = NULL;
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR operationName = NULL;
    BSTR objectName = NULL;
    BSTR taskName = NULL;
    BSTR bizRule = NULL;
    BSTR bizRuleLanguage = NULL;
    LONG operationID;
    HRESULT hr;
    VARIANT varOperationIdArray;
    VARIANT varOperationId;
    VARIANT varResultsArray;
    VARIANT varResult;
    VARIANT varParamName;
    VARIANT varParamValue;
    VARIANT nameString;
    VARIANT expenseAmount;
    void MyHandleError(char *s);

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

    //  Create a business rule for the Submit Expense task.

    //  Open the Submit Expense task.
    if(!(taskName = SysAllocString(L"Submit Expense")))
        MyHandleError("Could not allocate task name string.");
    hr = pApp->OpenTask(taskName, myVar, &pTask);

    //  Assign a business rule to the task.

    //  Set the business rule language to VBScript.
    if(!(bizRuleLanguage = SysAllocString(L"VBScript")))
        MyHandleError("Could not allocate business rule language string.");
    hr = pTask->put_BizRuleLanguage(bizRuleLanguage);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not allocate business rule language string.");

    //  Create a BSTR with the business rule code.
    if(!(bizRule = SysAllocString(
        L"Dim Amount \n"
        L"AzBizRuleContext.BusinessRuleResult = FALSE \n"
        L"Amount = AzBizRuleContext.GetParameter(\"ExpAmount\") \n"
        L"if Amount < 500 then AzBizRuleContext.BusinessRuleResult = TRUE"
        )))
         MyHandleError("Could not allocate business rule string.");

    
    hr = pTask->put_BizRule(bizRule);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not assign business rule.");

    //  Save the new task data to the store.
    hr = pTask->Submit(0, myVar);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not save task data.");

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
    
    //  Set SAFEARRAY type.
    varOperationIdArray.vt = VT_ARRAY | VT_VARIANT;

    //  Create business rule parameters.

    //  Create array of business rule parameter names.
    varParamName.parray = SafeArrayCreateVector(VT_VARIANT, 0, 1);
    varParamName.vt = VT_ARRAY | VT_VARIANT;
    nameString.vt = VT_BSTR;
    nameString.bstrVal = SysAllocString(L"ExpAmount");
    SafeArrayPutElement(varParamName.parray, index, &nameString);

    //  Create array of business rule parameter values.
    varParamValue.parray = SafeArrayCreateVector(VT_VARIANT, 0, 1);
    varParamValue.vt = VT_ARRAY | VT_VARIANT;
    expenseAmount.vt = VT_I4;
    expenseAmount.lVal = 100;  // access denied if 500 or more
    SafeArrayPutElement(varParamValue.parray, index, &expenseAmount);

    if(!(objectName = SysAllocString(L"UseFormControl")))//used for audit
        MyHandleError("Could not allocate object name string.");

    //  Check access.
    hr = pClientContext->AccessCheck(
        objectName,
        myVar,                  // use default application scope
        varOperationIdArray,
        varParamName,
        varParamValue,
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
    pOperation->Release();
    pClientContext->Release();
    pTask->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(operationName);
    SysFreeString(objectName);
    SysFreeString(taskName);
    SysFreeString(bizRule);
    SysFreeString(bizRuleLanguage);
    VariantClear(&myVar);
    VariantClear(&varOperationIdArray);
    VariantClear(&varOperationId);
    VariantClear(&varResultsArray);
    VariantClear(&varResult);
    VariantClear(&varParamName);
    VariantClear(&varParamValue);
    VariantClear(&nameString);
    VariantClear(&expenseAmount);
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



 

 



