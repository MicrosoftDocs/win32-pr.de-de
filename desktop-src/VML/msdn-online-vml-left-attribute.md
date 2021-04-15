---
title: VML Left-Attribut
description: VML Left-Attribut
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17810d7635d4b8194f2bd2df258a900cb534581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474028"
---
# <a name="vml-left-attribute"></a><span data-ttu-id="e5c5b-103">VML Left-Attribut</span><span class="sxs-lookup"><span data-stu-id="e5c5b-103">VML Left Attribute</span></span>

<span data-ttu-id="e5c5b-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e5c5b-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e5c5b-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e5c5b-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e5c5b-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e5c5b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e5c5b-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e5c5b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e5c5b-110">Bestimmt die Position der Form relativ zum Element, das im Dokument Fluss links davon liegt.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-110">Determines the position of the shape relative to the element left of it in the document flow.</span></span> <span data-ttu-id="e5c5b-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-111">Read/write.</span></span> <span data-ttu-id="e5c5b-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-112">**String**.</span></span>

<span data-ttu-id="e5c5b-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="e5c5b-113">**Applies To**</span></span>

[<span data-ttu-id="e5c5b-114">Form</span><span class="sxs-lookup"><span data-stu-id="e5c5b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="e5c5b-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="e5c5b-115">**Tag Syntax**</span></span>

<span data-ttu-id="e5c5b-116"><v: *Element* Style = "left: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e5c5b-116"><v: *element* style="left: *expression* "></span></span>

<span data-ttu-id="e5c5b-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="e5c5b-117">**Script Syntax**</span></span>

<span data-ttu-id="e5c5b-118">*Element* . Style. Left = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="e5c5b-118">*element* .style.left="*expression*"</span></span>

<span data-ttu-id="e5c5b-119">*Ausdruck* = *Element*. Style. Left</span><span class="sxs-lookup"><span data-stu-id="e5c5b-119">*expression*=*element*.style.left</span></span>

<span data-ttu-id="e5c5b-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="e5c5b-120">**Remarks**</span></span>

<span data-ttu-id="e5c5b-121">Das **left** -Attribut ähnelt dem standardmäßigen HTML-Attribut **left** für Stile.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-121">The **Left** attribute is similar to the standard HTML **Left** attribute for styles.</span></span>

<span data-ttu-id="e5c5b-122">Einheiten können dem übergeordneten Element zugeordnet werden, oder Sie können sich in absoluten Einheiten befinden.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-122">Units may be mapped to the parent element or may be in absolute units.</span></span> <span data-ttu-id="e5c5b-123">Dieses Attribut wird nicht für Formen geschrieben, die Inline verankert sind.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-123">This attribute will not be written out for shapes anchored inline.</span></span>

<span data-ttu-id="e5c5b-124">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="e5c5b-124">Values include:</span></span>



| <span data-ttu-id="e5c5b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e5c5b-125">Value</span></span>      | <span data-ttu-id="e5c5b-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5c5b-126">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c5b-127">Auto</span><span class="sxs-lookup"><span data-stu-id="e5c5b-127">Auto</span></span>       | <span data-ttu-id="e5c5b-128">Die Standardposition eines Elements im Fluss der Seite.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-128">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="e5c5b-129">units</span><span class="sxs-lookup"><span data-stu-id="e5c5b-129">units</span></span>      | <span data-ttu-id="e5c5b-130">Eine Zahl mit einem absoluten Einheiten Kenn Zeichner (cm, mm, in, PT, PC oder px) oder einem relativen Einheiten Kenn Zeichner (em oder Ex).</span><span class="sxs-lookup"><span data-stu-id="e5c5b-130">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="e5c5b-131">Wenn keine Einheiten angegeben werden, wird die Pixel (px) angenommen.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-131">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="e5c5b-132">Prozentwert</span><span class="sxs-lookup"><span data-stu-id="e5c5b-132">percentage</span></span> | <span data-ttu-id="e5c5b-133">Wert, ausgedrückt als Prozentsatz der Breite des übergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-133">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="e5c5b-134">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="e5c5b-134">*VML Standard Attribute*</span></span>

<span data-ttu-id="e5c5b-135">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="e5c5b-135">**See Also**</span></span>

[<span data-ttu-id="e5c5b-136">Einheiten</span><span class="sxs-lookup"><span data-stu-id="e5c5b-136">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="e5c5b-137">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="e5c5b-137">**Example**</span></span>

<span data-ttu-id="e5c5b-138">Der linke Wert der Form wird im folgenden Beispiel auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e5c5b-138">The left value of the shape is set to 1 in the example below.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="e5c5b-139">[Beispiel für das linke Attribut](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md).</span><span class="sxs-lookup"><span data-stu-id="e5c5b-139">[Left Attribute Example](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md).</span></span> <span data-ttu-id="e5c5b-140">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="e5c5b-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 