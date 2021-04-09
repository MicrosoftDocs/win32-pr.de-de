---
title: VML-Attribut "verdeckt"
description: VML-Attribut "verdeckt"
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e383061d3210c9c52dc8c89322bd617257555e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039194"
---
# <a name="vml-obscured-attribute"></a><span data-ttu-id="27aa2-103">VML-Attribut "verdeckt"</span><span class="sxs-lookup"><span data-stu-id="27aa2-103">VML Obscured Attribute</span></span>

<span data-ttu-id="27aa2-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="27aa2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="27aa2-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="27aa2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="27aa2-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="27aa2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="27aa2-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="27aa2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="27aa2-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="27aa2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="27aa2-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="27aa2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="27aa2-110">Bestimmt, ob ein Schatten transparent ist.</span><span class="sxs-lookup"><span data-stu-id="27aa2-110">Determines whether a shadow is transparent.</span></span> <span data-ttu-id="27aa2-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="27aa2-111">Read/write.</span></span> <span data-ttu-id="27aa2-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="27aa2-112">**VgTriState**.</span></span>

<span data-ttu-id="27aa2-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="27aa2-113">**Applies To**</span></span>

[<span data-ttu-id="27aa2-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="27aa2-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="27aa2-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="27aa2-115">**Tag Syntax**</span></span>

<span data-ttu-id="27aa2-116"><v: *Element* verdeckt = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="27aa2-116"><v: *element* obscured=" *expression* "></span></span>

<span data-ttu-id="27aa2-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="27aa2-117">**Script Syntax**</span></span>

<span data-ttu-id="27aa2-118">*Element* . verdeckt = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="27aa2-118">*element* .obscured="*expression*"</span></span>

<span data-ttu-id="27aa2-119">*Ausdruck* = *Element*. verdeckt</span><span class="sxs-lookup"><span data-stu-id="27aa2-119">*expression*=*element*.obscured</span></span>

<span data-ttu-id="27aa2-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="27aa2-120">**Remarks**</span></span>

<span data-ttu-id="27aa2-121">Wenn der Wert **true** ist, wird der Schatten angezeigt, wenn die Form nicht ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="27aa2-121">If **True**, lets you see through the shadow if there is no fill on the shape.</span></span> <span data-ttu-id="27aa2-122">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="27aa2-122">Default is **False**.</span></span>

<span data-ttu-id="27aa2-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="27aa2-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="27aa2-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="27aa2-124">**Example**</span></span>

<span data-ttu-id="27aa2-125">Der Hintergrund wird durch den Schatten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27aa2-125">The background shows through the shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 