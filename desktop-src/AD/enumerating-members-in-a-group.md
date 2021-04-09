---
title: Auflisten von Membern in einer Gruppe
description: Die Mitglieder einer Gruppe werden in einem mehrwertigen Attribut mit dem Namen "Member" gespeichert.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Auflisten von Membern in einer Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2d051999bf8efeadb0c5a8899b31f813b8bf42
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101451"
---
# <a name="enumerating-members-in-a-group"></a><span data-ttu-id="5ed2e-104">Auflisten von Membern in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="5ed2e-104">Enumerating Members in a Group</span></span>

<span data-ttu-id="5ed2e-105">Die Mitglieder einer Gruppe werden in einem mehrwertigen Attribut mit dem Namen " **Member**" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5ed2e-105">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="5ed2e-106">Verwenden Sie für Gruppen mit einer kleinen bis mittelgroßen Mitgliedschaft die [**IADsGroup. Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) -Methode, um einen Zeiger auf ein [**iadsmembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) -Objekt zu erhalten, das die Liste aller Member enthält.</span><span class="sxs-lookup"><span data-stu-id="5ed2e-106">For groups with a small to medium-sized membership, use the [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) method to get a pointer to an [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) object that contains the list of all members.</span></span> <span data-ttu-id="5ed2e-107">Verwenden Sie dann [**iadsmembers:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) ein Enumeratorobjekt, das Sie zum Auflisten der Elemente verwenden können.</span><span class="sxs-lookup"><span data-stu-id="5ed2e-107">Then use the [**IADsMembers::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) to get an enumerator object that you can use to enumerate the members.</span></span>

<span data-ttu-id="5ed2e-108">Wenn die erwartete Gruppenmitgliedschaft 1000 oder mehr Mitglieder sein wird, verwenden Sie den Bereich, um Benutzer jeweils einen Bereich abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5ed2e-108">If the anticipated group membership will be 1000 or more members, use ranging to retrieve users one range at a time.</span></span> <span data-ttu-id="5ed2e-109">Weitere Informationen zum Verwenden von Bereichen zum Auflisten von Membern finden Sie unter Auflisten von [Gruppen, die viele Member enthalten](enumerating-groups-that-contain-many-members.md).</span><span class="sxs-lookup"><span data-stu-id="5ed2e-109">For more information about using ranging to enumerate members, see [Enumerating Groups That Contain Many Members](enumerating-groups-that-contain-many-members.md).</span></span>

 

 