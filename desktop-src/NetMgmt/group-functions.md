---
title: Gruppenfunktionen
description: Eine globale Gruppe enthält Benutzerkonten aus einer Domäne, die unter einem Gruppenkonto Namen gruppiert sind.
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7696755cd5f5cbe75de11d386cb238fa3bd5d35d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390839"
---
# <a name="group-functions"></a><span data-ttu-id="de8c4-103">Gruppenfunktionen</span><span class="sxs-lookup"><span data-stu-id="de8c4-103">Group Functions</span></span>

<span data-ttu-id="de8c4-104">Eine *globale Gruppe* enthält Benutzerkonten aus einer Domäne, die unter einem Gruppenkonto Namen gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="de8c4-104">A *global group* contains user accounts from one domain that are grouped together under one group account name.</span></span> <span data-ttu-id="de8c4-105">Eine globale Gruppe kann nur Mitglieder (Benutzer) aus der Domäne enthalten, in der die globale Gruppe erstellt wird. Er darf keine lokalen Gruppen enthalten.</span><span class="sxs-lookup"><span data-stu-id="de8c4-105">A global group can contain only members (users) from the domain where the global group is created; it cannot contain local groups.</span></span> <span data-ttu-id="de8c4-106">Eine globale Gruppe ist innerhalb ihrer eigenen Domäne und innerhalb einer vertrauenden Domäne verfügbar.</span><span class="sxs-lookup"><span data-stu-id="de8c4-106">A global group is available within its own domain and within any trusting domain.</span></span>

<span data-ttu-id="de8c4-107">Die Funktionen der Netzwerk Verwaltungsgruppe steuern globale Gruppen.</span><span class="sxs-lookup"><span data-stu-id="de8c4-107">The network management group functions control global groups.</span></span> <span data-ttu-id="de8c4-108">Die Gruppenfunktionen sind nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="de8c4-108">The group functions are listed following.</span></span>



