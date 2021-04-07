---
description: Ein Autorisierungs Richtlinien Speicher enthält Informationen über die Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen.
ms.assetid: bce85da8-11de-4bc1-b097-d8efdbd28abf
title: Erstellen eines Autorisierungs Richtlinien-Speicher Objekts im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: feb02c80408210b663524e2aa914852a853e80ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863248"
---
# <a name="creating-an-authorization-policy-store-object-in-script"></a><span data-ttu-id="a4478-103">Erstellen eines Autorisierungs Richtlinien-Speicher Objekts im Skript</span><span class="sxs-lookup"><span data-stu-id="a4478-103">Creating an Authorization Policy Store Object in Script</span></span>

<span data-ttu-id="a4478-104">Ein Autorisierungs Richtlinien Speicher enthält Informationen über die Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a4478-104">An authorization policy store contains information about the security policy of an application or group of applications.</span></span> <span data-ttu-id="a4478-105">Zu diesen Informationen gehören die Anwendungen, Vorgänge, Tasks, Benutzer und Gruppen von Benutzern, die dem Speicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a4478-105">The information includes the applications, operations, tasks, users, and groups of users associated with the store.</span></span> <span data-ttu-id="a4478-106">Wenn eine Anwendung, die den Autorisierungs-Manager verwendet, initialisiert, lädt Sie diese Informationen aus dem Speicher.</span><span class="sxs-lookup"><span data-stu-id="a4478-106">When an application that uses Authorization Manager initializes, it loads this information from the store.</span></span> <span data-ttu-id="a4478-107">Der Autorisierungs Richtlinien Speicher muss sich in einem vertrauenswürdigen System befinden, da Administratoren auf diesem System über ein hohes Maß an Zugriff auf den Store verfügen.</span><span class="sxs-lookup"><span data-stu-id="a4478-107">The authorization policy store must be located on a trusted system because administrators on that system have a high degree of access to the store.</span></span>

<span data-ttu-id="a4478-108">Der Autorisierungs-Manager unterstützt das Speichern von Autorisierungs Richtlinien entweder im Active Directory Directory-Dienst oder in einer XML-Datei, wie in den folgenden Beispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a4478-108">Authorization Manager supports storing authorization policy either in the Active Directory directory service or in an XML file as shown in the following examples.</span></span> <span data-ttu-id="a4478-109">In der Autorisierungs-Manager-API wird ein Autorisierungs Richtlinien Speicher durch ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a4478-109">In the Authorization Manager API, an authorization policy store is represented by an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="a4478-110">In den Beispielen wird gezeigt, wie ein **AzAuthorizationStore** -Objekt für einen Active Directory-Speicher und einen XML-Speicher erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a4478-110">The examples show how to create an **AzAuthorizationStore** object for an Active Directory store and an XML store.</span></span>

