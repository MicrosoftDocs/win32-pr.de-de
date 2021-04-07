---
title: VML-aspektattribut
description: VML-aspektattribut
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f7cf666e9bb8d4bf3cfe0e47190a8127415ac1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728336"
---
# <a name="vml-aspect-attribute"></a><span data-ttu-id="2f26a-103">VML-aspektattribut</span><span class="sxs-lookup"><span data-stu-id="2f26a-103">VML Aspect Attribute</span></span>

<span data-ttu-id="2f26a-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="2f26a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2f26a-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="2f26a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2f26a-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="2f26a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2f26a-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="2f26a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2f26a-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2f26a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2f26a-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2f26a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2f26a-110">Gibt an, wie das Seitenverhältnis des Füll Bilds beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="2f26a-110">Specifies how the fill image aspect ratio will be preserved.</span></span> <span data-ttu-id="2f26a-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2f26a-111">Read/write.</span></span> <span data-ttu-id="2f26a-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="2f26a-112">**String**.</span></span>

<span data-ttu-id="2f26a-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="2f26a-113">**Applies To**</span></span>

[<span data-ttu-id="2f26a-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="2f26a-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="2f26a-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="2f26a-115">**Tag Syntax**</span></span>

<span data-ttu-id="2f26a-116"><v: *Element* Aspekt = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="2f26a-116"><v: *element* aspect=" *expression* "></span></span>

<span data-ttu-id="2f26a-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="2f26a-117">**Script Syntax**</span></span>

<span data-ttu-id="2f26a-118">*Element* . Aspect = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="2f26a-118">*element* .aspect="*expression*"</span></span>

<span data-ttu-id="2f26a-119">*Ausdruck* = *Element*. Aspekt</span><span class="sxs-lookup"><span data-stu-id="2f26a-119">*expression*=*element*.aspect</span></span>

<span data-ttu-id="2f26a-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="2f26a-120">**Remarks**</span></span>

<span data-ttu-id="2f26a-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="2f26a-121">Values include:</span></span>



| <span data-ttu-id="2f26a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2f26a-122">Value</span></span>   | <span data-ttu-id="2f26a-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f26a-123">Description</span></span>                           |
|---------|---------------------------------------|
| <span data-ttu-id="2f26a-124">ignore</span><span class="sxs-lookup"><span data-stu-id="2f26a-124">ignore</span></span>  | <span data-ttu-id="2f26a-125">Ignoriert Aspekte von Aspekten.</span><span class="sxs-lookup"><span data-stu-id="2f26a-125">Ignore aspect issues.</span></span> <span data-ttu-id="2f26a-126">Standard.</span><span class="sxs-lookup"><span data-stu-id="2f26a-126">Default.</span></span>        |
| <span data-ttu-id="2f26a-127">mindestens</span><span class="sxs-lookup"><span data-stu-id="2f26a-127">atleast</span></span> | <span data-ttu-id="2f26a-128">Image ist mindestens so groß wie die **Größe**.</span><span class="sxs-lookup"><span data-stu-id="2f26a-128">Image is at least as big as **Size**.</span></span> |
| <span data-ttu-id="2f26a-129">höchstens</span><span class="sxs-lookup"><span data-stu-id="2f26a-129">atmost</span></span>  | <span data-ttu-id="2f26a-130">Das Bild ist nicht größer als die **Größe**.</span><span class="sxs-lookup"><span data-stu-id="2f26a-130">Image is no bigger than **Size**.</span></span>     |



 

<span data-ttu-id="2f26a-131">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="2f26a-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="2f26a-132">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="2f26a-132">**Example**</span></span>

<span data-ttu-id="2f26a-133">Das Bild, das die Füllung bildet, ist größer als oder gleich einer Größe von 10 Punkten um 10 Punkte.</span><span class="sxs-lookup"><span data-stu-id="2f26a-133">The image that makes up the fill is greater than or equal to a size of 10 points by 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 