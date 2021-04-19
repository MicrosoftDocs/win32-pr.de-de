---
title: VML-Attribut "tdarrowlength"
description: VML-Attribut "tdarrowlength"
ms.assetid: aab898b6-4c59-4471-81fd-621f79610d63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d9d8bfbd24a6a1b79208d50d4d2aef956a5bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341938"
---
# <a name="vml-endarrowlength-attribute"></a><span data-ttu-id="7afca-103">VML-Attribut "tdarrowlength"</span><span class="sxs-lookup"><span data-stu-id="7afca-103">VML EndArrowLength Attribute</span></span>

<span data-ttu-id="7afca-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="7afca-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7afca-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="7afca-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7afca-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="7afca-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7afca-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7afca-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7afca-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7afca-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7afca-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7afca-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7afca-110">Definiert eine Pfeilspitzen Länge für das Ende einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="7afca-110">Defines an arrowhead length for the end of a line.</span></span> <span data-ttu-id="7afca-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7afca-111">Read/write.</span></span> <span data-ttu-id="7afca-112">**Vgarrowheadlength**.</span><span class="sxs-lookup"><span data-stu-id="7afca-112">**VgArrowheadLength**.</span></span>

<span data-ttu-id="7afca-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="7afca-113">**Applies To**</span></span>

[<span data-ttu-id="7afca-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="7afca-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="7afca-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="7afca-115">**Tag Syntax**</span></span>

<span data-ttu-id="7afca-116"><v: *Element* endarrowlength = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="7afca-116"><v: *element* endarrowlength=" *expression* "></span></span>

<span data-ttu-id="7afca-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="7afca-117">**Script Syntax**</span></span>

<span data-ttu-id="7afca-118">*Element* . endarrowlength = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="7afca-118">*element* .endarrowlength="*expression*"</span></span>

<span data-ttu-id="7afca-119">*Ausdruck* = *Element*. endarrowlength</span><span class="sxs-lookup"><span data-stu-id="7afca-119">*expression*=*element*.endarrowlength</span></span>

<span data-ttu-id="7afca-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="7afca-120">**Remarks**</span></span>

<span data-ttu-id="7afca-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="7afca-121">Values include:</span></span>

-   <span data-ttu-id="7afca-122">Short</span><span class="sxs-lookup"><span data-stu-id="7afca-122">Short</span></span>
-   <span data-ttu-id="7afca-123">Mittel (Standard)</span><span class="sxs-lookup"><span data-stu-id="7afca-123">Medium (default)</span></span>
-   <span data-ttu-id="7afca-124">Long</span><span class="sxs-lookup"><span data-stu-id="7afca-124">Long</span></span>

<span data-ttu-id="7afca-125">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="7afca-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="7afca-126">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="7afca-126">**Example**</span></span>

<span data-ttu-id="7afca-127">Eine Linie wird mit einer kurzen klassischen Pfeilspitze am Ende des Strichs gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7afca-127">A line is drawn with a short classic arrowhead on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowlength="short"/>
   </v:line>
```



 

 