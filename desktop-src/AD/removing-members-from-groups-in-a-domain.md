---
title: Entfernen von Mitgliedern aus Gruppen in einer Domäne
description: Sie können Benutzer, Gruppen oder Kontakte aus Gruppen entfernen.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- Gruppen anzeigen, Entfernen von Mitgliedern aus Gruppen in einer Domäne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab7600d98e75447c55fd84d783ff5263fc63bde
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724448"
---
# <a name="removing-members-from-groups-in-a-domain"></a><span data-ttu-id="51244-104">Entfernen von Mitgliedern aus Gruppen in einer Domäne</span><span class="sxs-lookup"><span data-stu-id="51244-104">Removing Members from Groups in a Domain</span></span>

<span data-ttu-id="51244-105">Sie können Benutzer, Gruppen oder Kontakte aus Gruppen entfernen.</span><span class="sxs-lookup"><span data-stu-id="51244-105">You can remove users, groups, or contacts from groups.</span></span> <span data-ttu-id="51244-106">Das **Member** -Attribut des **Group** -Objekts enthält alle direkten Mitglieder der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="51244-106">The **member** attribute of the **group** object contains all direct members of the group.</span></span>

<span data-ttu-id="51244-107">Die einfachste Möglichkeit, ein Mitglied aus einer Gruppe zu entfernen, besteht darin, die [**IADsGroup. Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) -Methode für die [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) -Schnittstelle des Gruppen Objekts aufzurufen, aus dem Sie Mitglieder entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="51244-107">The simplest way to remove a member from a group is to call the [**IADsGroup.Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) method on the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface of the group object you want to remove members from.</span></span>

 

 