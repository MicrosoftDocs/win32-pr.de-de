---
title: VML-XScale-Attribut
description: VML-XScale-Attribut
ms.assetid: b876201d-87d1-4795-8f7f-33712a8bf493
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3221ab44cad9eb9f422ce451f618eb8eeba55bcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315303"
---
# <a name="vml-xscale-attribute"></a><span data-ttu-id="0289b-103">VML-XScale-Attribut</span><span class="sxs-lookup"><span data-stu-id="0289b-103">VML XScale Attribute</span></span>

<span data-ttu-id="0289b-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="0289b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0289b-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="0289b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0289b-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="0289b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0289b-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0289b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0289b-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0289b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0289b-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0289b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0289b-110">Bestimmt, ob anstelle des Shape-Pfads ein geradliniger Textpfad verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0289b-110">Determines whether a straight textpath will be used instead of the shape path.</span></span> <span data-ttu-id="0289b-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0289b-111">Read/write.</span></span> <span data-ttu-id="0289b-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="0289b-112">**VgTriState**.</span></span>

<span data-ttu-id="0289b-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="0289b-113">**Applies To**</span></span>

[<span data-ttu-id="0289b-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="0289b-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="0289b-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="0289b-115">**Tag Syntax**</span></span>

<span data-ttu-id="0289b-116"><v: *Element* Style = "XScale: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="0289b-116"><v: *element* style="xscale: *expression* "></span></span>

<span data-ttu-id="0289b-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="0289b-117">**Script Syntax**</span></span>

<span data-ttu-id="0289b-118">*Element* . Style. XScale = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="0289b-118">*element* .style.xscale="*expression*"</span></span>

<span data-ttu-id="0289b-119">*Ausdruck* = *Element*. Style. XScale</span><span class="sxs-lookup"><span data-stu-id="0289b-119">*expression*=*element*.style.xscale</span></span>

<span data-ttu-id="0289b-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="0289b-120">**Remarks**</span></span>

<span data-ttu-id="0289b-121">Wenn der Wert **true** ist, wird der Text entlang von links nach rechts entlang des x-Werts der unteren Grenze der Form ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0289b-121">If **True**, the text runs along apath from left to right along the x value of the lower boundary of the shape.</span></span> <span data-ttu-id="0289b-122">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="0289b-122">The default value is **False**.</span></span>

<span data-ttu-id="0289b-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="0289b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="0289b-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="0289b-124">**Example**</span></span>

<span data-ttu-id="0289b-125">Der Text wird so angezeigt, als ob er in einer horizontalen Linie gezeichnet würde, auch wenn der Shape-Pfad diagonal ist.</span><span class="sxs-lookup"><span data-stu-id="0289b-125">The text will appear as if it were drawn on a horizontal line, even though the shape path is a diagonal.</span></span>


```HTML
   <v:line from="100 100" to="400 400">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="xscale:true;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 