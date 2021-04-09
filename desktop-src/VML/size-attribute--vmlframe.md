---
title: Size-Attribut (vmlframe)
description: Size-Attribut (vmlframe)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b0401c414a3536e22bdb7328b2b08b2fbcf45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039054"
---
# <a name="size-attribute-vmlframe"></a><span data-ttu-id="c3cda-103">Size-Attribut (vmlframe)</span><span class="sxs-lookup"><span data-stu-id="c3cda-103">Size Attribute (VMLFrame)</span></span>

<span data-ttu-id="c3cda-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="c3cda-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c3cda-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3cda-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c3cda-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="c3cda-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c3cda-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c3cda-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c3cda-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c3cda-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c3cda-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c3cda-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c3cda-110">Definiert die Größe des Clippingbereichs des Frames.</span><span class="sxs-lookup"><span data-stu-id="c3cda-110">Defines the size of the clipping region of the frame.</span></span> <span data-ttu-id="c3cda-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c3cda-111">Read/write.</span></span> <span data-ttu-id="c3cda-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="c3cda-112">**VgVector2D**.</span></span>

<span data-ttu-id="c3cda-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="c3cda-113">**Applies To**</span></span>

[<span data-ttu-id="c3cda-114">Vmlframe</span><span class="sxs-lookup"><span data-stu-id="c3cda-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="c3cda-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="c3cda-115">**Tag Syntax**</span></span>

<span data-ttu-id="c3cda-116"><v: *Element* size = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c3cda-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="c3cda-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="c3cda-117">**Script Syntax**</span></span>

<span data-ttu-id="c3cda-118">*Element* . Size = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="c3cda-118">*element* .size="*expression*"</span></span>

<span data-ttu-id="c3cda-119">*Ausdruck* = *Element*. Size</span><span class="sxs-lookup"><span data-stu-id="c3cda-119">*expression*=*element*.size</span></span>

<span data-ttu-id="c3cda-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="c3cda-120">**Remarks**</span></span>

<span data-ttu-id="c3cda-121">Der Standardwert ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="c3cda-121">The default value is 0,0.</span></span> <span data-ttu-id="c3cda-122">Beachten Sie, dass **size** nur funktioniert, wenn [Clip](msdn-online-vml-clip-attribute.md) den Wert **true** hat.</span><span class="sxs-lookup"><span data-stu-id="c3cda-122">Note that **Size** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="c3cda-123">In diesem Attribut wird die Größe als Breite und Höhe des Frames definiert.</span><span class="sxs-lookup"><span data-stu-id="c3cda-123">In this attribute, the size is defined as the width and height of the frame.</span></span>

<span data-ttu-id="c3cda-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="c3cda-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="c3cda-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="c3cda-125">**Example**</span></span>

<span data-ttu-id="c3cda-126">Die Größe des Clippingbereichs beträgt 50 PT, 50pt.</span><span class="sxs-lookup"><span data-stu-id="c3cda-126">The size of the clipping region will be 50pt, 50pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 