-   [<span data-ttu-id="a4478-111">Erstellen eines Active Directory Stores</span><span class="sxs-lookup"><span data-stu-id="a4478-111">Creating an Active Directory Store</span></span>](#creating-an-active-directory-store)
-   [<span data-ttu-id="a4478-112">Erstellen eines SQL Server Stores</span><span class="sxs-lookup"><span data-stu-id="a4478-112">Creating a SQL Server Store</span></span>](#creating-a-sql-server-store)
-   [<span data-ttu-id="a4478-113">Erstellen eines XML-Stores</span><span class="sxs-lookup"><span data-stu-id="a4478-113">Creating an XML Store</span></span>](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a><span data-ttu-id="a4478-114">Erstellen eines Active Directory Stores</span><span class="sxs-lookup"><span data-stu-id="a4478-114">Creating an Active Directory Store</span></span>

<span data-ttu-id="a4478-115">Um Active Directory zum Speichern der Autorisierungs Richtlinie zu verwenden, muss sich die Domäne auf der **Windows Server 2003** -Domänen Funktionsebene befinden.</span><span class="sxs-lookup"><span data-stu-id="a4478-115">To use Active Directory to store the authorization policy, the domain must be in the **Windows Server 2003** domain functional level.</span></span> <span data-ttu-id="a4478-116">Der Autorisierungs Richtlinien Speicher kann nicht in einem **nicht-Domänen-namens Kontext** (auch als Anwendungs Partition bezeichnet) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="a4478-116">The authorization policy store cannot be located in a **Non-Domain Naming Context** (also called an application partition).</span></span> <span data-ttu-id="a4478-117">Es wird empfohlen, dass sich der Speicher im **Programm Daten** Container unter einer neuen Organisationseinheit befindet, die speziell für den Autorisierungs Richtlinien Speicher erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4478-117">It is recommended that the store be located in the **Program Data** container under a new organizational unit created specifically for the authorization policy store.</span></span> <span data-ttu-id="a4478-118">Außerdem wird empfohlen, dass sich der Speicher innerhalb desselben lokalen Netzwerks befindet wie Anwendungsserver, die Anwendungen ausführen, die den Speicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4478-118">It is also recommended that the store be located within the same local area network as application servers that run applications that use the store.</span></span>

<span data-ttu-id="a4478-119">Im folgenden Beispiel wird gezeigt, wie ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt erstellt wird, das einen Autorisierungs Richtlinien Speicher in Active Directory darstellt.</span><span class="sxs-lookup"><span data-stu-id="a4478-119">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in Active Directory.</span></span> <span data-ttu-id="a4478-120">In diesem Beispiel wird davon ausgegangen, dass in einer Domäne mit dem Namen AuthManager.com eine vorhandene Organisationseinheit mit dem Namen Program Data Active Directory vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a4478-120">The example assumes that there is an existing Active Directory organizational unit named Program Data in a domain named authmanager.com.</span></span>


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _
    "msldap://CN=MyStore, CN=Program Data,DC=authmanager,DC=com"

'  Save the information to the store.
authStore.Submit
```



## <a name="creating-a-sql-server-store"></a><span data-ttu-id="a4478-121">Erstellen eines SQL Server Stores</span><span class="sxs-lookup"><span data-stu-id="a4478-121">Creating a SQL Server Store</span></span>

<span data-ttu-id="a4478-122">Der Autorisierungs-Manager unterstützt das Erstellen eines Microsoft SQL Server – basierten Autorisierungs Richtlinien Speicher.</span><span class="sxs-lookup"><span data-stu-id="a4478-122">Authorization Manager supports creating a Microsoft SQL Server–based authorization policy store.</span></span> <span data-ttu-id="a4478-123">Um einen SQL Server – basierten Autorisierungs Speicher zu erstellen, verwenden Sie eine URL, die mit dem Präfix **MSSQL://** beginnt.</span><span class="sxs-lookup"><span data-stu-id="a4478-123">To create a SQL Server–based authorization store, use a URL that begins with the prefix **MSSQL://**.</span></span> <span data-ttu-id="a4478-124">Die URL muss eine gültige SQL-Verbindungs Zeichenfolge, einen Datenbanknamen und den Namen des Autorisierungs Richtlinien Speicher enthalten: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _policystorename_.</span><span class="sxs-lookup"><span data-stu-id="a4478-124">The URL must contain a valid SQL connection string, a database name, and the name of the authorization policy store: **MSSQL://**_ConnectionString_*_/_*_DatabaseName_*_/_*_PolicyStoreName_.</span></span>

<span data-ttu-id="a4478-125">Wenn die Instanz von SQL Server die angegebene Autorisierungs-Manager-Datenbank nicht enthält, erstellt der Autorisierungs-Manager eine neue Datenbank mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="a4478-125">If the instance of SQL Server does not contain the specified Authorization Manager database, Authorization Manager creates a new database with that name.</span></span>

> [!Note]  
> <span data-ttu-id="a4478-126">Verbindungen mit einem SQL Server Speicher werden nur dann verschlüsselt, wenn Sie die SQL-Verschlüsselung für die Verbindung explizit einrichten oder die Verschlüsselung des Netzwerk Datenverkehrs einrichten, der IPSec (Internet Protocol Security) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4478-126">Connections to a SQL Server store are not encrypted unless you explicitly set up SQL encryption for the connection or set up encryption of the network traffic that uses Internet Protocol Security (IPsec).</span></span>

 

<span data-ttu-id="a4478-127">Im folgenden Beispiel wird gezeigt, wie ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt erstellt wird, das einen Autorisierungs Richtlinien Speicher in einer SQL Server-Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="a4478-127">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in a SQL Server database.</span></span>


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _ 
  "MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore"

'  Save information to the store.
authStore.Submit
```



## <a name="creating-an-xml-store"></a><span data-ttu-id="a4478-128">Erstellen eines XML-Stores</span><span class="sxs-lookup"><span data-stu-id="a4478-128">Creating an XML Store</span></span>

<span data-ttu-id="a4478-129">Der Autorisierungs-Manager unterstützt das Erstellen eines Autorisierungs Richtlinien Speicher im XML-Format</span><span class="sxs-lookup"><span data-stu-id="a4478-129">Authorization Manager supports creating an authorization policy store in XML format.</span></span> <span data-ttu-id="a4478-130">Der XML-Speicher kann sich auf demselben Computer befinden, auf dem die Anwendung ausgeführt wird, oder er kann Remote gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a4478-130">The XML store can be located on the same computer where the application runs, or it can be stored remotely.</span></span> <span data-ttu-id="a4478-131">Das direkte Bearbeiten der XML-Datei wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a4478-131">Editing the XML file directly is not supported.</span></span> <span data-ttu-id="a4478-132">Verwenden Sie das Autorisierungs-Manager-MMC-Snap-in oder die Autorisierungs-Manager-API zum Bearbeiten des Richtlinien Speicher.</span><span class="sxs-lookup"><span data-stu-id="a4478-132">Use the Authorization Manager MMC snap-in or the Authorization Manager API to edit the policy store.</span></span>

<span data-ttu-id="a4478-133">Der Autorisierungs-Manager unterstützt nicht die Delegierung der Verwaltung eines XML-Richtlinien Speicher.</span><span class="sxs-lookup"><span data-stu-id="a4478-133">Authorization Manager does not support delegating administration of an XML policy store.</span></span> <span data-ttu-id="a4478-134">Weitere Informationen zur Delegierung finden Sie unter [Delegieren der Definition von Berechtigungen in Skripts](delegating-the-defining-of-permissions-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="a4478-134">For information about delegation, see [Delegating the Defining of Permissions in Script](delegating-the-defining-of-permissions-in-script.md).</span></span>

<span data-ttu-id="a4478-135">Im folgenden Beispiel wird gezeigt, wie ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt erstellt wird, das einen Autorisierungs Richtlinien Speicher in einer XML-Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="a4478-135">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in an XML file.</span></span>


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



