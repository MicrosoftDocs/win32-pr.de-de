---
title: In VML gestreichelt Attribut
description: In VML gestreichelt Attribut
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9578027f305f9c720b42ae50befe8abd7e18a949
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102274"
---
# <a name="vml-stroked-attribute"></a><span data-ttu-id="65d42-103">In VML gestreichelt Attribut</span><span class="sxs-lookup"><span data-stu-id="65d42-103">VML Stroked Attribute</span></span>

<span data-ttu-id="65d42-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="65d42-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="65d42-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="65d42-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="65d42-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="65d42-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="65d42-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="65d42-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="65d42-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="65d42-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="65d42-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="65d42-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="65d42-110">Definiert, ob der Pfad gestreichelt wird.</span><span class="sxs-lookup"><span data-stu-id="65d42-110">Defines whether the path will be stroked.</span></span> <span data-ttu-id="65d42-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="65d42-111">Read/write.</span></span> <span data-ttu-id="65d42-112">[Vgder State](msdn-online-vml-vgtristate.md) .</span><span class="sxs-lookup"><span data-stu-id="65d42-112">[VgTriState](msdn-online-vml-vgtristate.md) .</span></span>

<span data-ttu-id="65d42-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="65d42-113">**Applies To**</span></span>

[<span data-ttu-id="65d42-114">Form</span><span class="sxs-lookup"><span data-stu-id="65d42-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="65d42-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="65d42-115">**Tag Syntax**</span></span>

<span data-ttu-id="65d42-116"><v: *Element* gestreichelt = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="65d42-116"><v: *element* stroked=" *expression* "></span></span>

<span data-ttu-id="65d42-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="65d42-117">**Script Syntax**</span></span>

<span data-ttu-id="65d42-118">*Element* . stroked = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="65d42-118">*element* .stroked="*expression*"</span></span>

<span data-ttu-id="65d42-119">*Ausdruck* = *Element*. stroked</span><span class="sxs-lookup"><span data-stu-id="65d42-119">*expression*=*element*.stroked</span></span>

<span data-ttu-id="65d42-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="65d42-120">**Remarks**</span></span>

<span data-ttu-id="65d42-121">Der Wert wird aus dem **on** -Attribut des [Stroke](msdn-online-vml-stroke-element.md) -Elements dupliziert.</span><span class="sxs-lookup"><span data-stu-id="65d42-121">The value is duplicated from the **On** attribute of the [Stroke](msdn-online-vml-stroke-element.md) element.</span></span>

<span data-ttu-id="65d42-122">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="65d42-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="65d42-123">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="65d42-123">**Example**</span></span>

<span data-ttu-id="65d42-124">Der Shape-Pfad ist gestreichelt.</span><span class="sxs-lookup"><span data-stu-id="65d42-124">The shape path is stroked.</span></span>


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="65d42-125">[Beispiel](/previous-versions/bb264094(v=vs.85))für einen Strich mit Strichen.</span><span class="sxs-lookup"><span data-stu-id="65d42-125">[Stroked Attribute Example](/previous-versions/bb264094(v=vs.85)).</span></span> <span data-ttu-id="65d42-126">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="65d42-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 