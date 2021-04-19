---
title: VML-Schriftart Attribut
description: VML-Schriftart Attribut
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bace73b90cac7519ea6abacb73c80506c655e133
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342158"
---
# <a name="vml-font-attribute"></a><span data-ttu-id="46291-103">VML-Schriftart Attribut</span><span class="sxs-lookup"><span data-stu-id="46291-103">VML Font Attribute</span></span>

<span data-ttu-id="46291-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="46291-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="46291-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="46291-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="46291-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="46291-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="46291-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="46291-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="46291-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="46291-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="46291-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="46291-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="46291-110">Gibt einen zusammengesetzten Wert für Schriftart Attribute an.</span><span class="sxs-lookup"><span data-stu-id="46291-110">Specifies a compound value of font attributes.</span></span> <span data-ttu-id="46291-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="46291-111">Read/write.</span></span> <span data-ttu-id="46291-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="46291-112">**String**.</span></span>

<span data-ttu-id="46291-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="46291-113">**Applies To**</span></span>

[<span data-ttu-id="46291-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="46291-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="46291-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="46291-115">**Tag Syntax**</span></span>

<span data-ttu-id="46291-116"><v: *Element* Style = "Font: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="46291-116"><v: *element* style="font: *expression* "></span></span>

<span data-ttu-id="46291-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="46291-117">**Script Syntax**</span></span>

<span data-ttu-id="46291-118">*Element* . Style. Font = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="46291-118">*element* .style.font="*expression*"</span></span>

<span data-ttu-id="46291-119">*Ausdruck* = *Element*. Style. Font</span><span class="sxs-lookup"><span data-stu-id="46291-119">*expression*=*element*.style.font</span></span>

<span data-ttu-id="46291-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="46291-120">**Remarks**</span></span>

<span data-ttu-id="46291-121">Definiert die Attribute einer Schriftart, einschließlich Familie, Stil, Gewichtung, Größe und Variant.</span><span class="sxs-lookup"><span data-stu-id="46291-121">Defines the attributes of a font, including family, style, weight, size, and variant.</span></span> <span data-ttu-id="46291-122">Die Reihenfolge der Definitionen in der Zeichenfolge lautet: **Schriftart**, **Schriftart, Schriftart, Schrift** **Grad,** Schrift **Grad,** **Zeilenhöhe** und **Schriftfamilie**.</span><span class="sxs-lookup"><span data-stu-id="46291-122">The order of definitions in the string is: **font-style**, **font-variant**, **font-weight**, **font-size**, **line-height**, and **font-family**.</span></span> <span data-ttu-id="46291-123">Die Werte sind identisch mit den standardmäßigen HTML-Format Attributen.</span><span class="sxs-lookup"><span data-stu-id="46291-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="46291-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="46291-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="46291-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="46291-125">**Example**</span></span>

<span data-ttu-id="46291-126">Die Schriftart des TextPath-Texts ist kursiv, Small-Caps, Bold, 36 Punkt Arial.</span><span class="sxs-lookup"><span data-stu-id="46291-126">The font of the textpath text is italic, small-caps, bold, 36 point Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 