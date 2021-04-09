---
title: VML-Font-Style Attribut
description: VML-Font-Style Attribut
ms.assetid: 3dfea8d0-d03b-46c0-b972-a529bc12b62c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f4fc2f299d78c3ccd8b194b8506cfce07abceb7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039064"
---
# <a name="vml-font-style-attribute"></a><span data-ttu-id="7c88c-103">VML-Font-Style Attribut</span><span class="sxs-lookup"><span data-stu-id="7c88c-103">VML Font-Style Attribute</span></span>

<span data-ttu-id="7c88c-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="7c88c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7c88c-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="7c88c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7c88c-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="7c88c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7c88c-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7c88c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7c88c-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7c88c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7c88c-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7c88c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7c88c-110">Definiert den Umfang der Rechts für eine Schriftart.</span><span class="sxs-lookup"><span data-stu-id="7c88c-110">Defines the amount of slant for a font.</span></span> <span data-ttu-id="7c88c-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7c88c-111">Read/write.</span></span> <span data-ttu-id="7c88c-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="7c88c-112">**String**.</span></span>

<span data-ttu-id="7c88c-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="7c88c-113">**Applies To**</span></span>

[<span data-ttu-id="7c88c-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="7c88c-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="7c88c-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="7c88c-115">**Tag Syntax**</span></span>

<span data-ttu-id="7c88c-116"><v: *Element* Style = "Font-Style: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="7c88c-116"><v: *element* style="font-style: *expression* "></span></span>

<span data-ttu-id="7c88c-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="7c88c-117">**Script Syntax**</span></span>

<span data-ttu-id="7c88c-118">*Element* . Style. FontStyle = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="7c88c-118">*element* .style.fontstyle="*expression*"</span></span>

<span data-ttu-id="7c88c-119">*Ausdruck* = *Element*. Style. FontStyle</span><span class="sxs-lookup"><span data-stu-id="7c88c-119">*expression*=*element*.style.fontstyle</span></span>

<span data-ttu-id="7c88c-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="7c88c-120">**Remarks**</span></span>

<span data-ttu-id="7c88c-121">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7c88c-121">The values are:</span></span>

-   <span data-ttu-id="7c88c-122">Normal (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c88c-122">normal (default)</span></span>
-   <span data-ttu-id="7c88c-123">schräg</span><span class="sxs-lookup"><span data-stu-id="7c88c-123">oblique</span></span>
-   <span data-ttu-id="7c88c-124">kursiv</span><span class="sxs-lookup"><span data-stu-id="7c88c-124">italic</span></span>

<span data-ttu-id="7c88c-125">Die meisten Browser Rendering als kursiv formatiert.</span><span class="sxs-lookup"><span data-stu-id="7c88c-125">Most browsers render oblique as italic.</span></span> <span data-ttu-id="7c88c-126">Die Werte sind identisch mit den standardmäßigen HTML-Format Attributen.</span><span class="sxs-lookup"><span data-stu-id="7c88c-126">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="7c88c-127">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="7c88c-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="7c88c-128">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="7c88c-128">**Example**</span></span>

<span data-ttu-id="7c88c-129">Die Schriftart ist kursiv formatiert (schlank).</span><span class="sxs-lookup"><span data-stu-id="7c88c-129">The font is italic (slanted).</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic normal normal 36pt Arial"/>
   </v:line>
```



 

 