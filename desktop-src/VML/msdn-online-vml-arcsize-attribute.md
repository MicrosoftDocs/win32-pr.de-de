---
title: VML-arcsize-Attribut
description: VML-arcsize-Attribut
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a4027f079ffb284125032570dd2293b1ab69e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337658"
---
# <a name="vml-arcsize-attribute"></a><span data-ttu-id="95201-103">VML-arcsize-Attribut</span><span class="sxs-lookup"><span data-stu-id="95201-103">VML ArcSize Attribute</span></span>

<span data-ttu-id="95201-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="95201-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="95201-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="95201-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="95201-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="95201-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="95201-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="95201-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="95201-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="95201-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="95201-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="95201-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="95201-110">Definiert die Menge der roundness für ein abgerundetes Rechteck.</span><span class="sxs-lookup"><span data-stu-id="95201-110">Defines the amount of roundness for a rounded rectangle.</span></span> <span data-ttu-id="95201-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="95201-111">Read/write.</span></span> <span data-ttu-id="95201-112">[Vgbruchteile](msdn-online-vml-vgfraction-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="95201-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span></span>

<span data-ttu-id="95201-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="95201-113">**Applies To**</span></span>

[<span data-ttu-id="95201-114">RoundRect</span><span class="sxs-lookup"><span data-stu-id="95201-114">RoundRect</span></span>](msdn-online-vml-roundrect-element.md)

<span data-ttu-id="95201-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="95201-115">**Tag Syntax**</span></span>

<span data-ttu-id="95201-116"><v: *Element* arcsize = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="95201-116"><v: *element* arcsize=" *expression* "></span></span>

<span data-ttu-id="95201-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="95201-117">**Script Syntax**</span></span>

<span data-ttu-id="95201-118">*Element* . arcsize = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="95201-118">*element* .arcSize="*expression*"</span></span>

<span data-ttu-id="95201-119">*Ausdruck* = *Element*. arcsize</span><span class="sxs-lookup"><span data-stu-id="95201-119">*expression*=*element*.arcSize</span></span>

<span data-ttu-id="95201-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="95201-120">**Remarks**</span></span>

<span data-ttu-id="95201-121">Definiert die abgerundeten Ecken eines gerundeten Rechtecks als Prozentsatz der Hälfte der kleineren Dimension der Länge und Breite eines Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="95201-121">Defines the rounded corners of a rounded rectangle as a percentage of half the smaller dimension of the length and width of a rectangle.</span></span> <span data-ttu-id="95201-122">0% hätte quadratische Ecken, und 100% würde kreisförmige Ecken bilden.</span><span class="sxs-lookup"><span data-stu-id="95201-122">0% would have square corners, and 100% would form circular corners.</span></span> <span data-ttu-id="95201-123">Ein Quadrat mit einem **arcsize** -Wert von 1,0 wäre ein Kreis.</span><span class="sxs-lookup"><span data-stu-id="95201-123">A square with an **ArcSize** value of 1.0 would be a circle.</span></span> <span data-ttu-id="95201-124">Der Standardwert ist 0,2 (20%).</span><span class="sxs-lookup"><span data-stu-id="95201-124">The default value is 0.2 (20%).</span></span>

<span data-ttu-id="95201-125">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="95201-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="95201-126">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="95201-126">**Example**</span></span>

<span data-ttu-id="95201-127">Das abgerundete Rechteck wird mit engen, aber abgerundeten Ecken gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="95201-127">The rounded rectangle is drawn with tight-but-rounded corners.</span></span>


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 