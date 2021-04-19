---
description: Verwenden der Autorisierungs-Manager-API, um den Zugriff auf Anwendungs Ressourcen zu steuern.
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: Verwenden der Autorisierung in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6771d16748d3c04680b545a83e382fa3d5ce78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363625"
---
# <a name="using-authorization-in-c"></a><span data-ttu-id="de029-103">Verwenden der Autorisierung in C++</span><span class="sxs-lookup"><span data-stu-id="de029-103">Using Authorization in C++</span></span>

<span data-ttu-id="de029-104">Sie können die Autorisierungs-Manager-API verwenden, um den Zugriff auf Anwendungs Ressourcen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="de029-104">You can use the Authorization Manager API to control access to application resources.</span></span>

<span data-ttu-id="de029-105">Wenn Sie über eine vorhandene Zugriffs Steuerungslösung verfügen, die auf [*Zugriffs Steuerungs Listen (Access Control Lists*](/windows/desktop/SecGloss/a-gly) , ACLs) basiert, und Sie die Projekt Mappe nicht zur Verwendung des Autorisierungs-Managers umrechnen möchten, können Sie weiterhin ACLs zum Steuern des Zugriffs auf Ressourcen verwenden</span><span class="sxs-lookup"><span data-stu-id="de029-105">If you have an existing access control solution based on [*access control lists*](/windows/desktop/SecGloss/a-gly) (ACLs) and want to avoid converting this solution to use Authorization Manager, you can continue to use ACLs to control access to resources.</span></span> <span data-ttu-id="de029-106">Informationen zum Steuern des Zugriffs auf Ressourcen mithilfe von ACLs finden Sie unter [Definieren von Berechtigungen mit ACLs in C++](defining-permissions-with-acls-in-c--.md), [Einrichten eines Client Kontexts aus einer SID in C++](establishing-a-client-context-from-a-sid-in-c--.md)und über [prüfen des Client Zugriffs mit ACLs in C++](verifying-client-access-with-acls-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="de029-106">For information about controlling access to resources using ACLs, see [Defining Permissions with ACLs in C++](defining-permissions-with-acls-in-c--.md), [Establishing a Client Context from a SID in C++](establishing-a-client-context-from-a-sid-in-c--.md), and [Verifying Client Access with ACLs in C++](verifying-client-access-with-acls-in-c--.md).</span></span>

> [!Note]  
> <span data-ttu-id="de029-107">Für große Unternehmen gibt es einen Kompromiss zwischen Verwaltungsaufwand und Leistung.</span><span class="sxs-lookup"><span data-stu-id="de029-107">For large enterprises, there is a trade-off between administrative overhead and performance.</span></span> <span data-ttu-id="de029-108">Wenn die Anzahl der gesicherten Ressourcen und Benutzer zunimmt, wird die Verwaltung von ACLs komplizierter.</span><span class="sxs-lookup"><span data-stu-id="de029-108">As the number of secured resources and users increases, the administration of ACLs becomes more complicated.</span></span> <span data-ttu-id="de029-109">Die Leistung wird nicht beeinträchtigt, da alle erforderlichen Informationen zu Zugriffsrechten an die gesicherten Ressourcen verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="de029-109">Performance is not affected because all required information about access rights is distributed to the secured resources.</span></span> <span data-ttu-id="de029-110">Die Leistung des Autorisierungs-Managers wird durch die Skalierung beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="de029-110">The performance of Authorization Manager is affected by scaling.</span></span>

 

<span data-ttu-id="de029-111">Weitere Informationen zu anderen Autorisierungs Aufgaben finden Sie [unter unterstützen von Aufgaben für die Autorisierung in C++](supporting-tasks-for-authorization-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="de029-111">For information about other authorization tasks, see [Supporting Tasks for Authorization in C++](supporting-tasks-for-authorization-in-c--.md).</span></span>



| <span data-ttu-id="de029-112">Thema</span><span class="sxs-lookup"><span data-stu-id="de029-112">Topic</span></span>                                                                                                                | <span data-ttu-id="de029-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de029-113">Description</span></span>                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de029-114">Definieren von Berechtigungen in C++</span><span class="sxs-lookup"><span data-stu-id="de029-114">Defining Permissions in C++</span></span>](defining-permissions-in-c--.md)                                                       | <span data-ttu-id="de029-115">Definieren Sie, welche Benutzer auf welche Anwendungs Ressourcen zugreifen können, indem Sie einen Autorisierungs Richtlinien Speicher erstellen.</span><span class="sxs-lookup"><span data-stu-id="de029-115">Define which users have access to which application resources by creating an authorization policy store.</span></span> |
| [<span data-ttu-id="de029-116">Überprüfen des Client Zugriffs auf eine angeforderte Ressource in C++</span><span class="sxs-lookup"><span data-stu-id="de029-116">Verifying Client Access to a Requested Resource in C++</span></span>](verifying-client-access-to-a-requested-resource-in-c--.md) | <span data-ttu-id="de029-117">Überprüfen Sie, ob der Client Zugriff auf einen oder mehrere Vorgänge hat.</span><span class="sxs-lookup"><span data-stu-id="de029-117">Check whether the client has access to one or more operations.</span></span>                                           |
| [<span data-ttu-id="de029-118">Delegieren der definierenden Berechtigungen in C++</span><span class="sxs-lookup"><span data-stu-id="de029-118">Delegating the Defining of Permissions in C++</span></span>](delegating-the-defining-of-permissions-in-c--.md)                   | <span data-ttu-id="de029-119">Delegieren Sie die Verwaltung der Autorisierungs Richtlinien Speicher, die in Active Directory gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="de029-119">Delegate the administration of authorization policy stores that are stored in Active Directory.</span></span>          |



 

 

 
