---
title: Ändern des Bereichs oder Typs einer Gruppe
description: In diesem Thema wird gezeigt, wie der Bereich einer Gruppe oder der Typ in Domänen im einheitlichen Modus geändert wird.
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- Gruppen anzeigen, Ändern des Gültigkeits Bereichs oder des Typs einer Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65c64b4a2dafe4bf6c0e65463ef16e0270c0be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707206"
---
# <a name="changing-a-groups-scope-or-type"></a><span data-ttu-id="9f621-104">Ändern des Bereichs oder Typs einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="9f621-104">Changing a Group's Scope or Type</span></span>

<span data-ttu-id="9f621-105">Das Ändern eines Gruppen Bereichs oder Typs ist in Domänen mit gemischtem Modus nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9f621-105">Changing a group scope or type is not allowed in mixed-mode domains.</span></span> <span data-ttu-id="9f621-106">Die folgenden Konvertierungen sind jedoch in Domänen im einheitlichen Modus zulässig:</span><span class="sxs-lookup"><span data-stu-id="9f621-106">However, the following conversions are allowed in native-mode domains:</span></span>

<span data-ttu-id="9f621-107">Globale Gruppe in universelle Gruppe: Dies ist nur zulässig, wenn die globale Gruppe nicht Mitglied einer anderen globalen Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="9f621-107">Global group to universal group: This is only allowed if the global group is not a member of another global group.</span></span>

<span data-ttu-id="9f621-108">Lokale Domänen Gruppe zu universeller Gruppe: die zu konvertierende lokale Domänen Gruppe darf keine andere lokale Domänen Gruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="9f621-108">Domain local group to universal group: The domain local group being converted cannot contain another domain local group.</span></span>

<span data-ttu-id="9f621-109">Universelle Gruppe in globale oder lokale Domänen Gruppe: für die Konvertierung in eine globale Gruppe kann die zu konvertierende universelle Gruppe keine Benutzer oder globalen Gruppen aus einer anderen Domäne enthalten.</span><span class="sxs-lookup"><span data-stu-id="9f621-109">Universal group to global or domain local group: For conversion to global group, the universal group being converted cannot contain users or global groups from another domain.</span></span> <span data-ttu-id="9f621-110">Bei der Konvertierung in eine lokale Domänen Gruppe kann die zu konvertierende universelle Gruppe nicht Mitglied einer universellen Gruppe oder einer lokalen Gruppe einer Domäne aus einer anderen Domäne sein.</span><span class="sxs-lookup"><span data-stu-id="9f621-110">For conversion to domain local group, the universal group being converted cannot be a member of any universal group or a domain local group from another domain.</span></span>

<span data-ttu-id="9f621-111">Im einheitlichen Modus kann ein Gruppentyp zwischen Sicherheitsgruppen und Verteiler Gruppen frei konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f621-111">In native mode, a group type can be converted freely between security groups and distribution groups.</span></span>

<span data-ttu-id="9f621-112">Beachten Sie, dass eine Änderung des Bereichs oder Typs die Zugriffs Steuerungs Einträge (ACEs), die diese Gruppe enthalten, beeinträchtigen kann, wenn eine Gruppe zum Festlegen der Zugriffs Steuerung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f621-112">Be aware that if a group is used to set access control, changing the scope or type can affect the access control entries (ACEs) that contain that group.</span></span> <span data-ttu-id="9f621-113">Das Sicherheitssystem ignoriert ACEs, die Gruppen enthalten, die keine Sicherheitsgruppen sind.</span><span class="sxs-lookup"><span data-stu-id="9f621-113">The security system will ignore ACEs that contain groups that are not security groups.</span></span>

 

 




