---
description: Die LaunchCondition-Tabelle wird von der LaunchConditions-Aktion verwendet. Es enthält eine Liste der Bedingungen, die alle für den Beginn der Installation erfüllt sein müssen.
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: LaunchCondition-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343307"
---
# <a name="launchcondition-table"></a><span data-ttu-id="bee86-104">LaunchCondition-Tabelle</span><span class="sxs-lookup"><span data-stu-id="bee86-104">LaunchCondition Table</span></span>

<span data-ttu-id="bee86-105">Die LaunchCondition-Tabelle wird von der [LaunchConditions-Aktion](launchconditions-action.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="bee86-105">The LaunchCondition table is used by the [LaunchConditions action](launchconditions-action.md).</span></span> <span data-ttu-id="bee86-106">Es enthält eine Liste der Bedingungen, die alle für den Beginn der Installation erfüllt sein müssen.</span><span class="sxs-lookup"><span data-stu-id="bee86-106">It contains a list of conditions that all must be satisfied for the installation to begin.</span></span>

<span data-ttu-id="bee86-107">Die LaunchCondition-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="bee86-107">The LaunchCondition table has the following columns.</span></span>



| <span data-ttu-id="bee86-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="bee86-108">Column</span></span>      | <span data-ttu-id="bee86-109">Typ</span><span class="sxs-lookup"><span data-stu-id="bee86-109">Type</span></span>                       | <span data-ttu-id="bee86-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="bee86-110">Key</span></span> | <span data-ttu-id="bee86-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="bee86-111">Nullable</span></span> |
|-------------|----------------------------|-----|----------|
| <span data-ttu-id="bee86-112">Bedingung</span><span class="sxs-lookup"><span data-stu-id="bee86-112">Condition</span></span>   | [<span data-ttu-id="bee86-113">Condition</span><span class="sxs-lookup"><span data-stu-id="bee86-113">Condition</span></span>](condition.md) | <span data-ttu-id="bee86-114">J</span><span class="sxs-lookup"><span data-stu-id="bee86-114">Y</span></span>   | <span data-ttu-id="bee86-115">N</span><span class="sxs-lookup"><span data-stu-id="bee86-115">N</span></span>        |
| <span data-ttu-id="bee86-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bee86-116">Description</span></span> | [<span data-ttu-id="bee86-117">Großformatige</span><span class="sxs-lookup"><span data-stu-id="bee86-117">Formatted</span></span>](formatted.md) | <span data-ttu-id="bee86-118">N</span><span class="sxs-lookup"><span data-stu-id="bee86-118">N</span></span>   | <span data-ttu-id="bee86-119">N</span><span class="sxs-lookup"><span data-stu-id="bee86-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="bee86-120">Spalten</span><span class="sxs-lookup"><span data-stu-id="bee86-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="bee86-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage</span><span class="sxs-lookup"><span data-stu-id="bee86-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="bee86-122">Ausdruck, der als true ausgewertet werden muss, damit die Installation beginnt.</span><span class="sxs-lookup"><span data-stu-id="bee86-122">Expression that must evaluate to True for installation to begin.</span></span>

</dd> <dt>

<span data-ttu-id="bee86-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bee86-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="bee86-124">Lokalisier barer Text, der angezeigt wird, wenn die Bedingung fehlschlägt und die Installation beendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="bee86-124">Localizable text to display when the condition fails and the installation must be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bee86-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bee86-125">Remarks</span></span>

<span data-ttu-id="bee86-126">Sie können die Reihenfolge, in der die Startbedingungen ausgewertet werden, nicht garantieren, indem Sie diese Tabelle erstellen.</span><span class="sxs-lookup"><span data-stu-id="bee86-126">You cannot guarantee the order in which the launch conditions are evaluated by authoring this table.</span></span> <span data-ttu-id="bee86-127">Wenn es erforderlich ist, die Reihenfolge zu steuern, in der die Bedingungen ausgewertet werden, sollten Sie hierfür benutzerdefinierte Aktionen vom Typ 19 benutzerdefinierte Aktionen in der Installation verwenden.</span><span class="sxs-lookup"><span data-stu-id="bee86-127">If it is necessary to control the order in which conditions are evaluated, you should do this by using Custom Action Type 19 custom actions in your installation.</span></span>

## <a name="validation"></a><span data-ttu-id="bee86-128">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="bee86-128">Validation</span></span>

<dl>

[<span data-ttu-id="bee86-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="bee86-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="bee86-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="bee86-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="bee86-131">ICE46</span><span class="sxs-lookup"><span data-stu-id="bee86-131">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="bee86-132">ICE79</span><span class="sxs-lookup"><span data-stu-id="bee86-132">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="bee86-133">ICE86</span><span class="sxs-lookup"><span data-stu-id="bee86-133">ICE86</span></span>](ice86.md)  
</dl>

 

 



