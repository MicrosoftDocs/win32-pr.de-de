---
description: ICE72 überprüft, ob nicht integrierte benutzerdefinierte Aktionen in der AdvtExecuteSequence-Tabelle nicht verwendet werden.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d8e1859ffd8123cc7aa3dc801c5484d28ccb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368978"
---
# <a name="ice72"></a><span data-ttu-id="33464-103">ICE72</span><span class="sxs-lookup"><span data-stu-id="33464-103">ICE72</span></span>

<span data-ttu-id="33464-104">ICE72 überprüft, ob nicht integrierte benutzerdefinierte Aktionen in der [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33464-104">ICE72 verifies that non-built-in custom actions are not used in the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span> <span data-ttu-id="33464-105">Insbesondere sind in der AdvtExecuteSequence-Tabelle nur benutzerdefinierte Aktionen vom Typ 19, Typ 35 und Type 51 zulässig.</span><span class="sxs-lookup"><span data-stu-id="33464-105">Specifically, only type 19, type 35, and type 51 custom actions are allowed in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="33464-106">Wenn andere benutzerdefinierte Aktionen verwendet werden, verhält sich die Ankündigung möglicherweise nicht wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="33464-106">If other custom actions are used, advertisement may not behave as expected.</span></span>

## <a name="result"></a><span data-ttu-id="33464-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="33464-107">Result</span></span>

<span data-ttu-id="33464-108">ICE72 gibt einen Fehler zurück, wenn die advexecutesequence-Tabelle andere benutzerdefinierte Aktionen als den Typ 35, den Typ 51 und den Typ 19 verwendet.</span><span class="sxs-lookup"><span data-stu-id="33464-108">ICE72 returns an error if the AdvExecuteSequence table uses custom actions other than type 35, type 51, and type 19.</span></span>

## <a name="example"></a><span data-ttu-id="33464-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="33464-109">Example</span></span>

<span data-ttu-id="33464-110">ICE72 meldet den folgenden Fehler für das gezeigte Beispiel:</span><span class="sxs-lookup"><span data-stu-id="33464-110">ICE72 reports the following error for the example shown:</span></span>

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

<span data-ttu-id="33464-111">Entfernen Sie "CA1" aus der AdvtExecuteSequence-Tabelle, um den Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="33464-111">To fix the error, remove 'CA1' from the AdvtExecuteSequence table.</span></span>

<span data-ttu-id="33464-112">[AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="33464-112">[AdvtExecuteSequence Table](advtexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="33464-113">Aktion</span><span class="sxs-lookup"><span data-stu-id="33464-113">Action</span></span> |
|--------|
| <span data-ttu-id="33464-114">KA1</span><span class="sxs-lookup"><span data-stu-id="33464-114">CA1</span></span>    |
| <span data-ttu-id="33464-115">CA35</span><span class="sxs-lookup"><span data-stu-id="33464-115">CA35</span></span>   |



 

<span data-ttu-id="33464-116">[CustomAction-Tabelle](customaction-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="33464-116">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="33464-117">Aktion</span><span class="sxs-lookup"><span data-stu-id="33464-117">Action</span></span> | <span data-ttu-id="33464-118">type</span><span class="sxs-lookup"><span data-stu-id="33464-118">Type</span></span> |
|--------|------|
| <span data-ttu-id="33464-119">KA1</span><span class="sxs-lookup"><span data-stu-id="33464-119">CA1</span></span>    | <span data-ttu-id="33464-120">1</span><span class="sxs-lookup"><span data-stu-id="33464-120">1</span></span>    |
| <span data-ttu-id="33464-121">CA35</span><span class="sxs-lookup"><span data-stu-id="33464-121">CA35</span></span>   | <span data-ttu-id="33464-122">35</span><span class="sxs-lookup"><span data-stu-id="33464-122">35</span></span>   |



 

## <a name="tables-used-during-execution"></a><span data-ttu-id="33464-123">Während der Ausführung verwendete Tabellen</span><span class="sxs-lookup"><span data-stu-id="33464-123">Tables used during execution</span></span>

[<span data-ttu-id="33464-124">AdvtExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="33464-124">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)

[<span data-ttu-id="33464-125">Tabelle "CustomAction"</span><span class="sxs-lookup"><span data-stu-id="33464-125">CustomAction Table</span></span>](customaction-table.md)

## <a name="related-topics"></a><span data-ttu-id="33464-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33464-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33464-127">Benutzerdefinierter Aktionstyp 19</span><span class="sxs-lookup"><span data-stu-id="33464-127">Custom Action Type 19</span></span>](custom-action-type-19.md)
</dt> <dt>

[<span data-ttu-id="33464-128">Benutzerdefinierter Aktionstyp 35</span><span class="sxs-lookup"><span data-stu-id="33464-128">Custom Action Type 35</span></span>](custom-action-type-35.md)
</dt> <dt>

[<span data-ttu-id="33464-129">Benutzerdefinierter Aktionstyp 51</span><span class="sxs-lookup"><span data-stu-id="33464-129">Custom Action Type 51</span></span>](custom-action-type-51.md)
</dt> <dt>

[<span data-ttu-id="33464-130">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="33464-130">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



