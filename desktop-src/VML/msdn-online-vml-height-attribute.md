---
title: VML Height-Attribut
description: VML Height-Attribut
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41751e4863fdb128dbbedf2e3abf8e7f0a6736d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101839"
---
# <a name="vml-height-attribute"></a><span data-ttu-id="db14d-103">VML Height-Attribut</span><span class="sxs-lookup"><span data-stu-id="db14d-103">VML Height Attribute</span></span>

<span data-ttu-id="db14d-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="db14d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="db14d-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="db14d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="db14d-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="db14d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="db14d-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="db14d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="db14d-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="db14d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="db14d-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="db14d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="db14d-110">Gibt die Höhe der Form an.</span><span class="sxs-lookup"><span data-stu-id="db14d-110">Specifies the height of the shape.</span></span> <span data-ttu-id="db14d-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="db14d-111">Read/write.</span></span> <span data-ttu-id="db14d-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="db14d-112">**String**.</span></span>

<span data-ttu-id="db14d-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="db14d-113">**Applies To**</span></span>

[<span data-ttu-id="db14d-114">Form</span><span class="sxs-lookup"><span data-stu-id="db14d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="db14d-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="db14d-115">**Tag Syntax**</span></span>

<span data-ttu-id="db14d-116"><v: *Element* Style = "height: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="db14d-116"><v: *element* style="height: *expression* "></span></span>

<span data-ttu-id="db14d-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="db14d-117">**Script Syntax**</span></span>

<span data-ttu-id="db14d-118">*Element* . Style. Height = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="db14d-118">*element* .style.height="*expression*"</span></span>

<span data-ttu-id="db14d-119">*Ausdruck* = *Element*. Style. Height</span><span class="sxs-lookup"><span data-stu-id="db14d-119">*expression*=*element*.style.height</span></span>

<span data-ttu-id="db14d-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="db14d-120">**Remarks**</span></span>

<span data-ttu-id="db14d-121">Das **height** -Attribut ähnelt dem standardmäßigen HTML- **height** -Attribut für Stile.</span><span class="sxs-lookup"><span data-stu-id="db14d-121">The **Height** attribute is similar to the standard HTML **Height** attribute for styles.</span></span>

<span data-ttu-id="db14d-122">Einheiten können dem übergeordneten Element zugeordnet werden, oder Sie können sich in absoluten Einheiten befinden.</span><span class="sxs-lookup"><span data-stu-id="db14d-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="db14d-123">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="db14d-123">Values include:</span></span>



| <span data-ttu-id="db14d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="db14d-124">Value</span></span>      | <span data-ttu-id="db14d-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db14d-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db14d-126">Auto</span><span class="sxs-lookup"><span data-stu-id="db14d-126">Auto</span></span>       | <span data-ttu-id="db14d-127">Die Standardposition eines Elements im Fluss der Seite.</span><span class="sxs-lookup"><span data-stu-id="db14d-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="db14d-128">units</span><span class="sxs-lookup"><span data-stu-id="db14d-128">units</span></span>      | <span data-ttu-id="db14d-129">Eine Zahl mit einem absoluten Einheiten Kenn Zeichner (cm, mm, in, PT, PC oder px) oder einem relativen Einheiten Kenn Zeichner (em oder Ex).</span><span class="sxs-lookup"><span data-stu-id="db14d-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="db14d-130">Wenn keine Einheiten angegeben werden, wird die Pixel (px) angenommen.</span><span class="sxs-lookup"><span data-stu-id="db14d-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="db14d-131">Prozentwert</span><span class="sxs-lookup"><span data-stu-id="db14d-131">percentage</span></span> | <span data-ttu-id="db14d-132">Wert, ausgedrückt als Prozentsatz der Höhe des übergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="db14d-132">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                   |



 

<span data-ttu-id="db14d-133">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="db14d-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="db14d-134">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="db14d-134">**See Also**</span></span>

[<span data-ttu-id="db14d-135">Einheiten</span><span class="sxs-lookup"><span data-stu-id="db14d-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="db14d-136">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="db14d-136">**Example**</span></span>

<span data-ttu-id="db14d-137">Die Höhe der Form ist auf 30 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="db14d-137">The height of the shape is set to 30.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



<span data-ttu-id="db14d-138">[Beispiel für Höhen Attribut](/previous-versions/bb229671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="db14d-138">[Height Attribute Example](/previous-versions/bb229671(v=vs.85)).</span></span> <span data-ttu-id="db14d-139">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="db14d-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 