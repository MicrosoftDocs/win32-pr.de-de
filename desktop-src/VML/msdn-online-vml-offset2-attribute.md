---
title: VML Offset2-Attribut
description: VML Offset2-Attribut
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b5253e1a27ce8292ee5fc4ce49259db9512a5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517051"
---
# <a name="vml-offset2-attribute"></a><span data-ttu-id="62119-103">VML Offset2-Attribut</span><span class="sxs-lookup"><span data-stu-id="62119-103">VML Offset2 Attribute</span></span>

<span data-ttu-id="62119-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="62119-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="62119-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="62119-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="62119-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="62119-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="62119-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="62119-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="62119-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="62119-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="62119-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="62119-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="62119-110">Bestimmt einen zweiten Offset.</span><span class="sxs-lookup"><span data-stu-id="62119-110">Determines a second offset.</span></span> <span data-ttu-id="62119-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="62119-111">Read/write.</span></span> <span data-ttu-id="62119-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="62119-112">**VgVector2D**.</span></span>

<span data-ttu-id="62119-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="62119-113">**Applies To**</span></span>

[<span data-ttu-id="62119-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="62119-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="62119-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="62119-115">**Tag Syntax**</span></span>

<span data-ttu-id="62119-116"><v: *Element* offset2 = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="62119-116"><v: *element* offset2=" *expression* "></span></span>

<span data-ttu-id="62119-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="62119-117">**Script Syntax**</span></span>

<span data-ttu-id="62119-118">*Element* . offset2 = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="62119-118">*element* .offset2="*expression*"</span></span>

<span data-ttu-id="62119-119">*Ausdruck* = *Element*. offset2</span><span class="sxs-lookup"><span data-stu-id="62119-119">*expression*=*element*.offset2</span></span>

<span data-ttu-id="62119-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="62119-120">**Remarks**</span></span>

<span data-ttu-id="62119-121">Der Standardwert für einen zweiten Offset für den x-Wert ist 0, und der Standardwert für den y-Wert ist 0.</span><span class="sxs-lookup"><span data-stu-id="62119-121">The default for a second offset for the x value is 0 and the default for the y value is 0.</span></span> <span data-ttu-id="62119-122">Werte sind entweder eine absolute Messung oder ein Bruchteil der Form.</span><span class="sxs-lookup"><span data-stu-id="62119-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="62119-123">Bei einem Bruchteil liegen die Werte zwischen 50% und-50%.</span><span class="sxs-lookup"><span data-stu-id="62119-123">If fractional, the values range from 50% to -50%.</span></span>

<span data-ttu-id="62119-124">Verwenden Sie einen zweiten Offset, um besondere Schatteneffekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="62119-124">Use a second offset to create special shadow effects.</span></span> <span data-ttu-id="62119-125">Weitere Informationen zu zweiten Offsets finden Sie unter dem [Type](type-attribute--shadow--vml.md) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="62119-125">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second offsets.</span></span>

<span data-ttu-id="62119-126">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="62119-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="62119-127">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="62119-127">**Example**</span></span>

<span data-ttu-id="62119-128">Für die Form wird ein doppelter Schatten erstellt.</span><span class="sxs-lookup"><span data-stu-id="62119-128">A double shadow is created for the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 