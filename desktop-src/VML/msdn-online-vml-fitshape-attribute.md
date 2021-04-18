---
title: VML-fitshape-Attribut
description: VML-fitshape-Attribut
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b05d7bc31afc52c664217ff21d14b40fd0c27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340284"
---
# <a name="vml-fitshape-attribute"></a><span data-ttu-id="bfebf-103">VML-fitshape-Attribut</span><span class="sxs-lookup"><span data-stu-id="bfebf-103">VML FitShape Attribute</span></span>

<span data-ttu-id="bfebf-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="bfebf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bfebf-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="bfebf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bfebf-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="bfebf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bfebf-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="bfebf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bfebf-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bfebf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bfebf-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bfebf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bfebf-110">Definiert, ob der Text dem umgebenden Feld einer Form entspricht.</span><span class="sxs-lookup"><span data-stu-id="bfebf-110">Defines whether the text fits bounding box of a shape.</span></span> <span data-ttu-id="bfebf-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="bfebf-111">Read/write.</span></span> <span data-ttu-id="bfebf-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="bfebf-112">**VgTriState**.</span></span>

<span data-ttu-id="bfebf-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="bfebf-113">**Applies To**</span></span>

[<span data-ttu-id="bfebf-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="bfebf-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="bfebf-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="bfebf-115">**Tag Syntax**</span></span>

<span data-ttu-id="bfebf-116"><v: *Element* fitshape = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="bfebf-116"><v: *element* fitshape=" *expression* "></span></span>

<span data-ttu-id="bfebf-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="bfebf-117">**Script Syntax**</span></span>

<span data-ttu-id="bfebf-118">*Element* . fitshape = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="bfebf-118">*element* .fitshape="*expression*"</span></span>

<span data-ttu-id="bfebf-119">*Ausdruck* = *Element*. fitshape</span><span class="sxs-lookup"><span data-stu-id="bfebf-119">*expression*=*element*.fitshape</span></span>

<span data-ttu-id="bfebf-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="bfebf-120">**Remarks**</span></span>

<span data-ttu-id="bfebf-121">Wenn **true**, wird der Text auf die Ränder des Felds gestreckt, das die gesamte Form definiert.</span><span class="sxs-lookup"><span data-stu-id="bfebf-121">If **True**, stretches the text out to the edges of the box that defines the entire shape.</span></span> <span data-ttu-id="bfebf-122">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="bfebf-122">The default is **False**.</span></span>

<span data-ttu-id="bfebf-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="bfebf-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="bfebf-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="bfebf-124">**Example**</span></span>

<span data-ttu-id="bfebf-125">Der Text wird so gestreckt, dass er der Form entspricht.</span><span class="sxs-lookup"><span data-stu-id="bfebf-125">The text will stretch to fit the shape.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 