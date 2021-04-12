---
description: Im Autorisierungs-Manager ist eine Anwendungs Gruppe eine Gruppe von Benutzern und Benutzergruppen. Eine Anwendungs Gruppe kann andere Anwendungs Gruppen enthalten, sodass Gruppen von Benutzern gruppiert werden können.
ms.assetid: b01883d6-eae6-4f3a-b269-90c22827f116
title: Hinzufügen von Benutzern zu einer Anwendungs Gruppe in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7fa08ddd93ba1743a20e3eb14a5f62344741c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130424"
---
# <a name="adding-users-to-an-application-group-in-c"></a><span data-ttu-id="d887d-104">Hinzufügen von Benutzern zu einer Anwendungs Gruppe in C++</span><span class="sxs-lookup"><span data-stu-id="d887d-104">Adding Users to an Application Group in C++</span></span>

<span data-ttu-id="d887d-105">Im Autorisierungs-Manager ist eine Anwendungs Gruppe eine Gruppe von Benutzern und Benutzergruppen.</span><span class="sxs-lookup"><span data-stu-id="d887d-105">In Authorization Manager, an application group is a group of users and user groups.</span></span> <span data-ttu-id="d887d-106">Eine Anwendungs Gruppe kann andere Anwendungs Gruppen enthalten, sodass Gruppen von Benutzern gruppiert werden können.</span><span class="sxs-lookup"><span data-stu-id="d887d-106">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="d887d-107">Eine Anwendungs Gruppe wird durch ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d887d-107">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>

<span data-ttu-id="d887d-108">Damit Mitglieder einer Anwendungs Gruppe eine Aufgabe oder eine Reihe von Tasks ausführen können, weisen Sie diese Anwendungs Gruppe einer Rolle zu, die diese Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="d887d-108">To allow members of an application group to perform a task or set of tasks, assign that application group to a role that contains those tasks.</span></span> <span data-ttu-id="d887d-109">Rollen werden durch [**iazrole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) -Objekte dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d887d-109">Roles are represented by [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) objects.</span></span>

<span data-ttu-id="d887d-110">Im folgenden Beispiel wird gezeigt, wie Sie eine Anwendungs Gruppe erstellen, einen Benutzer als Mitglied der Anwendungs Gruppe hinzufügen und die Anwendungs Gruppe einer vorhandenen Rolle zuweisen.</span><span class="sxs-lookup"><span data-stu-id="d887d-110">The following example shows how to create an application group, add a user as a member of the application group, and assign the application group to an existing role.</span></span> <span data-ttu-id="d887d-111">Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist, dass dieser Speicher eine Anwendung mit dem Namen "Kosten" enthält und dass diese Anwendung eine Rolle mit dem Namen "Kosten Administrator" enthält.</span><span class="sxs-lookup"><span data-stu-id="d887d-111">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains a role named Expense Administrator.</span></span>


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
    IAzApplicationGroup* pAppGroup = NULL;
    IAzRole* pRole = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR groupName = NULL;
    BSTR userName = NULL;
    BSTR roleName = NULL;
    
    
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

    //  Allocate a string for the name of the policy store.
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

    //  Allocate a string for the group name.
    if (!(groupName = SysAllocString(L"Approvers")))
        MyHandleError("Could not allocate group name string.");

    //  Create an IAzApplicationGroup object.
    hr = pApp->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Add a member to the group.
 //  Replace with valid domain and user name.
    if (!(userName = SysAllocString(L"domain\\username")))
        MyHandleError("Could not allocate user name string.");

    hr = pAppGroup->AddMemberName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add user to application group.");

    //  Save information to the store.
    hr = pAppGroup->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save group information.");

    //  Open an IAzRole object.
    if (!(roleName = SysAllocString(L"Expense Administrator")))
        MyHandleError("Could not allocate role name string.");

    hr = pApp->OpenRole(roleName, myVar, &pRole);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open role object.");

    //  Add the group to the role.
    hr = pRole->AddAppMember(groupName, myVar);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not add the application group to the role.");


    //  Save information to the store.
    hr = pRole->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save role data to the store.");

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pAppGroup->Release();
    pRole->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(groupName);
    SysFreeString(roleName);
    SysFreeString(userName);
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



 

 



