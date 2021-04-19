---
description: ICE21 überprüft, ob jede Komponente in der Komponenten Tabelle zu einer Funktion gehört. Er verwendet die FeatureComponents-Tabelle, um diese Zuordnung zu überprüfen.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c457d026b3dc57a718eabea704254a3448a3de26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348107"
---
# <a name="ice21"></a><span data-ttu-id="f55e7-104">ICE21</span><span class="sxs-lookup"><span data-stu-id="f55e7-104">ICE21</span></span>

<span data-ttu-id="f55e7-105">ICE21 überprüft, ob jede Komponente in der [Komponenten Tabelle](component-table.md) zu einer Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="f55e7-105">ICE21 validates that every component in the [Component table](component-table.md) belongs to a feature.</span></span> <span data-ttu-id="f55e7-106">Er verwendet die [FeatureComponents-Tabelle](featurecomponents-table.md) , um diese Zuordnung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f55e7-106">It uses the [FeatureComponents table](featurecomponents-table.md) to check for this mapping.</span></span>

## <a name="result"></a><span data-ttu-id="f55e7-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="f55e7-107">Result</span></span>

<span data-ttu-id="f55e7-108">ICE21 gibt eine Fehlermeldung aus, wenn das Installationspaket eine Komponente enthält, die nicht zu einer Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="f55e7-108">ICE21 posts an error message if the installation package contains a component that does not belong to a feature.</span></span>

## <a name="example"></a><span data-ttu-id="f55e7-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f55e7-109">Example</span></span>

<span data-ttu-id="f55e7-110">Im folgenden Beispiel gibt ICE21 eine Fehlermeldung aus, die besagt, dass die Komponente Comp1 keiner Funktion zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f55e7-110">For the following example, ICE21 posts an error message stating that the component Comp1 does not map to any feature.</span></span>

<span data-ttu-id="f55e7-111">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="f55e7-111">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="f55e7-112">Komponente</span><span class="sxs-lookup"><span data-stu-id="f55e7-112">Component</span></span> |
|-----------|
| <span data-ttu-id="f55e7-113">Comp1</span><span class="sxs-lookup"><span data-stu-id="f55e7-113">Comp1</span></span>     |
| <span data-ttu-id="f55e7-114">Comp2</span><span class="sxs-lookup"><span data-stu-id="f55e7-114">Comp2</span></span>     |



 

<span data-ttu-id="f55e7-115">[FeatureComponents-Tabelle](featurecomponents-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="f55e7-115">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="f55e7-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="f55e7-116">Feature</span></span>  | <span data-ttu-id="f55e7-117">Komponente</span><span class="sxs-lookup"><span data-stu-id="f55e7-117">Component</span></span> |
|----------|-----------|
| <span data-ttu-id="f55e7-118">Feature1</span><span class="sxs-lookup"><span data-stu-id="f55e7-118">Feature1</span></span> | <span data-ttu-id="f55e7-119">Comp2</span><span class="sxs-lookup"><span data-stu-id="f55e7-119">Comp2</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="f55e7-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f55e7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f55e7-121">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="f55e7-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



