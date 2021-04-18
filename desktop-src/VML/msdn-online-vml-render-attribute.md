---
title: VML-Attribut "Rendering"
description: VML-Attribut "Rendering"
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70872e823a2d43d6a605fbf07a817473b19a125a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340279"
---
# <a name="vml-render-attribute"></a><span data-ttu-id="b3bd8-103">VML-Attribut "Rendering"</span><span class="sxs-lookup"><span data-stu-id="b3bd8-103">VML Render Attribute</span></span>

<span data-ttu-id="b3bd8-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="b3bd8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b3bd8-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="b3bd8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b3bd8-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="b3bd8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b3bd8-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b3bd8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b3bd8-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b3bd8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b3bd8-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b3bd8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b3bd8-110">Definiert den Renderingmodus der-Extrusion.</span><span class="sxs-lookup"><span data-stu-id="b3bd8-110">Defines the rendering mode of the extrusion.</span></span> <span data-ttu-id="b3bd8-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b3bd8-111">Read/write.</span></span> <span data-ttu-id="b3bd8-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="b3bd8-112">**String**.</span></span>

<span data-ttu-id="b3bd8-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="b3bd8-113">**Applies To**</span></span>

[<span data-ttu-id="b3bd8-114">Schläuche</span><span class="sxs-lookup"><span data-stu-id="b3bd8-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="b3bd8-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="b3bd8-115">**Tag Syntax**</span></span>

<span data-ttu-id="b3bd8-116"><o: *Element* Rendering = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="b3bd8-116"><o: *element* render=" *expression* "></span></span>

<span data-ttu-id="b3bd8-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="b3bd8-117">**Script Syntax**</span></span>

<span data-ttu-id="b3bd8-118">*Element* . Rendering = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="b3bd8-118">*element* .render="*expression*"</span></span>

<span data-ttu-id="b3bd8-119">*Ausdruck* = *Element*. Rendering</span><span class="sxs-lookup"><span data-stu-id="b3bd8-119">*expression*=*element*.render</span></span>

<span data-ttu-id="b3bd8-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="b3bd8-120">**Remarks**</span></span>

<span data-ttu-id="b3bd8-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="b3bd8-121">Values include:</span></span>



| <span data-ttu-id="b3bd8-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b3bd8-122">Value</span></span>        | <span data-ttu-id="b3bd8-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3bd8-123">Description</span></span>                                                   |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="b3bd8-124">festem</span><span class="sxs-lookup"><span data-stu-id="b3bd8-124">solid</span></span>        | <span data-ttu-id="b3bd8-125">Rendering zeigt eine solide Form an.</span><span class="sxs-lookup"><span data-stu-id="b3bd8-125">Rendering displays a solid shape.</span></span> <span data-ttu-id="b3bd8-126">Standard.</span><span class="sxs-lookup"><span data-stu-id="b3bd8-126">Default.</span></span>                    |
| <span data-ttu-id="b3bd8-127">Draht Modell</span><span class="sxs-lookup"><span data-stu-id="b3bd8-127">wireframe</span></span>    | <span data-ttu-id="b3bd8-128">Rendering zeigt eine Draht Modell-Form an.</span><span class="sxs-lookup"><span data-stu-id="b3bd8-128">Rendering displays a wireframe shape.</span></span>                         |
| <span data-ttu-id="b3bd8-129">boundingcube</span><span class="sxs-lookup"><span data-stu-id="b3bd8-129">boundingcube</span></span> | <span data-ttu-id="b3bd8-130">Rendering zeigt den umgebenden Cube an, der die Form enthält.</span><span class="sxs-lookup"><span data-stu-id="b3bd8-130">Rendering displays the bounding cube that contains the shape.</span></span> |



 

<span data-ttu-id="b3bd8-131">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="b3bd8-131">*Microsoft Office Extensions Attribute*</span></span>

 

 