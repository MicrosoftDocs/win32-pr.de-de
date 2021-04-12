---
title: VML FillType-Attribut
description: VML FillType-Attribut
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e880f7d13c7db647c586431f492a301ccf1aba0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949092"
---
# <a name="vml-filltype-attribute"></a><span data-ttu-id="f1f82-103">VML FillType-Attribut</span><span class="sxs-lookup"><span data-stu-id="f1f82-103">VML FillType Attribute</span></span>

<span data-ttu-id="f1f82-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="f1f82-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f1f82-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="f1f82-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f1f82-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="f1f82-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f1f82-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="f1f82-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f1f82-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f1f82-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f1f82-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f1f82-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f1f82-110">Definiert den Fülltyp, der für den Hintergrund eines Strichs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1f82-110">Defines the type of fill used for the background of a stroke.</span></span> <span data-ttu-id="f1f82-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f1f82-111">Read/write.</span></span> <span data-ttu-id="f1f82-112">**Vgfilltype**.</span><span class="sxs-lookup"><span data-stu-id="f1f82-112">**VgFillType**.</span></span>

<span data-ttu-id="f1f82-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="f1f82-113">**Applies To**</span></span>

[<span data-ttu-id="f1f82-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="f1f82-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="f1f82-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="f1f82-115">**Tag Syntax**</span></span>

<span data-ttu-id="f1f82-116"><v: *Element* FillType = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="f1f82-116"><v: *element* filltype=" *expression* "></span></span>

<span data-ttu-id="f1f82-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="f1f82-117">**Script Syntax**</span></span>

<span data-ttu-id="f1f82-118">*Element* . FillType = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="f1f82-118">*element* .filltype="*expression*"</span></span>

<span data-ttu-id="f1f82-119">*Ausdruck* = *Element*. FillType</span><span class="sxs-lookup"><span data-stu-id="f1f82-119">*expression*=*element*.filltype</span></span>

<span data-ttu-id="f1f82-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="f1f82-120">**Remarks**</span></span>

<span data-ttu-id="f1f82-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="f1f82-121">Values include:</span></span>



| <span data-ttu-id="f1f82-122">DashStyle</span><span class="sxs-lookup"><span data-stu-id="f1f82-122">DashStyle</span></span> | <span data-ttu-id="f1f82-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1f82-123">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="f1f82-124">Basis</span><span class="sxs-lookup"><span data-stu-id="f1f82-124">Solid</span></span>     | <span data-ttu-id="f1f82-125">Das Füllmuster ist vollständig.</span><span class="sxs-lookup"><span data-stu-id="f1f82-125">The fill pattern is solid.</span></span> <span data-ttu-id="f1f82-126">Standardwert.</span><span class="sxs-lookup"><span data-stu-id="f1f82-126">Default value.</span></span>      |
| <span data-ttu-id="f1f82-127">Tile</span><span class="sxs-lookup"><span data-stu-id="f1f82-127">Tile</span></span>      | <span data-ttu-id="f1f82-128">Das Füllbild wird gekachelt.</span><span class="sxs-lookup"><span data-stu-id="f1f82-128">The fill image is tiled.</span></span>                       |
| <span data-ttu-id="f1f82-129">Muster</span><span class="sxs-lookup"><span data-stu-id="f1f82-129">Pattern</span></span>   | <span data-ttu-id="f1f82-130">Das Füllbild wird gestreckt, um ein Muster zu bilden.</span><span class="sxs-lookup"><span data-stu-id="f1f82-130">The fill image is stretched to form a pattern.</span></span> |
| <span data-ttu-id="f1f82-131">Frame</span><span class="sxs-lookup"><span data-stu-id="f1f82-131">Frame</span></span>     | <span data-ttu-id="f1f82-132">Das Füllbild wird zu einem Rahmen für die Form.</span><span class="sxs-lookup"><span data-stu-id="f1f82-132">The fill image becomes a border for the shape.</span></span> |



 

<span data-ttu-id="f1f82-133">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="f1f82-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="f1f82-134">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f1f82-134">**Example**</span></span>

<span data-ttu-id="f1f82-135">Der Strich der Form hat eine Kachel, die aus dem cylinder.gif Bild erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f1f82-135">The stroke of the shape has a tiled texture created from the cylinder.gif image.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 