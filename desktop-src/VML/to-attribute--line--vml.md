---
title: To-Attribut (Zeile) (VML)
description: To-Attribut (Zeile) (VML)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79246936e4885025d43dfe1fc8cc3b2f144403a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730129"
---
# <a name="to-attribute-linevml"></a><span data-ttu-id="3c164-103">To-Attribut (Zeile) (VML)</span><span class="sxs-lookup"><span data-stu-id="3c164-103">To Attribute (Line)(VML)</span></span>

<span data-ttu-id="3c164-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="3c164-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3c164-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="3c164-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3c164-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="3c164-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3c164-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3c164-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3c164-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3c164-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3c164-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3c164-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3c164-110">Definiert den Endpunkt einer Linie.</span><span class="sxs-lookup"><span data-stu-id="3c164-110">Defines the ending point of a line.</span></span> <span data-ttu-id="3c164-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3c164-111">Read/write.</span></span> <span data-ttu-id="3c164-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="3c164-112">**VgVector2D**.</span></span>

<span data-ttu-id="3c164-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="3c164-113">**Applies To**</span></span>

[<span data-ttu-id="3c164-114">Line</span><span class="sxs-lookup"><span data-stu-id="3c164-114">Line</span></span>](msdn-online-vml-line-element.md)

<span data-ttu-id="3c164-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="3c164-115">**Tag Syntax**</span></span>

<span data-ttu-id="3c164-116"><v: *Element* to = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3c164-116"><v: *element* to=" *expression* "></span></span>

<span data-ttu-id="3c164-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="3c164-117">**Script Syntax**</span></span>

<span data-ttu-id="3c164-118">*Element* . to = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="3c164-118">*element* .to="*expression*"</span></span>

<span data-ttu-id="3c164-119">*Ausdruck* = *Element*. to</span><span class="sxs-lookup"><span data-stu-id="3c164-119">*expression*=*element*.to</span></span>

<span data-ttu-id="3c164-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="3c164-120">**Remarks**</span></span>

<span data-ttu-id="3c164-121">Definiert den Endpunkt der Zeile im Koordinaten Bereich des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standard [Einheit](msdn-online-vml-units.md) ein Pixel (in, cm, mm, PT, kann jedoch auch der PC angegeben werden).</span><span class="sxs-lookup"><span data-stu-id="3c164-121">Defines the ending point of the line in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="3c164-122">Der Standardwert ist 10, 10.</span><span class="sxs-lookup"><span data-stu-id="3c164-122">Default is 10,10.</span></span>

<span data-ttu-id="3c164-123">**VML-Standard Attribut**</span><span class="sxs-lookup"><span data-stu-id="3c164-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="3c164-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3c164-124">**Example**</span></span>

<span data-ttu-id="3c164-125">Die Zeile endet an einer Position von 100 Punkten nach unten, und 100 zeigt rechts neben der oberen linken Ecke des übergeordneten Raums.</span><span class="sxs-lookup"><span data-stu-id="3c164-125">The line ends at a location 100 points down and 100 points to the right of the top left corner of the parent space.</span></span>


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 