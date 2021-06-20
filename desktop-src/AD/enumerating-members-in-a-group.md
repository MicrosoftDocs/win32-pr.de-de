---
title: Aufzählen von Mitgliedern in einer Gruppe
description: Erfahren Sie mehr über das Aufzählen von Mitgliedern in einer Azure Active Directory-Gruppe. Die Mitglieder einer Gruppe werden in einem Mehrwertattribut namens member gespeichert.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Aufzählen von Mitgliedern in einer Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916b988cd26ee4df59eaf27cc5ffd690bca1458a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407423"
---
# <a name="enumerating-members-in-a-group"></a><span data-ttu-id="54eaf-105">Aufzählen von Mitgliedern in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="54eaf-105">Enumerating Members in a Group</span></span>

<span data-ttu-id="54eaf-106">Die Mitglieder einer Gruppe werden in einem Mehrwertattribut gespeichert, das als **Member** bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="54eaf-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="54eaf-107">Verwenden Sie für Gruppen mit einer kleinen bis mittleren Mitgliedschaft die [**IADsGroup.Members-Methode,**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) um einen Zeiger auf ein [**IADsMembers-Objekt**](/windows/desktop/api/iads/nn-iads-iadsmembers) abzurufen, das die Liste aller Member enthält.</span><span class="sxs-lookup"><span data-stu-id="54eaf-107">For groups with a small to medium-sized membership, use the [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) method to get a pointer to an [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) object that contains the list of all members.</span></span> <span data-ttu-id="54eaf-108">Verwenden Sie dann [**IADsMembers::get \_ \_ NewEnum,**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) um ein Enumeratorobjekt abzurufen, das Sie zum Aufzählen der Member verwenden können.</span><span class="sxs-lookup"><span data-stu-id="54eaf-108">Then use the [**IADsMembers::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) to get an enumerator object that you can use to enumerate the members.</span></span>

<span data-ttu-id="54eaf-109">Wenn die erwartete Gruppenmitgliedschaft 1.000 oder mehr Mitglieder umfasst, verwenden Sie "ranging", um benutzer einen Bereich nach dem anderen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="54eaf-109">If the anticipated group membership will be 1000 or more members, use ranging to retrieve users one range at a time.</span></span> <span data-ttu-id="54eaf-110">Weitere Informationen zur Verwendung von zum Aufzählen von Membern im Bereich finden Sie unter [Aufzählen von Gruppen, die viele Elemente enthalten.](enumerating-groups-that-contain-many-members.md)</span><span class="sxs-lookup"><span data-stu-id="54eaf-110">For more information about using ranging to enumerate members, see [Enumerating Groups That Contain Many Members](enumerating-groups-that-contain-many-members.md).</span></span>

 

 