---
description: In Active Directory gespeicherte Autorisierungs Richtlinien Speicher unterstützen die Delegierung der Verwaltung.
ms.assetid: ccad4c19-7a16-4599-9a42-23cae7084418
title: Delegieren der definierenden Berechtigungen in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc299e3506300da1f0db2b4a9bacfce60def1c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366075"
---
# <a name="delegating-the-defining-of-permissions-in-c"></a>Delegieren der definierenden Berechtigungen in C++

In Active Directory gespeicherte Autorisierungs Richtlinien Speicher unterstützen die Delegierung der Verwaltung. Die Verwaltung kann an Benutzer und Gruppen auf Geschäfts-, Anwendungs-oder Bereichs Ebene delegiert werden.

Auf jeder Ebene ist eine Liste von Administratoren und Lesern vorhanden. Administratoren eines Stores, einer Anwendung oder eines Bereichs können den Richtlinien Speicher auf der Delegierten Ebene lesen und ändern. Leser können den Richtlinien Speicher auf der Delegierten Ebene lesen, den Speicher jedoch nicht ändern.

Ein Benutzer oder eine Gruppe, der entweder als Administrator oder als Leser einer Anwendung dient, muss auch als Delegierter Benutzer des Richtlinien Speicher hinzugefügt werden, der diese Anwendung enthält. Ebenso muss ein Benutzer oder eine Gruppe, der ein Administrator oder ein Leser eines Bereichs ist, als Delegierter Benutzer der Anwendung hinzugefügt werden, die diesen Bereich enthält.

Wenn Sie z. b. die Verwaltung eines Bereichs delegieren möchten, fügen Sie zuerst den Benutzer oder die Gruppe der Liste der Delegierten Benutzer des Stores mit dem Bereich hinzu, indem Sie die [**IAzAuthorizationStore:: adddelegatedpolicyuser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) -Methode aufrufen. Fügen Sie dann den Benutzer oder die Gruppe der Liste der Delegierten Benutzer der Anwendung hinzu, die den Bereich enthält, indem Sie die [**IAzApplication:: adddelegatedpolicyuser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) -Methode aufrufen. Fügen Sie schließlich den Benutzer oder die Gruppe der Liste der Administratoren des Bereichs hinzu, indem Sie die [**iazscope:: addpolicyadministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) -Methode aufrufen.

XML-basierte Richtlinien Speicher unterstützen nicht die Delegierung auf einer beliebigen Ebene.

Ein Bereich in einem Autorisierungs Speicher, der in Active Directory gespeichert ist, kann nicht delegiert werden, wenn der Bereich Aufgaben Definitionen enthält, die Autorisierungs Regeln oder Rollen Definitionen enthalten, die Autorisierungs Regeln enthalten.

Im folgenden Beispiel wird gezeigt, wie die Verwaltung einer Anwendung delegiert wird. Im Beispiel wird davon ausgegangen, dass am angegebenen Speicherort ein Active Directory Autorisierungs Richtlinien Speicher vorhanden ist, dass dieser Richtlinien Speicher eine Anwendung mit dem Namen "Kosten" enthält und dass diese Anwendung keine Aufgaben mit Geschäftsregel Skripts enthält.


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR userName = NULL;
    VARIANT myVar;
    
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
    myVar.vt = VT_NULL;

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize
   (AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Add a delegated policy user to the store.
    if (!(userName = SysAllocString(L"ExampleDomain\\UserName")))
        MyHandleError("Could not allocate username string.");
    hr = pStore->AddDelegatedPolicyUserName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to store as delegated policy user.");

    //  Add the user as an administrator of the application.
    hr = pApp->AddPolicyAdministratorName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to application as administrator.");

    

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(userName);
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



 

 



