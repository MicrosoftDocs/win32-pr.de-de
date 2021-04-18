---
title: Verwenden des Shadow-Elements
description: Verwenden des Shadow-Elements
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Webworkshop, Schatten Element
- Entwerfen von Webseiten, Schatten Element
- Vector Markup Language (VML), Schatten Element
- VML (Vector Markup Language), Schatten Element
- Vektorgrafiken, Schatten Element
- Shadow-Element
- VML-Elemente, Schatten
- VML-Formen, Schatten Element
- Vector Markup Language (VML), zeichnen mit Schatteneffekten
- VML (Vector Markup Language), zeichnen mit Schatteneffekten
- Vektorgrafiken, zeichnen mit Schatteneffekten
- VML-Formen, zeichnen mit Schatteneffekten
- Zeichnen mit Schatteneffekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe32651fbeab6b84b49a40bae05a08ba3d9c33a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390918"
---
# <a name="using-the-shadow-element"></a><span data-ttu-id="eacae-116">Verwenden des Shadow-Elements</span><span class="sxs-lookup"><span data-stu-id="eacae-116">Using the Shadow Element</span></span>

<span data-ttu-id="eacae-117">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="eacae-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="eacae-118">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="eacae-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="eacae-119">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="eacae-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="eacae-120">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="eacae-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="eacae-121">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="eacae-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="eacae-122">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="eacae-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="eacae-123">In diesem Thema wird veranschaulicht, wie Sie mit dem `<shadow>` untergeordneten Element eine Form mit verschiedenen Schatteneffekten zeichnen.</span><span class="sxs-lookup"><span data-stu-id="eacae-123">In this topic, we will illustrate how to use the `<shadow>` sub-element to draw a shape that has various shadow effects.</span></span>

<span data-ttu-id="eacae-124">Sie können das `<shadow>` untergeordnete Element in `<shape>` , oder einem `<shapetype>` beliebigen vordefinierten Shape-Element platzieren, um eine Form mit einem Schatten zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="eacae-124">You can place the `<shadow>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to draw a shape with a shadow.</span></span> <span data-ttu-id="eacae-125">Sie können dann die Eigenschafts Attribute des `<shadow>` unter Elements verwenden, um den Schatten anzupassen.</span><span class="sxs-lookup"><span data-stu-id="eacae-125">You can then use the property attributes of the `<shadow>` sub-element to customize the shadow.</span></span>

<span data-ttu-id="eacae-126">Wenn Sie z. b. eine Form mit einem Schatten erstellen möchten, wie in der folgenden Abbildung gezeigt, können Sie die folgenden Zeilen in den `<BODY>` Bereich der Webseite eingeben:</span><span class="sxs-lookup"><span data-stu-id="eacae-126">For example, to create a shape with a shadow, as shown in the following picture, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

![shape1.gif (887 bytes)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   <span data-ttu-id="eacae-128">`on="t"` und `type="perspective"` geben an, dass der Schatten mit dem Perspective-Typ aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="eacae-128">`on="t"` and `type="perspective"` indicate to turn on the shadow using the perspective type.</span></span>
-   <span data-ttu-id="eacae-129">Der **Ursprung** und der **Offset** geben an, wo der Schatten gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eacae-129">The **origin** and **offset** indicate where to draw the shadow.</span></span>
-   <span data-ttu-id="eacae-130">`matrix="..."` Gibt die Perspektiven Transformationsmatrix an.</span><span class="sxs-lookup"><span data-stu-id="eacae-130">`matrix="..."` specifies the perspective transform matrix.</span></span>

<span data-ttu-id="eacae-131">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858396) .</span><span class="sxs-lookup"><span data-stu-id="eacae-131">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858396) .</span></span>

 

 