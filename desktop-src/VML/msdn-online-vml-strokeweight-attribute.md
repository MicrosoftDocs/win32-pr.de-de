---
title: VML-Attribut "strokeweight"
description: VML-Attribut "strokeweight"
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8da9f7220315b066676f2439f37b97250cc7c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728072"
---
# <a name="vml-strokeweight-attribute"></a><span data-ttu-id="cb7af-103">VML-Attribut "strokeweight"</span><span class="sxs-lookup"><span data-stu-id="cb7af-103">VML StrokeWeight Attribute</span></span>

<span data-ttu-id="cb7af-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="cb7af-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cb7af-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="cb7af-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cb7af-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="cb7af-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cb7af-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="cb7af-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cb7af-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cb7af-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cb7af-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cb7af-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cb7af-110">Definiert die Pinsel Stärke, mit der der Pfad einer Form festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cb7af-110">Defines the brush thickness that strokes the path of a shape.</span></span> <span data-ttu-id="cb7af-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="cb7af-111">Read/write.</span></span> <span data-ttu-id="cb7af-112">**Vglength**.</span><span class="sxs-lookup"><span data-stu-id="cb7af-112">**VGLength**.</span></span>

<span data-ttu-id="cb7af-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="cb7af-113">**Applies To**</span></span>

[<span data-ttu-id="cb7af-114">Form</span><span class="sxs-lookup"><span data-stu-id="cb7af-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="cb7af-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="cb7af-115">**Tag Syntax**</span></span>

<span data-ttu-id="cb7af-116"><v: *Element* strokeweight = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="cb7af-116"><v: *element* strokeweight=" *expression* "></span></span>

<span data-ttu-id="cb7af-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="cb7af-117">**Script Syntax**</span></span>

<span data-ttu-id="cb7af-118">*Element* . strokeweight = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="cb7af-118">*element* .strokeweight="*expression*"</span></span>

<span data-ttu-id="cb7af-119">*Ausdruck* = *Element*. strokeweight</span><span class="sxs-lookup"><span data-stu-id="cb7af-119">*expression*=*element*.strokeweight</span></span>

<span data-ttu-id="cb7af-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="cb7af-120">**Remarks**</span></span>

<span data-ttu-id="cb7af-121">Der Wert wird aus dem **Weight** -Attribut des **Stroke** -Elements dupliziert.</span><span class="sxs-lookup"><span data-stu-id="cb7af-121">The value is duplicated from the **Weight** attribute of the **Stroke** element.</span></span> <span data-ttu-id="cb7af-122">Wenn eine Zahl angegeben, aber keine Einheiten hinzugefügt werden, ist die Standard Maßeinheit die EWU.</span><span class="sxs-lookup"><span data-stu-id="cb7af-122">If a number is specified, but no units are added, the default unit of measurement is the Emu.</span></span> <span data-ttu-id="cb7af-123">Wenn kein Wert angegeben wird, ist der Standardwert 1 Pixel (1px).</span><span class="sxs-lookup"><span data-stu-id="cb7af-123">If no value is specified, the default is 1 pixel (1px).</span></span>

<span data-ttu-id="cb7af-124">Bei der Skripterstellung wird jedoch die Standard Maßeinheit in Punkten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cb7af-124">For scripting, however, the default unit of measurement is in points.</span></span>

<span data-ttu-id="cb7af-125">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="cb7af-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="cb7af-126">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="cb7af-126">**See Also**</span></span>

<span data-ttu-id="cb7af-127">[Strich](msdn-online-vml-stroke-element.md), [ivglength](msdn-online-vml-vglength.md), [Einheiten](msdn-online-vml-units.md)</span><span class="sxs-lookup"><span data-stu-id="cb7af-127">[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)</span></span>

<span data-ttu-id="cb7af-128">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="cb7af-128">**Example**</span></span>

<span data-ttu-id="cb7af-129">Die Strich Gewichtung der Form ist 1 Punkt.</span><span class="sxs-lookup"><span data-stu-id="cb7af-129">The stroke weight of the shape is 1 point.</span></span>


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="cb7af-130">[Beispiel für ein strokeweight-Attribut](/previous-versions/bb264095(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cb7af-130">[StrokeWeight Attribute Example](/previous-versions/bb264095(v=vs.85)).</span></span> <span data-ttu-id="cb7af-131">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="cb7af-131">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 