| <span data-ttu-id="de8c4-109">Funktion</span><span class="sxs-lookup"><span data-stu-id="de8c4-109">Function</span></span>                                     | <span data-ttu-id="de8c4-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de8c4-110">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="de8c4-111">**"NetGroupAdd"**</span><span class="sxs-lookup"><span data-stu-id="de8c4-111">**NetGroupAdd**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | <span data-ttu-id="de8c4-112">Erstellt eine globale Gruppe.</span><span class="sxs-lookup"><span data-stu-id="de8c4-112">Creates a global group.</span></span>                                                           |
| [<span data-ttu-id="de8c4-113">**Netgroupadduser**</span><span class="sxs-lookup"><span data-stu-id="de8c4-113">**NetGroupAddUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | <span data-ttu-id="de8c4-114">Fügt einer vorhandenen globalen Gruppe einen Benutzer hinzu.</span><span class="sxs-lookup"><span data-stu-id="de8c4-114">Adds one user to an existing global group.</span></span>                                        |
| [<span data-ttu-id="de8c4-115">**Netgroupdel**</span><span class="sxs-lookup"><span data-stu-id="de8c4-115">**NetGroupDel**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | <span data-ttu-id="de8c4-116">Entfernt eine globale Gruppe, unabhängig davon, ob die Gruppe über Mitglieder verfügt.</span><span class="sxs-lookup"><span data-stu-id="de8c4-116">Removes a global group whether or not the group has any members.</span></span>                  |
| [<span data-ttu-id="de8c4-117">**Netgroupdelta User**</span><span class="sxs-lookup"><span data-stu-id="de8c4-117">**NetGroupDelUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | <span data-ttu-id="de8c4-118">Entfernt einen Benutzernamen aus einer globalen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="de8c4-118">Removes one user name from a global group.</span></span>                                        |
| [<span data-ttu-id="de8c4-119">**Netgroupum**</span><span class="sxs-lookup"><span data-stu-id="de8c4-119">**NetGroupEnum**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | <span data-ttu-id="de8c4-120">Listet alle globalen Gruppen auf einem Server auf.</span><span class="sxs-lookup"><span data-stu-id="de8c4-120">Lists all global groups on a server.</span></span>                                              |
| [<span data-ttu-id="de8c4-121">**Netgroupgetinfo**</span><span class="sxs-lookup"><span data-stu-id="de8c4-121">**NetGroupGetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | <span data-ttu-id="de8c4-122">Gibt Informationen zu einer bestimmten globalen Gruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="de8c4-122">Returns information about a particular global group.</span></span>                              |
| [<span data-ttu-id="de8c4-123">**Netgroupgetusers**</span><span class="sxs-lookup"><span data-stu-id="de8c4-123">**NetGroupGetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | <span data-ttu-id="de8c4-124">Listet alle Mitglieder einer bestimmten globalen Gruppe auf.</span><span class="sxs-lookup"><span data-stu-id="de8c4-124">Lists all members of a particular global group.</span></span>                                   |
| [<span data-ttu-id="de8c4-125">**Netgroupeintinfo**</span><span class="sxs-lookup"><span data-stu-id="de8c4-125">**NetGroupSetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | <span data-ttu-id="de8c4-126">Legt allgemeine Informationen zu einer globalen Gruppe fest.</span><span class="sxs-lookup"><span data-stu-id="de8c4-126">Sets general information about a global group.</span></span>                                    |
| [<span data-ttu-id="de8c4-127">**Netgroupsetusers**</span><span class="sxs-lookup"><span data-stu-id="de8c4-127">**NetGroupSetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | <span data-ttu-id="de8c4-128">Weist Mitglieder einer neuen globalen Gruppe zu. ersetzt die Mitglieder einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="de8c4-128">Assigns members to a new global group; replaces the members of an existing group.</span></span> |



 

<span data-ttu-id="de8c4-129">Wenn Sie die [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) -Funktion aufrufen, um eine globale Gruppe zu erstellen, müssen Sie einen Gruppennamen angeben.</span><span class="sxs-lookup"><span data-stu-id="de8c4-129">When you call the [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) function to create a global group, you must supply a group name.</span></span> <span data-ttu-id="de8c4-130">Anfänglich hat eine neue Gruppe keine Mitglieder.</span><span class="sxs-lookup"><span data-stu-id="de8c4-130">Initially, a new group has no members.</span></span>

<span data-ttu-id="de8c4-131">Benutzerkonten gehören automatisch zu den speziellen globalen Gruppen Domänen Benutzern.</span><span class="sxs-lookup"><span data-stu-id="de8c4-131">User accounts automatically belong to the special global group Domain Users.</span></span> <span data-ttu-id="de8c4-132">Die Mitgliedschaft in dieser Gruppe wird indirekt von den Funktionen " [**nettuseradd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)", " [**nettuserdel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)" und " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " gesteuert.</span><span class="sxs-lookup"><span data-stu-id="de8c4-132">Membership in this group is indirectly controlled by the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), and [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) functions.</span></span>

<span data-ttu-id="de8c4-133">Informationen zu globalen Gruppenkonten sind auf folgenden Ebenen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="de8c4-133">Global group account information is available at the following levels:</span></span>

-   [<span data-ttu-id="de8c4-134">**Gruppen \_ Informationen \_ 0**</span><span class="sxs-lookup"><span data-stu-id="de8c4-134">**GROUP\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [<span data-ttu-id="de8c4-135">**Gruppen \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="de8c4-135">**GROUP\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [<span data-ttu-id="de8c4-136">**Gruppen \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="de8c4-136">**GROUP\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [<span data-ttu-id="de8c4-137">**Gruppen \_ Informationen \_ 3**</span><span class="sxs-lookup"><span data-stu-id="de8c4-137">**GROUP\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [<span data-ttu-id="de8c4-138">**Gruppen \_ Informationen \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="de8c4-138">**GROUP\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [<span data-ttu-id="de8c4-139">**Gruppen \_ Informationen \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="de8c4-139">**GROUP\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

<span data-ttu-id="de8c4-140">Die 1002-und 1005-Ebenen sind nur für die [**netgroupsetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) -Funktion gültig.</span><span class="sxs-lookup"><span data-stu-id="de8c4-140">The 1002 and 1005 levels are valid only for the [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) function.</span></span>

<span data-ttu-id="de8c4-141">Informationen zu globalen Gruppenmitgliedern sind auf der folgenden Informationsebene verfügbar:</span><span class="sxs-lookup"><span data-stu-id="de8c4-141">Global group member information is available at the following information level:</span></span>

-   [<span data-ttu-id="de8c4-142">**Gruppen \_ Benutzer \_ Informationen \_ 0**</span><span class="sxs-lookup"><span data-stu-id="de8c4-142">**GROUP\_USERS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

<span data-ttu-id="de8c4-143">Weitere Informationen finden Sie in den Funktionen der [lokalen](local-group-functions.md)Netzwerk Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="de8c4-143">For more information, see the network management [Local Group Functions](local-group-functions.md).</span></span>

<span data-ttu-id="de8c4-144">Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Funktionen der Netzwerk Verwaltungsgruppe erreichen können.</span><span class="sxs-lookup"><span data-stu-id="de8c4-144">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management group functions.</span></span> <span data-ttu-id="de8c4-145">Weitere Informationen finden Sie unter [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span><span class="sxs-lookup"><span data-stu-id="de8c4-145">For more information, see [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span></span>

 

 