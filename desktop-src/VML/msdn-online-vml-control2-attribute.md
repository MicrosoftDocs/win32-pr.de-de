---
title: VML Control2-Attribut
description: VML Control2-Attribut
ms.assetid: fd0f92fa-ae70-46c9-bfbe-fad8deea34f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7af3871981e26ff7eff471651de555483fd540
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101686"
---
# <a name="vml-control2-attribute"></a><span data-ttu-id="57400-103">VML Control2-Attribut</span><span class="sxs-lookup"><span data-stu-id="57400-103">VML Control2 Attribute</span></span>

<span data-ttu-id="57400-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="57400-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="57400-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="57400-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="57400-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="57400-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="57400-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="57400-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="57400-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="57400-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="57400-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="57400-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="57400-110">Definiert den zweiten Kontrollpunkt einer Bézier-Kurve.</span><span class="sxs-lookup"><span data-stu-id="57400-110">Defines the second control point of a bezier curve.</span></span> <span data-ttu-id="57400-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="57400-111">Read/write.</span></span> <span data-ttu-id="57400-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="57400-112">**VgVector2D**.</span></span>

<span data-ttu-id="57400-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="57400-113">**Applies To**</span></span>

[<span data-ttu-id="57400-114">FF</span><span class="sxs-lookup"><span data-stu-id="57400-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="57400-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="57400-115">**Tag Syntax**</span></span>

<span data-ttu-id="57400-116"><v: *Element* Control2 = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="57400-116"><v: *element* control2=" *expression* "></span></span>

<span data-ttu-id="57400-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="57400-117">**Script Syntax**</span></span>

<span data-ttu-id="57400-118">*Element* . Control2 = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="57400-118">*element* .control2="*expression*"</span></span>

<span data-ttu-id="57400-119">*Ausdruck* = *Element*. Control2</span><span class="sxs-lookup"><span data-stu-id="57400-119">*expression*=*element*.control2</span></span>

<span data-ttu-id="57400-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="57400-120">**Remarks**</span></span>

<span data-ttu-id="57400-121">Definiert den zweiten Kontrollpunkt einer kubischen Bézier-Kurve im Koordinaten Bereich des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standard [Einheit](msdn-online-vml-units.md) ein Pixel (in, cm, mm, PT, kann jedoch auch der PC angegeben werden).</span><span class="sxs-lookup"><span data-stu-id="57400-121">Defines the second control point of a cubic bezier curve in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="57400-122">Der Standardwert ist 20,0.</span><span class="sxs-lookup"><span data-stu-id="57400-122">Default is 20.0.</span></span>

<span data-ttu-id="57400-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="57400-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="57400-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="57400-124">**Example**</span></span>

<span data-ttu-id="57400-125">Die Kurve wird Lächeln.</span><span class="sxs-lookup"><span data-stu-id="57400-125">The curve is smiling.</span></span> <span data-ttu-id="57400-126">Sie beginnt auf der linken Seite und endet auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="57400-126">It starts at the left and ends at the right.</span></span> <span data-ttu-id="57400-127">Die beiden Kontrollpunkte sind auf dem Weg, um die Kurve nach unten zu ziehen, um die Darstellung eines Lächelns zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="57400-127">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 