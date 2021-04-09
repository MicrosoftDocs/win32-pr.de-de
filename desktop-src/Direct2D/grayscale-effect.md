---
title: Graustufen Effekt
description: Konvertiert ein Bild in ein monochromes Graustufenbild.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc3cb6a807d282649a2826713cdf48fa966d9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741969"
---
# <a name="grayscale-effect"></a><span data-ttu-id="34006-103">Graustufen Effekt</span><span class="sxs-lookup"><span data-stu-id="34006-103">Grayscale effect</span></span>

<span data-ttu-id="34006-104">Konvertiert ein Bild in ein monochromes Graustufenbild.</span><span class="sxs-lookup"><span data-stu-id="34006-104">Converts an image to monochromatic gray.</span></span>

<span data-ttu-id="34006-105">Grayscale verwendet den Farbmatrix Effekt für die Konvertierung in Graustufen mithilfe der folgenden Matrix:</span><span class="sxs-lookup"><span data-stu-id="34006-105">Grayscale uses the color matrix effect to convert to grayscale, using the following matrix:</span></span>

![Konvertierungs Matrix](images/grayscale-effect-matrix.png)

<span data-ttu-id="34006-107">Die CLSID für diesen Effekt ist CLSID \_ D2D1Grayscale.</span><span class="sxs-lookup"><span data-stu-id="34006-107">The CLSID for this effect is CLSID\_D2D1Grayscale.</span></span>

-   [<span data-ttu-id="34006-108">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="34006-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="34006-109">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34006-109">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="34006-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34006-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="34006-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34006-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="34006-112">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="34006-112">Example image</span></span>

![Beispiel für Effekte Ausgabe](images/grayscale-effect.png)

## <a name="effect-properties"></a><span data-ttu-id="34006-114">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34006-114">Effect properties</span></span>

<span data-ttu-id="34006-115">Dieser Effekt hat keine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="34006-115">This effect has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="34006-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34006-116">Requirements</span></span>



| <span data-ttu-id="34006-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34006-117">Requirement</span></span> | <span data-ttu-id="34006-118">Wert</span><span class="sxs-lookup"><span data-stu-id="34006-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="34006-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34006-119">Minimum supported client</span></span> | <span data-ttu-id="34006-120">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34006-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="34006-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34006-121">Minimum supported server</span></span> | <span data-ttu-id="34006-122">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34006-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="34006-123">Header</span><span class="sxs-lookup"><span data-stu-id="34006-123">Header</span></span>                   | <span data-ttu-id="34006-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="34006-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="34006-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34006-125">Library</span></span>                  | <span data-ttu-id="34006-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="34006-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="34006-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34006-127">Related topics</span></span>

* [<span data-ttu-id="34006-128">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="34006-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
