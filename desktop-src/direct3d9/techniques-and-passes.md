---
description: Techniken stellen den renderingmuskel bereit. Eine Technik kapselt den Effekt Zustand, der einen Renderingstil bestimmt. Eine Technik besteht aus einem oder mehreren Durchläufen.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Techniken und Pässe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345602"
---
# <a name="techniques-and-passes-direct3d-9"></a><span data-ttu-id="7483e-105">Techniken und Pässe (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7483e-105">Techniques and Passes (Direct3D 9)</span></span>

<span data-ttu-id="7483e-106">Techniken stellen den renderingmuskel bereit.</span><span class="sxs-lookup"><span data-stu-id="7483e-106">Techniques provide the rendering muscle.</span></span> <span data-ttu-id="7483e-107">Eine Technik kapselt den Effekt Zustand, der einen Renderingstil bestimmt.</span><span class="sxs-lookup"><span data-stu-id="7483e-107">A technique encapsulates the effect state that determines a rendering style.</span></span> <span data-ttu-id="7483e-108">Eine Technik besteht aus einem oder mehreren Durchläufen.</span><span class="sxs-lookup"><span data-stu-id="7483e-108">A technique is made up of one or more passes.</span></span>

## <a name="techniques"></a><span data-ttu-id="7483e-109">O</span><span class="sxs-lookup"><span data-stu-id="7483e-109">Techniques</span></span>

<span data-ttu-id="7483e-110">Die Syntax zum Aufrufen einer Technik lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7483e-110">The syntax for calling a technique is as follows:</span></span>


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



<span data-ttu-id="7483e-111">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="7483e-111">Where:</span></span>

-   <span data-ttu-id="7483e-112">ID ist ein optionaler eindeutiger Name.</span><span class="sxs-lookup"><span data-stu-id="7483e-112">id is an optional unique name.</span></span>
-   <span data-ttu-id="7483e-113">die Anmerkung ist 0 (null) oder mehr optionale benutzerspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="7483e-113">annotation is zero or more optional pieces of user-specific information.</span></span> <span data-ttu-id="7483e-114">Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effekt Parametern mit \_ Anmerkungen](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="7483e-114">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="7483e-115">"Pass (es)" ist 0 (null) oder größer.</span><span class="sxs-lookup"><span data-stu-id="7483e-115">pass(es) is zero or more passes.</span></span> <span data-ttu-id="7483e-116">Jeder Durchlauf enthält Zustands Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="7483e-116">Each pass contains state assignments.</span></span> <span data-ttu-id="7483e-117">Siehe unten.</span><span class="sxs-lookup"><span data-stu-id="7483e-117">See below.</span></span>

## <a name="passes"></a><span data-ttu-id="7483e-118">Ausweisen</span><span class="sxs-lookup"><span data-stu-id="7483e-118">Passes</span></span>

<span data-ttu-id="7483e-119">Ein Durchlauf enthält die zum renderbedarf erforderlichen Zustands Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="7483e-119">A pass contains the state assignments required to render.</span></span>


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



<span data-ttu-id="7483e-120">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="7483e-120">Where:</span></span>

-   <span data-ttu-id="7483e-121">ID ist ein optionaler eindeutiger Name.</span><span class="sxs-lookup"><span data-stu-id="7483e-121">id is an optional unique name.</span></span>
-   <span data-ttu-id="7483e-122">die Anmerkung ist eine oder mehrere optionale benutzerspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="7483e-122">annotation is one or more optional piece of user-specific information.</span></span> <span data-ttu-id="7483e-123">Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effekt Parametern mit \_ Anmerkungen](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="7483e-123">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="7483e-124">Zuweisung (en) weist NULL oder mehr Zustands Werte zu oder wertet mindestens einen Ausdruck aus.</span><span class="sxs-lookup"><span data-stu-id="7483e-124">assignment(s) assigns zero or more state values, or evaluates one or more expressions.</span></span> <span data-ttu-id="7483e-125">Weitere Informationen finden Sie unter [Wirkungs Zustände (Direct3D 9)](effect-states.md) und [Ausdrücke (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="7483e-125">See [Effect States (Direct3D 9)](effect-states.md) and [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="7483e-126">Übergibt alle außer der letzten Zuweisung in einem Satz von wiederholten Zuweisungen in denselben Zustand.</span><span class="sxs-lookup"><span data-stu-id="7483e-126">Passes ignore all but the last assignment in a set of repeated assignments to the same state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7483e-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7483e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7483e-128">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="7483e-128">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



