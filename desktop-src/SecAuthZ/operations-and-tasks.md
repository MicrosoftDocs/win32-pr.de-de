---
description: Bei einem Vorgang handelt es sich um eine Computer Aktion auf niedriger Ebene.
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: Vorgänge und Aufgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a198d8844a9f34030b8b6a40eba759eed4057119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363587"
---
# <a name="operations-and-tasks"></a><span data-ttu-id="88ee3-103">Vorgänge und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="88ee3-103">Operations and Tasks</span></span>

<span data-ttu-id="88ee3-104">Bei einem Vorgang handelt es sich um eine Computer Aktion auf niedriger Ebene.</span><span class="sxs-lookup"><span data-stu-id="88ee3-104">An operation is a low-level computer action.</span></span> <span data-ttu-id="88ee3-105">In der Autorisierungs-Manager-API wird ein Vorgang durch ein [**iazoperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="88ee3-105">In the Authorization Manager API, an operation is represented by an [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) object.</span></span> <span data-ttu-id="88ee3-106">Im Allgemeinen sind Vorgänge zu viele und zu niedrig, um die Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="88ee3-106">In general, operations are too many in number and too low-level to facilitate administration.</span></span> <span data-ttu-id="88ee3-107">Gruppieren von Vorgängen in Aufgaben zur Vereinfachung der Verwaltung von Autorisierungs Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="88ee3-107">Group operations into tasks to simplify administration of authorization policy.</span></span>

<span data-ttu-id="88ee3-108">Eine Aufgabe wird durch ein [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt dargestellt und kann ein oder mehrere [**iazoperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) -Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="88ee3-108">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object and can contain one or more [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) objects.</span></span> <span data-ttu-id="88ee3-109">Ein **iaztask** -Objekt kann auch andere **iaztask** -Objekte enthalten, sodass Aufgaben in den Netz Körper eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="88ee3-109">An **IAzTask** object can also contain other **IAzTask** objects, so that tasks can be nested.</span></span> <span data-ttu-id="88ee3-110">Um die Verwaltung zu vereinfachen, sollte ein **iaztask** -Objekt eine Aufgabe darstellen, die ein echter Benutzer ausführen möchte.</span><span class="sxs-lookup"><span data-stu-id="88ee3-110">To facilitate administration, an **IAzTask** object should represent a task that a real user wants to perform.</span></span>

<span data-ttu-id="88ee3-111">Der Zugriff auf die Vorgänge, die in einer Aufgabe enthalten sind, kann zur Laufzeit durch ein Geschäftsregel Skript qualifiziert werden, das dem [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt zugeordnet ist, das diese Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="88ee3-111">Access to the operations contained by a task can be qualified at run time by a business rule script associated with the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents that task.</span></span> <span data-ttu-id="88ee3-112">Weitere Informationen zu Geschäftsregel Skripts finden Sie [unter Geschäftsregeln](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="88ee3-112">For more information about business rule scripts, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="88ee3-113">Ein [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt kann auch eine Rollendefinition darstellen, indem seine [**isroledefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) -Eigenschaft auf **true** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="88ee3-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can also represent a role definition by setting its [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property to **TRUE**.</span></span> <span data-ttu-id="88ee3-114">Die MMC-Snap-in-Benutzeroberfläche des **Autorisierungs-Managers** zeigt dann dieses **iaztask** -Objekt als Rolle an.</span><span class="sxs-lookup"><span data-stu-id="88ee3-114">The **Authorization Manager** MMC snap-in user interface then displays that **IAzTask** object as a role.</span></span> <span data-ttu-id="88ee3-115">Weitere Informationen zu Rollen Definitionen finden Sie unter [Rollen](roles.md).</span><span class="sxs-lookup"><span data-stu-id="88ee3-115">For more information about role definitions, see [Roles](roles.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="88ee3-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="88ee3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88ee3-117">Definieren von Vorgängen in C++</span><span class="sxs-lookup"><span data-stu-id="88ee3-117">Defining Operations in C++</span></span>](defining-operations-in-c--.md)
</dt> <dt>

[<span data-ttu-id="88ee3-118">Gruppieren von Vorgängen in Aufgaben in C++</span><span class="sxs-lookup"><span data-stu-id="88ee3-118">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[<span data-ttu-id="88ee3-119">Gruppieren von Aufgaben in Rollen in C++</span><span class="sxs-lookup"><span data-stu-id="88ee3-119">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="88ee3-120">Benutzer und Gruppen</span><span class="sxs-lookup"><span data-stu-id="88ee3-120">Users and Groups</span></span>](users-and-groups.md)
</dt> </dl>

 

 



