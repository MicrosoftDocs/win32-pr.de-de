---
title: Häufige Fehler (AD DS)
description: In der folgenden Tabelle finden Sie eine Liste mit häufigen Fehlern, die auf der Grundlage des Bereichs der zu Gruppier enden Gruppe auftreten können.
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- Allgemeine Fehler anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c719aad39690932de51c58d0f8081a8c855980bd
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2019
ms.locfileid: "104472180"
---
# <a name="common-errors-ad-ds"></a><span data-ttu-id="413ac-104">Häufige Fehler (AD DS)</span><span class="sxs-lookup"><span data-stu-id="413ac-104">Common Errors (AD DS)</span></span>

<span data-ttu-id="413ac-105">In der folgenden Tabelle finden Sie eine Liste mit häufigen Fehlern, die auf der Grundlage des Bereichs der zu Gruppier enden Gruppe auftreten können.</span><span class="sxs-lookup"><span data-stu-id="413ac-105">The following table contains a list of common errors that can occur based on the scope of the group being nested.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="413ac-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="413ac-106">HRESULT</span></span></th>
<th><span data-ttu-id="413ac-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="413ac-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="413ac-108">0x8007001f</span><span class="sxs-lookup"><span data-stu-id="413ac-108">0x8007001F</span></span></td>
<td><span data-ttu-id="413ac-109">Allgemeiner Fehler.</span><span class="sxs-lookup"><span data-stu-id="413ac-109">General failure.</span></span> <span data-ttu-id="413ac-110">Dieser Fehler tritt auf, wenn Sie Folgendes versuchen:</span><span class="sxs-lookup"><span data-stu-id="413ac-110">This error occurs if you attempt to:</span></span>
<ul>
<li><span data-ttu-id="413ac-111">Fügen Sie einer globalen oder universellen Gruppe oder einer lokalen Gruppe einer Domäne in einer anderen Domäne eine lokale Domänen Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="413ac-111">Add a domain local group to a global or universal group or a domain local group in another domain.</span></span> <span data-ttu-id="413ac-112">Lokale Domänen Gruppen können nur anderen lokalen Domänen Gruppen in derselben Domäne als Mitglieder hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="413ac-112">Domain local groups can only be added as members to other domain local groups in the same domain.</span></span></li>
<li><span data-ttu-id="413ac-113">Fügen Sie einer globalen Gruppe eine universelle Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="413ac-113">Add a universal group to a global group.</span></span> <span data-ttu-id="413ac-114">Universelle Gruppen können universellen und lokalen Domänen Gruppen, aber nicht globalen Gruppen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="413ac-114">Universal groups can be added to universal and domain local groups, but not global groups.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="413ac-115">0x8007202f</span><span class="sxs-lookup"><span data-stu-id="413ac-115">0x8007202F</span></span></td>
<td><span data-ttu-id="413ac-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>.</span><span class="sxs-lookup"><span data-stu-id="413ac-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>.</span></span> <span data-ttu-id="413ac-117">Dieser Fehler tritt auf, wenn Sie versuchen, einer anderen Gruppe in einer Domäne, die im gemischten Modus ausgeführt wird, eine Sicherheitsgruppe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="413ac-117">This error occurs if you attempt to add a security group to another group in a domain running in mixed mode.</span></span> <span data-ttu-id="413ac-118">Sicherheitsgruppen können nicht im gemischten Modus eingefügt werden. Sicherheitsgruppen können nur im einheitlichen Modus eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="413ac-118">Security groups cannot be nested in mixed mode; security groups can only be nested in native mode.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




