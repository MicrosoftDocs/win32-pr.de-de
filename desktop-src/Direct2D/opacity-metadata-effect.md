---
title: Auswirkungen der Deckkraft-Metadaten
description: Mit diesem Effekt können Sie einen Bereich eines Eingabe Bilds als nicht transparent markieren, sodass interne renderinoptimierungen für das Diagramm möglich sind.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84d90ba1c4b1186e3e682ec94a0c9c17bdfc73e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105447"
---
# <a name="opacity-metadata-effect"></a><span data-ttu-id="6fd14-103">Auswirkungen der Deckkraft-Metadaten</span><span class="sxs-lookup"><span data-stu-id="6fd14-103">Opacity metadata effect</span></span>

<span data-ttu-id="6fd14-104">Mit diesem Effekt können Sie einen Bereich eines Eingabe Bilds als nicht transparent markieren, sodass interne renderinoptimierungen für das Diagramm möglich sind.</span><span class="sxs-lookup"><span data-stu-id="6fd14-104">You can use this effect to mark an area of an input image as opaque, so internal rendering optimizations to the graph are possible.</span></span>

> [!Note]  
> <span data-ttu-id="6fd14-105">Durch diesen Effekt wird das Abbild nicht als nicht transparent geändert.</span><span class="sxs-lookup"><span data-stu-id="6fd14-105">This effect doesn't modify the image itself to be opaque.</span></span> <span data-ttu-id="6fd14-106">Er ändert die dem Bild zugeordneten Daten, sodass der Renderer annimmt, dass der angegebene Bereich nicht transparent ist.</span><span class="sxs-lookup"><span data-stu-id="6fd14-106">It modifies data associated with the image so the renderer assumes the specified region is opaque.</span></span>

 

<span data-ttu-id="6fd14-107">Die CLSID für diesen Effekt ist CLSID \_ D2D1OpacityMetadata.</span><span class="sxs-lookup"><span data-stu-id="6fd14-107">The CLSID for this effect is CLSID\_D2D1OpacityMetadata.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="6fd14-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6fd14-108">Effect properties</span></span>



| <span data-ttu-id="6fd14-109">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="6fd14-109">Display name and index enumeration</span></span>                                                 | <span data-ttu-id="6fd14-110">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="6fd14-110">Type and default value</span></span>                                                             | <span data-ttu-id="6fd14-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fd14-111">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd14-112">Outputrect</span><span class="sxs-lookup"><span data-stu-id="6fd14-112">OutputRect</span></span><br/> <span data-ttu-id="6fd14-113">D2D1 \_ opacitymetadata \_ Prop \_ Input nicht transparent \_ \_ Rect</span><span class="sxs-lookup"><span data-stu-id="6fd14-113">D2D1\_OPACITYMETADATA\_PROP\_INPUT\_OPAQUE\_RECT</span></span> <br/> | <span data-ttu-id="6fd14-114">D2D1 \_ Vector \_ 4f</span><span class="sxs-lookup"><span data-stu-id="6fd14-114">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="6fd14-115">(-F \_ Max,-f Max, maximal zulässige Anzahl, maximal zulässige Größe \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="6fd14-115">(-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX)</span></span> <br/> | <span data-ttu-id="6fd14-116">Der Teil des Quell Bilds, der nicht transparent ist.</span><span class="sxs-lookup"><span data-stu-id="6fd14-116">The portion of the source image that is opaque.</span></span> <span data-ttu-id="6fd14-117">Der Standardwert ist das gesamte Eingabebild.</span><span class="sxs-lookup"><span data-stu-id="6fd14-117">The default is the entire input image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6fd14-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fd14-118">Requirements</span></span>



| <span data-ttu-id="6fd14-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fd14-119">Requirement</span></span> | <span data-ttu-id="6fd14-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6fd14-120">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd14-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6fd14-121">Minimum supported client</span></span> | <span data-ttu-id="6fd14-122">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fd14-122">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6fd14-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6fd14-123">Minimum supported server</span></span> | <span data-ttu-id="6fd14-124">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fd14-124">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6fd14-125">Header</span><span class="sxs-lookup"><span data-stu-id="6fd14-125">Header</span></span>                   | <span data-ttu-id="6fd14-126">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="6fd14-126">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="6fd14-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6fd14-127">Library</span></span>                  | <span data-ttu-id="6fd14-128">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="6fd14-128">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="6fd14-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6fd14-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fd14-130">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="6fd14-130">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

