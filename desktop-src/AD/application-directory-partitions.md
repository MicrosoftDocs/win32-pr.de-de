---
title: Anwendungsverzeichnis Partitionen
description: In Windows Server 2003 unterstützen Active Directory Domain Services Anwendungsverzeichnis Partitionen.
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- Anwendungsverzeichnis Partitionen AD
- Anwendungsverzeichnis Partitionen AD, using
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a8e035231aa24569b6fad6d5a7e0e62eaa5a30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038805"
---
# <a name="application-directory-partitions"></a><span data-ttu-id="aca3b-105">Anwendungsverzeichnis Partitionen</span><span class="sxs-lookup"><span data-stu-id="aca3b-105">Application Directory Partitions</span></span>

<span data-ttu-id="aca3b-106">In Windows Server 2003 unterstützen Active Directory Domain Services Anwendungsverzeichnis Partitionen.</span><span class="sxs-lookup"><span data-stu-id="aca3b-106">In Windows Server 2003, Active Directory Domain Services support application directory partitions.</span></span> <span data-ttu-id="aca3b-107">Eine Anwendungsverzeichnis Partition kann eine Hierarchie beliebiger Objekttypen enthalten, mit Ausnahme von Sicherheits Prinzipale, und kann so konfiguriert werden, dass Sie auf eine beliebige Gruppe von Domänen Controllern in der Gesamtstruktur repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="aca3b-107">An application directory partition can contain a hierarchy of any type of objects, except security principals, and can be configured to replicate to any set of domain controllers in the forest.</span></span> <span data-ttu-id="aca3b-108">Im Gegensatz zu einer Domänen Partition ist eine Anwendungsverzeichnis Partition nicht für die Replikation auf alle Domänen Controller in einer Domäne erforderlich, und die Partition kann auf Domänen Controllern in verschiedenen Domänen der Gesamtstruktur repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="aca3b-108">Unlike a domain partition, an application directory partition is not required to replicate to all domain controllers in a domain and the partition can replicate to domain controllers in different domains of the forest.</span></span> <span data-ttu-id="aca3b-109">Weitere Informationen zu Anwendungsverzeichnis Partitionen finden Sie unter Informationen [zu Anwendungsverzeichnis Partitionen](about-application-directory-partitions.md).</span><span class="sxs-lookup"><span data-stu-id="aca3b-109">For more information about application directory partitions, see [About Application Directory Partitions](about-application-directory-partitions.md).</span></span>

<span data-ttu-id="aca3b-110">Eine Anwendungsverzeichnis Partition kann erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="aca3b-110">An application directory partition can be created.</span></span> <span data-ttu-id="aca3b-111">geändert und gelöscht mit standardmäßigen ADSI-, LDAP-und [System. Director yservices](/dotnet/api/system.directoryservices) -Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="aca3b-111">modified and deleted using standard ADSI, LDAP and [System.DirectoryServices](/dotnet/api/system.directoryservices) operations.</span></span> <span data-ttu-id="aca3b-112">Der Sicherheitskontext, der erforderlich ist, um eine Anwendungsverzeichnis Partition zu erstellen und zu ändern, ist identisch mit der zum Erstellen einer Domänen Partition.</span><span class="sxs-lookup"><span data-stu-id="aca3b-112">The security context required to create and modify an application directory partition is the same as that for creating a domain partition.</span></span>

<span data-ttu-id="aca3b-113">In den folgenden Themen wird beschrieben, wie Sie mit Anwendungsverzeichnis Partitionen arbeiten:</span><span class="sxs-lookup"><span data-stu-id="aca3b-113">The following topics describe how to work with application directory partitions:</span></span>

-   [<span data-ttu-id="aca3b-114">Anwendungsverzeichnis-Partitions Replikation</span><span class="sxs-lookup"><span data-stu-id="aca3b-114">Application Directory Partition Replication</span></span>](application-directory-partition-replication.md)
-   [<span data-ttu-id="aca3b-115">Sicherheit der Anwendungsverzeichnis Partition</span><span class="sxs-lookup"><span data-stu-id="aca3b-115">Application Directory Partition Security</span></span>](application-directory-partition-security.md)
-   [<span data-ttu-id="aca3b-116">Erstellen einer Anwendungsverzeichnis Partition</span><span class="sxs-lookup"><span data-stu-id="aca3b-116">Creating an Application Directory Partition</span></span>](creating-an-application-directory-partition.md)
-   [<span data-ttu-id="aca3b-117">Löschen einer Anwendungsverzeichnis Partition</span><span class="sxs-lookup"><span data-stu-id="aca3b-117">Deleting an Application Directory Partition</span></span>](deleting-an-application-directory-partition.md)
-   [<span data-ttu-id="aca3b-118">Auflisten von Anwendungsverzeichnis Partitionen in einer Gesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="aca3b-118">Enumerating Application Directory Partitions in a Forest</span></span>](enumerating-application-directory-partitions-in-a-forest.md)
-   [<span data-ttu-id="aca3b-119">Suchen eines Anwendungsverzeichnis-Partitions Host Servers</span><span class="sxs-lookup"><span data-stu-id="aca3b-119">Locating an Application Directory Partition Host Server</span></span>](locating-an-application-directory-partition-host-server.md)
-   [<span data-ttu-id="aca3b-120">Hinzufügen oder Löschen eines Anwendungsverzeichnis-Partitions Replikats</span><span class="sxs-lookup"><span data-stu-id="aca3b-120">Adding or Deleting an Application Directory Partition Replica</span></span>](adding-or-deleting-an-application-directory-partition-replica.md)
-   [<span data-ttu-id="aca3b-121">Auflisten von Replikaten einer Anwendungsverzeichnis Partition</span><span class="sxs-lookup"><span data-stu-id="aca3b-121">Enumerating Replicas of an Application Directory Partition</span></span>](enumerating-replicas-of-an-application-directory-partition.md)
-   [<span data-ttu-id="aca3b-122">Ändern der Konfiguration der Anwendungsverzeichnis Partition</span><span class="sxs-lookup"><span data-stu-id="aca3b-122">Modifying Application Directory Partition Configuration</span></span>](modifying-application-directory-partition-configuration.md)

 

 