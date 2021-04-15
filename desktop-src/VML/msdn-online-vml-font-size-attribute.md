---
title: VML-Font-Size Attribut
description: VML-Font-Size Attribut
ms.assetid: 49394cd5-3009-424a-97d3-28c85d874bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c02b2df8fb0076ed6df6342e40b980ed8aa248e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474180"
---
# <a name="vml-font-size-attribute"></a><span data-ttu-id="421a0-103">VML-Font-Size Attribut</span><span class="sxs-lookup"><span data-stu-id="421a0-103">VML Font-Size Attribute</span></span>

<span data-ttu-id="421a0-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="421a0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="421a0-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="421a0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="421a0-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="421a0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="421a0-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="421a0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="421a0-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="421a0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="421a0-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="421a0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="421a0-110">Definiert die Größe der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="421a0-110">Defines the size of the font.</span></span> <span data-ttu-id="421a0-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="421a0-111">Read/write.</span></span> <span data-ttu-id="421a0-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="421a0-112">**String**.</span></span>

<span data-ttu-id="421a0-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="421a0-113">**Applies To**</span></span>

[<span data-ttu-id="421a0-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="421a0-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="421a0-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="421a0-115">**Tag Syntax**</span></span>

<span data-ttu-id="421a0-116"><v: *Element* Style = "Font-size: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="421a0-116"><v: *element* style="font-size: *expression* "></span></span>

<span data-ttu-id="421a0-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="421a0-117">**Script Syntax**</span></span>

<span data-ttu-id="421a0-118">*Element* . Style. FontSize = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="421a0-118">*element* .style.fontsize="*expression*"</span></span>

<span data-ttu-id="421a0-119">*Ausdruck* = *Element*. Style. FontSize</span><span class="sxs-lookup"><span data-stu-id="421a0-119">*expression*=*element*.style.fontsize</span></span>

<span data-ttu-id="421a0-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="421a0-120">**Remarks**</span></span>

<span data-ttu-id="421a0-121">Der Schrift Grad wird in Punkten definiert.</span><span class="sxs-lookup"><span data-stu-id="421a0-121">The font size is defined in points.</span></span> <span data-ttu-id="421a0-122">Die Werte sind identisch mit den standardmäßigen HTML-Format Attributen.</span><span class="sxs-lookup"><span data-stu-id="421a0-122">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="421a0-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="421a0-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="421a0-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="421a0-124">**Example**</span></span>

<span data-ttu-id="421a0-125">Die Schriftgröße beträgt 36 Punkte.</span><span class="sxs-lookup"><span data-stu-id="421a0-125">The font size is 36 points.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 