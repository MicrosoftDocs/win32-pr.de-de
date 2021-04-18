---
title: Positions Attribut (H) (VML)
description: Positions Attribut (H) (VML)
ms.assetid: 0bae708d-5409-4609-a102-7f799f2c1fbb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac310c0fad457beaf3b9aeb04671b7ffbb1dbd8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340936"
---
# <a name="position-attribute-hvml"></a><span data-ttu-id="8c9d0-103">Positions Attribut (H) (VML)</span><span class="sxs-lookup"><span data-stu-id="8c9d0-103">Position Attribute (H)(VML)</span></span>

<span data-ttu-id="8c9d0-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8c9d0-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8c9d0-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8c9d0-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8c9d0-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8c9d0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8c9d0-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8c9d0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8c9d0-110">Gibt THEX-und y-Werte des Handles an.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-110">Specifies thex and y values of the handle.</span></span> <span data-ttu-id="8c9d0-111">Lese-/Schreib-VgVector2D. </span><span class="sxs-lookup"><span data-stu-id="8c9d0-111">Read/write **VgVector2D**.</span></span>

<span data-ttu-id="8c9d0-112">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="8c9d0-112">**Applies To**</span></span>

<span data-ttu-id="8c9d0-113">[H](msdn-online-vml-h-element.md) (Unterelement von [Handles](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="8c9d0-113">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="8c9d0-114">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="8c9d0-114">**Tag Syntax**</span></span>

<span data-ttu-id="8c9d0-115"><v: *Element* Position = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="8c9d0-115"><v: *element* position=" *expression* "></span></span>

<span data-ttu-id="8c9d0-116">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="8c9d0-116">**Remarks**</span></span>

<span data-ttu-id="8c9d0-117">x-und y-Werte können einen der folgenden Typen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="8c9d0-117">x and y values can be one of the following types:</span></span>

-   <span data-ttu-id="8c9d0-118">Konstante</span><span class="sxs-lookup"><span data-stu-id="8c9d0-118">constant</span></span>
-   <span data-ttu-id="8c9d0-119">Formel (z. b. @2 )</span><span class="sxs-lookup"><span data-stu-id="8c9d0-119">formula (for example, @2)</span></span>
-   <span data-ttu-id="8c9d0-120">anpassen (z. b. \# 3)</span><span class="sxs-lookup"><span data-stu-id="8c9d0-120">adjust (for example, \#3)</span></span>
-   <span data-ttu-id="8c9d0-121">Zentrum</span><span class="sxs-lookup"><span data-stu-id="8c9d0-121">center</span></span>
-   <span data-ttu-id="8c9d0-122">TopLeft</span><span class="sxs-lookup"><span data-stu-id="8c9d0-122">topleft</span></span>
-   <span data-ttu-id="8c9d0-123">BottomRight</span><span class="sxs-lookup"><span data-stu-id="8c9d0-123">bottomright</span></span>

<span data-ttu-id="8c9d0-124">Wenn einer der obigen Typen außer " *Anpassen* " angegeben ist, wird die Position des Handles in dieser Dimension korrigiert.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-124">If any of the above types except *adjust* are specified, the handle position is fixed in that dimension.</span></span> <span data-ttu-id="8c9d0-125">Wenn ein Anpassungs handle angegeben ist, kann das Handle in dieser Dimension verschoben werden, und der Anpassungswert wird durch die Position des Handles bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-125">If an adjust handle is specified, the handle is free to move in that dimension and the adjust value is determined by the position of the handle.</span></span>

<span data-ttu-id="8c9d0-126">Wenn ein [Polar](msdn-online-vml-polar-attribute.md) Attribut angegeben wird, stellt das **Positions** Attribut die RADIUS-und Winkelwerte des Handles anstelle von x und y dar.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-126">If a [Polar](msdn-online-vml-polar-attribute.md) attribute is specified, the **Position** attribute represents the radius and angle values of the handle instead of x and y.</span></span>

<span data-ttu-id="8c9d0-127">Der Standardwert ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-127">The default value is 0,0.</span></span>

<span data-ttu-id="8c9d0-128">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="8c9d0-128">*VML Standard Attribute*</span></span>

 

 