---
description: ICE28 wird häufig verwendet, um zu überprüfen, ob die ForceReboot-Aktion vor oder nach und nie innerhalb einer bestimmten Gruppe von Aktionen in den Aktions Sequenz Tabellen platziert wird. Informationen zu den Aktionen, aus denen diese Gruppe besteht, finden Sie im Thema "ForceReboot Action".
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65878bdc3db4f9b79ba95b4a170b694a4728ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750129"
---
# <a name="ice28"></a><span data-ttu-id="30335-104">ICE28</span><span class="sxs-lookup"><span data-stu-id="30335-104">ICE28</span></span>

<span data-ttu-id="30335-105">ICE28 wird häufig verwendet, um zu überprüfen, ob die ForceReboot-Aktion vor oder nach und nie innerhalb einer bestimmten Gruppe von Aktionen in den Aktions Sequenz Tabellen platziert wird.</span><span class="sxs-lookup"><span data-stu-id="30335-105">ICE28 is commonly used to validate that the ForceReboot action is placed before or after, and never within, a specific group of actions in the action sequence tables.</span></span> <span data-ttu-id="30335-106">Informationen zu den Aktionen, aus denen diese Gruppe besteht, finden Sie im Thema " [ForceReboot Action](forcereboot-action.md) ".</span><span class="sxs-lookup"><span data-stu-id="30335-106">See the [ForceReboot action](forcereboot-action.md) topic to determine the actions that comprise this group.</span></span>

<span data-ttu-id="30335-107">ICE28 überprüft Aktionen in den folgenden Sequenz Tabellen:</span><span class="sxs-lookup"><span data-stu-id="30335-107">ICE28 validates actions in the following sequence tables:</span></span>

[<span data-ttu-id="30335-108">AdminUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="30335-108">AdminUISequence table</span></span>](adminuisequence-table.md)

[<span data-ttu-id="30335-109">AdminExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="30335-109">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)

[<span data-ttu-id="30335-110">InstallUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="30335-110">InstallUISequence table</span></span>](installuisequence-table.md)

[<span data-ttu-id="30335-111">InstallExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="30335-111">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="30335-112">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="30335-112">Result</span></span>

<span data-ttu-id="30335-113">ICE28 gibt eine Fehlermeldung aus, wenn ForceReboot innerhalb der angegebenen Aktionsgruppe sequenziert wird.</span><span class="sxs-lookup"><span data-stu-id="30335-113">ICE28 posts an error message if ForceReboot is sequenced within the specified action group.</span></span>

## <a name="example"></a><span data-ttu-id="30335-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="30335-114">Example</span></span>

<span data-ttu-id="30335-115">Im gezeigten Beispiel gibt ICE28 die folgende Fehlermeldung aus:</span><span class="sxs-lookup"><span data-stu-id="30335-115">For the example shown, ICE28 posts the following error message:</span></span>

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[<span data-ttu-id="30335-116">InstallExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="30335-116">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="30335-117">Aktion</span><span class="sxs-lookup"><span data-stu-id="30335-117">Action</span></span>             | <span data-ttu-id="30335-118">Sequenz</span><span class="sxs-lookup"><span data-stu-id="30335-118">Sequence</span></span> |
|--------------------|----------|
| <span data-ttu-id="30335-119">ForceReboot</span><span class="sxs-lookup"><span data-stu-id="30335-119">ForceReboot</span></span>        | <span data-ttu-id="30335-120">10</span><span class="sxs-lookup"><span data-stu-id="30335-120">10</span></span>       |
| <span data-ttu-id="30335-121">Registermimeinfo</span><span class="sxs-lookup"><span data-stu-id="30335-121">RegisterMIMEInfo</span></span>   |   <span data-ttu-id="30335-122">5</span><span class="sxs-lookup"><span data-stu-id="30335-122">5</span></span>      |
| <span data-ttu-id="30335-123">Registerprogidinfo</span><span class="sxs-lookup"><span data-stu-id="30335-123">RegisterProgIdInfo</span></span> | <span data-ttu-id="30335-124">15</span><span class="sxs-lookup"><span data-stu-id="30335-124">15</span></span>       |



 

<span data-ttu-id="30335-125">Die Sequenznummer 10, die für ForceReboot-Unterbrechungen angegeben wird, generiert den Fehler, da Sie zwischen den Sequenznummern von registermimeinfo und registerprogidinfo liegt.</span><span class="sxs-lookup"><span data-stu-id="30335-125">The sequence number of 10 given to ForceReboot breaks generates the error, because it comes between the sequence numbers of RegisterMIMEInfo and RegisterProgIdInfo.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30335-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="30335-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30335-127">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="30335-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



