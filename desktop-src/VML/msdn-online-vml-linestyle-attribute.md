---
title: VML LineStyle-Attribut
description: VML LineStyle-Attribut
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e69371e61a3d81f97de0243af19381f36c0555
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727425"
---
# <a name="vml-linestyle-attribute"></a><span data-ttu-id="3cb58-103">VML LineStyle-Attribut</span><span class="sxs-lookup"><span data-stu-id="3cb58-103">VML LineStyle Attribute</span></span>

<span data-ttu-id="3cb58-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="3cb58-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3cb58-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="3cb58-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3cb58-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="3cb58-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3cb58-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3cb58-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3cb58-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3cb58-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3cb58-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3cb58-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3cb58-110">Definiert die Linienart des Strichs.</span><span class="sxs-lookup"><span data-stu-id="3cb58-110">Defines the line style of the stroke.</span></span> <span data-ttu-id="3cb58-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3cb58-111">Read/write.</span></span> <span data-ttu-id="3cb58-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="3cb58-112">**String**.</span></span>

<span data-ttu-id="3cb58-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="3cb58-113">**Applies To**</span></span>

[<span data-ttu-id="3cb58-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="3cb58-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="3cb58-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="3cb58-115">**Tag Syntax**</span></span>

<span data-ttu-id="3cb58-116"><v: *Element* LineStyle = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3cb58-116"><v: *element* linestyle=" *expression* "></span></span>

<span data-ttu-id="3cb58-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="3cb58-117">**Script Syntax**</span></span>

<span data-ttu-id="3cb58-118">*Element* . LineStyle = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="3cb58-118">*element* .linestyle="*expression*"</span></span>

<span data-ttu-id="3cb58-119">*Ausdruck* = *Element*. LineStyle</span><span class="sxs-lookup"><span data-stu-id="3cb58-119">*expression*=*element*.linestyle</span></span>

<span data-ttu-id="3cb58-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="3cb58-120">**Remarks**</span></span>

<span data-ttu-id="3cb58-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="3cb58-121">Values include:</span></span>

-   <span data-ttu-id="3cb58-122">Single (Standard)</span><span class="sxs-lookup"><span data-stu-id="3cb58-122">Single (default)</span></span>
-   <span data-ttu-id="3cb58-123">Dünn</span><span class="sxs-lookup"><span data-stu-id="3cb58-123">ThinThin</span></span>
-   <span data-ttu-id="3cb58-124">Dünn</span><span class="sxs-lookup"><span data-stu-id="3cb58-124">ThinThick</span></span>
-   <span data-ttu-id="3cb58-125">Dickes dünn</span><span class="sxs-lookup"><span data-stu-id="3cb58-125">ThickThin</span></span>
-   <span data-ttu-id="3cb58-126">Thickbetweenthin</span><span class="sxs-lookup"><span data-stu-id="3cb58-126">ThickBetweenThin</span></span>

<span data-ttu-id="3cb58-127">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="3cb58-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="3cb58-128">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3cb58-128">**Example**</span></span>

<span data-ttu-id="3cb58-129">Eine doppelte Linie wird mit zwei schmalen Strichen gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3cb58-129">A double line is drawn with two thin strokes.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 