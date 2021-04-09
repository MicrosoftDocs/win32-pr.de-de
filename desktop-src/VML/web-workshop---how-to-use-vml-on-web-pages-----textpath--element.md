---
title: Verwenden des TextPath-Elements
description: Verwenden des TextPath-Elements
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- Webworkshop, TextPath-Element
- Entwerfen von Webseiten, TextPath-Element
- Vector Markup Language (VML), TextPath-Element
- VML (Vector Markup Language), TextPath-Element
- Vektorgrafiken, TextPath-Element
- TextPath-Element
- VML-Elemente, TextPath
- VML-Formen, TextPath-Element
- Vector Markup Language (VML), Zeichnen von Text
- VML (Vector Markup Language), Zeichnen von Text
- Vektorgrafiken, Zeichnen von VML-Text
- Zeichnen von Text
- VML-Formen, Zeichnen von Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148c032d14307dc07ec56911f4c5cc45a4c69664
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102263"
---
# <a name="using-the-textpath-element"></a><span data-ttu-id="77b87-116">Verwenden des TextPath-Elements</span><span class="sxs-lookup"><span data-stu-id="77b87-116">Using the Textpath Element</span></span>

<span data-ttu-id="77b87-117">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="77b87-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="77b87-118">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="77b87-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="77b87-119">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="77b87-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="77b87-120">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="77b87-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="77b87-121">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="77b87-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="77b87-122">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="77b87-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="77b87-123">In diesem Thema wird veranschaulicht, wie das-Element verwendet wird, `<textpath>` um Text mit verschiedenen Stilen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="77b87-123">In this topic, we will illustrate how to use the `<textpath>` element to draw text with various styles.</span></span>

<span data-ttu-id="77b87-124">Sie können das `<textpath>` untergeordnete Element innerhalb `<shape>` von oder platzieren `<shapetype>` , um Text zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="77b87-124">You can place the `<textpath>` sub-element inside `<shape>` or `<shapetype>` to draw text.</span></span> <span data-ttu-id="77b87-125">Sie können dann die Eigenschafts Attribute des `<textpath>` unter Elements verwenden, um den Text anzupassen.</span><span class="sxs-lookup"><span data-stu-id="77b87-125">You can then use the property attributes of the `<textpath>` sub-element to customize the text.</span></span> <span data-ttu-id="77b87-126">Sie können auch das `<formulas>` untergeordnete-Element verwenden, um die Kontur des Texts zu definieren.</span><span class="sxs-lookup"><span data-stu-id="77b87-126">You can also use the `<formulas>` sub-element to define the outline of the text.</span></span>

<span data-ttu-id="77b87-127">Wenn Sie z. b. den in der folgenden Abbildung gezeigten Text erstellen möchten, können Sie die VML-Darstellung unten eingeben.</span><span class="sxs-lookup"><span data-stu-id="77b87-127">For example, to create the text shown in the following picture, you can type the VML representation below.</span></span> <span data-ttu-id="77b87-128">Beachten Sie, dass wir das- `<shapetype>` Element verwenden, um einen Prototyp für den Text Umriss zu definieren.</span><span class="sxs-lookup"><span data-stu-id="77b87-128">Notice that we use the `<shapetype>` element to define a prototype for the outline of the text.</span></span> <span data-ttu-id="77b87-129">Anschließend werden zwei Formen aus dem gleichen ShapeType instanziiert.</span><span class="sxs-lookup"><span data-stu-id="77b87-129">We then instantiate two shapes from the same shapetype.</span></span> <span data-ttu-id="77b87-130">Sie können einfach das Attribut der **Zeichen** folgen Eigenschaft ändern, um anderen Text anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="77b87-130">You can simply change the **string** property attribute to display different text.</span></span>

![shape1 \-1.gif (4898 Bytes)](images/shape1-1t.gif)

![shape1 \-2.gif (2789 Bytes)](images/shape1-2t.gif)


```HTML
<v:shapetype id="MyShape"
coordsize="21600,21600" adj="9931"
path="m0@0c7200@2,14400@1,21600,0m0@5c7200@6,14400@6,21600@5e">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="prod #0 3 4"/>
<v:f eqn="prod #0 5 4"/>
<v:f eqn="prod #0 3 8"/>
<v:f eqn="prod #0 1 8"/>
<v:f eqn="sum 21600 0 @3"/>
<v:f eqn="sum @4 21600 0"/>
<v:f eqn="prod #0 1 2"/>
<v:f eqn="prod @5 1 2"/>
<v:f eqn="sum @7 @8 0"/>
<v:f eqn="prod #0 7 8"/>
<v:f eqn="prod @5 1 3"/>
<v:f eqn="sum @1 @2 0"/>
<v:f eqn="sum @12 @0 0"/>
<v:f eqn="prod @13 1 4"/>
<v:f eqn="sum @11 14400 @14"/>
</v:formulas>
<v:path textpathok="t" />
<v:textpath on="t" fitshape="t" xscale="t"/>
</v:shapetype>

<v:shape type="#MyShape" style='position:relative; top:5; left:5;
width:261.6pt;height:71.45pt;' adj="8717" fillcolor="red" strokeweight="1pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/> <v:textpath
style='font-family:"Arial Black";v-text-kern:t' trim="t"
fitpath="t" xscale="f" string="Hello World !"/>
</v:shape>

<v:shape type="#MyShape" style='position:relative; top:120; left:5; width:207pt;
height:63pt;' adj="8717" fillcolor="blue" strokeweight="2pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/>
<v:textpath style='font-family:"Times New Roman";v-text-kern:t'
trim="t" fitpath="t" xscale="f" string="VML"/>
</v:shape>
```





<span data-ttu-id="77b87-133">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858398) .</span><span class="sxs-lookup"><span data-stu-id="77b87-133">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858398) .</span></span>

 

 