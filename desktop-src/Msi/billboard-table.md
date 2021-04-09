---
description: In der Tabelle "Billboard" sind die in der vollständigen Benutzeroberfläche angezeigten Karten Steuerelemente aufgeführt.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Tabelle "Billboard"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959504"
---
# <a name="billboard-table"></a><span data-ttu-id="d4788-103">Tabelle "Billboard"</span><span class="sxs-lookup"><span data-stu-id="d4788-103">Billboard Table</span></span>

<span data-ttu-id="d4788-104">In der Tabelle "Billboard" sind die in der vollständigen Benutzeroberfläche angezeigten Karten Steuer [Elemente](billboard-control.md) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4788-104">The Billboard table lists the [Billboard controls](billboard-control.md) displayed in the full user interface.</span></span>

<span data-ttu-id="d4788-105">Die Tabelle "Billboard" weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="d4788-105">The Billboard table has the following columns.</span></span>



| <span data-ttu-id="d4788-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="d4788-106">Column</span></span>    | <span data-ttu-id="d4788-107">Typ</span><span class="sxs-lookup"><span data-stu-id="d4788-107">Type</span></span>                         | <span data-ttu-id="d4788-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d4788-108">Key</span></span> | <span data-ttu-id="d4788-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="d4788-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="d4788-110">Billboard</span><span class="sxs-lookup"><span data-stu-id="d4788-110">Billboard</span></span> | [<span data-ttu-id="d4788-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d4788-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="d4788-112">J</span><span class="sxs-lookup"><span data-stu-id="d4788-112">Y</span></span>   | <span data-ttu-id="d4788-113">N</span><span class="sxs-lookup"><span data-stu-id="d4788-113">N</span></span>        |
| <span data-ttu-id="d4788-114">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="d4788-114">Feature\_</span></span> | [<span data-ttu-id="d4788-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d4788-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="d4788-116">N</span><span class="sxs-lookup"><span data-stu-id="d4788-116">N</span></span>   | <span data-ttu-id="d4788-117">N</span><span class="sxs-lookup"><span data-stu-id="d4788-117">N</span></span>        |
| <span data-ttu-id="d4788-118">Aktion</span><span class="sxs-lookup"><span data-stu-id="d4788-118">Action</span></span>    | [<span data-ttu-id="d4788-119">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d4788-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="d4788-120">N</span><span class="sxs-lookup"><span data-stu-id="d4788-120">N</span></span>   | <span data-ttu-id="d4788-121">J</span><span class="sxs-lookup"><span data-stu-id="d4788-121">Y</span></span>        |
| <span data-ttu-id="d4788-122">Sortieren</span><span class="sxs-lookup"><span data-stu-id="d4788-122">Ordering</span></span>  | [<span data-ttu-id="d4788-123">Integer</span><span class="sxs-lookup"><span data-stu-id="d4788-123">Integer</span></span>](integer.md)       | <span data-ttu-id="d4788-124">N</span><span class="sxs-lookup"><span data-stu-id="d4788-124">N</span></span>   | <span data-ttu-id="d4788-125">J</span><span class="sxs-lookup"><span data-stu-id="d4788-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d4788-126">Spalten</span><span class="sxs-lookup"><span data-stu-id="d4788-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d4788-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Billboard</span><span class="sxs-lookup"><span data-stu-id="d4788-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Billboard</span></span>
</dt> <dd>

<span data-ttu-id="d4788-128">Der Name des [Billboard-Steuer](billboard-control.md)Elements.</span><span class="sxs-lookup"><span data-stu-id="d4788-128">Name of the [Billboard control](billboard-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4788-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_</span><span class="sxs-lookup"><span data-stu-id="d4788-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="d4788-130">Ein externer Schlüssel für die erste Spalte der [Merkmals Tabelle](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="d4788-130">An external key to the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="d4788-131">Das Billboard wird nur angezeigt, wenn dieses Feature installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d4788-131">The billboard is displayed only if this feature is being installed.</span></span>

</dd> <dt>

<span data-ttu-id="d4788-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel</span><span class="sxs-lookup"><span data-stu-id="d4788-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="d4788-133">Der Name einer Aktion.</span><span class="sxs-lookup"><span data-stu-id="d4788-133">The name of an action.</span></span> <span data-ttu-id="d4788-134">Das Billboard wird während der von dieser Aktion empfangenen Fortschrittsmeldungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d4788-134">The billboard is displayed during the progress messages received from this action.</span></span>

</dd> <dt>

<span data-ttu-id="d4788-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Stelle</span><span class="sxs-lookup"><span data-stu-id="d4788-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="d4788-136">Wenn mehr als ein Billboard einer Aktion entspricht, werden diese in der von dieser Spalte definierten Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d4788-136">If there is more than one billboard corresponding to an action, then they are displayed in the order defined by this column.</span></span> <span data-ttu-id="d4788-137">Diese Zahl darf nicht negativ sein.</span><span class="sxs-lookup"><span data-stu-id="d4788-137">This number must be non-negative.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="d4788-138">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="d4788-138">Validation</span></span>

<dl>

[<span data-ttu-id="d4788-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="d4788-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d4788-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="d4788-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d4788-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="d4788-141">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d4788-142">ICE95</span><span class="sxs-lookup"><span data-stu-id="d4788-142">ICE95</span></span>](ice95.md)  
</dl>

 

 



