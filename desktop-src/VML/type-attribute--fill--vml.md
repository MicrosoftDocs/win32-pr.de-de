---
title: Type-Attribut (Fill) (VML)
description: Type-Attribut (Fill) (VML)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb40999b9596a41a8469e586dcc8a7f934577e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728808"
---
# <a name="type-attribute-fillvml"></a><span data-ttu-id="746bf-103">Type-Attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="746bf-103">Type Attribute (Fill)(VML)</span></span>

<span data-ttu-id="746bf-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="746bf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="746bf-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="746bf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="746bf-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="746bf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="746bf-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="746bf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="746bf-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="746bf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="746bf-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="746bf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="746bf-110">Bestimmt den Fülltyp.</span><span class="sxs-lookup"><span data-stu-id="746bf-110">Determines the type of fill.</span></span> <span data-ttu-id="746bf-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="746bf-111">Read/write.</span></span> <span data-ttu-id="746bf-112">**Vgfilltype**.</span><span class="sxs-lookup"><span data-stu-id="746bf-112">**VgFillType**.</span></span>

<span data-ttu-id="746bf-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="746bf-113">**Applies To**</span></span>

[<span data-ttu-id="746bf-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="746bf-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="746bf-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="746bf-115">**Tag Syntax**</span></span>

<span data-ttu-id="746bf-116"><v: *Elementtyp* = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="746bf-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="746bf-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="746bf-117">**Script Syntax**</span></span>

<span data-ttu-id="746bf-118">*Element* . Type = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="746bf-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="746bf-119">*Ausdruck* = *Element*. Type</span><span class="sxs-lookup"><span data-stu-id="746bf-119">*expression*=*element*.type</span></span>

<span data-ttu-id="746bf-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="746bf-120">**Remarks**</span></span>

<span data-ttu-id="746bf-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="746bf-121">Values include:</span></span>



| <span data-ttu-id="746bf-122">type</span><span class="sxs-lookup"><span data-stu-id="746bf-122">Type</span></span>           | <span data-ttu-id="746bf-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="746bf-123">Description</span></span>                                                             |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="746bf-124">festem</span><span class="sxs-lookup"><span data-stu-id="746bf-124">solid</span></span>          | <span data-ttu-id="746bf-125">Das Füllmuster ist vollständig.</span><span class="sxs-lookup"><span data-stu-id="746bf-125">The fill pattern is solid.</span></span> <span data-ttu-id="746bf-126">Standard.</span><span class="sxs-lookup"><span data-stu-id="746bf-126">Default.</span></span>                                     |
| <span data-ttu-id="746bf-127">Farbverlauf</span><span class="sxs-lookup"><span data-stu-id="746bf-127">gradient</span></span>       | <span data-ttu-id="746bf-128">Die Füll Farben vermischen sich in einem linearen Farbverlauf von unten nach oben.</span><span class="sxs-lookup"><span data-stu-id="746bf-128">The fill colors blend together in a linear gradient from bottom to top.</span></span> |
| <span data-ttu-id="746bf-129">gradientradiale</span><span class="sxs-lookup"><span data-stu-id="746bf-129">gradientradial</span></span> | <span data-ttu-id="746bf-130">Die Füllfarben werden in einem radialen Farbverlauf miteinander verknüpft.</span><span class="sxs-lookup"><span data-stu-id="746bf-130">The fill colors blend together in a radial gradient.</span></span>                    |
| <span data-ttu-id="746bf-131">tile</span><span class="sxs-lookup"><span data-stu-id="746bf-131">tile</span></span>           | <span data-ttu-id="746bf-132">Das Füllbild wird gekachelt.</span><span class="sxs-lookup"><span data-stu-id="746bf-132">The fill image is tiled.</span></span>                                                |
| <span data-ttu-id="746bf-133">pattern</span><span class="sxs-lookup"><span data-stu-id="746bf-133">pattern</span></span>        | <span data-ttu-id="746bf-134">Das Bild wird zum Erstellen eines Musters mithilfe der Füllfarben verwendet.</span><span class="sxs-lookup"><span data-stu-id="746bf-134">The image is used to create a pattern using the fill colors.</span></span>            |
| <span data-ttu-id="746bf-135">frame</span><span class="sxs-lookup"><span data-stu-id="746bf-135">frame</span></span>          | <span data-ttu-id="746bf-136">Das Bild wird gestreckt, um die Form auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="746bf-136">The image is stretched to fill the shape.</span></span>                               |



 

<span data-ttu-id="746bf-137">**VML-Standard Attribut**</span><span class="sxs-lookup"><span data-stu-id="746bf-137">**VML Standard Attribute**</span></span>

<span data-ttu-id="746bf-138">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="746bf-138">**Example**</span></span>

<span data-ttu-id="746bf-139">Eine rote Vordergrund-und blaue Hintergrund Füllung wird mithilfe des Musters der Bild myimage.gif erstellt.</span><span class="sxs-lookup"><span data-stu-id="746bf-139">A red foreground and blue background fill is created using the pattern of the image myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 