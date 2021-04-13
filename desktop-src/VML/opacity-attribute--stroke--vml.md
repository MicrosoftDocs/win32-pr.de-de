---
title: Opacity-Attribut (Strich) (VML)
description: Opacity-Attribut (Strich) (VML)
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc97f445ede54676d73e95a60ec039ab214f4a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474157"
---
# <a name="opacity-attribute-strokevml"></a><span data-ttu-id="e3347-103">Opacity-Attribut (Strich) (VML)</span><span class="sxs-lookup"><span data-stu-id="e3347-103">Opacity Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="e3347-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="e3347-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e3347-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="e3347-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e3347-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="e3347-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e3347-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e3347-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e3347-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e3347-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e3347-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e3347-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e3347-110">Definiert den Umfang der Transparenz eines Strichs.</span><span class="sxs-lookup"><span data-stu-id="e3347-110">Defines the amount of transparency of a stroke.</span></span> <span data-ttu-id="e3347-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e3347-111">Read/write.</span></span> <span data-ttu-id="e3347-112">**Vgbruchteile**.</span><span class="sxs-lookup"><span data-stu-id="e3347-112">**VgFraction**.</span></span>

<span data-ttu-id="e3347-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="e3347-113">**Applies To**</span></span>

[<span data-ttu-id="e3347-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="e3347-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="e3347-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="e3347-115">**Tag Syntax**</span></span>

<span data-ttu-id="e3347-116"><v: *Element* Deckkraft = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="e3347-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="e3347-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="e3347-117">**Script Syntax**</span></span>

<span data-ttu-id="e3347-118">*Element* . Opacity = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="e3347-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="e3347-119">*Ausdruck* = *Element*. Deckkraft</span><span class="sxs-lookup"><span data-stu-id="e3347-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="e3347-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="e3347-120">**Remarks**</span></span>

<span data-ttu-id="e3347-121">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="e3347-121">The default value is 1.0.</span></span>

<span data-ttu-id="e3347-122">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="e3347-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="e3347-123">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="e3347-123">**Example**</span></span>

<span data-ttu-id="e3347-124">Der Strich ist 50% transparent.</span><span class="sxs-lookup"><span data-stu-id="e3347-124">The stroke is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 