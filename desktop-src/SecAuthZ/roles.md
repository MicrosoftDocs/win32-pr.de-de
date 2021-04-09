---
description: Rollen dienen zwei unterschiedlichen Zwecken im Autorisierungs-Manager.
ms.assetid: 6d045ecb-432e-4ba6-b5d2-37db82ab1884
title: Rollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65d140faa22c72d098c7a4ba2f13e952b2713f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863019"
---
# <a name="roles"></a><span data-ttu-id="50e99-103">Rollen</span><span class="sxs-lookup"><span data-stu-id="50e99-103">Roles</span></span>

<span data-ttu-id="50e99-104">Rollen dienen zwei unterschiedlichen Zwecken im Autorisierungs-Manager.</span><span class="sxs-lookup"><span data-stu-id="50e99-104">Roles serve two different purposes in Authorization Manager.</span></span> <span data-ttu-id="50e99-105">Eine Rolle besteht aus einer Reihe von Tasks oder Vorgängen, auf die eine Kategorie von Benutzern zugreifen muss. Außerdem handelt es sich um eine Gruppe von Benutzern und Gruppen, die in diese Kategorie passen.</span><span class="sxs-lookup"><span data-stu-id="50e99-105">A role is a set of tasks or operations to which a category of users requires access, and it is also a set of users and groups that fit into that category.</span></span>

-   [<span data-ttu-id="50e99-106">Rollen als Satz von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="50e99-106">Roles as Sets of Tasks</span></span>](#roles-as-sets-of-tasks)
-   [<span data-ttu-id="50e99-107">Rollen als Gruppen von Benutzern und Gruppen</span><span class="sxs-lookup"><span data-stu-id="50e99-107">Roles as Sets of Users and Groups</span></span>](#roles-as-sets-of-users-and-groups)
-   [<span data-ttu-id="50e99-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50e99-108">Related topics</span></span>](#related-topics)

## <a name="roles-as-sets-of-tasks"></a><span data-ttu-id="50e99-109">Rollen als Satz von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="50e99-109">Roles as Sets of Tasks</span></span>

<span data-ttu-id="50e99-110">Eine Autorisierungs Richtlinie weist [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekte einem [**iazrole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) -Objekt zu, um Aufgaben Sätze zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="50e99-110">An authorization policy assigns [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) objects to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to create sets of tasks.</span></span> <span data-ttu-id="50e99-111">Alle Benutzer und Gruppen, die diesem **iazrole** -Objekt zugewiesen sind, verfügen dann über die Berechtigung für den Zugriff auf alle Vorgänge, die von diesen **iaztask** -Objekten</span><span class="sxs-lookup"><span data-stu-id="50e99-111">All users and groups assigned to that **IAzRole** object then have permission to access all operations contained by those **IAzTask** objects.</span></span>

<span data-ttu-id="50e99-112">Da ein [**iazrole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) -Objekt eine Reihe von Tasks und eine Gruppe von Benutzern und Gruppen mit Zugriff auf diese Aufgaben darstellt, bietet der Autorisierungs-Manager eine Möglichkeit, Rollen Definitionen zu erstellen, die mehreren **iazrole** -Objekten zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="50e99-112">Because an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object represents both a set of tasks and a set of users and groups that have access to those tasks, Authorization Manager provides a way to create role definitions that can be assigned to more than one **IAzRole** object.</span></span> <span data-ttu-id="50e99-113">Ein [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt kann andere **iaztask** -Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="50e99-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can contain other **IAzTask** objects.</span></span> <span data-ttu-id="50e99-114">Anschließend können Sie dieses **iaztask** -Objekt als Rollendefinition verwenden, indem Sie es einem oder mehreren **iazrole** -Objekten zuweisen.</span><span class="sxs-lookup"><span data-stu-id="50e99-114">You can then use that **IAzTask** object as a role definition by assigning it to one or more **IAzRole** objects.</span></span> <span data-ttu-id="50e99-115">Legen Sie [**die isroledefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) -Eigenschaft des **iaztask** -Objekts auf " **true** " fest, damit die Benutzeroberfläche des **Autorisierungs-Managers** für den MMC-Snap-in als Rolle angezeigt wird. </span><span class="sxs-lookup"><span data-stu-id="50e99-115">Set the [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property of the **IAzTask** object to **TRUE** to cause the **Authorization Manager** MMC snap-in user interface to display the **IAzTask** object as a role.</span></span>

## <a name="roles-as-sets-of-users-and-groups"></a><span data-ttu-id="50e99-116">Rollen als Gruppen von Benutzern und Gruppen</span><span class="sxs-lookup"><span data-stu-id="50e99-116">Roles as Sets of Users and Groups</span></span>

<span data-ttu-id="50e99-117">Zuweisen von Benutzern und Gruppen zu einem [**iazrole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) -Objekt, um diesen Benutzern und Gruppen Zugriff auf die Aufgaben zu gewähren, die diesem **iazrole** -Objekt zugewiesen sind, indem die [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) -oder [**AddMembership Name**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="50e99-117">Assign users and groups to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to grant those users and groups access to the tasks assigned to that **IAzRole** object by calling the [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) or [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) method.</span></span> <span data-ttu-id="50e99-118">Zuweisen vorhandener Anwendungs Gruppen, die durch [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekte dargestellt werden, zu einem **iazrole** -Objekt durch Aufrufen der [**addappmember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) -Methode.</span><span class="sxs-lookup"><span data-stu-id="50e99-118">Assign existing application groups, represented by [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) objects, to an **IAzRole** object by calling the [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) method.</span></span> <span data-ttu-id="50e99-119">Alle Benutzer und Gruppen, die dem **iazrole** -Objekt zugewiesen sind, haben Zugriff auf die Aufgaben und Vorgänge, die dieser Rolle zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="50e99-119">All users and groups assigned to the **IAzRole** object have access to the tasks and operations assigned to that role.</span></span> <span data-ttu-id="50e99-120">Weitere Informationen zu Anwendungs Gruppen finden Sie unter [Benutzer und Gruppen](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="50e99-120">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="50e99-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50e99-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50e99-122">Gruppieren von Aufgaben in Rollen in C++</span><span class="sxs-lookup"><span data-stu-id="50e99-122">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="50e99-123">Definieren von Benutzergruppen in C++</span><span class="sxs-lookup"><span data-stu-id="50e99-123">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> <dt>

[<span data-ttu-id="50e99-124">Hinzufügen von Benutzern zu einer Anwendungs Gruppe in C++</span><span class="sxs-lookup"><span data-stu-id="50e99-124">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



