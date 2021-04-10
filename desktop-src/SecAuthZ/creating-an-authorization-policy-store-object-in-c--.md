---
description: Ein Autorisierungs Richtlinien Speicher enthält Informationen über die Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen. Zu diesen Informationen gehören die Anwendungen, Vorgänge, Tasks, Benutzer und Gruppen von Benutzern, die dem Speicher zugeordnet sind.
ms.assetid: 6fc84944-8050-4000-8856-36558d94e2fd
title: Erstellen eines Autorisierungs Richtlinien-Speicher Objekts in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b50bfa4234f5adaf162b1499f85785a7d65f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959215"
---
# <a name="creating-an-authorization-policy-store-object-in-c"></a><span data-ttu-id="d60e9-104">Erstellen eines Autorisierungs Richtlinien-Speicher Objekts in C++</span><span class="sxs-lookup"><span data-stu-id="d60e9-104">Creating an Authorization Policy Store Object in C++</span></span>

<span data-ttu-id="d60e9-105">Ein Autorisierungs Richtlinien Speicher enthält Informationen über die Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="d60e9-105">An authorization policy store contains information about the security policy of an application or group of applications.</span></span> <span data-ttu-id="d60e9-106">Zu diesen Informationen gehören die Anwendungen, Vorgänge, Tasks, Benutzer und Gruppen von Benutzern, die dem Speicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d60e9-106">The information includes the applications, operations, tasks, users, and groups of users associated with the store.</span></span> <span data-ttu-id="d60e9-107">Wenn eine Anwendung, die den Autorisierungs-Manager verwendet, initialisiert, lädt Sie diese Informationen aus dem Speicher.</span><span class="sxs-lookup"><span data-stu-id="d60e9-107">When an application that uses Authorization Manager initializes, it loads this information from the store.</span></span> <span data-ttu-id="d60e9-108">Der Autorisierungs Richtlinien Speicher muss sich in einem vertrauenswürdigen System befinden, da Administratoren auf diesem System über ein hohes Maß an Zugriff auf den Store verfügen.</span><span class="sxs-lookup"><span data-stu-id="d60e9-108">The authorization policy store must be located on a trusted system because administrators on that system have a high degree of access to the store.</span></span>

<span data-ttu-id="d60e9-109">Der Autorisierungs-Manager unterstützt das Speichern von Autorisierungs Richtlinien entweder im Active Directory Directory-Dienst oder in einer XML-Datei, wie in den folgenden Beispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d60e9-109">Authorization Manager supports storing authorization policy either in the Active Directory directory service or in an XML file as shown in the following examples.</span></span> <span data-ttu-id="d60e9-110">In der Autorisierungs-Manager-API wird ein Autorisierungs Richtlinien Speicher durch ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d60e9-110">In the Authorization Manager API, an authorization policy store is represented by an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="d60e9-111">In den Beispielen wird gezeigt, wie ein **AzAuthorizationStore** -Objekt für einen Active Directory-Speicher und einen XML-Speicher erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d60e9-111">The examples show how to create an **AzAuthorizationStore** object for an Active Directory store and an XML store.</span></span>

