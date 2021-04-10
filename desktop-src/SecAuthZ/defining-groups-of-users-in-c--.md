---
description: Im Autorisierungs-Manager stellt ein iazapplicationgroup-Objekt eine Gruppe von Benutzern dar. Rollen können dieser Gruppe von Benutzern gemeinsam zugewiesen werden.
ms.assetid: 13950da1-b04f-4346-b216-9713cbdcd5b5
title: Definieren von Benutzergruppen in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b4931d3b35658539284305e98096d7ecfc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868440"
---
# <a name="defining-groups-of-users-in-c"></a><span data-ttu-id="7f751-104">Definieren von Benutzergruppen in C++</span><span class="sxs-lookup"><span data-stu-id="7f751-104">Defining Groups of Users in C++</span></span>

<span data-ttu-id="7f751-105">Im Autorisierungs-Manager stellt ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt eine Gruppe von Benutzern dar.</span><span class="sxs-lookup"><span data-stu-id="7f751-105">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="7f751-106">Rollen können dieser Gruppe von Benutzern gemeinsam zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="7f751-106">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="7f751-107">Ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt kann auch andere **iazapplicationgroup** -Objekte als Member enthalten.</span><span class="sxs-lookup"><span data-stu-id="7f751-107">An [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object can also include other **IAzApplicationGroup** objects as members.</span></span> <span data-ttu-id="7f751-108">Weitere Informationen zu Anwendungs Gruppen finden Sie unter [Benutzer und Gruppen](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="7f751-108">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

<span data-ttu-id="7f751-109">Eine Gruppe kann entweder durch explizite Listen von Membern und nicht-Membern oder durch eine LDAP-Abfrage ( [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) ) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7f751-109">A group can be defined either by explicit lists of members and nonmembers, or by a [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP) query.</span></span> <span data-ttu-id="7f751-110">In den folgenden Beispielen wird gezeigt, wie die einzelnen Anwendungs Gruppen Typen erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="7f751-110">The following examples show how to create each type of application group:</span></span>

-   [<span data-ttu-id="7f751-111">Erstellen einer einfachen Gruppe</span><span class="sxs-lookup"><span data-stu-id="7f751-111">Creating a Basic Group</span></span>](#creating-a-basic-group)
-   [<span data-ttu-id="7f751-112">Erstellen einer LDAP-Abfrage Gruppe</span><span class="sxs-lookup"><span data-stu-id="7f751-112">Creating an LDAP Query Group</span></span>](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a><span data-ttu-id="7f751-113">Erstellen einer einfachen Gruppe</span><span class="sxs-lookup"><span data-stu-id="7f751-113">Creating a Basic Group</span></span>

<span data-ttu-id="7f751-114">Eine einfache Anwendungs Gruppe wird durch die Elemente definiert [**, die in**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) den Membern und [**nonmembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) -Eigenschaften des [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekts enthalten sind, das die Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="7f751-114">A basic application group is defined by the members included in the [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) and [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) properties of the [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object that represents the group.</span></span> <span data-ttu-id="7f751-115">Benutzer und Gruppen, die in der Eigenschaft **Members** aufgeführt sind, sind in der Anwendungs Gruppe enthalten, und Benutzer und Gruppen, die in der Eigenschaft **nonmembers** aufgeführt sind, werden aus der Anwendungs Gruppe ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7f751-115">Users and groups listed in the **Members** property are included in the application group, and users and groups listed in the **NonMembers** property are excluded from the application group.</span></span> <span data-ttu-id="7f751-116">Das Auflisten in der **nonmembers** -Eigenschaft ersetzt das Auflisten in der **Members** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7f751-116">Being listed in the **NonMembers** property supersedes being listed in the **Members** property.</span></span>

<span data-ttu-id="7f751-117">Im folgenden Beispiel wird gezeigt, wie eine einfache Anwendungs Gruppe erstellt und alle lokalen Benutzer als Mitglieder dieser Gruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7f751-117">The following example shows how to create a basic application group and add all local users as members of that group.</span></span> <span data-ttu-id="7f751-118">Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7f751-118">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR sidString = NULL;

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

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Add well-known SID for all local users to the group.
    if (!(sidString = SysAllocString(L"S-1-2-0")))
        MyHandleError("Could not allocate SID string name");
    hr = pAppGroup->AddMember(sidString, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add member to group");

    //  Save changes to the store.
    pAppGroup->Submit(0, myVar);

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(sidString);
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



## <a name="creating-an-ldap-query-group"></a><span data-ttu-id="7f751-119">Erstellen einer LDAP-Abfrage Gruppe</span><span class="sxs-lookup"><span data-stu-id="7f751-119">Creating an LDAP Query Group</span></span>

<span data-ttu-id="7f751-120">Eine LDAP-Abfrage Gruppe verfügt über eine-Mitgliedschaft, die durch die Abfrage definiert ist, die im Wert Ihrer [**ldapquery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) -Eigenschaft enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7f751-120">An LDAP query group has a membership defined by the query contained in the value of its [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) property.</span></span>

<span data-ttu-id="7f751-121">Im folgenden Beispiel wird gezeigt, wie eine LDAP-Abfrage Anwendungs Gruppe erstellt und alle Benutzer als Mitglieder dieser Gruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7f751-121">The following example shows how to create an LDAP query application group and add all users as members of that group.</span></span> <span data-ttu-id="7f751-122">Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7f751-122">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR ldapString = NULL;

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
    
    VARIANT myVar; 
    myVar.vt = VT_NULL;

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users3")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Set the Type property to AZ_GROUPTYPE_LDAP_QUERY.
    hr = pAppGroup->put_Type(AZ_GROUPTYPE_LDAP_QUERY);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Error changing type to LDAP query");

    //  Add LDAP query for all users.
    if (!(ldapString =
   SysAllocString(L"(&(objectCategory=person)(objectClass=user))")))
        MyHandleError("Could not allocate LDAP query string");
    hr = pAppGroup->put_LdapQuery(ldapString);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add query to group");

    //  Save changes to the store.
    hr = pAppGroup->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save changes to store.");

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(ldapString);
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



 

 
