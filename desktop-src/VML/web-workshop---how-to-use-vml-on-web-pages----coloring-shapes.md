---
title: Färben von Formen
description: In diesem Artikel werden Färbungsformen in VML beschrieben, einem Feature, das seit Windows Internet Explorer 9 veraltet ist.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Web-Workshop, Färben von Formen
- Entwerfen von Webseiten, Färben von Formen
- Vector Markup Language (VML), färbende Formen
- VML (Vector Markup Language),färbende Formen
- Vektorgrafiken, färbende Formen
- VML-Formen, Färbung
- Färben von Formen
- Vector Markup Language (VML), Schlüsselwortfarbnamen
- VML (Vector Markup Language),Schlüsselwortfarbnamen
- Vektorgrafiken, Schlüsselwortfarbnamen
- Schlüsselwortfarbnamen
- Vector Markup Language (VML),RGB-Triplets
- VML (Vector Markup Language),RGB-Triplets
- Vektorgrafiken, RGB-Triplets
- RGB-Triplets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c203debd01d4234ae58900a023944511f9fc73c1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407743"
---
# <a name="coloring-shapes"></a><span data-ttu-id="5a623-118">Färben von Formen</span><span class="sxs-lookup"><span data-stu-id="5a623-118">Coloring Shapes</span></span>

<span data-ttu-id="5a623-119">In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="5a623-119">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5a623-120">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="5a623-120">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5a623-121">Seit Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="5a623-121">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5a623-122">Daher wird sie nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="5a623-122">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5a623-123">Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="5a623-123">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5a623-124">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="5a623-124">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5a623-125">Wie bereits in früheren Abschnitten erwähnt, können Sie "red" verwenden, um eine Farbe in Rot, "blue" für eine Farbe in Blau und so weiter zu darstellen.</span><span class="sxs-lookup"><span data-stu-id="5a623-125">As we mentioned in earlier sections, you can use "red" to represent a color in red, "blue" to represent a color in blue, and so on.</span></span> <span data-ttu-id="5a623-126">In diesem Thema wird veranschaulicht, wie Sie Formen in einer beliebigen Farbe zeichnen.</span><span class="sxs-lookup"><span data-stu-id="5a623-126">In this topic, we will illustrate how to draw shapes in any color you want.</span></span>

