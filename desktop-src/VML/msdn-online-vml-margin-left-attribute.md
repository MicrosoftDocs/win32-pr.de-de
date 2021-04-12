---
title: VML-Margin-Left Attribut
description: VML-Margin-Left Attribut
ms.assetid: 65488c47-06c2-4a8f-8d29-4837865465f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f98900e862f22f31ad444bc6fb6f372627eca1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315801"
---
# <a name="vml-margin-left-attribute"></a><span data-ttu-id="bac87-103">VML-Margin-Left Attribut</span><span class="sxs-lookup"><span data-stu-id="bac87-103">VML Margin-Left Attribute</span></span>

<span data-ttu-id="bac87-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="bac87-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bac87-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="bac87-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bac87-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="bac87-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bac87-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="bac87-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bac87-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bac87-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bac87-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bac87-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bac87-110">Gibt den linken Rand des enthaltenden Rechtecks der Form an, das relativ zum Shape-Anker ist.</span><span class="sxs-lookup"><span data-stu-id="bac87-110">Specifies the left edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="bac87-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="bac87-111">Read/write.</span></span> <span data-ttu-id="bac87-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="bac87-112">**String**.</span></span>

<span data-ttu-id="bac87-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="bac87-113">**Applies To**</span></span>

[<span data-ttu-id="bac87-114">Form</span><span class="sxs-lookup"><span data-stu-id="bac87-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="bac87-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="bac87-115">**Tag Syntax**</span></span>

<span data-ttu-id="bac87-116"><v: *Element* Style = "margin-left: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="bac87-116"><v: *element* style="margin-left: *expression* "></span></span>

<span data-ttu-id="bac87-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="bac87-117">**Script Syntax**</span></span>

<span data-ttu-id="bac87-118">*Element* . Style. MarginLeft = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="bac87-118">*element* .style.marginleft="*expression*"</span></span>

<span data-ttu-id="bac87-119">*Ausdruck* = *Element*. Style. MarginLeft</span><span class="sxs-lookup"><span data-stu-id="bac87-119">*expression*=*element*.style.marginleft</span></span>

<span data-ttu-id="bac87-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="bac87-120">**Remarks**</span></span>

<span data-ttu-id="bac87-121">Das Attribut " **margin-left** " ähnelt dem standardmäßigen HTML-Attribut " **margin-left** ", das mit Stylesheets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bac87-121">The **Margin-Left** attribute is similar to the standard HTML **Margin-Left** attribute used with style sheets.</span></span>

<span data-ttu-id="bac87-122">Beachten Sie, dass **MarginLeft** anstelle von **margin-left** für die Skripterstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bac87-122">Note that **marginleft** is used instead of **margin-left** for scripting.</span></span> <span data-ttu-id="bac87-123">Beachten Sie auch, dass der Rand nicht geändert werden kann, wenn die **Position** **absolut** ist.</span><span class="sxs-lookup"><span data-stu-id="bac87-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="bac87-124">Diese Eigenschaft wird anstelle von **left** für Formen in Microsoft Word und Microsoft Excel verwendet, die in einer Position relativ zu einem Ankerpunkt schweben.</span><span class="sxs-lookup"><span data-stu-id="bac87-124">This property is used instead of **Left** for shapes in Microsoft Word and Microsoft Excel that are floating in a position relative to an anchor point.</span></span>

<span data-ttu-id="bac87-125">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="bac87-125">Values include:</span></span>



| <span data-ttu-id="bac87-126">Wert</span><span class="sxs-lookup"><span data-stu-id="bac87-126">Value</span></span>      | <span data-ttu-id="bac87-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bac87-127">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bac87-128">Auto</span><span class="sxs-lookup"><span data-stu-id="bac87-128">Auto</span></span>       | <span data-ttu-id="bac87-129">Die Standardposition eines Elements im Fluss der Seite.</span><span class="sxs-lookup"><span data-stu-id="bac87-129">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="bac87-130">units</span><span class="sxs-lookup"><span data-stu-id="bac87-130">units</span></span>      | <span data-ttu-id="bac87-131">Standard.</span><span class="sxs-lookup"><span data-stu-id="bac87-131">Default.</span></span> <span data-ttu-id="bac87-132">Eine Zahl mit einem absoluten Einheiten Kenn Zeichner (cm, mm, in, PT, PC oder px) oder einem relativen Einheiten Kenn Zeichner (em oder Ex).</span><span class="sxs-lookup"><span data-stu-id="bac87-132">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="bac87-133">Wenn keine Einheiten angegeben werden, wird die Pixel (px) angenommen.</span><span class="sxs-lookup"><span data-stu-id="bac87-133">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="bac87-134">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="bac87-134">The default value is 0.</span></span> |
| <span data-ttu-id="bac87-135">Prozentwert</span><span class="sxs-lookup"><span data-stu-id="bac87-135">percentage</span></span> | <span data-ttu-id="bac87-136">Wert, ausgedrückt als Prozentsatz der Höhe des übergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="bac87-136">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="bac87-137">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="bac87-137">*VML Standard Attribute*</span></span>

<span data-ttu-id="bac87-138">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="bac87-138">**See Also**</span></span>

[<span data-ttu-id="bac87-139">Einheiten</span><span class="sxs-lookup"><span data-stu-id="bac87-139">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="bac87-140">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="bac87-140">**Example**</span></span>

<span data-ttu-id="bac87-141">Der linke Rand ist auf 25 Pixel festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bac87-141">The left margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-left:25px">
   </v:rect>
```



<span data-ttu-id="bac87-142">[Beispiel für das margin-left-Attribut](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples).</span><span class="sxs-lookup"><span data-stu-id="bac87-142">[Margin-Left Attribute Example](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples).</span></span> <span data-ttu-id="bac87-143">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="bac87-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 