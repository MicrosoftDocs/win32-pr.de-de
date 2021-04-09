---
title: Verwenden des Formeln-Elements
description: Verwenden des Formeln-Elements
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Webworkshop, Formeln-Element
- Entwerfen von Webseiten, Formeln-Element
- Vector Markup Language (VML), Formeln-Element
- VML (Vector Markup Language), Formeln-Element
- Vektorgrafiken, Formeln-Element
- Formeln-Element
- VML-Elemente, Formeln
- VML-Formen, Formeln-Element
- Vector Markup Language (VML), Definieren von Pfaden für Formen
- VML (Vector Markup Language), Definieren von Pfaden für Formen
- Vektorgrafiken, Definieren von Pfaden für Formen
- VML-Formen, Definieren von Pfaden
- Definieren von Pfaden für Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85ce4ebb6eea05895edf974e3ca86b1fa2ad923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039049"
---
# <a name="using-the-formulas-element"></a><span data-ttu-id="af0c6-116">Verwenden des Formeln-Elements</span><span class="sxs-lookup"><span data-stu-id="af0c6-116">Using the Formulas Element</span></span>

<span data-ttu-id="af0c6-117">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="af0c6-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="af0c6-118">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="af0c6-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="af0c6-119">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="af0c6-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="af0c6-120">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="af0c6-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="af0c6-121">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="af0c6-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="af0c6-122">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="af0c6-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="af0c6-123">In diesem Thema wird veranschaulicht, wie Sie mit dem `<formulas>` untergeordneten Element einen anpassbaren Pfad für eine Form definieren.</span><span class="sxs-lookup"><span data-stu-id="af0c6-123">In this topic, we will illustrate how to use the `<formulas>` sub-element to define an adjustable path for a shape.</span></span>

<span data-ttu-id="af0c6-124">Sie können das <formulas> untergeordnete Element innerhalb `<shape>` von oder platzieren `<shapetype>` , um Formeln zu definieren, die den Pfad einer Form variieren können.</span><span class="sxs-lookup"><span data-stu-id="af0c6-124">You can place the <formulas> sub-element inside `<shape>` or `<shapetype>` to define formulas that can vary the path of a shape.</span></span> <span data-ttu-id="af0c6-125">Innerhalb des `<formulas>` untergeordneten Elements definiert ein **f** -Unterelement eine Formel, sodass ein Wert basierend auf dieser Formel ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="af0c6-125">Inside the `<formulas>` sub-element, one **f** sub-element defines one formula so that one value is evaluated based upon that formula.</span></span> <span data-ttu-id="af0c6-126">Die Formel definiert z. b `<v:f eqn="prod 10 4 5"/>` . einen Wert, der "10 x 4/5" entspricht.</span><span class="sxs-lookup"><span data-stu-id="af0c6-126">For example, the formula, `<v:f eqn="prod 10 4 5"/>` defines a value that is equivalent to "10 x 4 / 5".</span></span>

<span data-ttu-id="af0c6-127">Sie können viele **f** -unter Elemente in einem `<formulas>` Unterelement platzieren.</span><span class="sxs-lookup"><span data-stu-id="af0c6-127">You can place many **f** sub-elements inside one`<formulas>` sub-element.</span></span> <span data-ttu-id="af0c6-128">Formeln können auf die Werte verweisen, die zuvor in anderen Formeln innerhalb desselben `<formulas>` unter Elements definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="af0c6-128">Formulas can reference the values that are defined earlier in other formulas within the same `<formulas>` sub-element.</span></span> <span data-ttu-id="af0c6-129">Der in der ersten Formel definierte Wert kann als bezeichnet werden @0 . der in der zweiten Formel definierte Wert kann als bezeichnet werden @1 usw.</span><span class="sxs-lookup"><span data-stu-id="af0c6-129">The value that is defined in the first formula can be referred to as @0, the value that is defined in the second formula can be referred to as @1, and so on.</span></span>

