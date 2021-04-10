---
title: VML focusposition-Attribut
description: VML focusposition-Attribut
ms.assetid: 1aebf79d-c887-4a61-b50c-01a4ebfd68a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a418916efb1721c41b7db37256ac3a040ea4b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102318"
---
# <a name="vml-focusposition-attribute"></a><span data-ttu-id="90209-103">VML focusposition-Attribut</span><span class="sxs-lookup"><span data-stu-id="90209-103">VML FocusPosition Attribute</span></span>

<span data-ttu-id="90209-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="90209-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="90209-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="90209-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="90209-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="90209-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="90209-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="90209-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="90209-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="90209-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="90209-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="90209-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="90209-110">Definiert den Mittelpunkt eines radialen Farbverlaufs.</span><span class="sxs-lookup"><span data-stu-id="90209-110">Defines the center of a radial gradient.</span></span> <span data-ttu-id="90209-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="90209-111">Read/write.</span></span> <span data-ttu-id="90209-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="90209-112">**VgVector2D**.</span></span>

<span data-ttu-id="90209-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="90209-113">**Applies To**</span></span>

[<span data-ttu-id="90209-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="90209-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="90209-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="90209-115">**Tag Syntax**</span></span>

<span data-ttu-id="90209-116"><v: *Element* focusposition = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="90209-116"><v: *element* focusposition=" *expression* "></span></span>

<span data-ttu-id="90209-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="90209-117">**Script Syntax**</span></span>

<span data-ttu-id="90209-118">*Element* . focusposition = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="90209-118">*element* .focusposition="*expression*"</span></span>

<span data-ttu-id="90209-119">*Ausdruck* = *Element*. focusposition</span><span class="sxs-lookup"><span data-stu-id="90209-119">*expression*=*element*.focusposition</span></span>

<span data-ttu-id="90209-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="90209-120">**Remarks**</span></span>

<span data-ttu-id="90209-121">Gibt die Mittelpunkt Positionierung für radiale Farbverläufe an.</span><span class="sxs-lookup"><span data-stu-id="90209-121">Specifies the center positionfor radial gradients.</span></span> <span data-ttu-id="90209-122">Der Vektor ist ein Bruchteil der Breite und Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="90209-122">The vector is a fraction of the width and height of the shape.</span></span> <span data-ttu-id="90209-123">Der erste Wert ist ein Prozentsatz der Füllung am linken Rand. der zweite Wert ist ein Prozentsatz der Füllung im oberen Bereich.</span><span class="sxs-lookup"><span data-stu-id="90209-123">The first is a percentage of the fill to the left edge; the second is a percentage of the fill to the top.</span></span> <span data-ttu-id="90209-124">Der Standardwert ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="90209-124">The default value is 0,0.</span></span> <span data-ttu-id="90209-125">Um eine radiale Füllung in der Mitte einer Form zu positionieren, verwenden Sie den Wert von 50%, 50%.</span><span class="sxs-lookup"><span data-stu-id="90209-125">To position a radial fill at the center of a shape, use the value of 50%,50%.</span></span>

<span data-ttu-id="90209-126">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="90209-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="90209-127">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="90209-127">**Example**</span></span>

<span data-ttu-id="90209-128">Die radiale Füllung wird so zentriert, dass blau in der Mitte beginnt und nach außen strahlt und sich allmählich zu rot ändert, wenn die äußeren Ränder und Ecken erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="90209-128">The radial fill will be centered so that blue will start in the center and radiate outward, gradually changing to red by the time it reaches the outside edges and corners.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="GradientRadial" color="red" color2="blue"
   focusposition="50%,50%"/>
   </v:shape>
```



 

 