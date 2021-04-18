---
title: VML-lockrotationcenter-Attribut
description: VML-lockrotationcenter-Attribut
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338487"
---
# <a name="vml-lockrotationcenter-attribute"></a><span data-ttu-id="a0d8e-103">VML-lockrotationcenter-Attribut</span><span class="sxs-lookup"><span data-stu-id="a0d8e-103">VML LockRotationCenter Attribute</span></span>

<span data-ttu-id="a0d8e-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a0d8e-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a0d8e-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a0d8e-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a0d8e-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a0d8e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a0d8e-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a0d8e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a0d8e-110">Bestimmt, ob die Drehung des extrudierten Objekts durch das [RotationAngle](msdn-online-vml-rotationangle-attribute.md) -Attribut angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-110">Determines whether the rotation of the extruded object is specified by the [RotationAngle](msdn-online-vml-rotationangle-attribute.md) attribute.</span></span> <span data-ttu-id="a0d8e-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-111">Read/write.</span></span> <span data-ttu-id="a0d8e-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-112">**VgTriState**.</span></span>

<span data-ttu-id="a0d8e-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="a0d8e-113">**Applies To**</span></span>

[<span data-ttu-id="a0d8e-114">Schläuche</span><span class="sxs-lookup"><span data-stu-id="a0d8e-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="a0d8e-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="a0d8e-115">**Tag Syntax**</span></span>

<span data-ttu-id="a0d8e-116"><o: *Element* lockrotationcenter = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a0d8e-116"><o: *element* lockrotationcenter=" *expression* "></span></span>

<span data-ttu-id="a0d8e-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="a0d8e-117">**Script Syntax**</span></span>

<span data-ttu-id="a0d8e-118">*Element* . lockrotationcenter = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="a0d8e-118">*element* .lockrotationcenter="*expression*"</span></span>

<span data-ttu-id="a0d8e-119">*Ausdruck* = *Element*. lockrotationcenter</span><span class="sxs-lookup"><span data-stu-id="a0d8e-119">*expression*=*element*.lockrotationcenter</span></span>

<span data-ttu-id="a0d8e-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="a0d8e-120">**Remarks**</span></span>

<span data-ttu-id="a0d8e-121">Wenn der Wert **false** ist, wird die Drehung durch das [Orientation](msdn-online-vml-orientation-attribute.md) -Attribut angegeben.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-121">If **False**, the rotation is specified by the [Orientation](msdn-online-vml-orientation-attribute.md) attribute.</span></span> <span data-ttu-id="a0d8e-122">Der Standardwert ist **True**.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-122">The default is **True**.</span></span>

<span data-ttu-id="a0d8e-123">Beachten Sie dabei Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a0d8e-123">Note that:</span></span>


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



<span data-ttu-id="a0d8e-124">der gleiche wie:</span><span class="sxs-lookup"><span data-stu-id="a0d8e-124">is the same as:</span></span>


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



<span data-ttu-id="a0d8e-125">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="a0d8e-125">*Microsoft Office Extensions Attribute*</span></span>

 

 