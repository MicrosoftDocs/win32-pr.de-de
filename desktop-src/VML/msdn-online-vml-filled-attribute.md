---
title: Ausgefülltes VML-Attribut
description: Ausgefülltes VML-Attribut
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 232d8b36b6d272c3a1ee8c17f3ddeca023ab4708
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474188"
---
# <a name="vml-filled-attribute"></a><span data-ttu-id="c0db4-103">Ausgefülltes VML-Attribut</span><span class="sxs-lookup"><span data-stu-id="c0db4-103">VML Filled Attribute</span></span>

<span data-ttu-id="c0db4-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="c0db4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c0db4-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="c0db4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c0db4-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="c0db4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c0db4-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c0db4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c0db4-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c0db4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c0db4-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c0db4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c0db4-110">Bestimmt, ob der geschlossene Pfad ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="c0db4-110">Determines whether the closed path will be filled.</span></span> <span data-ttu-id="c0db4-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c0db4-111">Read/write.</span></span> <span data-ttu-id="c0db4-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="c0db4-112">**VgTriState**.</span></span>

<span data-ttu-id="c0db4-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="c0db4-113">**Applies To**</span></span>

[<span data-ttu-id="c0db4-114">Form</span><span class="sxs-lookup"><span data-stu-id="c0db4-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c0db4-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="c0db4-115">**Tag Syntax**</span></span>

<span data-ttu-id="c0db4-116"><v: *Element* ausgefüllt = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="c0db4-116"><v: *element* filled=" *expression* "></span></span>

<span data-ttu-id="c0db4-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="c0db4-117">**Script Syntax**</span></span>

<span data-ttu-id="c0db4-118">*Element* . Fill = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="c0db4-118">*element* .filled="*expression*"</span></span>

<span data-ttu-id="c0db4-119">*Ausdruck* = *Element*. ausgefüllt</span><span class="sxs-lookup"><span data-stu-id="c0db4-119">*expression*=*element*.filled</span></span>

<span data-ttu-id="c0db4-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="c0db4-120">**Remarks**</span></span>

<span data-ttu-id="c0db4-121">Der Wert wird aus dem **on** -Attribut des [Fill](msdn-online-vml-fill-element.md) -Elements dupliziert.</span><span class="sxs-lookup"><span data-stu-id="c0db4-121">The value is duplicated from the **On** attribute of the [Fill](msdn-online-vml-fill-element.md) element.</span></span>

<span data-ttu-id="c0db4-122">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="c0db4-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="c0db4-123">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="c0db4-123">**Example**</span></span>

<span data-ttu-id="c0db4-124">Der Shape-Pfad ist ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="c0db4-124">The shape path is filled.</span></span>


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="c0db4-125">[Beispiel für ausgefülltes Attribut](/previous-versions/bb229669(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c0db4-125">[Filled Attribute Example](/previous-versions/bb229669(v=vs.85)).</span></span> <span data-ttu-id="c0db4-126">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="c0db4-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 