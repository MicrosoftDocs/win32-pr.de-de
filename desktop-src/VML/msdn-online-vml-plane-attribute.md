---
title: VML-Ebene-Attribut
description: VML-Ebene-Attribut
ms.assetid: e1de630b-8e25-4052-b316-251046f73e98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f279f008adf8f12f78d6edd790cc533678adc9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948841"
---
# <a name="vml-plane-attribute"></a><span data-ttu-id="ee37f-103">VML-Ebene-Attribut</span><span class="sxs-lookup"><span data-stu-id="ee37f-103">VML Plane Attribute</span></span>

<span data-ttu-id="ee37f-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="ee37f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ee37f-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="ee37f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ee37f-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="ee37f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ee37f-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ee37f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ee37f-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ee37f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ee37f-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ee37f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ee37f-110">Gibt die Ebene an, die sich im rechten Winkel der-Extrusion befindet.</span><span class="sxs-lookup"><span data-stu-id="ee37f-110">Specifies the plane that is at right angles to the extrusion.</span></span> <span data-ttu-id="ee37f-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ee37f-111">Read/write.</span></span> <span data-ttu-id="ee37f-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-112">**String**.</span></span>

<span data-ttu-id="ee37f-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="ee37f-113">**Applies To**</span></span>

[<span data-ttu-id="ee37f-114">Schläuche</span><span class="sxs-lookup"><span data-stu-id="ee37f-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="ee37f-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="ee37f-115">**Tag Syntax**</span></span>

<span data-ttu-id="ee37f-116"><o: *Element* Plane = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="ee37f-116"><o: *element* plane=" *expression* "></span></span>

<span data-ttu-id="ee37f-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="ee37f-117">**Script Syntax**</span></span>

<span data-ttu-id="ee37f-118">*Element* . Plane = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="ee37f-118">*element* .plane="*expression*"</span></span>

<span data-ttu-id="ee37f-119">*Ausdruck* = *Element*. Plane</span><span class="sxs-lookup"><span data-stu-id="ee37f-119">*expression*=*element*.plane</span></span>

<span data-ttu-id="ee37f-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="ee37f-120">**Remarks**</span></span>

<span data-ttu-id="ee37f-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="ee37f-121">Values include:</span></span>



| <span data-ttu-id="ee37f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ee37f-122">Value</span></span> | <span data-ttu-id="ee37f-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee37f-123">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="ee37f-124">xy</span><span class="sxs-lookup"><span data-stu-id="ee37f-124">xy</span></span>    | <span data-ttu-id="ee37f-125">Die-Extrusion erfolgt im rechten Winkel der XY-Ebene.</span><span class="sxs-lookup"><span data-stu-id="ee37f-125">Extrusion is at right angles to the xy -plane.</span></span> <span data-ttu-id="ee37f-126">Standard</span><span class="sxs-lookup"><span data-stu-id="ee37f-126">Default</span></span> |
| <span data-ttu-id="ee37f-127">ZX</span><span class="sxs-lookup"><span data-stu-id="ee37f-127">zx</span></span>    | <span data-ttu-id="ee37f-128">Die-Extrusion erfolgt in der rechten Ecke der ZX-Ebene.</span><span class="sxs-lookup"><span data-stu-id="ee37f-128">Extrusion is at right angles to the zx -plane.</span></span>         |
| <span data-ttu-id="ee37f-129">YZ</span><span class="sxs-lookup"><span data-stu-id="ee37f-129">yz</span></span>    | <span data-ttu-id="ee37f-130">Die-Extrusion ist im rechten Winkel zur YZ-Ebene.</span><span class="sxs-lookup"><span data-stu-id="ee37f-130">Extrusion is at right angles to the yz -plane.</span></span>         |



 

<span data-ttu-id="ee37f-131">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="ee37f-131">*Microsoft Office Extensions Attribute*</span></span>

 

 