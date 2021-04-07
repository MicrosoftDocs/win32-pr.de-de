---
title: Top-Attribut von VML
description: Top-Attribut von VML
ms.assetid: faad0c76-3566-4a51-962b-971667df2025
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c76a39035bc3dd3f0ae348280561e614d7dab4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728241"
---
# <a name="vml-top-attribute"></a><span data-ttu-id="24e78-103">Top-Attribut von VML</span><span class="sxs-lookup"><span data-stu-id="24e78-103">VML Top Attribute</span></span>

<span data-ttu-id="24e78-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="24e78-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="24e78-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="24e78-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="24e78-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="24e78-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="24e78-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="24e78-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="24e78-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="24e78-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="24e78-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="24e78-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="24e78-110">Definiert die Position der Form relativ zum übergeordneten Element im Fluss der Seite.</span><span class="sxs-lookup"><span data-stu-id="24e78-110">Defines the position of the shape relative to the element above it in the flow of the page.</span></span> <span data-ttu-id="24e78-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="24e78-111">Read/write.</span></span> <span data-ttu-id="24e78-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="24e78-112">**String**.</span></span>

<span data-ttu-id="24e78-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="24e78-113">**Applies To**</span></span>

[<span data-ttu-id="24e78-114">Form</span><span class="sxs-lookup"><span data-stu-id="24e78-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="24e78-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="24e78-115">**Tag Syntax**</span></span>

<span data-ttu-id="24e78-116"><v: *Element* Style = "Top: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="24e78-116"><v: *element* style="top: *expression* "></span></span>

<span data-ttu-id="24e78-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="24e78-117">**Script Syntax**</span></span>

<span data-ttu-id="24e78-118">*Element* . Style.Top = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="24e78-118">*element* .style.top="*expression*"</span></span>

<span data-ttu-id="24e78-119">*Ausdruck* = *Element*. Style.Top</span><span class="sxs-lookup"><span data-stu-id="24e78-119">*expression*=*element*.style.top</span></span>

<span data-ttu-id="24e78-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="24e78-120">**Remarks**</span></span>

<span data-ttu-id="24e78-121">Das **Top** -Attribut ähnelt dem standardmäßigen HTML- **Top** -Attribut für Stile.</span><span class="sxs-lookup"><span data-stu-id="24e78-121">The **Top** attribute is similar to the standard HTML **Top** attribute for styles.</span></span>

<span data-ttu-id="24e78-122">Einheiten können dem übergeordneten Element zugeordnet werden, oder Sie können sich in absoluten Einheiten befinden.</span><span class="sxs-lookup"><span data-stu-id="24e78-122">Units may be mapped to the parent element or may be in absolute units.</span></span> <span data-ttu-id="24e78-123">Dieses Attribut kann nicht für Formen geschrieben werden, die Inline verankert sind.</span><span class="sxs-lookup"><span data-stu-id="24e78-123">This attribute may not be written out for shapes anchored inline.</span></span>

<span data-ttu-id="24e78-124">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="24e78-124">Values include:</span></span>



| <span data-ttu-id="24e78-125">Wert</span><span class="sxs-lookup"><span data-stu-id="24e78-125">Value</span></span>      | <span data-ttu-id="24e78-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24e78-126">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24e78-127">Auto</span><span class="sxs-lookup"><span data-stu-id="24e78-127">Auto</span></span>       | <span data-ttu-id="24e78-128">Die Standardposition eines Elements im Fluss der Seite.</span><span class="sxs-lookup"><span data-stu-id="24e78-128">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="24e78-129">units</span><span class="sxs-lookup"><span data-stu-id="24e78-129">units</span></span>      | <span data-ttu-id="24e78-130">Eine Zahl mit einem absoluten Einheiten Kenn Zeichner (cm, mm, in, PT, PC oder px) oder einem relativen Einheiten Kenn Zeichner (em oder Ex).</span><span class="sxs-lookup"><span data-stu-id="24e78-130">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="24e78-131">Wenn keine Einheiten angegeben werden, wird die Pixel (px) angenommen.</span><span class="sxs-lookup"><span data-stu-id="24e78-131">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="24e78-132">Prozentwert</span><span class="sxs-lookup"><span data-stu-id="24e78-132">percentage</span></span> | <span data-ttu-id="24e78-133">Wert, ausgedrückt als Prozentsatz der Höhe des übergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="24e78-133">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                   |



 

<span data-ttu-id="24e78-134">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="24e78-134">*VML Standard Attribute*</span></span>

<span data-ttu-id="24e78-135">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="24e78-135">**See Also**</span></span>

[<span data-ttu-id="24e78-136">Einheiten</span><span class="sxs-lookup"><span data-stu-id="24e78-136">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="24e78-137">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="24e78-137">**Example**</span></span>

<span data-ttu-id="24e78-138">Der obere Rand der Form ist 5 Pixel unterhalb des Objekts, das ihm im Fluss der Seite vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="24e78-138">The top edge of the shape is 5 pixels below the object that precedes it in the flow of the page.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:5;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="24e78-139">[Beispiel](/previous-versions/bb264098(v=vs.85))für das Top-Attribut.</span><span class="sxs-lookup"><span data-stu-id="24e78-139">[Top Attribute Example](/previous-versions/bb264098(v=vs.85)).</span></span> <span data-ttu-id="24e78-140">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="24e78-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 