<span data-ttu-id="5a623-127">VML erweitert die HTML- und CSS-Farbsyntax.</span><span class="sxs-lookup"><span data-stu-id="5a623-127">VML extends HTML and CSS color syntax.</span></span> <span data-ttu-id="5a623-128">Wenn der Attributtyp eines VML-Elements farblich ist , z. B. **fillcolor** und [](#keyword-color-name) **strokecolor,** können Sie die Farbe ausdrücken, indem Sie entweder einen Schlüsselwortfarbnamen oder ein [RGB-Triplet verwenden.](#rgb-triplet)</span><span class="sxs-lookup"><span data-stu-id="5a623-128">When the attribute type of a VML element is color -- such as **fillcolor** and **strokecolor** -- you can express the color by using either a [keyword color name](#keyword-color-name) or an [RGB triplet](#rgb-triplet).</span></span>

<span data-ttu-id="5a623-129">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="5a623-129">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="keyword-color-name"></a><span data-ttu-id="5a623-130">Schlüsselwortfarbname</span><span class="sxs-lookup"><span data-stu-id="5a623-130">Keyword Color Name</span></span>

<span data-ttu-id="5a623-131">HTML 4.0 definiert eine Liste von Schlüsselwortfarbnamen.</span><span class="sxs-lookup"><span data-stu-id="5a623-131">HTML 4.0 defines a list of keyword color names.</span></span> <span data-ttu-id="5a623-132">Sie sind "aqua", "black", "blue", "ia", "gray", "green", "lime", "maroon", "violett", "red", "silver", "teal", "white" und "yellow".</span><span class="sxs-lookup"><span data-stu-id="5a623-132">They are aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, and yellow.</span></span> <span data-ttu-id="5a623-133">Der RGB-Wert für diese 16 Farben wird in der [HTML 4.0-Spezifikation definiert.](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5)</span><span class="sxs-lookup"><span data-stu-id="5a623-133">The RGB value for these 16 colors are defined in [HTML 4.0 specification](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span></span>

<span data-ttu-id="5a623-134">Sie können z. B. ein mit Gelb gefülltes Rechteck zeichnen, indem Sie angeben, und ihm eine blaue Kontur geben, indem Sie angeben, wie in der folgenden `fillcolor="yellow"` `strokecolor="blue"` VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="5a623-134">For example, you can draw a rectangle filled with yellow by specifying `fillcolor="yellow"`, and give it a blue outline by specifying `strokecolor="blue"`, as shown in the following VML representation:</span></span>

![color1.gif (305 Bytes)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





<span data-ttu-id="5a623-136">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="5a623-136">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rgb-triplet"></a><span data-ttu-id="5a623-137">RGB-Triplet</span><span class="sxs-lookup"><span data-stu-id="5a623-137">RGB Triplet</span></span>

<span data-ttu-id="5a623-138">Wenn die Farbe [](#keyword-color-name)kein Schlüsselwortfarbname ist, können Sie die Farbe entweder als RGB-Dezimaldreifach oder als RGB-Hexadezimal-Triplet ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="5a623-138">If the color is not a [keyword color name](#keyword-color-name), you can express the color as either an RGB decimal triplet or an RGB hexadecimal triplet.</span></span> <span data-ttu-id="5a623-139">Mit RGB-Triplets können Sie Werte für die roten, grünen und blauen Komponenten der Farbe angeben, indem Sie jede Komponente auf einen Wert zwischen 0 und 255 dezimal oder 00 bis FF im Hexadezimalformat festlegen.</span><span class="sxs-lookup"><span data-stu-id="5a623-139">With RGB triplets, you can specify values for the red, green, and blue components of the color, setting each component to a value ranging from 0 through 255 in decimal, or 00 through FF in hexadecimal.</span></span>

<span data-ttu-id="5a623-140">Beispielsweise können Sie ein Rechteck erstellen, das mit einer benutzerdefinierten Farbe mit einem RGB-Wert von 253, 249 und 186 als Dezimalzahl gefüllt ist, indem Sie entweder oder angeben, wie in der folgenden `fillcolor="rgb(253,249, 186)"` `fillcolor="#FDF9BA"` VML-Darstellung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5a623-140">For example, you can create a rectangle that is filled with a customized color with an RGB value of 253, 249, 186 in decimal by specifying either `fillcolor="rgb(253,249, 186)"` or `fillcolor="#FDF9BA"`, as shown in the following VML representation.</span></span> <span data-ttu-id="5a623-141">Im Hexadezimalwert wird der Wert 253 zu FD, 249 zu F9 und 186 zu BA.</span><span class="sxs-lookup"><span data-stu-id="5a623-141">In hexadecimal, the value 253 becomes FD, 249 becomes F9, and 186 becomes BA.</span></span>

![color2.gif (305 Bytes)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





<span data-ttu-id="5a623-143">Wenn rgb im Hexadezimal-Format ein Muster wie XXYYZZ auftauen kann, können Sie es in XYZ abkürzen.</span><span class="sxs-lookup"><span data-stu-id="5a623-143">If the RGB in hexadecimal has a pattern such as XXYYZZ, you can abbreviate it to XYZ.</span></span> <span data-ttu-id="5a623-144">Beispielsweise kann \# "66FF99" als \# "6F9" geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="5a623-144">For example, "\#66FF99" can be written out as "\#6F9".</span></span>

<span data-ttu-id="5a623-145">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="5a623-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="5a623-146">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5a623-146">Summary</span></span>

<span data-ttu-id="5a623-147">In VML können Sie eine Farbe in einem der folgenden Formate darstellen:</span><span class="sxs-lookup"><span data-stu-id="5a623-147">In VML, you can represent a color in one of the following formats:</span></span>

1.  <span data-ttu-id="5a623-148">fillcolor="blue"</span><span class="sxs-lookup"><span data-stu-id="5a623-148">fillcolor="blue"</span></span>
2.  <span data-ttu-id="5a623-149">fillcolor="rgb(0,0,255)"</span><span class="sxs-lookup"><span data-stu-id="5a623-149">fillcolor="rgb(0,0,255)"</span></span>
3.  <span data-ttu-id="5a623-150">fillcolor=" \# 0000ff"</span><span class="sxs-lookup"><span data-stu-id="5a623-150">fillcolor="\#0000ff"</span></span>

 

 