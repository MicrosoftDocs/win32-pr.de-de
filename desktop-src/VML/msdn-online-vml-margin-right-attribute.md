---
title: VML-Margin-Right Attribut
description: VML-Margin-Right Attribut
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5529257a0e21c8a8f8c7a1a2f8381c10a6e3b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039582"
---
# <a name="vml-margin-right-attribute"></a><span data-ttu-id="a59f9-103">VML-Margin-Right Attribut</span><span class="sxs-lookup"><span data-stu-id="a59f9-103">VML Margin-Right Attribute</span></span>

<span data-ttu-id="a59f9-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a59f9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a59f9-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="a59f9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a59f9-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="a59f9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a59f9-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a59f9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a59f9-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a59f9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a59f9-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a59f9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a59f9-110">Gibt den rechten Rand des enthaltenden Rechtecks der Form an, das relativ zum Shape-Anker ist.</span><span class="sxs-lookup"><span data-stu-id="a59f9-110">Specifies the right edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="a59f9-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a59f9-111">Read/write.</span></span> <span data-ttu-id="a59f9-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="a59f9-112">**String**.</span></span>

<span data-ttu-id="a59f9-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="a59f9-113">**Applies To**</span></span>

[<span data-ttu-id="a59f9-114">Form</span><span class="sxs-lookup"><span data-stu-id="a59f9-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a59f9-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="a59f9-115">**Tag Syntax**</span></span>

<span data-ttu-id="a59f9-116"><v: *Element* Style = "margin-right: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a59f9-116"><v: *element* style="margin-right: *expression* "></span></span>

<span data-ttu-id="a59f9-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="a59f9-117">**Script Syntax**</span></span>

<span data-ttu-id="a59f9-118">*Element* . Style. MarginRight = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="a59f9-118">*element* .style.marginright="*expression*"</span></span>

<span data-ttu-id="a59f9-119">*Ausdruck* = *Element*. Style. MarginRight</span><span class="sxs-lookup"><span data-stu-id="a59f9-119">*expression*=*element*.style.marginright</span></span>

<span data-ttu-id="a59f9-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="a59f9-120">**Remarks**</span></span>

<span data-ttu-id="a59f9-121">Das Attribut " **margin-right** " ähnelt dem standardmäßigen HTML-Attribut " **margin-right** ", das mit Stylesheets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a59f9-121">The **Margin-Right** attribute is similar to the standard HTML **Margin-Right** attribute used with style sheets.</span></span>

<span data-ttu-id="a59f9-122">Beachten Sie, dass **MarginRight** anstelle von **margin-right** für die Skripterstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a59f9-122">Note that **marginright** is used instead of **margin-right** for scripting.</span></span> <span data-ttu-id="a59f9-123">Beachten Sie auch, dass der Rand nicht geändert werden kann, wenn die **Position** **absolut** ist.</span><span class="sxs-lookup"><span data-stu-id="a59f9-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="a59f9-124">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="a59f9-124">Values include:</span></span>



| <span data-ttu-id="a59f9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a59f9-125">Value</span></span>      | <span data-ttu-id="a59f9-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a59f9-126">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a59f9-127">Auto</span><span class="sxs-lookup"><span data-stu-id="a59f9-127">Auto</span></span>       | <span data-ttu-id="a59f9-128">Die Standardposition eines Elements im Fluss der Seite.</span><span class="sxs-lookup"><span data-stu-id="a59f9-128">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="a59f9-129">units</span><span class="sxs-lookup"><span data-stu-id="a59f9-129">units</span></span>      | <span data-ttu-id="a59f9-130">Standard.</span><span class="sxs-lookup"><span data-stu-id="a59f9-130">Default.</span></span> <span data-ttu-id="a59f9-131">Eine Zahl mit einem absoluten Einheiten Kenn Zeichner (cm, mm, in, PT, PC oder px) oder einem relativen Einheiten Kenn Zeichner (em oder Ex).</span><span class="sxs-lookup"><span data-stu-id="a59f9-131">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="a59f9-132">Wenn keine Einheiten angegeben werden, wird die Pixel (px) angenommen.</span><span class="sxs-lookup"><span data-stu-id="a59f9-132">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="a59f9-133">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a59f9-133">The default value is 0.</span></span> |
| <span data-ttu-id="a59f9-134">Prozentwert</span><span class="sxs-lookup"><span data-stu-id="a59f9-134">percentage</span></span> | <span data-ttu-id="a59f9-135">Wert, ausgedrückt als Prozentsatz der Höhe des übergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="a59f9-135">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="a59f9-136">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="a59f9-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="a59f9-137">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="a59f9-137">**See Also**</span></span>

[<span data-ttu-id="a59f9-138">Einheiten</span><span class="sxs-lookup"><span data-stu-id="a59f9-138">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="a59f9-139">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="a59f9-139">**Example**</span></span>

<span data-ttu-id="a59f9-140">Der Rechte Rand ist auf 25 Pixel festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a59f9-140">The right margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



<span data-ttu-id="a59f9-141">[Beispiel für das margin-right-Attribut](/previous-versions/bb229677(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a59f9-141">[Margin-Right Attribute Example](/previous-versions/bb229677(v=vs.85)).</span></span> <span data-ttu-id="a59f9-142">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="a59f9-142">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 