<span data-ttu-id="af0c6-130">Außerdem können Sie das **ADJ** -Eigenschafts Attribut des- `<shape>` Elements angeben, z. b. adj = "100, 200, 150".</span><span class="sxs-lookup"><span data-stu-id="af0c6-130">In addition, you can specify the **adj** property attribute of the `<shape>` element, such as adj="100, 200, 150".</span></span> <span data-ttu-id="af0c6-131">Innerhalb des- `<formulas>` Elements können Sie auf diese Werte in der **ADJ** -Liste verweisen.</span><span class="sxs-lookup"><span data-stu-id="af0c6-131">Inside the `<formulas>` element, you can then reference those values in the **adj** list.</span></span> <span data-ttu-id="af0c6-132">Der erste Wert (100) in der **ADJ** -Liste kann auf 0 (NULL \# ), auf den zweiten Wert (200) als \# 1 usw. verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="af0c6-132">The first value (100) in the **adj** list can be referred to as \#0, the second value (200) can be referred to as \#1, and so on.</span></span>

<span data-ttu-id="af0c6-133">Wenn Sie z. b. ein lächelndes Gesicht zeichnen möchten, können Sie die folgende VML-Darstellung eingeben:</span><span class="sxs-lookup"><span data-stu-id="af0c6-133">For example, to draw a smiling face, you can type the following VML representation:</span></span>

![shape1.gif (735 bytes)](images/shape1f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="17520"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





-   <span data-ttu-id="af0c6-135">`adj="17520"` definiert einen Wert (= 17520).</span><span class="sxs-lookup"><span data-stu-id="af0c6-135">`adj="17520"` defines a value (= 17520).</span></span> <span data-ttu-id="af0c6-136">Auf diesen Wert kann als 0 verwiesen werden \# .</span><span class="sxs-lookup"><span data-stu-id="af0c6-136">This value can be referenced as \#0.</span></span>
-   <span data-ttu-id="af0c6-137">Die erste Formel, `<v:f eqn="sum 33030 0 #0"/>` , definiert den Wert (= 33030 + 0- \# 0).</span><span class="sxs-lookup"><span data-stu-id="af0c6-137">The first formula, `<v:f eqn="sum 33030 0 #0"/>`, defines the value (= 33030 + 0 - \#0).</span></span> <span data-ttu-id="af0c6-138">Auf diesen Wert kann als verwiesen werden @0 .</span><span class="sxs-lookup"><span data-stu-id="af0c6-138">This value can be referenced as @0.</span></span>
-   <span data-ttu-id="af0c6-139">Die zweite Formel `<v:f eqn="prod #0 4 3"/>` definiert den Wert (= \# 0 \* 4/3).</span><span class="sxs-lookup"><span data-stu-id="af0c6-139">The second formula, `<v:f eqn="prod #0 4 3"/>`, defines the value (= \#0 \* 4 / 3).</span></span> <span data-ttu-id="af0c6-140">Auf diesen Wert kann als verwiesen werden @1 .</span><span class="sxs-lookup"><span data-stu-id="af0c6-140">This value can be referenced as @1.</span></span>
-   <span data-ttu-id="af0c6-141">Die dritte Formel `<v:f eqn="prod @0 1 3"/>` definiert den Wert (= @0 \* 1/3).</span><span class="sxs-lookup"><span data-stu-id="af0c6-141">The third formula, `<v:f eqn="prod @0 1 3"/>`, defines the value (= @0 \* 1 / 3).</span></span> <span data-ttu-id="af0c6-142">Auf diesen Wert kann als verwiesen werden @2 .</span><span class="sxs-lookup"><span data-stu-id="af0c6-142">This value can be referenced as @2.</span></span>
-   <span data-ttu-id="af0c6-143">Die vierte Formel, `<v:f eqn="sum @1 0 @2"/>` , definiert den Wert (= @1 + 0 -@2 ).</span><span class="sxs-lookup"><span data-stu-id="af0c6-143">The fourth formula, `<v:f eqn="sum @1 0 @2"/>`, defines the value (=@1 + 0 -@2).</span></span> <span data-ttu-id="af0c6-144">Auf diesen Wert kann als verwiesen werden @3 .</span><span class="sxs-lookup"><span data-stu-id="af0c6-144">This value can be referenced as @3.</span></span>
-   <span data-ttu-id="af0c6-145">Innerhalb des- `<path>` Elements werden die Werte, die in der ersten ( @0 ) und vierten ( @3 )-Formel definiert sind, verwendet, um die Kontur der Form zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="af0c6-145">Inside the `<path>` element, the values defined in the first (@0) and the fourth (@3) formulas are used to determine the outline of the shape.</span></span>

<span data-ttu-id="af0c6-146">Wenn Sie die **ADJ** -Liste ändern (z. b.), werden `adj="20000"` die Werte der Formeln, die auf die **ADJ** -Liste verweisen, ebenfalls geändert. Dies wirkt sich auf das lächelnde Gesicht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="af0c6-146">If you change the **adj** list, such as `adj="20000"`, the values of the formulas that reference the **adj** list will be changed as well, affecting the smiling face as follows:</span></span>

![shape2.gif (765 bytes)](images/shape2f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="20000"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





<span data-ttu-id="af0c6-148">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858392) .</span><span class="sxs-lookup"><span data-stu-id="af0c6-148">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858392) .</span></span>

 

 