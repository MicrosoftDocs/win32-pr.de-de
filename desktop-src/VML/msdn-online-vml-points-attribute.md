---
title: VML-Punkte Attribut
description: VML-Punkte Attribut
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039085"
---
# <a name="vml-points-attribute"></a><span data-ttu-id="ed61c-103">VML-Punkte Attribut</span><span class="sxs-lookup"><span data-stu-id="ed61c-103">VML Points Attribute</span></span>

<span data-ttu-id="ed61c-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="ed61c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ed61c-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="ed61c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ed61c-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="ed61c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ed61c-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ed61c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ed61c-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ed61c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ed61c-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ed61c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ed61c-110">Definiert einen Satz von Punkten, die eine Polylinie bilden.</span><span class="sxs-lookup"><span data-stu-id="ed61c-110">Defines a set of points that make up a polyline.</span></span> <span data-ttu-id="ed61c-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ed61c-111">Read/write.</span></span> <span data-ttu-id="ed61c-112">[Ivgpoints](msdn-online-vml-ivgpoints-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="ed61c-112">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .</span></span>

<span data-ttu-id="ed61c-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="ed61c-113">**Applies To**</span></span>

[<span data-ttu-id="ed61c-114">Polylinie</span><span class="sxs-lookup"><span data-stu-id="ed61c-114">Polyline</span></span>](msdn-online-vml-polyline-element.md)

<span data-ttu-id="ed61c-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="ed61c-115">**Tag Syntax**</span></span>

<span data-ttu-id="ed61c-116"><v: *Element* Points = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="ed61c-116"><v: *element* points=" *expression* "></span></span>

<span data-ttu-id="ed61c-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="ed61c-117">**Script Syntax**</span></span>

<span data-ttu-id="ed61c-118">*Element* . Points = "*Ausdruck \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="ed61c-118">*element* .points="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="ed61c-119">*Ausdruck* = *Element*. Points</span><span class="sxs-lookup"><span data-stu-id="ed61c-119">*expression*=*element*.points</span></span>

<span data-ttu-id="ed61c-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="ed61c-120">**Remarks**</span></span>

<span data-ttu-id="ed61c-121">Definiert einen Satz von geraden Liniensegmenten, die aus einer Reihe von Punkten bestehen.</span><span class="sxs-lookup"><span data-stu-id="ed61c-121">Defines a set of straight line segments that are composed of a series of points.</span></span> <span data-ttu-id="ed61c-122">Wenn das übergeordnete Element kein VML-Element ist, ist die Standard [Einheit](msdn-online-vml-units.md) ein Pixel (in, cm, mm, PT, kann jedoch auch der PC angegeben werden).</span><span class="sxs-lookup"><span data-stu-id="ed61c-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="ed61c-123">Der Standardwert ist "0, 0 10, 10".</span><span class="sxs-lookup"><span data-stu-id="ed61c-123">The default value is "0,0 10,10".</span></span> <span data-ttu-id="ed61c-124">Beachten Sie, dass Kommas nicht erforderlich sind, aber für eine einfachere Lesbarkeit sorgen.</span><span class="sxs-lookup"><span data-stu-id="ed61c-124">Note that commas are not required, but they make for easier readability.</span></span>

<span data-ttu-id="ed61c-125">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="ed61c-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="ed61c-126">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="ed61c-126">**Example**</span></span>

<span data-ttu-id="ed61c-127">Die Polylinie beginnt am Punkt 10, 10 und endet bei 100.100 mit den Bewertungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="ed61c-127">The polyline starts at the point 10,10 and ends at 100,100, with the valuesin points.</span></span>


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 