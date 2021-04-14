---
title: From-Attribut (Kurve) (VML)
description: From-Attribut (Kurve) (VML)
ms.assetid: 70e940c1-3fa8-4a30-9ca8-584483cea485
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d5f78dee46192efed48172a7d1f4d9cc77582f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390925"
---
# <a name="from-attribute-curvevml"></a><span data-ttu-id="7a4f6-103">From-Attribut (Kurve) (VML)</span><span class="sxs-lookup"><span data-stu-id="7a4f6-103">From Attribute (Curve)(VML)</span></span>

<span data-ttu-id="7a4f6-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="7a4f6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7a4f6-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="7a4f6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7a4f6-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="7a4f6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7a4f6-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7a4f6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7a4f6-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7a4f6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7a4f6-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7a4f6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7a4f6-110">Definiert den Anfangspunkt einer Kurve.</span><span class="sxs-lookup"><span data-stu-id="7a4f6-110">Defines the starting point of a curve.</span></span> <span data-ttu-id="7a4f6-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7a4f6-111">Read/write.</span></span> <span data-ttu-id="7a4f6-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="7a4f6-112">**VgVector2D**.</span></span>

<span data-ttu-id="7a4f6-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="7a4f6-113">**Applies To**</span></span>

[<span data-ttu-id="7a4f6-114">FF</span><span class="sxs-lookup"><span data-stu-id="7a4f6-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="7a4f6-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="7a4f6-115">**Tag Syntax**</span></span>

<span data-ttu-id="7a4f6-116"><v: *Element* from = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="7a4f6-116"><v: *element* from=" *expression* "></span></span>

<span data-ttu-id="7a4f6-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="7a4f6-117">**Script Syntax**</span></span>

<span data-ttu-id="7a4f6-118">*Element* . from = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="7a4f6-118">*element* .from="*expression*"</span></span>

<span data-ttu-id="7a4f6-119">*Ausdruck* = *Element*. from</span><span class="sxs-lookup"><span data-stu-id="7a4f6-119">*expression*=*element*.from</span></span>

<span data-ttu-id="7a4f6-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="7a4f6-120">**Remarks**</span></span>

<span data-ttu-id="7a4f6-121">Definiert den Anfangspunkt einer kubischen Bézier-Kurve im Koordinaten Bereich des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="7a4f6-121">Defines the starting point of a cubic bezier curve in the coordinate space of the parent element.</span></span> <span data-ttu-id="7a4f6-122">Wenn das übergeordnete Element kein VML-Element ist, ist die Standard [Einheit](msdn-online-vml-units.md) ein Pixel (in, cm, mm, PT, kann jedoch auch der PC angegeben werden).</span><span class="sxs-lookup"><span data-stu-id="7a4f6-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="7a4f6-123">Der Standardwert ist 0, 0.</span><span class="sxs-lookup"><span data-stu-id="7a4f6-123">Default is 0,0.</span></span>

<span data-ttu-id="7a4f6-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="7a4f6-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="7a4f6-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="7a4f6-125">**Example**</span></span>

<span data-ttu-id="7a4f6-126">Die Kurve wird Lächeln.</span><span class="sxs-lookup"><span data-stu-id="7a4f6-126">The curve is smiling.</span></span> <span data-ttu-id="7a4f6-127">Sie beginnt auf der linken Seite und endet auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="7a4f6-127">It starts at the left and ends at the right.</span></span> <span data-ttu-id="7a4f6-128">Die beiden Kontrollpunkte sind auf dem Weg, um die Kurve nach unten zu ziehen, um die Darstellung eines Lächelns zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="7a4f6-128">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```



 

 