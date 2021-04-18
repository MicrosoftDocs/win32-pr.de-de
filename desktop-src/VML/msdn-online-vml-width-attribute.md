---
title: VML Width-Attribut
description: VML Width-Attribut
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b3d4917d76b3c8820186b04b2e77537e6a6ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337851"
---
# <a name="vml-width-attribute"></a><span data-ttu-id="00ed5-103">VML Width-Attribut</span><span class="sxs-lookup"><span data-stu-id="00ed5-103">VML Width Attribute</span></span>

<span data-ttu-id="00ed5-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="00ed5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="00ed5-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="00ed5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="00ed5-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="00ed5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="00ed5-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="00ed5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="00ed5-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="00ed5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="00ed5-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="00ed5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="00ed5-110">Definiert die Breite der Form.</span><span class="sxs-lookup"><span data-stu-id="00ed5-110">Defines the width of the shape.</span></span> <span data-ttu-id="00ed5-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="00ed5-111">Read/write.</span></span> <span data-ttu-id="00ed5-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="00ed5-112">**String**.</span></span>

<span data-ttu-id="00ed5-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="00ed5-113">**Applies To**</span></span>

[<span data-ttu-id="00ed5-114">Form</span><span class="sxs-lookup"><span data-stu-id="00ed5-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="00ed5-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="00ed5-115">**Tag Syntax**</span></span>

<span data-ttu-id="00ed5-116"><v: *Element* Style = "width: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="00ed5-116"><v: *element* style="width: *expression* "></span></span>

<span data-ttu-id="00ed5-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="00ed5-117">**Script Syntax**</span></span>

<span data-ttu-id="00ed5-118">*Element* . Style. Width = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="00ed5-118">*element* .style.width="*expression*"</span></span>

<span data-ttu-id="00ed5-119">*Ausdruck* = *Element*. Style. Width</span><span class="sxs-lookup"><span data-stu-id="00ed5-119">*expression*=*element*.style.width</span></span>

<span data-ttu-id="00ed5-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="00ed5-120">**Remarks**</span></span>

<span data-ttu-id="00ed5-121">Das **Width** -Attribut ähnelt dem standardmäßigen HTML- **Width** -Attribut für Stile.</span><span class="sxs-lookup"><span data-stu-id="00ed5-121">The **Width** attribute is similar to the standard HTML **Width** attribute for styles.</span></span>

<span data-ttu-id="00ed5-122">Einheiten können dem übergeordneten Element zugeordnet werden, oder Sie können sich in absoluten Einheiten befinden.</span><span class="sxs-lookup"><span data-stu-id="00ed5-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="00ed5-123">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="00ed5-123">Values include:</span></span>



| <span data-ttu-id="00ed5-124">Wert</span><span class="sxs-lookup"><span data-stu-id="00ed5-124">Value</span></span>      | <span data-ttu-id="00ed5-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00ed5-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00ed5-126">Auto</span><span class="sxs-lookup"><span data-stu-id="00ed5-126">Auto</span></span>       | <span data-ttu-id="00ed5-127">Die Standardposition eines Elements im Fluss der Seite.</span><span class="sxs-lookup"><span data-stu-id="00ed5-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="00ed5-128">units</span><span class="sxs-lookup"><span data-stu-id="00ed5-128">units</span></span>      | <span data-ttu-id="00ed5-129">Eine Zahl mit einem absoluten Einheiten Kenn Zeichner (cm, mm, in, PT, PC oder px) oder einem relativen Einheiten Kenn Zeichner (em oder Ex).</span><span class="sxs-lookup"><span data-stu-id="00ed5-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="00ed5-130">Wenn keine Einheiten angegeben werden, wird die Pixel (px) angenommen.</span><span class="sxs-lookup"><span data-stu-id="00ed5-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="00ed5-131">Prozentwert</span><span class="sxs-lookup"><span data-stu-id="00ed5-131">percentage</span></span> | <span data-ttu-id="00ed5-132">Wert, ausgedrückt als Prozentsatz der Breite des übergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="00ed5-132">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="00ed5-133">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="00ed5-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="00ed5-134">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="00ed5-134">**See Also**</span></span>

[<span data-ttu-id="00ed5-135">Einheiten</span><span class="sxs-lookup"><span data-stu-id="00ed5-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="00ed5-136">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="00ed5-136">**Example**</span></span>

<span data-ttu-id="00ed5-137">Die Breite der Form ist 25.</span><span class="sxs-lookup"><span data-stu-id="00ed5-137">The width of the shape is 25.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:25;height:20">
   </v:rect>
```



<span data-ttu-id="00ed5-138">[Beispiel](/previous-versions/bb264101(v=vs.85))für das width-Attribut.</span><span class="sxs-lookup"><span data-stu-id="00ed5-138">[Width Attribute Example](/previous-versions/bb264101(v=vs.85)).</span></span> <span data-ttu-id="00ed5-139">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="00ed5-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 