---
title: Origin-Attribut (Fill) (VML)
description: Origin-Attribut (Fill) (VML)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1d26f5e544ffa19b347ceec1549885c1ff6b90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390969"
---
# <a name="origin-attribute-fillvml"></a><span data-ttu-id="32a66-103">Origin-Attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="32a66-103">Origin Attribute (Fill)(VML)</span></span>

<span data-ttu-id="32a66-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="32a66-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="32a66-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="32a66-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="32a66-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="32a66-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="32a66-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="32a66-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="32a66-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="32a66-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="32a66-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="32a66-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="32a66-110">Definiert den Mittelpunkt eines Füllbilds.</span><span class="sxs-lookup"><span data-stu-id="32a66-110">Defines the center of a fill image.</span></span> <span data-ttu-id="32a66-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="32a66-111">Read/write.</span></span> <span data-ttu-id="32a66-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="32a66-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="32a66-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="32a66-113">**Applies To**</span></span>

[<span data-ttu-id="32a66-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="32a66-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="32a66-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="32a66-115">**Tag Syntax**</span></span>

<span data-ttu-id="32a66-116"><v: *Element* Origin = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="32a66-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="32a66-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="32a66-117">**Script Syntax**</span></span>

<span data-ttu-id="32a66-118">*Element* . Origin = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="32a66-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="32a66-119">*Ausdruck* = *Element*. Origin</span><span class="sxs-lookup"><span data-stu-id="32a66-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="32a66-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="32a66-120">**Remarks**</span></span>

<span data-ttu-id="32a66-121">Gibt einen Punkt relativ zur oberen linken Ecke des Bilds an. Dieser Punkt wird als der Ursprung des Bilds behandelt.</span><span class="sxs-lookup"><span data-stu-id="32a66-121">Specifies a point relative to the upper left corner of the image; this point is treated as the origin of the image.</span></span> <span data-ttu-id="32a66-122">Der Standardwert ist der Mittelpunkt des Bilds.</span><span class="sxs-lookup"><span data-stu-id="32a66-122">Default is the center of the image.</span></span> <span data-ttu-id="32a66-123">Der Vektor ist ein Bruchteil der Breite und Höhe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="32a66-123">The vector is a fraction of the width and height of the image.</span></span>

<span data-ttu-id="32a66-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="32a66-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="32a66-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="32a66-125">**Example**</span></span>

<span data-ttu-id="32a66-126">Das Bild der Füllung wird nach Links zu einem Punkt 50% der Breite der Form verschoben.</span><span class="sxs-lookup"><span data-stu-id="32a66-126">The image of the fill is shifted left to a point 50% of the width of the shape .</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 