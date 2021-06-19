---
description: Erfahren Sie mehr über ParameterRef-Elemente im Druckschemaframework. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: ParameterRef-Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2935317bc4107e2071911ab1df826426b2bcec17
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396525"
---
# <a name="parameterref-elements"></a><span data-ttu-id="aa776-105">ParameterRef-Elemente</span><span class="sxs-lookup"><span data-stu-id="aa776-105">ParameterRef Elements</span></span>

<span data-ttu-id="aa776-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="aa776-106">This topic is not current.</span></span> <span data-ttu-id="aa776-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="aa776-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="aa776-108">ParameterRef-Elemente gelten speziell für Option-Elemente, sodass dieses Option-Element auf ein bestimmtes ParameterDef-Element verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="aa776-108">ParameterRef elements specifically apply to Option elements, allowing the ability for that Option element to refer to a particular ParameterDef element.</span></span> <span data-ttu-id="aa776-109">Für diese Option-Elemente wird ein ScoredProperty-Element, das die Option kennzeichnet, im PrintCapabilities-Dokument nicht als Wert hart codiert, sondern ist stattdessen variabel.</span><span class="sxs-lookup"><span data-stu-id="aa776-109">For these Option elements, a ScoredProperty element that characterizes the Option is not hard-coded in the PrintCapabilities document as a Value, but instead is variable.</span></span> <span data-ttu-id="aa776-110">Um diese Variabilität zu ermöglichen, enthalten diese ScoredProperty-Elemente ein ParameterRef-Element.</span><span class="sxs-lookup"><span data-stu-id="aa776-110">To enable this variability, these ScoredProperty elements contain a ParameterRef element.</span></span> <span data-ttu-id="aa776-111">Ein ScoredProperty-Element darf nicht sowohl ein Value-Element als auch ein ParameterRef-Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa776-111">A ScoredProperty element may not contain both a Value element and a ParameterRef element.</span></span> <span data-ttu-id="aa776-112">Optionselemente, die ein oder mehrere ParameterRef-Elemente enthalten, werden als parametrisierte Option-Elemente bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="aa776-112">Option elements containing one or more ParameterRef elements are called parameterized Option elements.</span></span>

<span data-ttu-id="aa776-113">Das Druckschemaframework ermöglicht es einem Option-Element, eine beliebige Anzahl von ScoredProperty-Elementen, die auf Parameter-Elemente verweisen, zusammen mit einer beliebigen Anzahl von ScoredProperty-Elementen, die Value-Elemente enthalten, zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa776-113">The Print Schema Framework allows an Option element to contain any number of ScoredProperty elements that refer to Parameter elements, together with any number of ScoredProperty elements that contain Value elements.</span></span> <span data-ttu-id="aa776-114">Das Framework lässt auch zu, dass eine beliebige Anzahl von Feature-Elementen parametrisierte Option-Elemente enthält, und eine beliebige Anzahl parametrisierter Option-Elemente ist für jedes Feature-Element zulässig.</span><span class="sxs-lookup"><span data-stu-id="aa776-114">The Framework also allows any number of Feature elements to contain parameterized Option elements, and any number of parameterized Option elements are permitted for each Feature element.</span></span> <span data-ttu-id="aa776-115">Außerdem kann auf das gleiche Parameterkonstrukt von mehreren verschiedenen Option-Elementen, Option-Elementen, die zu denselben oder verschiedenen Feature-Elementen gehören können, verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="aa776-115">Also, the same parameter construct can be referred to by several different Option elements, Option elements that can belong to the same or different Feature elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa776-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aa776-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa776-117">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="aa776-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



