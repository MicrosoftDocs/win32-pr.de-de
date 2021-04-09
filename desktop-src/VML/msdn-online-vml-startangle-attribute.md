---
title: VML-startAngle-Attribut
description: VML-startAngle-Attribut
ms.assetid: 334ae52a-cde4-427e-8080-ec789b4d9d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e779d343061ef65decb1dd21f615e054d561da28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039235"
---
# <a name="vml-startangle-attribute"></a><span data-ttu-id="aa837-103">VML-startAngle-Attribut</span><span class="sxs-lookup"><span data-stu-id="aa837-103">VML StartAngle Attribute</span></span>

<span data-ttu-id="aa837-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="aa837-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="aa837-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="aa837-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="aa837-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="aa837-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="aa837-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="aa837-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="aa837-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="aa837-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="aa837-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="aa837-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="aa837-110">Definiert den Anfangspunkt des Bogens. Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="aa837-110">Defines the starting point of the arc. Read/write.</span></span> <span data-ttu-id="aa837-111">[Vganglin Grad](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="aa837-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="aa837-112">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="aa837-112">**Applies To**</span></span>

[<span data-ttu-id="aa837-113">Arc</span><span class="sxs-lookup"><span data-stu-id="aa837-113">Arc</span></span>](msdn-online-vml-arc-element.md)

<span data-ttu-id="aa837-114">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="aa837-114">**Tag Syntax**</span></span>

<span data-ttu-id="aa837-115"><v: *Element* EndAngle = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="aa837-115"><v: *element* endangle=" *expression* "></span></span>

<span data-ttu-id="aa837-116">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="aa837-116">**Script Syntax**</span></span>

<span data-ttu-id="aa837-117">*Element* . EndAngle = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="aa837-117">*element* .endAngle="*expression*"</span></span>

<span data-ttu-id="aa837-118">*Ausdruck* = *Element*. EndAngle</span><span class="sxs-lookup"><span data-stu-id="aa837-118">*expression*=*element*.endAngle</span></span>

<span data-ttu-id="aa837-119">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="aa837-119">**Remarks**</span></span>

<span data-ttu-id="aa837-120">Der Bogen wird als ein durch ein Oval gezeichneter Strich definiert, der durch die **Stil** Attribute einer Form begrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="aa837-120">The arc is defined as a stroke drawn along an oval bounded by the **Style** attributes of a shape.</span></span> <span data-ttu-id="aa837-121">Der Anfang des Strichs wird durch einen Winkel definiert, der von der geraden im Uhrzeigersinn (12 Uhr) gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="aa837-121">The start of the stroke is defined by an angle measured from straight up (12 o'clock) clockwise.</span></span> <span data-ttu-id="aa837-122">Der Standardwert ist 0 Grad.</span><span class="sxs-lookup"><span data-stu-id="aa837-122">The default value is 0 degrees.</span></span>

<span data-ttu-id="aa837-123">VML-Standard Attribut</span><span class="sxs-lookup"><span data-stu-id="aa837-123">VML Standard Attribute</span></span>

<span data-ttu-id="aa837-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="aa837-124">**Example**</span></span>

<span data-ttu-id="aa837-125">Der Bogen ist Lächeln.</span><span class="sxs-lookup"><span data-stu-id="aa837-125">The arc is smiling.</span></span> <span data-ttu-id="aa837-126">Der Startpunkt befindet sich am 90-Grad-Punkt eines Oval, das innerhalb des umgebenden Felds der Form verankert ist.</span><span class="sxs-lookup"><span data-stu-id="aa837-126">The start point is at the 90-degree point of an oval inscribed inside the shape bounding box.</span></span> <span data-ttu-id="aa837-127">Der Endpunkt befindet sich am 270-Grad-Punkt der Oval.</span><span class="sxs-lookup"><span data-stu-id="aa837-127">The end point is at the 270-degree point of the oval.</span></span>


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 