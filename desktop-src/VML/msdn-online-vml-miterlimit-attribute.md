---
title: VML-Attribut "MiterLimit"
description: VML-Attribut "MiterLimit"
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b2d5b0a186ca416bb6af25df38c4f29964efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473429"
---
# <a name="vml-miterlimit-attribute"></a><span data-ttu-id="49706-103">VML-Attribut "MiterLimit"</span><span class="sxs-lookup"><span data-stu-id="49706-103">VML MiterLimit Attribute</span></span>

<span data-ttu-id="49706-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="49706-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="49706-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="49706-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="49706-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="49706-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="49706-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="49706-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="49706-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="49706-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="49706-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="49706-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="49706-110">Definiert die Glätte des Haupt Trennzeichens.</span><span class="sxs-lookup"><span data-stu-id="49706-110">Defines the smoothness of the miter joint.</span></span> <span data-ttu-id="49706-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="49706-111">Read/write.</span></span> <span data-ttu-id="49706-112">**Vgnumber**.</span><span class="sxs-lookup"><span data-stu-id="49706-112">**VgNumber**.</span></span>

<span data-ttu-id="49706-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="49706-113">**Applies To**</span></span>

[<span data-ttu-id="49706-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="49706-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="49706-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="49706-115">**Tag Syntax**</span></span>

<span data-ttu-id="49706-116"><v: *Element* MiterLimit = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="49706-116"><v: *element* miterlimit=" *expression* "></span></span>

<span data-ttu-id="49706-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="49706-117">**Script Syntax**</span></span>

<span data-ttu-id="49706-118">*Element* . MiterLimit = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="49706-118">*element* .miterlimit="*expression*"</span></span>

<span data-ttu-id="49706-119">*Ausdruck* = *Element*. miterLimit</span><span class="sxs-lookup"><span data-stu-id="49706-119">*expression*=*element*.miterlimit</span></span>

<span data-ttu-id="49706-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="49706-120">**Remarks**</span></span>

<span data-ttu-id="49706-121">Der maximale Abstand zwischen dem inneren und dem äußeren Punkt eines gemeinsamen Punkts.</span><span class="sxs-lookup"><span data-stu-id="49706-121">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="49706-122">Diese Zahl ist ein Vielfaches der Linienstärke.</span><span class="sxs-lookup"><span data-stu-id="49706-122">This number is a multiple of the thickness of the line.</span></span>

<span data-ttu-id="49706-123">Der Standardwert ist 8.</span><span class="sxs-lookup"><span data-stu-id="49706-123">The default value is 8.</span></span>

<span data-ttu-id="49706-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="49706-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="49706-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="49706-125">**Example**</span></span>

<span data-ttu-id="49706-126">Die Gelenke auf der Polylinie werden mit einem Grenzwert von 10 gemessen, d. h. 5 mal 2 Punkten.</span><span class="sxs-lookup"><span data-stu-id="49706-126">The joints on the polyline are mitered with a limit of 10, that is, 5 times 2 points.</span></span>


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 