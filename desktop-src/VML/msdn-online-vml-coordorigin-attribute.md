---
title: VML coordorigin-Attribut
description: VML coordorigin-Attribut
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb08d35aac7e26cc15aa7699439ea9f7ab4dba94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858280"
---
# <a name="vml-coordorigin-attribute"></a><span data-ttu-id="1416c-103">VML coordorigin-Attribut</span><span class="sxs-lookup"><span data-stu-id="1416c-103">VML CoordOrigin Attribute</span></span>

<span data-ttu-id="1416c-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="1416c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1416c-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="1416c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1416c-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="1416c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1416c-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1416c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1416c-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1416c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1416c-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1416c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1416c-110">Gibt den Koordinaten Einheits Ursprung des Rechtecks an, das eine Form umschließt.</span><span class="sxs-lookup"><span data-stu-id="1416c-110">Specifies the coordinate unit origin of the rectangle that bounds a shape.</span></span> <span data-ttu-id="1416c-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1416c-111">Read/write.</span></span> <span data-ttu-id="1416c-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1416c-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="1416c-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="1416c-113">**Applies To**</span></span>

[<span data-ttu-id="1416c-114">Form</span><span class="sxs-lookup"><span data-stu-id="1416c-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="1416c-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="1416c-115">**Tag Syntax**</span></span>

<span data-ttu-id="1416c-116"><v: *Element* coordorigin = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="1416c-116"><v: *element* coordorigin=" *expression* "></span></span>

<span data-ttu-id="1416c-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="1416c-117">**Script Syntax**</span></span>

<span data-ttu-id="1416c-118">*Element* . coordorigin = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="1416c-118">*element* .coordorigin="*expression*"</span></span>

<span data-ttu-id="1416c-119">*Ausdruck* = *Element*. coordorigin</span><span class="sxs-lookup"><span data-stu-id="1416c-119">*expression*=*element*.coordorigin</span></span>

<span data-ttu-id="1416c-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="1416c-120">**Remarks**</span></span>

<span data-ttu-id="1416c-121">Wenn kein Wert angegeben wird, sind die Ursprungs Koordinaten (0,0) in der oberen linken Ecke des umgebenden Felds der Form.</span><span class="sxs-lookup"><span data-stu-id="1416c-121">If not specified, the origin coordinates are (0,0) at the top left corner of the shape bounding box.</span></span>

<span data-ttu-id="1416c-122">Der x-Wert von **coordsize** wird dem x-Wert von **coordorigin** hinzugefügt, um den Bereich der horizontalen Werte zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="1416c-122">The x value of **CoordSize** is added to the x value of **CoordOrigin** to determine the range of the horizontal values.</span></span> <span data-ttu-id="1416c-123">Wenn der x-Wert von **coordorigin** z. b.-100 und der x-Wert von **coordsize** 200 beträgt, liegen die horizontalen Einheiten zwischen-100 und + 100.</span><span class="sxs-lookup"><span data-stu-id="1416c-123">For example,if the x value of **CoordOrigin** is -100 and the x value of **CoordSize** is 200, the horizontal units will range from -100 to +100.</span></span> <span data-ttu-id="1416c-124">Wenn der x-Wert von **coordorigin** 100 und der x-Wert von **coordsize** 200 ist, reichen die horizontalen Einheiten zwischen 100 und 300, alle innerhalb des umgebenden Felds.</span><span class="sxs-lookup"><span data-stu-id="1416c-124">If the x value of **CoordOrigin** is 100 and the x value of **CoordSize** is 200, the horizontal units will range from 100 to 300, all within the bounding box.</span></span> <span data-ttu-id="1416c-125">Das gleiche gilt für die y-Werte.</span><span class="sxs-lookup"><span data-stu-id="1416c-125">The same is true for the y values.</span></span>

<span data-ttu-id="1416c-126">Beachten Sie, dass es sich bei diesem Attribut um einen Vektor handelt und dass die Einheiten denselben Typ von Einheit wie [coordsize](msdn-online-vml-coordsize-attribute.md) haben.</span><span class="sxs-lookup"><span data-stu-id="1416c-126">Note that this attribute is a vector and that the units are the same type of unit as [CoordSize](msdn-online-vml-coordsize-attribute.md) .</span></span>

<span data-ttu-id="1416c-127">Da es sich hierbei um einen 2-D-Vektor handelt, können Sie bei der Skripterstellung separat auf die x-und y-Werte zugreifen und auch den Typ der erwarteten Einheiten festlegen.</span><span class="sxs-lookup"><span data-stu-id="1416c-127">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="1416c-128">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="1416c-128">*VML Standard Attribute*</span></span>

<span data-ttu-id="1416c-129">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="1416c-129">**Example**</span></span>

<span data-ttu-id="1416c-130">Der Mittelpunkt des umgebenden Felds ist der Ursprung (0,0) des Pfads für die Form.</span><span class="sxs-lookup"><span data-stu-id="1416c-130">The center of the bounding box will be the origin (0,0) of the path for the shape.</span></span> <span data-ttu-id="1416c-131">Da **coordorigin** den Wert "-500-500" und **coordsize** den Wert "1000 1000" hat, reichen die horizontalen und vertikalen Einheiten zwischen-500 und + 500.</span><span class="sxs-lookup"><span data-stu-id="1416c-131">Because **CoordOrigin** is "-500 -500" and **CoordSize** is "1000 1000", the horizontal and vertical units will range from -500 to +500.</span></span> <span data-ttu-id="1416c-132">Die linke und obere Ecke des Pfads befinden sich in der Mitte des umgebenden Felds, das durch den linken und den oberen Punkt definiert wird, wie durch **Style** definiert.</span><span class="sxs-lookup"><span data-stu-id="1416c-132">The left and top corner of the path will be at the center of the bounding box defined by the left and top points as defined by **Style**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="1416c-133">[Beispiel für das coordorigin-Attribut](/previous-versions/bb229664(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1416c-133">[CoordOrigin Attribute Example](/previous-versions/bb229664(v=vs.85)).</span></span> <span data-ttu-id="1416c-134">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="1416c-134">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 