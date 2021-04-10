---
title: Offset-Attribut (Schatten) (VML)
description: Offset-Attribut (Schatten) (VML)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61daaf3b311a87a3e3bcf064ceffc491e1134fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948805"
---
# <a name="offset-attribute-shadowvml"></a><span data-ttu-id="f8eb4-103">Offset-Attribut (Schatten) (VML)</span><span class="sxs-lookup"><span data-stu-id="f8eb4-103">Offset Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="f8eb4-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="f8eb4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f8eb4-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="f8eb4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f8eb4-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="f8eb4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f8eb4-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="f8eb4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f8eb4-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f8eb4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f8eb4-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f8eb4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f8eb4-110">Definiert, wie weit der Schatten sich hinter der Form erstreckt.</span><span class="sxs-lookup"><span data-stu-id="f8eb4-110">Defines how far the shadow extends past the shape.</span></span> <span data-ttu-id="f8eb4-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f8eb4-111">Read/write.</span></span> <span data-ttu-id="f8eb4-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="f8eb4-112">**VgVector2D**.</span></span>

<span data-ttu-id="f8eb4-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="f8eb4-113">**Applies To**</span></span>

[<span data-ttu-id="f8eb4-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="f8eb4-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="f8eb4-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="f8eb4-115">**Tag Syntax**</span></span>

<span data-ttu-id="f8eb4-116"><v: *Element* Offset = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="f8eb4-116"><v: *element* offset=" *expression* "></span></span>

<span data-ttu-id="f8eb4-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="f8eb4-117">**Script Syntax**</span></span>

<span data-ttu-id="f8eb4-118">*Element* . Offset = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="f8eb4-118">*element* .offset="*expression*"</span></span>

<span data-ttu-id="f8eb4-119">*Ausdruck* = *Element*. Offset</span><span class="sxs-lookup"><span data-stu-id="f8eb4-119">*expression*=*element*.offset</span></span>

<span data-ttu-id="f8eb4-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="f8eb4-120">**Remarks**</span></span>

<span data-ttu-id="f8eb4-121">Der Standard Offset für den x-Wert ist 2pt, und der Standardwert für den y-Wert ist 2pt.</span><span class="sxs-lookup"><span data-stu-id="f8eb4-121">The default offset for the x value is 2pt and the default for the y value is 2pt.</span></span> <span data-ttu-id="f8eb4-122">Werte sind entweder eine absolute Messung oder ein Bruchteil der Form.</span><span class="sxs-lookup"><span data-stu-id="f8eb4-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="f8eb4-123">Bei einem Bruchteil liegen Sie zwischen 50% und-50%.</span><span class="sxs-lookup"><span data-stu-id="f8eb4-123">If fractional, they range from 50% to -50%.</span></span>

<span data-ttu-id="f8eb4-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="f8eb4-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="f8eb4-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f8eb4-125">**Example**</span></span>

<span data-ttu-id="f8eb4-126">Die Form weist einen Schatten mit einem Offset von 5 Punkten nach unten und 10 nach rechts auf.</span><span class="sxs-lookup"><span data-stu-id="f8eb4-126">The shape has a shadow with an offset of 5 points down and 10 points to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 