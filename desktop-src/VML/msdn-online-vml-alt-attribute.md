---
title: VML-alt-Attribut
description: VML-alt-Attribut
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b420d556e69ed2f987a3a3b10a5709f926dc5c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209337"
---
# <a name="vml-alt-attribute"></a><span data-ttu-id="3088a-103">VML-alt-Attribut</span><span class="sxs-lookup"><span data-stu-id="3088a-103">VML Alt Attribute</span></span>

<span data-ttu-id="3088a-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="3088a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3088a-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="3088a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3088a-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="3088a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3088a-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3088a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3088a-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3088a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3088a-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3088a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3088a-110">Definiert alternativen Text, der anstelle einer Grafik angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3088a-110">Defines alternative text to be displayed instead of a graphic.</span></span> <span data-ttu-id="3088a-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3088a-111">Read/write.</span></span> <span data-ttu-id="3088a-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="3088a-112">**String**.</span></span>

<span data-ttu-id="3088a-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="3088a-113">**Applies To**</span></span>

[<span data-ttu-id="3088a-114">Form</span><span class="sxs-lookup"><span data-stu-id="3088a-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3088a-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="3088a-115">**Tag Syntax**</span></span>

<span data-ttu-id="3088a-116"><v: *Element* alt = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="3088a-116"><v: *element* alt=" *expression* "></span></span>

<span data-ttu-id="3088a-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="3088a-117">**Script Syntax**</span></span>

<span data-ttu-id="3088a-118">*Element* . alt = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="3088a-118">*element* .alt="*expression*"</span></span>

<span data-ttu-id="3088a-119">*Ausdruck* = *Element*. alt</span><span class="sxs-lookup"><span data-stu-id="3088a-119">*expression*=*element*.alt</span></span>

<span data-ttu-id="3088a-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="3088a-120">**Remarks**</span></span>

<span data-ttu-id="3088a-121">Das **alt** -Attribut ähnelt dem standardmäßigen HTML- **alt** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="3088a-121">The **Alt** attribute is similar to the standard HTML **Alt** attribute.</span></span> <span data-ttu-id="3088a-122">Dieses Attribut bietet eine Möglichkeit für Browser, die Text in Sprache konvertieren, um grafische Elemente auf einer Seite zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3088a-122">This attribute provides a way for browsers that convert text to speech to describe graphical elements on a page.</span></span>

<span data-ttu-id="3088a-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="3088a-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3088a-124">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="3088a-124">**See Also**</span></span>

[<span data-ttu-id="3088a-125">Form</span><span class="sxs-lookup"><span data-stu-id="3088a-125">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3088a-126">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3088a-126">**Example**</span></span>

<span data-ttu-id="3088a-127">Das **alt** -Element unten zeigt den Ausdruck "rotes Rechteck" in Browsern an, in denen Webseiten in gesprochene Ausdrücke konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="3088a-127">The **Alt** element below will display the phrase "Red rectangle" in browsers that convert Web pages to spoken phrases.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="3088a-128">[Beispiel](/previous-versions/bb229663(v=vs.85))für ein alt-Attribut.</span><span class="sxs-lookup"><span data-stu-id="3088a-128">[Alt Attribute Example](/previous-versions/bb229663(v=vs.85)).</span></span> <span data-ttu-id="3088a-129">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="3088a-129">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 