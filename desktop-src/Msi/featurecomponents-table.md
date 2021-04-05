---
description: Die FeatureComponents-Tabelle definiert die Beziehung zwischen Features und Komponenten. Für jede Funktion werden in dieser Tabelle alle Komponenten aufgelistet, aus denen diese Funktion besteht.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: FeatureComponents-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c93a7c020f179843916b063b48e2e4d19f7bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754225"
---
# <a name="featurecomponents-table"></a><span data-ttu-id="886e3-104">FeatureComponents-Tabelle</span><span class="sxs-lookup"><span data-stu-id="886e3-104">FeatureComponents Table</span></span>

<span data-ttu-id="886e3-105">Die FeatureComponents-Tabelle definiert die Beziehung zwischen Features und Komponenten.</span><span class="sxs-lookup"><span data-stu-id="886e3-105">The FeatureComponents table defines the relationship between features and components.</span></span> <span data-ttu-id="886e3-106">Für jede Funktion werden in dieser Tabelle alle Komponenten aufgelistet, aus denen diese Funktion besteht.</span><span class="sxs-lookup"><span data-stu-id="886e3-106">For each feature, this table lists all the components that make up that feature.</span></span>

<span data-ttu-id="886e3-107">Die FeatureComponents-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="886e3-107">The FeatureComponents table has the following columns.</span></span>



| <span data-ttu-id="886e3-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="886e3-108">Column</span></span>      | <span data-ttu-id="886e3-109">Typ</span><span class="sxs-lookup"><span data-stu-id="886e3-109">Type</span></span>                         | <span data-ttu-id="886e3-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="886e3-110">Key</span></span> | <span data-ttu-id="886e3-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="886e3-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="886e3-112">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="886e3-112">Feature\_</span></span>   | [<span data-ttu-id="886e3-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="886e3-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="886e3-114">J</span><span class="sxs-lookup"><span data-stu-id="886e3-114">Y</span></span>   | <span data-ttu-id="886e3-115">N</span><span class="sxs-lookup"><span data-stu-id="886e3-115">N</span></span>        |
| <span data-ttu-id="886e3-116">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="886e3-116">Component\_</span></span> | [<span data-ttu-id="886e3-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="886e3-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="886e3-118">J</span><span class="sxs-lookup"><span data-stu-id="886e3-118">Y</span></span>   | <span data-ttu-id="886e3-119">N</span><span class="sxs-lookup"><span data-stu-id="886e3-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="886e3-120">Spalten</span><span class="sxs-lookup"><span data-stu-id="886e3-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="886e3-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_</span><span class="sxs-lookup"><span data-stu-id="886e3-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="886e3-122">Ein externer Schlüssel in die erste Spalte der Funktions [Tabelle](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="886e3-122">An external key into the first column of the Feature [table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e3-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="886e3-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="886e3-124">Ein externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="886e3-124">An external key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="886e3-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="886e3-125">Remarks</span></span>

<span data-ttu-id="886e3-126">Es gibt eine Obergrenze von 1600 Komponenten pro Feature.</span><span class="sxs-lookup"><span data-stu-id="886e3-126">There is a maximum limit of 1600 components per feature.</span></span>

<span data-ttu-id="886e3-127">Komponenten können von zwei oder mehr Features gemeinsam genutzt werden, d. h., auf dieselbe Komponente kann von mehreren Features verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="886e3-127">Components can be shared by two or more features, that is, the same component can be referred to by more than one feature.</span></span>

<span data-ttu-id="886e3-128">Auf diese Tabelle wird verwiesen, wenn die [publishfeatures-Aktion](publishfeatures-action.md) oder die [unpublishfeatures-Aktion](unpublishfeatures-action.md) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="886e3-128">This table is referred to when the [PublishFeatures action](publishfeatures-action.md) or the [UnpublishFeatures action](unpublishfeatures-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="886e3-129">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="886e3-129">Validation</span></span>

<dl>

[<span data-ttu-id="886e3-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="886e3-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="886e3-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="886e3-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="886e3-132">ICE21</span><span class="sxs-lookup"><span data-stu-id="886e3-132">ICE21</span></span>](ice21.md)  
[<span data-ttu-id="886e3-133">ICE22</span><span class="sxs-lookup"><span data-stu-id="886e3-133">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="886e3-134">ICE32</span><span class="sxs-lookup"><span data-stu-id="886e3-134">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="886e3-135">ICE41</span><span class="sxs-lookup"><span data-stu-id="886e3-135">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="886e3-136">ICE47</span><span class="sxs-lookup"><span data-stu-id="886e3-136">ICE47</span></span>](ice47.md)  
[<span data-ttu-id="886e3-137">ICE59</span><span class="sxs-lookup"><span data-stu-id="886e3-137">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="886e3-138">ICE62</span><span class="sxs-lookup"><span data-stu-id="886e3-138">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="886e3-139">ICE69</span><span class="sxs-lookup"><span data-stu-id="886e3-139">ICE69</span></span>](ice69.md)  
</dl>

 

 



