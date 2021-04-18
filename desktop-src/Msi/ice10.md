---
description: ICE10 überprüft, ob der Ankündigungs Status von untergeordneten Funktionen mit dem des übergeordneten Features übereinstimmt.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac8f1304f4444a0f087d747328cdea4b3d714ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357869"
---
# <a name="ice10"></a><span data-ttu-id="f76ce-103">ICE10</span><span class="sxs-lookup"><span data-stu-id="f76ce-103">ICE10</span></span>

<span data-ttu-id="f76ce-104">ICE10 überprüft, ob der Ankündigungs Status von untergeordneten Funktionen mit dem des übergeordneten Features übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f76ce-104">ICE10 validates that the advertise state of child features matches that of its parent feature.</span></span>

<span data-ttu-id="f76ce-105">Eine untergeordnete Funktion lässt eine Ankündigung möglicherweise nicht zu, während ihre übergeordnete Funktion eine Ankündigung zulässt.</span><span class="sxs-lookup"><span data-stu-id="f76ce-105">A child feature may not disallow advertisement while its parent feature allows advertisement.</span></span> <span data-ttu-id="f76ce-106">Die folgende Kombination aus über-und untergeordneten Attributen ist daher ungültig.</span><span class="sxs-lookup"><span data-stu-id="f76ce-106">The following combination of parent and child attributes is therefore invalid.</span></span>

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

<span data-ttu-id="f76ce-107">Diese Kombination ist ungültig, da Sie das übergeordnete Element ausschalten würde, wenn das übergeordnete Element angekündigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f76ce-107">This combination is invalid because it would turn off the parent whenever the parent was supposed to be advertised.</span></span> <span data-ttu-id="f76ce-108">Der umgekehrte Wert ist jedoch zulässig.</span><span class="sxs-lookup"><span data-stu-id="f76ce-108">However, the reverse is allowed.</span></span> <span data-ttu-id="f76ce-109">Ein untergeordnetes Element kann gekennzeichnet werden, um Ankündigungen zu bevorzugen, während das übergeordnete Element als nicht zulassen gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="f76ce-109">A child can be marked to favor advertisement while the parent is marked to disallow advertisement.</span></span>

<span data-ttu-id="f76ce-110">Die benutzerdefinierte Aktion ICE10 bestimmt den Status von übergeordneten und untergeordneten Funktionen [in der Spalte](feature-table.md) Attribute der Featuretabelle.</span><span class="sxs-lookup"><span data-stu-id="f76ce-110">The ICE10 custom action determines the state of parent and child features from the Attributes column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="f76ce-111">Beachten Sie, dass es zulässig ist, den Status einer Funktion auf 0 festzulegen und das übergeordnete oder untergeordnete Element festzulegen, um Ankündigungen zu bevorzugen oder zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="f76ce-111">Note that it is valid to set the state of a feature to 0 and have its parent or child set to favor or disallow advertisement.</span></span>

## <a name="result"></a><span data-ttu-id="f76ce-112">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="f76ce-112">Result</span></span>

<span data-ttu-id="f76ce-113">ICE10 gibt einen Fehler aus, wenn die Spalte Attribute der [Merkmals](feature-table.md) Tabelle eine fehlende Übereinstimmung im Ankündigungs Status enthält.</span><span class="sxs-lookup"><span data-stu-id="f76ce-113">ICE10 posts an error if the Attributes column of the [Feature](feature-table.md) table contains a mismatch in the advertise state.</span></span>

## <a name="example"></a><span data-ttu-id="f76ce-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f76ce-114">Example</span></span>

<span data-ttu-id="f76ce-115">ICE10 gibt die folgende Fehlermeldung für das gezeigte Beispiel aus.</span><span class="sxs-lookup"><span data-stu-id="f76ce-115">ICE10 posts the following error message for the example shown.</span></span>

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

<span data-ttu-id="f76ce-116">Beachten Sie in diesem Beispiel, dass Microsoft Excel und Microsoft Word untergeordnete Funktionen von Microsoft Office sind.</span><span class="sxs-lookup"><span data-stu-id="f76ce-116">Note for this example that Microsoft Excel and Microsoft Word are child features of Microsoft Office.</span></span>

<span data-ttu-id="f76ce-117">[Funktions](feature-table.md) Tabelle (partiell)</span><span class="sxs-lookup"><span data-stu-id="f76ce-117">[Feature](feature-table.md) table (partial)</span></span>



| <span data-ttu-id="f76ce-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="f76ce-118">Feature</span></span> | <span data-ttu-id="f76ce-119">Über \_ geordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f76ce-119">Feature\_Parent</span></span> | <span data-ttu-id="f76ce-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="f76ce-120">Attributes</span></span> |
|---------|-----------------|------------|
| <span data-ttu-id="f76ce-121">Office</span><span class="sxs-lookup"><span data-stu-id="f76ce-121">Office</span></span>  | <span data-ttu-id="f76ce-122">Null</span><span class="sxs-lookup"><span data-stu-id="f76ce-122">Null</span></span>            | <span data-ttu-id="f76ce-123">4</span><span class="sxs-lookup"><span data-stu-id="f76ce-123">4</span></span>          |
| <span data-ttu-id="f76ce-124">Excel</span><span class="sxs-lookup"><span data-stu-id="f76ce-124">Excel</span></span>   | <span data-ttu-id="f76ce-125">Office</span><span class="sxs-lookup"><span data-stu-id="f76ce-125">Office</span></span>          | <span data-ttu-id="f76ce-126">4</span><span class="sxs-lookup"><span data-stu-id="f76ce-126">4</span></span>          |
| <span data-ttu-id="f76ce-127">Word</span><span class="sxs-lookup"><span data-stu-id="f76ce-127">Word</span></span>    | <span data-ttu-id="f76ce-128">Office</span><span class="sxs-lookup"><span data-stu-id="f76ce-128">Office</span></span>          | <span data-ttu-id="f76ce-129">8</span><span class="sxs-lookup"><span data-stu-id="f76ce-129">8</span></span>          |



 

<span data-ttu-id="f76ce-130">Im Beispiel wird Word so festgelegt, dass keine Ankündigung zugelassen wird. Dies steht in Konflikt mit dem Status "Ankündigung zulassen" des übergeordneten Office.</span><span class="sxs-lookup"><span data-stu-id="f76ce-130">In the example, Word is set to disallow advertisement, which conflicts with the allow advertisement state of its parent, Office.</span></span>

<span data-ttu-id="f76ce-131">In einigen Fällen gibt ICE10 den folgenden Fehler aus:</span><span class="sxs-lookup"><span data-stu-id="f76ce-131">In some cases ICE10 posts the following error:</span></span>

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

<span data-ttu-id="f76ce-132">Dies bezieht sich auf einen ungültigen Fremdschlüssel Verweis.</span><span class="sxs-lookup"><span data-stu-id="f76ce-132">This refers to an invalid foreign key reference.</span></span> <span data-ttu-id="f76ce-133">Die Korrektur besteht darin, dass ' Child ' [auf die richtige](feature-table.md) übergeordnete Funktion verweist, oder Sie fügt der Featuretabelle einen Eintrag für das übergeordnete Feature ' Parent ' hinzu.</span><span class="sxs-lookup"><span data-stu-id="f76ce-133">The fix is to have 'Child' point to its correct parent feature, or add an entry for the parent feature 'Parent' to the [Feature](feature-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f76ce-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f76ce-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f76ce-135">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="f76ce-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



