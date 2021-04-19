---
description: ICE22 verwendet die FeatureComponents-Tabelle, um die Zuordnung von Features und Komponenten zu überprüfen, auf die in der PublishComponent-Tabelle verwiesen wird.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26574b11f9d908026d901a74632766998246d31a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347662"
---
# <a name="ice22"></a><span data-ttu-id="52124-103">ICE22</span><span class="sxs-lookup"><span data-stu-id="52124-103">ICE22</span></span>

<span data-ttu-id="52124-104">ICE22 verwendet die [FeatureComponents-Tabelle](featurecomponents-table.md) , um die Zuordnung von Features und Komponenten zu überprüfen, auf die in der [PublishComponent-Tabelle](publishcomponent-table.md)verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="52124-104">ICE22 uses the [FeatureComponents table](featurecomponents-table.md) to validate the mapping of features and components referenced in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="52124-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="52124-105">Result</span></span>

<span data-ttu-id="52124-106">ICE22 gibt eine Fehlermeldung aus, wenn die Features und Komponenten in der [Tabelle PublishComponent](publishcomponent-table.md)nicht ordnungsgemäß zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="52124-106">ICE22 posts an error message if the features and components are mapped incorrectly in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="52124-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="52124-107">Example</span></span>

<span data-ttu-id="52124-108">Im folgenden Beispiel gibt ICE22 einen Fehler aus, {00000003-0004-0000-0000-624474732465} der nicht über die richtige Zuordnung für die Funktion \_ und die Komponenten \_ Spalten verfügt.</span><span class="sxs-lookup"><span data-stu-id="52124-108">For the following example ICE22 posts an error that {00000003-0004-0000-0000-624474732465} does not have the correct mapping for the Feature\_ and Component\_ columns.</span></span>

<span data-ttu-id="52124-109">[PublishComponent-Tabelle](publishcomponent-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="52124-109">[PublishComponent Table](publishcomponent-table.md) (partial)</span></span>



| <span data-ttu-id="52124-110">ComponentID</span><span class="sxs-lookup"><span data-stu-id="52124-110">ComponentId</span></span>                            | <span data-ttu-id="52124-111">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="52124-111">Feature\_</span></span> | <span data-ttu-id="52124-112">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="52124-112">Component\_</span></span> |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="52124-113">Feat1</span><span class="sxs-lookup"><span data-stu-id="52124-113">Feat1</span></span>     | <span data-ttu-id="52124-114">Comp1</span><span class="sxs-lookup"><span data-stu-id="52124-114">Comp1</span></span>       |
| {00000003-0004-0000-0000-624474732465} | <span data-ttu-id="52124-115">Feat1</span><span class="sxs-lookup"><span data-stu-id="52124-115">Feat1</span></span>     | <span data-ttu-id="52124-116">Comp2</span><span class="sxs-lookup"><span data-stu-id="52124-116">Comp2</span></span>       |



 

<span data-ttu-id="52124-117">[FeatureComponents-Tabelle](featurecomponents-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="52124-117">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="52124-118">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="52124-118">Feature\_</span></span> | <span data-ttu-id="52124-119">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="52124-119">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="52124-120">Feat1</span><span class="sxs-lookup"><span data-stu-id="52124-120">Feat1</span></span>     | <span data-ttu-id="52124-121">Comp1</span><span class="sxs-lookup"><span data-stu-id="52124-121">Comp1</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="52124-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52124-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52124-123">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="52124-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



