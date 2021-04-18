---
title: VML-Farben (Attribut)
description: VML-Farben (Attribut)
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c5df5b2dc97c19441d6abaf6cd6c03d949c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516964"
---
# <a name="vml-colors-attribute"></a><span data-ttu-id="35f7e-103">VML-Farben (Attribut)</span><span class="sxs-lookup"><span data-stu-id="35f7e-103">VML Colors Attribute</span></span>

<span data-ttu-id="35f7e-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="35f7e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="35f7e-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="35f7e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="35f7e-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="35f7e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="35f7e-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="35f7e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="35f7e-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="35f7e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="35f7e-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="35f7e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="35f7e-110">Definiert mehrere Farben für eine Farbverlaufsfüllung.</span><span class="sxs-lookup"><span data-stu-id="35f7e-110">Defines multiple colors for a gradient fill.</span></span> <span data-ttu-id="35f7e-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="35f7e-111">Read/write.</span></span> <span data-ttu-id="35f7e-112">**Ivggradientcolorarray**.</span><span class="sxs-lookup"><span data-stu-id="35f7e-112">**IVgGradientColorArray**.</span></span>

<span data-ttu-id="35f7e-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="35f7e-113">**Applies To**</span></span>

[<span data-ttu-id="35f7e-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="35f7e-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="35f7e-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="35f7e-115">**Tag Syntax**</span></span>

<span data-ttu-id="35f7e-116"><v: *Element* Farben = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="35f7e-116"><v: *element* colors=" *expression* "></span></span>

<span data-ttu-id="35f7e-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="35f7e-117">**Script Syntax**</span></span>

<span data-ttu-id="35f7e-118">*Element* . Colors = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="35f7e-118">*element* .colors="*expression*"</span></span>

<span data-ttu-id="35f7e-119">*Ausdruck* = *Element*. Colors</span><span class="sxs-lookup"><span data-stu-id="35f7e-119">*expression*=*element*.colors</span></span>

<span data-ttu-id="35f7e-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="35f7e-120">**Remarks**</span></span>

<span data-ttu-id="35f7e-121">Wird verwendet, um ein Array zu definieren, das aus paarweise zugeordneten Werten von Prozentsätzen ([vgbruch](msdn-online-vml-vgfraction-data-type.md)) und Color ([vgcolor](msdn-online-vml-ivgcolor.md)) besteht.</span><span class="sxs-lookup"><span data-stu-id="35f7e-121">Used to define an array consisting of paired values of percentages ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) and color ([VgColor](msdn-online-vml-ivgcolor.md)).</span></span> <span data-ttu-id="35f7e-122">Das Array erstellt eine gemischte Füllung mithilfe der einzelnen Punkte im Array, beginnend bei 0% (durch **Farbe** definiert) und endet bei 100% (durch **color2** definiert).</span><span class="sxs-lookup"><span data-stu-id="35f7e-122">The array creates a blended fill using each point in the array, starting at 0% (defined by **Color**) and ending at 100% (defined by **Color2**).</span></span> <span data-ttu-id="35f7e-123">Zwischen Farben können definiert werden, indem ein Farbwert einem Prozentsatz zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="35f7e-123">Intermediate colors along the way can be defined by assigning a color value to a percentage.</span></span> <span data-ttu-id="35f7e-124">Das Prozent-und Farbpaar ist nicht durch ein Komma getrennt, aber Paare werden durch Kommas voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="35f7e-124">The percent and color pair are not separated by a comma, but pairs are separated from each other by commas.</span></span>

<span data-ttu-id="35f7e-125">VML-Standard Attribut</span><span class="sxs-lookup"><span data-stu-id="35f7e-125">VML Standard Attribute</span></span>

<span data-ttu-id="35f7e-126">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="35f7e-126">**Example**</span></span>

<span data-ttu-id="35f7e-127">Die Form hat eine Farbverlaufsfüllung, die aus vier Farben besteht, beginnend mit rot, mit gelb, dann grün und finallyblue.</span><span class="sxs-lookup"><span data-stu-id="35f7e-127">The shape has a gradient fill consisting of four colors, starting with red, blending to yellow, then green, and finallyblue.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 