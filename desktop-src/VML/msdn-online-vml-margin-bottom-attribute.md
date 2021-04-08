---
title: VML-Margin-Bottom Attribut
description: VML-Margin-Bottom Attribut
ms.assetid: c1101430-f4fc-4fa5-8e02-7cee126c2c1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35712733179a3c03dc291c4d5efcf4fee68c2865
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728824"
---
# <a name="vml-margin-bottom-attribute"></a><span data-ttu-id="80e84-103">VML-Margin-Bottom Attribut</span><span class="sxs-lookup"><span data-stu-id="80e84-103">VML Margin-Bottom Attribute</span></span>

<span data-ttu-id="80e84-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="80e84-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="80e84-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="80e84-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="80e84-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="80e84-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="80e84-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="80e84-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="80e84-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="80e84-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="80e84-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="80e84-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="80e84-110">Gibt den unteren Rand des enthaltenden Rechtecks der Form an, das relativ zum Shape-Anker ist.</span><span class="sxs-lookup"><span data-stu-id="80e84-110">Specifies the bottom edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="80e84-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="80e84-111">Read/write.</span></span> <span data-ttu-id="80e84-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="80e84-112">**String**.</span></span>

<span data-ttu-id="80e84-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="80e84-113">**Applies To**</span></span>

[<span data-ttu-id="80e84-114">Form</span><span class="sxs-lookup"><span data-stu-id="80e84-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="80e84-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="80e84-115">**Tag Syntax**</span></span>

<span data-ttu-id="80e84-116"><v: *Element* margin-bottom = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="80e84-116"><v: *element* margin-bottom=" *expression* "></span></span>

<span data-ttu-id="80e84-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="80e84-117">**Script Syntax**</span></span>

<span data-ttu-id="80e84-118">*Element* . MarginBottom = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="80e84-118">*element* .marginbottom="*expression*"</span></span>

<span data-ttu-id="80e84-119">*Ausdruck* = *Element*. MarginBottom</span><span class="sxs-lookup"><span data-stu-id="80e84-119">*expression*=*element*.marginbottom</span></span>

<span data-ttu-id="80e84-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="80e84-120">**Remarks**</span></span>

<span data-ttu-id="80e84-121">Das Attribut " **margin-bottom** " ähnelt dem standardmäßigen HTML-Attribut " **margin-bottom** ", das mit Stylesheets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="80e84-121">The **Margin-Bottom** attribute is similar to the standard HTML **Margin-Bottom** attribute used with style sheets.</span></span>

<span data-ttu-id="80e84-122">Beachten Sie, dass **MarginBottom** anstelle von **margin-bottom** für die Skripterstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="80e84-122">Note that **marginbottom** is used instead of **margin-bottom** for scripting.</span></span> <span data-ttu-id="80e84-123">Beachten Sie auch, dass der Rand nicht geändert werden kann, wenn die **Position** **absolut** ist.</span><span class="sxs-lookup"><span data-stu-id="80e84-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="80e84-124">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="80e84-124">Values include:</span></span>



| <span data-ttu-id="80e84-125">Wert</span><span class="sxs-lookup"><span data-stu-id="80e84-125">Value</span></span>      | <span data-ttu-id="80e84-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80e84-126">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80e84-127">Auto</span><span class="sxs-lookup"><span data-stu-id="80e84-127">Auto</span></span>       | <span data-ttu-id="80e84-128">Die Standardposition eines Elements im Fluss der Seite.</span><span class="sxs-lookup"><span data-stu-id="80e84-128">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="80e84-129">units</span><span class="sxs-lookup"><span data-stu-id="80e84-129">units</span></span>      | <span data-ttu-id="80e84-130">Standard.</span><span class="sxs-lookup"><span data-stu-id="80e84-130">Default.</span></span> <span data-ttu-id="80e84-131">Eine Zahl mit einem absoluten Einheiten Kenn Zeichner (cm, mm, in, PT, PC oder px) oder einem relativen Einheiten Kenn Zeichner (em oder Ex).</span><span class="sxs-lookup"><span data-stu-id="80e84-131">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="80e84-132">Wenn keine Einheiten angegeben werden, wird die Pixel (px) angenommen.</span><span class="sxs-lookup"><span data-stu-id="80e84-132">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="80e84-133">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="80e84-133">The default value is 0.</span></span> |
| <span data-ttu-id="80e84-134">Prozentwert</span><span class="sxs-lookup"><span data-stu-id="80e84-134">percentage</span></span> | <span data-ttu-id="80e84-135">Wert, ausgedrückt als Prozentsatz der Höhe des übergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="80e84-135">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="80e84-136">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="80e84-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="80e84-137">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="80e84-137">**See Also**</span></span>

[<span data-ttu-id="80e84-138">Einheiten</span><span class="sxs-lookup"><span data-stu-id="80e84-138">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="80e84-139">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="80e84-139">**Example**</span></span>

<span data-ttu-id="80e84-140">Der untere Rand ist auf 25 Pixel festgelegt.</span><span class="sxs-lookup"><span data-stu-id="80e84-140">The bottom margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-bottom:25px">
   </v:rect>
```



<span data-ttu-id="80e84-141">[Beispiel für das margin-bottom-Attribut](/previous-versions/bb229675(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="80e84-141">[Margin-Bottom Attribute Example](/previous-versions/bb229675(v=vs.85)).</span></span> <span data-ttu-id="80e84-142">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="80e84-142">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 