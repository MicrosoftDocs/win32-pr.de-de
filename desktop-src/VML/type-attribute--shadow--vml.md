---
title: Type-Attribut (Schatten) (VML)
description: Type-Attribut (Schatten) (VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea4fb54c04847a8ed5c4446cfb999f74161aa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390665"
---
# <a name="type-attribute-shadowvml"></a><span data-ttu-id="22327-103">Type-Attribut (Schatten) (VML)</span><span class="sxs-lookup"><span data-stu-id="22327-103">Type Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="22327-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="22327-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="22327-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="22327-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="22327-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="22327-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="22327-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="22327-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="22327-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="22327-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="22327-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="22327-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="22327-110">Gibt den Typ des Schattens an.</span><span class="sxs-lookup"><span data-stu-id="22327-110">Specifies the type of shadow.</span></span> <span data-ttu-id="22327-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="22327-111">Read/write.</span></span> <span data-ttu-id="22327-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="22327-112">**String**.</span></span>

<span data-ttu-id="22327-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="22327-113">**Applies To**</span></span>

[<span data-ttu-id="22327-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="22327-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="22327-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="22327-115">**Tag Syntax**</span></span>

<span data-ttu-id="22327-116"><v: *Elementtyp* = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="22327-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="22327-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="22327-117">**Script Syntax**</span></span>

<span data-ttu-id="22327-118">*Element* . Type = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="22327-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="22327-119">*Ausdruck* = *Element*. Type</span><span class="sxs-lookup"><span data-stu-id="22327-119">*expression*=*element*.type</span></span>

<span data-ttu-id="22327-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="22327-120">**Remarks**</span></span>

<span data-ttu-id="22327-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="22327-121">Values include:</span></span>



| <span data-ttu-id="22327-122">Wert</span><span class="sxs-lookup"><span data-stu-id="22327-122">Value</span></span>           | <span data-ttu-id="22327-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22327-123">Description</span></span>                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22327-124">single</span><span class="sxs-lookup"><span data-stu-id="22327-124">single</span></span>          | <span data-ttu-id="22327-125">Einzelner Schatten.</span><span class="sxs-lookup"><span data-stu-id="22327-125">Single shadow.</span></span> <span data-ttu-id="22327-126">Standard.</span><span class="sxs-lookup"><span data-stu-id="22327-126">Default.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="22327-127">double</span><span class="sxs-lookup"><span data-stu-id="22327-127">double</span></span>          | <span data-ttu-id="22327-128">Ein doppelter Schatten.</span><span class="sxs-lookup"><span data-stu-id="22327-128">A double shadow.</span></span> <span data-ttu-id="22327-129">[Color2](color2-attribute--shadow--vml.md) wird für die Farbe des zweiten Schattens verwendet, und [Offset2](msdn-online-vml-offset2-attribute.md) wird für den Offset des zweiten Schattens verwendet.</span><span class="sxs-lookup"><span data-stu-id="22327-129">[Color2](color2-attribute--shadow--vml.md) is used for the color of the second shadow and [Offset2](msdn-online-vml-offset2-attribute.md) is used for the second shadow's offset.</span></span> |
| <span data-ttu-id="22327-130">Perspektive</span><span class="sxs-lookup"><span data-stu-id="22327-130">perspective</span></span>     | <span data-ttu-id="22327-131">Ein Perspektiven Schatten.</span><span class="sxs-lookup"><span data-stu-id="22327-131">A perspective shadow.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="22327-132">shaperelative</span><span class="sxs-lookup"><span data-stu-id="22327-132">shapeRelative</span></span>   | <span data-ttu-id="22327-133">Der Schatten wird relativ zur Form erstellt.</span><span class="sxs-lookup"><span data-stu-id="22327-133">The shadow is created relative to the shape.</span></span>                                                                                                                                                         |
| <span data-ttu-id="22327-134">drawingrelative</span><span class="sxs-lookup"><span data-stu-id="22327-134">drawingRelative</span></span> | <span data-ttu-id="22327-135">Der Schatten wird relativ zum Zeichnen erstellt.</span><span class="sxs-lookup"><span data-stu-id="22327-135">The shadow is created relative to the drawing.</span></span>                                                                                                                                                       |
| <span data-ttu-id="22327-136">Prägung</span><span class="sxs-lookup"><span data-stu-id="22327-136">emboss</span></span>          | <span data-ttu-id="22327-137">Der Schatten hat ein geprägte aussehen.</span><span class="sxs-lookup"><span data-stu-id="22327-137">The shadow has an embossed look.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="22327-138">**VML-Standard Attribut**</span><span class="sxs-lookup"><span data-stu-id="22327-138">**VML Standard Attribute**</span></span>

<span data-ttu-id="22327-139">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="22327-139">**Example**</span></span>

<span data-ttu-id="22327-140">Ein doppelter Schatten wird mit dem zweiten Schatten grün und Offset 5 nach unten und nach rechts erstellt.</span><span class="sxs-lookup"><span data-stu-id="22327-140">A double shadow is created with the second shadow green and offset 5 points down and to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 