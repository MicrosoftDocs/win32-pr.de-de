---
title: VML-Attribut "strokeColor"
description: VML-Attribut "strokeColor"
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d379f41f3d2c1f03349beae8d0420a7c1a26429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039150"
---
# <a name="vml-strokecolor-attribute"></a><span data-ttu-id="be69f-103">VML-Attribut "strokeColor"</span><span class="sxs-lookup"><span data-stu-id="be69f-103">VML StrokeColor Attribute</span></span>

<span data-ttu-id="be69f-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="be69f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="be69f-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="be69f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="be69f-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="be69f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="be69f-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="be69f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="be69f-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="be69f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="be69f-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="be69f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="be69f-110">Definiert die Pinsel Farbe, mit der der Pfad einer Form festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="be69f-110">Defines the brush color that strokes the path of a shape.</span></span> <span data-ttu-id="be69f-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="be69f-111">Read/write.</span></span> <span data-ttu-id="be69f-112">[Ivgcolor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="be69f-112">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span>

<span data-ttu-id="be69f-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="be69f-113">**Applies To**</span></span>

[<span data-ttu-id="be69f-114">Form</span><span class="sxs-lookup"><span data-stu-id="be69f-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="be69f-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="be69f-115">**Tag Syntax**</span></span>

<span data-ttu-id="be69f-116"><v: *Element* strokeColor = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="be69f-116"><v: *element* strokecolor=" *expression* "></span></span>

<span data-ttu-id="be69f-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="be69f-117">**Script Syntax**</span></span>

<span data-ttu-id="be69f-118">*Element* . strokeColor = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="be69f-118">*element* .strokecolor="*expression*"</span></span>

<span data-ttu-id="be69f-119">*Ausdruck* = *Element*. strokeColor</span><span class="sxs-lookup"><span data-stu-id="be69f-119">*expression*=*element*.strokecolor</span></span>

<span data-ttu-id="be69f-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="be69f-120">**Remarks**</span></span>

<span data-ttu-id="be69f-121">Der Wert wird aus dem **Color** -Attribut des [Stroke](msdn-online-vml-stroke-element.md) -Elements dupliziert.</span><span class="sxs-lookup"><span data-stu-id="be69f-121">The value is duplicated from the **Color** attribute of the [Stroke](msdn-online-vml-stroke-element.md) element.</span></span>

<span data-ttu-id="be69f-122">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="be69f-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="be69f-123">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="be69f-123">**Example**</span></span>

<span data-ttu-id="be69f-124">Die Farbe des Strichs des Rechtecks ist rot.</span><span class="sxs-lookup"><span data-stu-id="be69f-124">The color of the stroke of the rectangle is red.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="be69f-125">[Beispiel für ein strokeColor-Attribut](/previous-versions/bb264093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be69f-125">[StrokeColor Attribute Example](/previous-versions/bb264093(v=vs.85)).</span></span> <span data-ttu-id="be69f-126">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="be69f-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 