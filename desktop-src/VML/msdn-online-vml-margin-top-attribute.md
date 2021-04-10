---
title: VML-Margin-Top Attribut
description: VML-Margin-Top Attribut
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14b6f4743f04740fe3fdbac4cc1d03f7bbe0282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316406"
---
# <a name="vml-margin-top-attribute"></a><span data-ttu-id="f73d0-103">VML-Margin-Top Attribut</span><span class="sxs-lookup"><span data-stu-id="f73d0-103">VML Margin-Top Attribute</span></span>

<span data-ttu-id="f73d0-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="f73d0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f73d0-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="f73d0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f73d0-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="f73d0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f73d0-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="f73d0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f73d0-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f73d0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f73d0-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f73d0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f73d0-110">Gibt den oberen Rand des enthaltenden Rechtecks der Form an, das relativ zum Shape-Anker ist.</span><span class="sxs-lookup"><span data-stu-id="f73d0-110">Specifies the top edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="f73d0-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f73d0-111">Read/write.</span></span> <span data-ttu-id="f73d0-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="f73d0-112">**String**.</span></span>

<span data-ttu-id="f73d0-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="f73d0-113">**Applies To**</span></span>

[<span data-ttu-id="f73d0-114">Form</span><span class="sxs-lookup"><span data-stu-id="f73d0-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="f73d0-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="f73d0-115">**Tag Syntax**</span></span>

<span data-ttu-id="f73d0-116"><v: *Element* Margin-Top = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="f73d0-116"><v: *element* margin-top=" *expression* "></span></span>

<span data-ttu-id="f73d0-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="f73d0-117">**Script Syntax**</span></span>

<span data-ttu-id="f73d0-118">*Element* . Margin-Top = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="f73d0-118">*element* .margin-top="*expression*"</span></span>

<span data-ttu-id="f73d0-119">*Ausdruck* = *Element*. Margin-Top</span><span class="sxs-lookup"><span data-stu-id="f73d0-119">*expression*=*element*.margin-top</span></span>

<span data-ttu-id="f73d0-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="f73d0-120">**Remarks**</span></span>

<span data-ttu-id="f73d0-121">Das Attribut " **Margin-Top** " ähnelt dem standardmäßigen HTML-Attribut " **Margin-Top** ", das mit Stylesheets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f73d0-121">The **Margin-Top** attribute is similar to the standard HTML **Margin-Top** attribute used with style sheets.</span></span>

<span data-ttu-id="f73d0-122">Beachten Sie, dass **MarginBottom** anstelle von **Margin-Top** für die Skripterstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f73d0-122">Note that **margintop** is used instead of **margin-top** for scripting.</span></span> <span data-ttu-id="f73d0-123">Beachten Sie auch, dass der Rand nicht geändert werden kann, wenn die **Position** **absolut** ist.</span><span class="sxs-lookup"><span data-stu-id="f73d0-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="f73d0-124">Diese Eigenschaft wird anstelle von **Top** für Formen in Microsoft Word und Microsoft Excel verwendet, die in einer Position relativ zu einem Ankerpunkt schweben.</span><span class="sxs-lookup"><span data-stu-id="f73d0-124">This property is used instead of **Top** for shapes in Microsoft Word and Microsoft Excel that are floating in a position relative to an anchor point.</span></span>

<span data-ttu-id="f73d0-125">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="f73d0-125">Values include:</span></span>



| <span data-ttu-id="f73d0-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f73d0-126">Value</span></span>      | <span data-ttu-id="f73d0-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f73d0-127">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f73d0-128">Auto</span><span class="sxs-lookup"><span data-stu-id="f73d0-128">Auto</span></span>       | <span data-ttu-id="f73d0-129">Die Standardposition eines Elements im Fluss der Seite.</span><span class="sxs-lookup"><span data-stu-id="f73d0-129">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="f73d0-130">units</span><span class="sxs-lookup"><span data-stu-id="f73d0-130">units</span></span>      | <span data-ttu-id="f73d0-131">Standard.</span><span class="sxs-lookup"><span data-stu-id="f73d0-131">Default.</span></span> <span data-ttu-id="f73d0-132">Eine Zahl mit einem absoluten Einheiten Kenn Zeichner (cm, mm, in, PT, PC oder px) oder einem relativen Einheiten Kenn Zeichner (em oder Ex).</span><span class="sxs-lookup"><span data-stu-id="f73d0-132">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="f73d0-133">Wenn keine Einheiten angegeben werden, wird die Pixel (px) angenommen.</span><span class="sxs-lookup"><span data-stu-id="f73d0-133">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="f73d0-134">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="f73d0-134">The default value is 0.</span></span> |
| <span data-ttu-id="f73d0-135">Prozentwert</span><span class="sxs-lookup"><span data-stu-id="f73d0-135">percentage</span></span> | <span data-ttu-id="f73d0-136">Wert, ausgedrückt als Prozentsatz der Höhe des übergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="f73d0-136">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="f73d0-137">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="f73d0-137">*VML Standard Attribute*</span></span>

<span data-ttu-id="f73d0-138">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="f73d0-138">**See Also**</span></span>

[<span data-ttu-id="f73d0-139">Einheiten</span><span class="sxs-lookup"><span data-stu-id="f73d0-139">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="f73d0-140">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f73d0-140">**Example**</span></span>

<span data-ttu-id="f73d0-141">Der obere Rand ist auf 25 Pixel festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f73d0-141">The top margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



<span data-ttu-id="f73d0-142">[Beispiel für das margin-top-Attribut](/previous-versions/bb264087(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f73d0-142">[Margin-Top Attribute Example](/previous-versions/bb264087(v=vs.85)).</span></span> <span data-ttu-id="f73d0-143">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="f73d0-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 