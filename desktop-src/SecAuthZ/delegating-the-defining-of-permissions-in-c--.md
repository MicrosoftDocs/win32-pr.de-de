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
# <a name="delegating-the-defining-of-permissions-in-c"></a><span data-ttu-id="29029-103">Delegieren der definierenden Berechtigungen in C++</span><span class="sxs-lookup"><span data-stu-id="29029-103">Delegating the Defining of Permissions in C++</span></span>

<span data-ttu-id="29029-104">In Active Directory gespeicherte Autorisierungs Richtlinien Speicher unterstützen die Delegierung der Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="29029-104">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="29029-105">Die Verwaltung kann an Benutzer und Gruppen auf Geschäfts-, Anwendungs-oder Bereichs Ebene delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="29029-105">Administration can be delegated to users and groups at the store, application, or scope level.</span></span>

<span data-ttu-id="29029-106">Auf jeder Ebene ist eine Liste von Administratoren und Lesern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="29029-106">At each level, there is a list of administrators and readers.</span></span> <span data-ttu-id="29029-107">Administratoren eines Stores, einer Anwendung oder eines Bereichs können den Richtlinien Speicher auf der Delegierten Ebene lesen und ändern.</span><span class="sxs-lookup"><span data-stu-id="29029-107">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="29029-108">Leser können den Richtlinien Speicher auf der Delegierten Ebene lesen, den Speicher jedoch nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="29029-108">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

<span data-ttu-id="29029-109">Ein Benutzer oder eine Gruppe, der entweder als Administrator oder als Leser einer Anwendung dient, muss auch als Delegierter Benutzer des Richtlinien Speicher hinzugefügt werden, der diese Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="29029-109">A user or group that is either an administrator or a reader of an application must also be added as a delegated user of the policy store that contains that application.</span></span> <span data-ttu-id="29029-110">Ebenso muss ein Benutzer oder eine Gruppe, der ein Administrator oder ein Leser eines Bereichs ist, als Delegierter Benutzer der Anwendung hinzugefügt werden, die diesen Bereich enthält.</span><span class="sxs-lookup"><span data-stu-id="29029-110">Similarly, a user or group that is an administrator or a reader of a scope must be added as a delegated user of the application that contains that scope.</span></span>

<span data-ttu-id="29029-111">Wenn Sie z. b. die Verwaltung eines Bereichs delegieren möchten, fügen Sie zuerst den Benutzer oder die Gruppe der Liste der Delegierten Benutzer des Stores mit dem Bereich hinzu, indem Sie die [**IAzAuthorizationStore:: adddelegatedpolicyuser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="29029-111">For example, to delegate administration of a scope, first add the user or group to the list of delegated users of the store that contains the scope by calling the [**IAzAuthorizationStore::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="29029-112">Fügen Sie dann den Benutzer oder die Gruppe der Liste der Delegierten Benutzer der Anwendung hinzu, die den Bereich enthält, indem Sie die [**IAzApplication:: adddelegatedpolicyuser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="29029-112">Then add the user or group to the list of delegated users of the application that contains the scope by calling the [**IAzApplication::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="29029-113">Fügen Sie schließlich den Benutzer oder die Gruppe der Liste der Administratoren des Bereichs hinzu, indem Sie die [**iazscope:: addpolicyadministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="29029-113">Finally, add the user or group to the list of administrators of the scope by calling the [**IAzScope::AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) method.</span></span>

<span data-ttu-id="29029-114">XML-basierte Richtlinien Speicher unterstützen nicht die Delegierung auf einer beliebigen Ebene.</span><span class="sxs-lookup"><span data-stu-id="29029-114">XML-based policy stores do not support delegation at any level.</span></span>

<span data-ttu-id="29029-115">Ein Bereich in einem Autorisierungs Speicher, der in Active Directory gespeichert ist, kann nicht delegiert werden, wenn der Bereich Aufgaben Definitionen enthält, die Autorisierungs Regeln oder Rollen Definitionen enthalten, die Autorisierungs Regeln enthalten.</span><span class="sxs-lookup"><span data-stu-id="29029-115">A scope within an authorization store that is stored in Active Directory cannot be delegated if the scope contains task definitions that include authorization rules or role definitions that include authorization rules.</span></span>

<span data-ttu-id="29029-116">Im folgenden Beispiel wird gezeigt, wie die Verwaltung einer Anwendung delegiert wird.</span><span class="sxs-lookup"><span data-stu-id="29029-116">The following example shows how to delegate administration of an application.</span></span> <span data-ttu-id="29029-117">Im Beispiel wird davon ausgegangen, dass am angegebenen Speicherort ein Active Directory Autorisierungs Richtlinien Speicher vorhanden ist, dass dieser Richtlinien Speicher eine Anwendung mit dem Namen "Kosten" enthält und dass diese Anwendung keine Aufgaben mit Geschäftsregel Skripts enthält.</span><span class="sxs-lookup"><span data-stu-id="29029-117">The example assumes that there is an existing Active Directory authorization policy store at the specified location, that this policy store contains an application named Expense, and that this application contains no tasks with business rule scripts.</span></span>


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



 

 



