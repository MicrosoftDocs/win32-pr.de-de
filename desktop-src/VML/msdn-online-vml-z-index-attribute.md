---
title: VML-Z-Index-Attribut
description: VML-Z-Index-Attribut
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc358719f3fa15fa40293e40eef924bd248286c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948806"
---
# <a name="vml-z-index-attribute"></a><span data-ttu-id="8f03c-103">VML-Z-Index-Attribut</span><span class="sxs-lookup"><span data-stu-id="8f03c-103">VML Z-Index Attribute</span></span>

<span data-ttu-id="8f03c-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="8f03c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8f03c-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="8f03c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8f03c-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="8f03c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8f03c-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8f03c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8f03c-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8f03c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8f03c-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8f03c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8f03c-110">Bestimmt die Anzeigereihenfolge von überlappenden Formen.</span><span class="sxs-lookup"><span data-stu-id="8f03c-110">Determines the display order of overlapping shapes.</span></span> <span data-ttu-id="8f03c-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8f03c-111">Read/write.</span></span> <span data-ttu-id="8f03c-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="8f03c-112">**String**.</span></span>

<span data-ttu-id="8f03c-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="8f03c-113">**Applies To**</span></span>

[<span data-ttu-id="8f03c-114">Form</span><span class="sxs-lookup"><span data-stu-id="8f03c-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="8f03c-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="8f03c-115">**Tag Syntax**</span></span>

<span data-ttu-id="8f03c-116"><v: *Element* Style = "z-Index: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="8f03c-116"><v: *element* style="z-index: *expression* "></span></span>

<span data-ttu-id="8f03c-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="8f03c-117">**Script Syntax**</span></span>

<span data-ttu-id="8f03c-118">*Element* . Style. ZIndex = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="8f03c-118">*element* .style.zindex="*expression*"</span></span>

<span data-ttu-id="8f03c-119">*Ausdruck* = *Element*. Style. ZIndex</span><span class="sxs-lookup"><span data-stu-id="8f03c-119">*expression*=*element*.style.zindex</span></span>

<span data-ttu-id="8f03c-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="8f03c-120">**Remarks**</span></span>

<span data-ttu-id="8f03c-121">Das **z-Index-** Attribut ähnelt dem standardmäßigen HTML **-z-Index-** Attribut für Stile.</span><span class="sxs-lookup"><span data-stu-id="8f03c-121">The **Z-Index** attribute is similar to the standard HTML **Z-Index** attribute for styles.</span></span>

<span data-ttu-id="8f03c-122">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="8f03c-122">Values include:</span></span>



| <span data-ttu-id="8f03c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8f03c-123">Value</span></span> | <span data-ttu-id="8f03c-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f03c-124">Description</span></span>                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f03c-125">Auto</span><span class="sxs-lookup"><span data-stu-id="8f03c-125">Auto</span></span>  | <span data-ttu-id="8f03c-126">Die Reihenfolge, in der die Formen auf der HTML-Seite angezeigt werden, wird von unten nach oben verwendet.</span><span class="sxs-lookup"><span data-stu-id="8f03c-126">The order that the shapes appear in the HTML page will be used, bottom to top.</span></span>                                                                                                                         |
| <span data-ttu-id="8f03c-127">order</span><span class="sxs-lookup"><span data-stu-id="8f03c-127">order</span></span> | <span data-ttu-id="8f03c-128">Eine Zahl, die die Stapel Rangfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f03c-128">A number that represents the stacking precedence.</span></span> <span data-ttu-id="8f03c-129">Eine Form mit einer höheren Zahl wird so angezeigt, als ob Sie sich überlappen (im "Vordergrund") einer Form mit einer niedrigeren Zahl.</span><span class="sxs-lookup"><span data-stu-id="8f03c-129">A shape with a a higher number will be displayed as if it wereoverlapping (in "front" of) a shape with a lower number.</span></span> <span data-ttu-id="8f03c-130">Negative Zahlen können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f03c-130">Negative numbers can be used.</span></span> |



 

<span data-ttu-id="8f03c-131">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="8f03c-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="8f03c-132">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="8f03c-132">**Example**</span></span>

<span data-ttu-id="8f03c-133">Die rote Form wird in "Front" der blauen Form angezeigt, da Sie einen höheren z-Index aufweist.</span><span class="sxs-lookup"><span data-stu-id="8f03c-133">The red shape will be displayed in "front" of the blue shape, because it has a higher z-index.</span></span>


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



<span data-ttu-id="8f03c-134">[Beispiel für den Z-Index-Attribut](/previous-versions/ms530275(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8f03c-134">[Z-Index Attribute Example](/previous-versions/ms530275(v=vs.85)).</span></span> <span data-ttu-id="8f03c-135">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="8f03c-135">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 