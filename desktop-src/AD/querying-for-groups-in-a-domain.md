---
title: Abfragen von Gruppen in einer Domäne
description: Gruppen können in einem beliebigen Container oder einer Organisationseinheit in einer Domäne und im Stammverzeichnis der Domäne abgelegt werden.
ms.assetid: 338a93dd-445d-4f74-a6d6-e5c8ba2e765e
ms.tgt_platform: multiple
keywords:
- Abfragen von Gruppen in einer Domänen-AD
- Gruppen anzeigen, Abfragen von Gruppen in einer Domäne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3abd4ec393fbeca1308ed59e08131b9b73e6b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858126"
---
# <a name="querying-for-groups-in-a-domain"></a><span data-ttu-id="c080e-105">Abfragen von Gruppen in einer Domäne</span><span class="sxs-lookup"><span data-stu-id="c080e-105">Querying for Groups in a Domain</span></span>

<span data-ttu-id="c080e-106">Gruppen können in einem beliebigen Container oder einer Organisationseinheit in einer Domäne und im Stammverzeichnis der Domäne abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c080e-106">Groups can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="c080e-107">Gruppen dürfen sich nicht immer in einem Container befinden.</span><span class="sxs-lookup"><span data-stu-id="c080e-107">Groups may not always be in one container.</span></span> <span data-ttu-id="c080e-108">Daher ist es erforderlich, die gesamte Domäne zu durchsuchen, um alle Gruppen in der Domäne zu finden.</span><span class="sxs-lookup"><span data-stu-id="c080e-108">Therefore, it is necessary to search the entire domain to find all groups in the domain.</span></span>

<span data-ttu-id="c080e-109">Wenn Sie nach allen Gruppen in einer Domäne suchen möchten, legen Sie den Ausgangspunkt für die Suche auf den Stamm der Domäne fest, legen Sie den Suchbereich auf Unterstruktur fest, und suchen Sie nach allen Objekten, die den [**objectClass**](/windows/desktop/ADSchema/a-objectclass) -Wert "Group" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c080e-109">To search for all groups in a domain, set the search start point to the root of the domain, set the search scope to subtree and search for all objects that have an [**objectClass**](/windows/desktop/ADSchema/a-objectclass) value of "group".</span></span>

<span data-ttu-id="c080e-110">Wenn Gruppen vorhanden sind, die bestimmte [**ADS- \_ \_ Gruppentyp \_**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) -Enumerationswerte enthalten, können Sie mit dem **\_ \_ \_ bitvergleichs Regel \_ -Bit und** dem passenden Regel Operator nach Gruppen suchen, für die bestimmte Bits im [**GroupType**](/windows/desktop/ADSchema/a-grouptype) -Attribut festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="c080e-110">If groups that contain particular [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) values must be found, the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator can be used to search for groups that have particular bits set in the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="c080e-111">Weitere Informationen zum Verwenden von abgleichsregeln finden Sie unter [Such Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="c080e-111">For more information about using matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="c080e-112">Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie Gruppen in einer Domäne suchen, finden Sie unter [Beispielcode für die Suche nach Gruppen in einer Domäne](example-code-for-performing-a-query-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="c080e-112">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

 

 