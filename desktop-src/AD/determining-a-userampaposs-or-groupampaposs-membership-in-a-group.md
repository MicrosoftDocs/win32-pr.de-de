---
title: Bestimmen der Mitgliedschaft eines Benutzers oder einer Gruppe in einer Gruppe
description: Die IADsGroup. IsMember-Methode kann verwendet werden, um zu bestimmen, ob ein Objekt ein Mitglied einer Gruppe ist.
ms.assetid: c7168781-4ae4-4ce3-8d8a-2eefc7def62b
ms.tgt_platform: multiple
keywords:
- Bestimmen der Mitgliedschaft eines Benutzers oder einer Gruppe in einer Gruppen Anzeige
- Gruppen anzeigen, bestimmen der Mitgliedschaft eines Benutzers oder einer Gruppe in einer Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b520146079fdfaa5fa1adc99975b3b25d2e78c05
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038769"
---
# <a name="determining-a-users-or-groups-membership-in-a-group"></a><span data-ttu-id="a78b1-105">Bestimmen der Mitgliedschaft eines Benutzers oder einer Gruppe in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="a78b1-105">Determining a User's or Group's Membership in a Group</span></span>

<span data-ttu-id="a78b1-106">Die [**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) -Methode kann verwendet werden, um zu bestimmen, ob ein Objekt ein Mitglied einer Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="a78b1-106">The [**IADsGroup.IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) method can be used to determine if an object is a member of a group.</span></span> <span data-ttu-id="a78b1-107">Diese Methode gibt **true** zurück, wenn das angegebene Objekt ein direkter Member der Gruppe ist, d. h., die Member-Eigenschaft der Gruppe enthält das angegebene Objekt.</span><span class="sxs-lookup"><span data-stu-id="a78b1-107">This method returns **TRUE** if the specified object is a direct member of the group, that is, the group's member property contains the specified object.</span></span>

<span data-ttu-id="a78b1-108">Eine Gruppe kann andere Gruppen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a78b1-108">A group can contain other groups.</span></span> <span data-ttu-id="a78b1-109">Die [**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) -Methode überprüft die Mitglieder von Gruppen in der zugehörigen Element Eigenschaft, Gruppen innerhalb dieser Gruppen usw. nicht rekursiv.</span><span class="sxs-lookup"><span data-stu-id="a78b1-109">The [**IADsGroup.IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) method does not recursively verify the members of groups in its member property, groups within those groups, and so on.</span></span> <span data-ttu-id="a78b1-110">Wenn Sie rekursiv überprüfen möchten, ob ein Objekt ein Mitglied einer Gruppe ist, auflisten Sie die Gruppen in der Element Eigenschaft, überprüfen Sie die Mitglieder dieser Gruppen, um festzustellen, ob das Objekt ein Element ist, und wenn diese Gruppen andere Gruppen enthalten, überprüfen Sie Ihre Member usw.</span><span class="sxs-lookup"><span data-stu-id="a78b1-110">To recursively verify that an object is a member of a group, enumerate the groups in the member property, verify the members of those groups to see if the object is a member, and if those groups contain other groups, check their members, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="a78b1-111">Da Gruppen gruppiert werden können, kann die Gruppenmitgliedschaft über Schleifen verfügen.</span><span class="sxs-lookup"><span data-stu-id="a78b1-111">Since groups can be nested, group membership may have loops.</span></span> <span data-ttu-id="a78b1-112">Jedes Skript, das viele Gruppen auflistet, sollte eine interne Liste von Gruppen zum Beenden der Rekursion behalten, wenn eine Gruppe bereits besucht wurde.</span><span class="sxs-lookup"><span data-stu-id="a78b1-112">Any script that enumerates over many groups should keep an internal list of groups to end recursion if a group has already been visited.</span></span>

 

 

 