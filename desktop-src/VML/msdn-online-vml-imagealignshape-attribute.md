---
title: VML imagealignshape-Attribut
description: VML imagealignshape-Attribut
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82aaab9c4c470b41bcf9fdb96ee2c048a7d0b81d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315620"
---
# <a name="vml-imagealignshape-attribute"></a><span data-ttu-id="21893-103">VML imagealignshape-Attribut</span><span class="sxs-lookup"><span data-stu-id="21893-103">VML ImageAlignShape Attribute</span></span>

<span data-ttu-id="21893-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="21893-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="21893-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="21893-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="21893-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="21893-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="21893-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="21893-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="21893-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="21893-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="21893-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="21893-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="21893-110">Bestimmt die Ausrichtung des Strich Bilds.</span><span class="sxs-lookup"><span data-stu-id="21893-110">Determines the alignment of the stroke image.</span></span> <span data-ttu-id="21893-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="21893-111">Read/write.</span></span> <span data-ttu-id="21893-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="21893-112">**VgTriState**.</span></span>

<span data-ttu-id="21893-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="21893-113">**Applies To**</span></span>

[<span data-ttu-id="21893-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="21893-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="21893-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="21893-115">**Tag Syntax**</span></span>

<span data-ttu-id="21893-116"><v:</span><span class="sxs-lookup"><span data-stu-id="21893-116"><v:</span></span>

<span data-ttu-id="21893-117">Element *imagealignshape = "* Expression *" #b0*</span><span class="sxs-lookup"><span data-stu-id="21893-117">element *imagealignshape="* expression *">*</span></span>

<span data-ttu-id="21893-118">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="21893-118">**Script Syntax**</span></span>

<span data-ttu-id="21893-119">Element *. imagealignshape = "* Ausdruck *"*</span><span class="sxs-lookup"><span data-stu-id="21893-119">element *.imagealignshape="* expression *"*</span></span>

<span data-ttu-id="21893-120">Expression- *=* Element *. imagealignshape*</span><span class="sxs-lookup"><span data-stu-id="21893-120">expression *=* element *.imagealignshape*</span></span>

<span data-ttu-id="21893-121">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="21893-121">**Remarks**</span></span>

<span data-ttu-id="21893-122">Wenn **true**, wird das Bild mit der Form ausgerichtet, andernfalls wird das Bild an das Fenster ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="21893-122">If **True**, align the image with the shape, else align the image with the window.</span></span> <span data-ttu-id="21893-123">Der Standardwert ist **True**.</span><span class="sxs-lookup"><span data-stu-id="21893-123">The default is **True**.</span></span>

<span data-ttu-id="21893-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="21893-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="21893-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="21893-125">**Example**</span></span>

<span data-ttu-id="21893-126">Das Bild wird am Fenster ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="21893-126">The image is aligned with the window.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 