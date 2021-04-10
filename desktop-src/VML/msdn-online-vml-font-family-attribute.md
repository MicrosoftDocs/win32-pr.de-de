---
title: VML-Font-Family Attribut
description: VML-Font-Family Attribut
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29aa72775e8f00e195462cf3df06097d267b908
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039584"
---
# <a name="vml-font-family-attribute"></a><span data-ttu-id="a4adf-103">VML-Font-Family Attribut</span><span class="sxs-lookup"><span data-stu-id="a4adf-103">VML Font-Family Attribute</span></span>

<span data-ttu-id="a4adf-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a4adf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a4adf-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="a4adf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a4adf-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="a4adf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a4adf-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a4adf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a4adf-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a4adf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a4adf-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a4adf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a4adf-110">Definiert die Familie der TextPath-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="a4adf-110">Defines the family of the textpath font.</span></span> <span data-ttu-id="a4adf-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a4adf-111">Read/write.</span></span> <span data-ttu-id="a4adf-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="a4adf-112">**String**.</span></span>

<span data-ttu-id="a4adf-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="a4adf-113">**Applies To**</span></span>

[<span data-ttu-id="a4adf-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="a4adf-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="a4adf-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="a4adf-115">**Tag Syntax**</span></span>

<span data-ttu-id="a4adf-116"><v: *Element* Style = "Font-Family: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a4adf-116"><v: *element* style="font-family: *expression* "></span></span>

<span data-ttu-id="a4adf-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="a4adf-117">**Script Syntax**</span></span>

<span data-ttu-id="a4adf-118">*Element* . Style. FontFamily = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="a4adf-118">*element* .style.fontfamily="*expression*"</span></span>

<span data-ttu-id="a4adf-119">*Ausdruck* = *Element*. Style. FontFamily</span><span class="sxs-lookup"><span data-stu-id="a4adf-119">*expression*=*element*.style.fontfamily</span></span>

<span data-ttu-id="a4adf-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="a4adf-120">**Remarks**</span></span>

<span data-ttu-id="a4adf-121">Definiert den Schriftart Namen.</span><span class="sxs-lookup"><span data-stu-id="a4adf-121">Defines the font name.</span></span> <span data-ttu-id="a4adf-122">Bestimmte Namen wie z. b. Arial können verwendet werden oder generische Typen wie Serif, Sans-Serif, currsive, Fantasy oder Monospace.</span><span class="sxs-lookup"><span data-stu-id="a4adf-122">Specific names such as Arial can be used or generic types such as serif, sans-serif, cursive, fantasy, or monospace.</span></span> <span data-ttu-id="a4adf-123">Die Werte sind identisch mit den standardmäßigen HTML-Format Attributen.</span><span class="sxs-lookup"><span data-stu-id="a4adf-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="a4adf-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="a4adf-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="a4adf-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="a4adf-125">**Example**</span></span>

<span data-ttu-id="a4adf-126">Die Schriftfamilie des Texts ist Arial.</span><span class="sxs-lookup"><span data-stu-id="a4adf-126">The font family of the text is Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 