---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: ParameterRef-Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c0e145e99b1ee705d63449cf693c6fc87f6463
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104050732"
---
# <a name="parameterref-elements"></a><span data-ttu-id="086ff-104">ParameterRef-Elemente</span><span class="sxs-lookup"><span data-stu-id="086ff-104">ParameterRef Elements</span></span>

<span data-ttu-id="086ff-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="086ff-105">This topic is not current.</span></span> <span data-ttu-id="086ff-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="086ff-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="086ff-107">ParameterRef-Elemente gelten speziell für options Elemente, sodass das Option-Element auf ein bestimmtes ParameterDef-Element verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="086ff-107">ParameterRef elements specifically apply to Option elements, allowing the ability for that Option element to refer to a particular ParameterDef element.</span></span> <span data-ttu-id="086ff-108">Für diese Options Elemente ist ein ScoredProperty-Element, das die Option kennzeichnet, im printfunktionalitäten-Dokument nicht als Wert hart codiert, sondern ist eine Variable.</span><span class="sxs-lookup"><span data-stu-id="086ff-108">For these Option elements, a ScoredProperty element that characterizes the Option is not hard-coded in the PrintCapabilities document as a Value, but instead is variable.</span></span> <span data-ttu-id="086ff-109">Diese ScoredProperty-Elemente enthalten ein ParameterRef-Element, um diese Variabilität zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="086ff-109">To enable this variability, these ScoredProperty elements contain a ParameterRef element.</span></span> <span data-ttu-id="086ff-110">Ein ScoredProperty-Element darf nicht sowohl ein Value-Element als auch ein ParameterRef-Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="086ff-110">A ScoredProperty element may not contain both a Value element and a ParameterRef element.</span></span> <span data-ttu-id="086ff-111">Options Elemente, die ein oder mehrere ParameterRef-Elemente enthalten, werden als parametrisierte Options Elemente bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="086ff-111">Option elements containing one or more ParameterRef elements are called parameterized Option elements.</span></span>

<span data-ttu-id="086ff-112">Das Print Schema-Framework ermöglicht, dass ein Option-Element eine beliebige Anzahl von ScoredProperty-Elementen enthält, die auf Parameter Elemente verweisen, sowie eine beliebige Anzahl von ScoredProperty-Elementen, die value-Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="086ff-112">The Print Schema Framework allows an Option element to contain any number of ScoredProperty elements that refer to Parameter elements, together with any number of ScoredProperty elements that contain Value elements.</span></span> <span data-ttu-id="086ff-113">Das Framework ermöglicht außerdem, dass eine beliebige Anzahl von Featureelementen parametrisierte Options Elemente enthalten kann, und jede beliebige Anzahl von parametrisierten Options Elementen ist für jedes Feature-Element zulässig.</span><span class="sxs-lookup"><span data-stu-id="086ff-113">The Framework also allows any number of Feature elements to contain parameterized Option elements, and any number of parameterized Option elements are permitted for each Feature element.</span></span> <span data-ttu-id="086ff-114">Außerdem kann auf dasselbe Parameter Konstrukt durch mehrere unterschiedliche Options Elemente verwiesen werden, Options Elemente, die zu denselben oder unterschiedlichen Funktions Elementen gehören können.</span><span class="sxs-lookup"><span data-stu-id="086ff-114">Also, the same parameter construct can be referred to by several different Option elements, Option elements that can belong to the same or different Feature elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="086ff-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="086ff-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="086ff-116">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="086ff-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