-   [<span data-ttu-id="d60e9-112">Erstellen eines Active Directory Stores</span><span class="sxs-lookup"><span data-stu-id="d60e9-112">Creating an Active Directory Store</span></span>](#creating-an-active-directory-store)
-   [<span data-ttu-id="d60e9-113">Erstellen eines SQL Server Stores</span><span class="sxs-lookup"><span data-stu-id="d60e9-113">Creating a SQL Server Store</span></span>](#creating-a-sql-server-store)
-   [<span data-ttu-id="d60e9-114">Erstellen eines XML-Stores</span><span class="sxs-lookup"><span data-stu-id="d60e9-114">Creating an XML Store</span></span>](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a><span data-ttu-id="d60e9-115">Erstellen eines Active Directory Stores</span><span class="sxs-lookup"><span data-stu-id="d60e9-115">Creating an Active Directory Store</span></span>

<span data-ttu-id="d60e9-116">Um Active Directory zum Speichern der Autorisierungs Richtlinie zu verwenden, muss sich die Domäne auf der **Windows Server 2003** -Domänen Funktionsebene befinden.</span><span class="sxs-lookup"><span data-stu-id="d60e9-116">To use Active Directory to store the authorization policy, the domain must be in the **Windows Server 2003** domain functional level.</span></span> <span data-ttu-id="d60e9-117">Der Autorisierungs Richtlinien Speicher kann nicht in einem **nicht-Domänen-namens Kontext** (auch als Anwendungs Partition bezeichnet) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d60e9-117">The authorization policy store cannot be located in a **Non-Domain Naming Context** (also called an application partition).</span></span> <span data-ttu-id="d60e9-118">Es wird empfohlen, dass sich der Speicher im **Programm Daten** Container unter einer neuen Organisationseinheit befindet, die speziell für den Autorisierungs Richtlinien Speicher erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d60e9-118">It is recommended that the store be located in the **Program Data** container under a new organizational unit created specifically for the authorization policy store.</span></span> <span data-ttu-id="d60e9-119">Außerdem wird empfohlen, dass sich der Speicher innerhalb desselben lokalen Netzwerks befindet wie Anwendungsserver, die Anwendungen ausführen, die den Speicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="d60e9-119">It is also recommended that the store be located within the same local area network as application servers that run applications that use the store.</span></span>

<span data-ttu-id="d60e9-120">Im folgenden Beispiel wird gezeigt, wie ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt erstellt wird, das einen Autorisierungs Richtlinien Speicher in Active Directory darstellt.</span><span class="sxs-lookup"><span data-stu-id="d60e9-120">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in Active Directory.</span></span> <span data-ttu-id="d60e9-121">In diesem Beispiel wird davon ausgegangen, dass in einer Domäne mit dem Namen AuthManager.com eine vorhandene Organisationseinheit mit dem Namen Program Data Active Directory vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d60e9-121">The example assumes that there is an existing Active Directory organizational unit named Program Data in a domain named authmanager.com.</span></span>


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
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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
    
    //  Create a null VARIANT for function parameters.
    VARIANT myVar;
    VariantInit(&myVar);

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in Active Directory. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    VariantClear(&myVar);
    SysFreeString(storeName);
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



## <a name="creating-a-sql-server-store"></a><span data-ttu-id="d60e9-122">Erstellen eines SQL Server Stores</span><span class="sxs-lookup"><span data-stu-id="d60e9-122">Creating a SQL Server Store</span></span>

<span data-ttu-id="d60e9-123">Der Autorisierungs-Manager unterstützt das Erstellen eines Microsoft SQL Server – basierten Autorisierungs Richtlinien Speicher.</span><span class="sxs-lookup"><span data-stu-id="d60e9-123">Authorization Manager supports creating a Microsoft SQL Server–based authorization policy store.</span></span> <span data-ttu-id="d60e9-124">Um einen SQL Server – basierten Autorisierungs Speicher zu erstellen, verwenden Sie eine URL, die mit dem Präfix **MSSQL://** beginnt.</span><span class="sxs-lookup"><span data-stu-id="d60e9-124">To create a SQL Server–based authorization store, use a URL that begins with the prefix **MSSQL://**.</span></span> <span data-ttu-id="d60e9-125">Die URL muss eine gültige SQL-Verbindungs Zeichenfolge, einen Datenbanknamen und den Namen des Autorisierungs Richtlinien Speicher enthalten: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _policystorename_.</span><span class="sxs-lookup"><span data-stu-id="d60e9-125">The URL must contain a valid SQL connection string, a database name, and the name of the authorization policy store: **MSSQL://**_ConnectionString_*_/_*_DatabaseName_*_/_*_PolicyStoreName_.</span></span>

<span data-ttu-id="d60e9-126">Wenn die Instanz von SQL Server die angegebene Autorisierungs-Manager-Datenbank nicht enthält, erstellt der Autorisierungs-Manager eine neue Datenbank mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="d60e9-126">If the instance of SQL Server does not contain the specified Authorization Manager database, Authorization Manager creates a new database with that name.</span></span>

> [!Note]  
> <span data-ttu-id="d60e9-127">Verbindungen mit einem SQL Server Speicher werden nur dann verschlüsselt, wenn Sie die SQL-Verschlüsselung für die Verbindung explizit einrichten oder die Verschlüsselung des Netzwerk Datenverkehrs einrichten, der IPSec (Internet Protocol Security) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d60e9-127">Connections to a SQL Server store are not encrypted unless you explicitly set up SQL encryption for the connection or set up encryption of the network traffic that uses Internet Protocol Security (IPsec).</span></span>

 

<span data-ttu-id="d60e9-128">Im folgenden Beispiel wird gezeigt, wie ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt erstellt wird, das einen Autorisierungs Richtlinien Speicher in einer SQL Server-Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="d60e9-128">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in a SQL Server database.</span></span>


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
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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

    //  Allocate a string for the SQL Server store.
    if(!(storeName = SysAllocString
   (L"MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
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



## <a name="creating-an-xml-store"></a><span data-ttu-id="d60e9-129">Erstellen eines XML-Stores</span><span class="sxs-lookup"><span data-stu-id="d60e9-129">Creating an XML Store</span></span>

<span data-ttu-id="d60e9-130">Der Autorisierungs-Manager unterstützt das Erstellen eines Autorisierungs Richtlinien Speicher im XML-Format</span><span class="sxs-lookup"><span data-stu-id="d60e9-130">Authorization Manager supports creating an authorization policy store in XML format.</span></span> <span data-ttu-id="d60e9-131">Der XML-Speicher kann sich auf demselben Computer befinden, auf dem die Anwendung ausgeführt wird, oder er kann Remote gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d60e9-131">The XML store can be located on the same computer where the application runs, or it can be stored remotely.</span></span> <span data-ttu-id="d60e9-132">Das direkte Bearbeiten der XML-Datei wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d60e9-132">Editing the XML file directly is not supported.</span></span> <span data-ttu-id="d60e9-133">Verwenden Sie das Autorisierungs-Manager-MMC-Snap-in oder die Autorisierungs-Manager-API zum Bearbeiten des Richtlinien Speicher.</span><span class="sxs-lookup"><span data-stu-id="d60e9-133">Use the Authorization Manager MMC snap-in or the Authorization Manager API to edit the policy store.</span></span>

<span data-ttu-id="d60e9-134">Der Autorisierungs-Manager unterstützt nicht die Delegierung der Verwaltung eines XML-Richtlinien Speicher.</span><span class="sxs-lookup"><span data-stu-id="d60e9-134">Authorization Manager does not support delegating administration of an XML policy store.</span></span> <span data-ttu-id="d60e9-135">Weitere Informationen zur Delegierung finden Sie unter [Delegieren der Definition von Berechtigungen in C++](delegating-the-defining-of-permissions-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="d60e9-135">For information about delegation, see [Delegating the Defining of Permissions in C++](delegating-the-defining-of-permissions-in-c--.md).</span></span>

<span data-ttu-id="d60e9-136">Im folgenden Beispiel wird gezeigt, wie ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt erstellt wird, das einen Autorisierungs Richtlinien Speicher in einer XML-Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="d60e9-136">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in an XML file.</span></span>


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
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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

    //  Allocate a string for the distinguished name of the XML store.
    if(!(storeName = SysAllocString(L"msxml://C:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in an XML file. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
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



 

 



