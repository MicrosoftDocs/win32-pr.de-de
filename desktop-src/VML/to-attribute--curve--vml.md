---
title: To-Attribut (Kurve) (VML)
description: To-Attribut (Kurve) (VML)
ms.assetid: 61469921-5095-4cb6-b032-f3e250874958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c0c9a858ff2cc8304ffacefb1cae477614e470
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858463"
---
# <a name="to-attribute-curvevml"></a><span data-ttu-id="92d90-103">To-Attribut (Kurve) (VML)</span><span class="sxs-lookup"><span data-stu-id="92d90-103">To Attribute (Curve)(VML)</span></span>

<span data-ttu-id="92d90-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="92d90-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="92d90-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="92d90-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="92d90-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="92d90-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="92d90-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="92d90-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="92d90-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="92d90-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="92d90-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="92d90-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="92d90-110">Definiert den Endpunkt einer Kurve.</span><span class="sxs-lookup"><span data-stu-id="92d90-110">Defines the ending point of a curve.</span></span> <span data-ttu-id="92d90-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="92d90-111">Read/write.</span></span> <span data-ttu-id="92d90-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="92d90-112">**VgVector2D**.</span></span>

<span data-ttu-id="92d90-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="92d90-113">**Applies To**</span></span>

[<span data-ttu-id="92d90-114">FF</span><span class="sxs-lookup"><span data-stu-id="92d90-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="92d90-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="92d90-115">**Tag Syntax**</span></span>

<span data-ttu-id="92d90-116"><v: *Element* to = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="92d90-116"><v: *element* to=" *expression* "></span></span>

<span data-ttu-id="92d90-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="92d90-117">**Script Syntax**</span></span>

<span data-ttu-id="92d90-118">*Element* . to = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="92d90-118">*element* .to="*expression*"</span></span>

<span data-ttu-id="92d90-119">*Ausdruck* = *Element*. to</span><span class="sxs-lookup"><span data-stu-id="92d90-119">*expression*=*element*.to</span></span>

<span data-ttu-id="92d90-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="92d90-120">**Remarks**</span></span>

<span data-ttu-id="92d90-121">Definiert den Endpunkt einer kubischen Bézier-Kurve im Koordinaten Bereich des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="92d90-121">Defines the ending point of a cubic bezier curve in the coordinate space of the parent element.</span></span> <span data-ttu-id="92d90-122">Wenn das übergeordnete Element kein VML-Element ist, ist die Standard [Einheit](msdn-online-vml-units.md) ein Pixel (in, cm, mm, PT, kann jedoch auch der PC angegeben werden).</span><span class="sxs-lookup"><span data-stu-id="92d90-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="92d90-123">Der Standardwert ist 30, 20.</span><span class="sxs-lookup"><span data-stu-id="92d90-123">Default is 30,20.</span></span>

<span data-ttu-id="92d90-124">**VML-Standard Attribut**</span><span class="sxs-lookup"><span data-stu-id="92d90-124">**VML Standard Attribute**</span></span>

<span data-ttu-id="92d90-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="92d90-125">**Example**</span></span>

<span data-ttu-id="92d90-126">Die Kurve wird Lächeln.</span><span class="sxs-lookup"><span data-stu-id="92d90-126">The curve is smiling.</span></span> <span data-ttu-id="92d90-127">Sie beginnt auf der linken Seite und endet auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="92d90-127">It starts at the left and ends at the right.</span></span> <span data-ttu-id="92d90-128">Die beiden Kontrollpunkte sind auf dem Weg, um die Kurve nach unten zu ziehen, um die Darstellung eines Lächelns zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="92d90-128">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```



 

 