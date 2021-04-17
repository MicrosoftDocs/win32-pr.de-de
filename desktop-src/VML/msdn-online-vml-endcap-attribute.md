---
title: VML-EndCap-Attribut
description: VML-EndCap-Attribut
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 726d2bba2128ebb1897f306ae608f4bebb48d63f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316418"
---
# <a name="vml-endcap-attribute"></a><span data-ttu-id="ca54b-103">VML-EndCap-Attribut</span><span class="sxs-lookup"><span data-stu-id="ca54b-103">VML EndCap Attribute</span></span>

<span data-ttu-id="ca54b-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="ca54b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ca54b-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="ca54b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ca54b-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="ca54b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ca54b-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ca54b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ca54b-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ca54b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ca54b-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ca54b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ca54b-110">Definiert den Stil für das Ende eines Strichs.</span><span class="sxs-lookup"><span data-stu-id="ca54b-110">Defines the cap style for the end of a stroke.</span></span> <span data-ttu-id="ca54b-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ca54b-111">Read/write.</span></span> <span data-ttu-id="ca54b-112">**Vglineendcapstyle**.</span><span class="sxs-lookup"><span data-stu-id="ca54b-112">**VgLineEndCapStyle**.</span></span>

<span data-ttu-id="ca54b-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="ca54b-113">**Applies To**</span></span>

[<span data-ttu-id="ca54b-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="ca54b-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="ca54b-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="ca54b-115">**Tag Syntax**</span></span>

<span data-ttu-id="ca54b-116"><v: *Element* EndCap = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="ca54b-116"><v: *element* endcap=" *expression* "></span></span>

<span data-ttu-id="ca54b-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="ca54b-117">**Script Syntax**</span></span>

<span data-ttu-id="ca54b-118">*Element* . EndCap = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="ca54b-118">*element* .endcap="*expression*"</span></span>

<span data-ttu-id="ca54b-119">*Ausdruck* = *Element*. EndCap</span><span class="sxs-lookup"><span data-stu-id="ca54b-119">*expression*=*element*.endcap</span></span>

<span data-ttu-id="ca54b-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="ca54b-120">**Remarks**</span></span>

<span data-ttu-id="ca54b-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="ca54b-121">Values include:</span></span>

-   <span data-ttu-id="ca54b-122">Flat (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca54b-122">Flat (default)</span></span>
-   <span data-ttu-id="ca54b-123">Square</span><span class="sxs-lookup"><span data-stu-id="ca54b-123">Square</span></span>
-   <span data-ttu-id="ca54b-124">Round</span><span class="sxs-lookup"><span data-stu-id="ca54b-124">Round</span></span>

<span data-ttu-id="ca54b-125">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="ca54b-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="ca54b-126">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="ca54b-126">**Example**</span></span>

<span data-ttu-id="ca54b-127">Eine Linie wird mit einer flachen Obergrenze am Ende des Strichs gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ca54b-127">A line is drawn with a flat cap on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 