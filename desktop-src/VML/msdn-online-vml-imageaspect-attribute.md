---
title: VML imageaspect-Attribut
description: VML imageaspect-Attribut
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b873f7577907acb6d8f88f0290117651077b3c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315615"
---
# <a name="vml-imageaspect-attribute"></a><span data-ttu-id="912dd-103">VML imageaspect-Attribut</span><span class="sxs-lookup"><span data-stu-id="912dd-103">VML ImageAspect Attribute</span></span>

<span data-ttu-id="912dd-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="912dd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="912dd-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="912dd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="912dd-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="912dd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="912dd-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="912dd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="912dd-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="912dd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="912dd-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="912dd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="912dd-110">Definiert, wie das Seitenverhältnis des Strich Bilds beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="912dd-110">Defines how the stroke image aspect ratio will be preserved.</span></span> <span data-ttu-id="912dd-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="912dd-111">Read/write.</span></span> <span data-ttu-id="912dd-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="912dd-112">**String**.</span></span>

<span data-ttu-id="912dd-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="912dd-113">**Applies To**</span></span>

[<span data-ttu-id="912dd-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="912dd-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="912dd-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="912dd-115">**Tag Syntax**</span></span>

<span data-ttu-id="912dd-116"><v:</span><span class="sxs-lookup"><span data-stu-id="912dd-116"><v:</span></span>

<span data-ttu-id="912dd-117">Element *imageaspect = "* Expression *" #b0*</span><span class="sxs-lookup"><span data-stu-id="912dd-117">element *imageaspect="* expression *">*</span></span>

<span data-ttu-id="912dd-118">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="912dd-118">**Script Syntax**</span></span>

<span data-ttu-id="912dd-119">Element *. imageaspect = "* Ausdruck *"*</span><span class="sxs-lookup"><span data-stu-id="912dd-119">element *.imageaspect="* expression *"*</span></span>

<span data-ttu-id="912dd-120">Expression- *=* Element *. imageaspect*</span><span class="sxs-lookup"><span data-stu-id="912dd-120">expression *=* element *.imageaspect*</span></span>

<span data-ttu-id="912dd-121">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="912dd-121">**Remarks**</span></span>

<span data-ttu-id="912dd-122">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="912dd-122">Values include:</span></span>



| <span data-ttu-id="912dd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="912dd-123">Value</span></span>   | <span data-ttu-id="912dd-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="912dd-124">Description</span></span>                                |
|---------|--------------------------------------------|
| <span data-ttu-id="912dd-125">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="912dd-125">Ignore</span></span>  | <span data-ttu-id="912dd-126">Ignoriert Aspekte von Aspekten.</span><span class="sxs-lookup"><span data-stu-id="912dd-126">Ignore aspect issues.</span></span>                      |
| <span data-ttu-id="912dd-127">Mindestens</span><span class="sxs-lookup"><span data-stu-id="912dd-127">AtLeast</span></span> | <span data-ttu-id="912dd-128">Image ist mindestens so groß wie **ImageSize**.</span><span class="sxs-lookup"><span data-stu-id="912dd-128">Image is at least as big as **ImageSize**.</span></span> |
| <span data-ttu-id="912dd-129">Höchstens</span><span class="sxs-lookup"><span data-stu-id="912dd-129">AtMost</span></span>  | <span data-ttu-id="912dd-130">Image ist nicht größer als **ImageSize**.</span><span class="sxs-lookup"><span data-stu-id="912dd-130">Image is no bigger than **ImageSize**.</span></span>     |



 

<span data-ttu-id="912dd-131">In jedem Fall wird das **ImageSize** -Attribut angepasst, um den Aspekt des Bilds zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="912dd-131">In each case, the **ImageSize** attribute will be adjusted to preserve the aspect of the image.</span></span>

<span data-ttu-id="912dd-132">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="912dd-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="912dd-133">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="912dd-133">**Example**</span></span>

<span data-ttu-id="912dd-134">Das Strich Bild ist mindestens so groß wie die Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="912dd-134">The stroke image will be at least as big as the image size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 