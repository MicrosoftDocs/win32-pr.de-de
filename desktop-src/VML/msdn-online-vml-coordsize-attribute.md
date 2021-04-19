---
title: VML coordsize-Attribut
description: VML coordsize-Attribut
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e1fee484071c04c7184e0f200aed9b52aadf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341939"
---
# <a name="vml-coordsize-attribute"></a><span data-ttu-id="3a566-103">VML coordsize-Attribut</span><span class="sxs-lookup"><span data-stu-id="3a566-103">VML CoordSize Attribute</span></span>

<span data-ttu-id="3a566-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="3a566-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3a566-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="3a566-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3a566-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="3a566-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3a566-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3a566-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3a566-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3a566-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3a566-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3a566-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3a566-110">Gibt die horizontalen und vertikalen Einheiten des Rechtecks an, das eine Form umschließt.</span><span class="sxs-lookup"><span data-stu-id="3a566-110">Specifies the horizontal and vertical units of the rectangle that bounds a shape.</span></span> <span data-ttu-id="3a566-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3a566-111">Read/write.</span></span> <span data-ttu-id="3a566-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3a566-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="3a566-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="3a566-113">**Applies To**</span></span>

[<span data-ttu-id="3a566-114">Form</span><span class="sxs-lookup"><span data-stu-id="3a566-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3a566-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="3a566-115">**Tag Syntax**</span></span>

<span data-ttu-id="3a566-116"><v: *Element* coordsize = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3a566-116"><v: *element* coordsize=" *expression* "></span></span>

<span data-ttu-id="3a566-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="3a566-117">**Script Syntax**</span></span>

<span data-ttu-id="3a566-118">*Element* . coordsize = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="3a566-118">*element* .coordsize="*expression*"</span></span>

<span data-ttu-id="3a566-119">*Ausdruck* = *Element*. coordsize</span><span class="sxs-lookup"><span data-stu-id="3a566-119">*expression*=*element*.coordsize</span></span>

<span data-ttu-id="3a566-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="3a566-120">**Remarks**</span></span>

<span data-ttu-id="3a566-121">Wenn nicht angegeben, ist die Koordinaten Größe mit dem umgebenden Feld der Form identisch.</span><span class="sxs-lookup"><span data-stu-id="3a566-121">If not specified, the coordinate size is the same as the bounding box of the shape.</span></span>

<span data-ttu-id="3a566-122">Beachten Sie, dass es sich bei diesem Attribut um einen Vektor handelt und dass die Einheiten relativ zur Länge und Breite des umgebenden Rechtecks sind.</span><span class="sxs-lookup"><span data-stu-id="3a566-122">Note that this attribute is a vector and that the units are relative to the length and width of the bounding rectangle.</span></span>

<span data-ttu-id="3a566-123">Beachten Sie auch, dass die Zuordnung zwischen **coordsize** und dem umgebenden Feld zu einem anisotrope gemacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="3a566-123">Also note that mapping between **coordsize** and the bounding box can be made anisotropic.</span></span> <span data-ttu-id="3a566-124">Stellen Sie sicher, dass die **Breite** und die Höhe von **coordsize** mit der **Breite und** **Höhe** des Formats identisch sind, wenn Sie die Form nicht verzerren möchten.</span><span class="sxs-lookup"><span data-stu-id="3a566-124">Make sure that the **coordsize width** and **coordsize height** is the same as the **style width** and **height** if you don't want to distort the shape.</span></span>

<span data-ttu-id="3a566-125">Da es sich hierbei um einen 2-D-Vektor handelt, können Sie bei der Skripterstellung separat auf die x-und y-Werte zugreifen und auch den Typ der erwarteten Einheiten festlegen.</span><span class="sxs-lookup"><span data-stu-id="3a566-125">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="3a566-126">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="3a566-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="3a566-127">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3a566-127">**Example**</span></span>

<span data-ttu-id="3a566-128">Die Form ist 100 Punkte hoch und 100 Punkte breit, aber jede horizontale und vertikale Einheit im Koordinaten Bereich ist 1/10 eines Punkts.</span><span class="sxs-lookup"><span data-stu-id="3a566-128">The shape is 100 points high and 100 points wide, but each horizontal and vertical unit in the coordinate space is 1/10 of a point.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="3a566-129">[Beispiel für das coordsize-Attribut](/previous-versions/bb229665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a566-129">[CoordSize Attribute Example](/previous-versions/bb229665(v=vs.85)).</span></span> <span data-ttu-id="3a566-130">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="3a566-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 