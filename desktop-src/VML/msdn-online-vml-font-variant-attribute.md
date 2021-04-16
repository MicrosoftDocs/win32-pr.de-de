---
title: VML-Font-Variant Attribut
description: VML-Font-Variant Attribut
ms.assetid: f58bf3e0-e285-474c-83b1-203fce4f3c3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 243f8b36d36d8bb9b210a916cef239cda6061e0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390384"
---
# <a name="vml-font-variant-attribute"></a><span data-ttu-id="bfbaf-103">VML-Font-Variant Attribut</span><span class="sxs-lookup"><span data-stu-id="bfbaf-103">VML Font-Variant Attribute</span></span>

<span data-ttu-id="bfbaf-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="bfbaf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bfbaf-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="bfbaf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bfbaf-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="bfbaf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bfbaf-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="bfbaf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bfbaf-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bfbaf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bfbaf-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bfbaf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bfbaf-110">Definiert den Variant-Stil einer Schriftart.</span><span class="sxs-lookup"><span data-stu-id="bfbaf-110">Defines the variant style of a font.</span></span> <span data-ttu-id="bfbaf-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="bfbaf-111">Read/write.</span></span> <span data-ttu-id="bfbaf-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="bfbaf-112">**String**.</span></span>

<span data-ttu-id="bfbaf-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="bfbaf-113">**Applies To**</span></span>

[<span data-ttu-id="bfbaf-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="bfbaf-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="bfbaf-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="bfbaf-115">**Tag Syntax**</span></span>

<span data-ttu-id="bfbaf-116"><v: *Element* Style = "Font-Variant: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="bfbaf-116"><v: *element* style="font-variant: *expression* "></span></span>

<span data-ttu-id="bfbaf-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="bfbaf-117">**Script Syntax**</span></span>

<span data-ttu-id="bfbaf-118">*Element* . Style. fontVariant = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="bfbaf-118">*element* .style.fontvariant="*expression*"</span></span>

<span data-ttu-id="bfbaf-119">*Ausdruck* = *Element*. Style. fontVariant</span><span class="sxs-lookup"><span data-stu-id="bfbaf-119">*expression*=*element*.style.fontvariant</span></span>

<span data-ttu-id="bfbaf-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="bfbaf-120">**Remarks**</span></span>

<span data-ttu-id="bfbaf-121">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="bfbaf-121">The values are:</span></span>

-   <span data-ttu-id="bfbaf-122">Normal (Standard)</span><span class="sxs-lookup"><span data-stu-id="bfbaf-122">normal (default)</span></span>
-   <span data-ttu-id="bfbaf-123">kleine Obergrenzen</span><span class="sxs-lookup"><span data-stu-id="bfbaf-123">small-caps</span></span>

<span data-ttu-id="bfbaf-124">Die Werte sind identisch mit den standardmäßigen HTML-Format Attributen.</span><span class="sxs-lookup"><span data-stu-id="bfbaf-124">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="bfbaf-125">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="bfbaf-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="bfbaf-126">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="bfbaf-126">**Example**</span></span>

<span data-ttu-id="bfbaf-127">Die Schriftart wird als kleine Großbuchstaben gerendert.</span><span class="sxs-lookup"><span data-stu-id="bfbaf-127">The font is rendered as small capital letters.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal small-caps normal 36pt Arial"/>
   </v:line>
```



 

 