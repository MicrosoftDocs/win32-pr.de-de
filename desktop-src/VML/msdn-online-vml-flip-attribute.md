---
title: VML-Attribut "Kippen"
description: VML-Attribut "Kippen"
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7d17c224ee8ec04a5dcf301ad501de51323efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730145"
---
# <a name="vml-flip-attribute"></a><span data-ttu-id="0b2d6-103">VML-Attribut "Kippen"</span><span class="sxs-lookup"><span data-stu-id="0b2d6-103">VML Flip Attribute</span></span>

<span data-ttu-id="0b2d6-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="0b2d6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0b2d6-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="0b2d6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0b2d6-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="0b2d6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0b2d6-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0b2d6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0b2d6-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0b2d6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0b2d6-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0b2d6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0b2d6-110">Schaltet die Ausrichtung einer Form um.</span><span class="sxs-lookup"><span data-stu-id="0b2d6-110">Switches the orientation of a shape.</span></span> <span data-ttu-id="0b2d6-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0b2d6-111">Read/write.</span></span> <span data-ttu-id="0b2d6-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="0b2d6-112">**String**.</span></span>

<span data-ttu-id="0b2d6-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="0b2d6-113">**Applies To**</span></span>

[<span data-ttu-id="0b2d6-114">Form</span><span class="sxs-lookup"><span data-stu-id="0b2d6-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="0b2d6-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="0b2d6-115">**Tag Syntax**</span></span>

<span data-ttu-id="0b2d6-116"><v: *Element* Style = "Flip: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="0b2d6-116"><v: *element* style="flip: *expression* "></span></span>

<span data-ttu-id="0b2d6-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="0b2d6-117">**Script Syntax**</span></span>

<span data-ttu-id="0b2d6-118">*Element* . Style. Flip = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="0b2d6-118">*element* .style.flip="*expression*"</span></span>

<span data-ttu-id="0b2d6-119">*Ausdruck* = *Element*. Style. Flip</span><span class="sxs-lookup"><span data-stu-id="0b2d6-119">*expression*=*element*.style.flip</span></span>

<span data-ttu-id="0b2d6-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="0b2d6-120">**Remarks**</span></span>

<span data-ttu-id="0b2d6-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="0b2d6-121">Values include:</span></span>



| <span data-ttu-id="0b2d6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0b2d6-122">Value</span></span> | <span data-ttu-id="0b2d6-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b2d6-123">Description</span></span>                                           |
|-------|-------------------------------------------------------|
| <span data-ttu-id="0b2d6-124">x</span><span class="sxs-lookup"><span data-stu-id="0b2d6-124">x</span></span>     | <span data-ttu-id="0b2d6-125">Kippen Sie entlang der y-Achse, und umkehren Sie die *x*-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="0b2d6-125">Flip along the y-axis, reversing the *x*-coordinates.</span></span> |
| <span data-ttu-id="0b2d6-126">Y</span><span class="sxs-lookup"><span data-stu-id="0b2d6-126">y</span></span>     | <span data-ttu-id="0b2d6-127">Kippen Sie entlang der *x*-Achse, und umkehren Sie die y-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="0b2d6-127">Flip along the *x*-axis, reversing the y-coordinates.</span></span> |
| <span data-ttu-id="0b2d6-128">xy</span><span class="sxs-lookup"><span data-stu-id="0b2d6-128">xy</span></span>    | <span data-ttu-id="0b2d6-129">Kippen Sie sowohl auf die y-als auch auf die *x*-Achse.</span><span class="sxs-lookup"><span data-stu-id="0b2d6-129">Flip along both the y- and *x*-axis.</span></span>                  |
| <span data-ttu-id="0b2d6-130">YX</span><span class="sxs-lookup"><span data-stu-id="0b2d6-130">yx</span></span>    | <span data-ttu-id="0b2d6-131">Kippen Sie entlang der *x*-und *y*-Achse.</span><span class="sxs-lookup"><span data-stu-id="0b2d6-131">Flip along both the *x*- and *y*-axis.</span></span>                |



 

<span data-ttu-id="0b2d6-132">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="0b2d6-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="0b2d6-133">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="0b2d6-133">**See Also**</span></span>

[<span data-ttu-id="0b2d6-134">Vgfliporientation</span><span class="sxs-lookup"><span data-stu-id="0b2d6-134">VgFlipOrientation</span></span>](msdn-online-vector-markup-language-object-model-reference.md)

<span data-ttu-id="0b2d6-135">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="0b2d6-135">**Example**</span></span>

<span data-ttu-id="0b2d6-136">Die Form wird entlang der *y* -Achse durch Umkehren der *x* -Koordinaten gekippt.</span><span class="sxs-lookup"><span data-stu-id="0b2d6-136">The shape is flipped along the *y* -axis by reversing the *x* -coordinates.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



<span data-ttu-id="0b2d6-137">[Beispiel](/previous-versions/bb229670(v=vs.85))für das Flip-Attribut.</span><span class="sxs-lookup"><span data-stu-id="0b2d6-137">[Flip Attribute Example](/previous-versions/bb229670(v=vs.85)).</span></span> <span data-ttu-id="0b2d6-138">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="0b2d6-138">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 