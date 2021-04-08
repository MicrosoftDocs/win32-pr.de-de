---
title: From-Attribut (Zeile) (VML)
description: From-Attribut (Zeile) (VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950b3cae8e3b73efdc3a92bdc49a0b9e4366e224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730008"
---
# <a name="from-attribute-linevml"></a><span data-ttu-id="0e293-103">From-Attribut (Zeile) (VML)</span><span class="sxs-lookup"><span data-stu-id="0e293-103">From Attribute (Line)(VML)</span></span>

<span data-ttu-id="0e293-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="0e293-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0e293-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="0e293-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0e293-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="0e293-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0e293-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0e293-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0e293-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0e293-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0e293-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0e293-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0e293-110">Definiert den Anfangspunkt einer Linie.</span><span class="sxs-lookup"><span data-stu-id="0e293-110">Defines the starting point of a line.</span></span> <span data-ttu-id="0e293-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0e293-111">Read/write.</span></span> <span data-ttu-id="0e293-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="0e293-112">**VgVector2D**.</span></span>

<span data-ttu-id="0e293-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="0e293-113">**Applies To**</span></span>

[<span data-ttu-id="0e293-114">Line</span><span class="sxs-lookup"><span data-stu-id="0e293-114">Line</span></span>](msdn-online-vml-line-element.md)

<span data-ttu-id="0e293-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="0e293-115">**Tag Syntax**</span></span>

<span data-ttu-id="0e293-116"><v: *Element* from = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="0e293-116"><v: *element* from=" *expression* "></span></span>

<span data-ttu-id="0e293-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="0e293-117">**Script Syntax**</span></span>

<span data-ttu-id="0e293-118">*Element* . from = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="0e293-118">*element* .from="*expression*"</span></span>

<span data-ttu-id="0e293-119">*Ausdruck* = *Element*. from</span><span class="sxs-lookup"><span data-stu-id="0e293-119">*expression*=*element*.from</span></span>

<span data-ttu-id="0e293-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="0e293-120">**Remarks**</span></span>

<span data-ttu-id="0e293-121">Definiert den Anfangspunkt der Linie im Koordinaten Bereich des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standard [Einheit](msdn-online-vml-units.md) ein Pixel (in, cm, mm, PT, kann jedoch auch der PC angegeben werden).</span><span class="sxs-lookup"><span data-stu-id="0e293-121">Defines the starting point of the line in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="0e293-122">Der Standardwert ist 0, 0.</span><span class="sxs-lookup"><span data-stu-id="0e293-122">Default is 0,0.</span></span>

<span data-ttu-id="0e293-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="0e293-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="0e293-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="0e293-124">**Example**</span></span>

<span data-ttu-id="0e293-125">Die Zeile beginnt an einer Position, die 10 zeigt, und 10 zeigt rechts neben der oberen linken Ecke des übergeordneten Raums.</span><span class="sxs-lookup"><span data-stu-id="0e293-125">The line starts at a location 10 points down and 10 points to the right of the top left corner of the parent space.</span></span>


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 