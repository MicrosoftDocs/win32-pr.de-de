---
title: VML-Attribut mit BiLevel
description: VML-Attribut mit BiLevel
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263a9d538a76ba0c9b203cbcf04f8413d4286c34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728312"
---
# <a name="vml-bilevel-attribute"></a><span data-ttu-id="4bd96-103">VML-Attribut mit BiLevel</span><span class="sxs-lookup"><span data-stu-id="4bd96-103">VML Bilevel Attribute</span></span>

<span data-ttu-id="4bd96-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="4bd96-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4bd96-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="4bd96-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4bd96-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="4bd96-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4bd96-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4bd96-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4bd96-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4bd96-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4bd96-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4bd96-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4bd96-110">Bestimmt, ob ein Bild in schwarz und weiß angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4bd96-110">Determines whether an image will be displayed in black and white.</span></span> <span data-ttu-id="4bd96-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4bd96-111">Read/write.</span></span> <span data-ttu-id="4bd96-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="4bd96-112">**VgTriState**.</span></span>

<span data-ttu-id="4bd96-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="4bd96-113">**Applies To**</span></span>

[<span data-ttu-id="4bd96-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="4bd96-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="4bd96-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="4bd96-115">**Tag Syntax**</span></span>

<span data-ttu-id="4bd96-116"><v: *Element* BiLevel = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="4bd96-116"><v: *element* bilevel=" *expression* "></span></span>

<span data-ttu-id="4bd96-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="4bd96-117">**Script Syntax**</span></span>

<span data-ttu-id="4bd96-118">*Element* . BiLevel = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="4bd96-118">*element* .bilevel="*expression*"</span></span>

<span data-ttu-id="4bd96-119">*Ausdruck* = *Element*. BiLevel</span><span class="sxs-lookup"><span data-stu-id="4bd96-119">*expression*=*element*.bilevel</span></span>

<span data-ttu-id="4bd96-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="4bd96-120">**Remarks**</span></span>

<span data-ttu-id="4bd96-121">**True** gibt an, dass das Bild mit zwei Farben (schwarz und weiß) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4bd96-121">If **True**, the image will be displayed using two colors (black and white).</span></span> <span data-ttu-id="4bd96-122">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="4bd96-122">The default is **False**.</span></span> <span data-ttu-id="4bd96-123">Dadurch wird eine ähnliche Wirkung wie bei der Nachlässigkeit erzielt.</span><span class="sxs-lookup"><span data-stu-id="4bd96-123">This creates an effect similar to posterization.</span></span>

<span data-ttu-id="4bd96-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="4bd96-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="4bd96-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="4bd96-125">**Example**</span></span>

<span data-ttu-id="4bd96-126">Das Bild wird nur in schwarz und weiß angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4bd96-126">The image will be displayed in black and white only.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 