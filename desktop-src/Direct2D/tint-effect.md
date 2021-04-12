---
title: Tint-Effekt
description: Dieser Effekt zeigt das Quell Bild, indem das Quell Bild mit der angegebenen Farbe multipliziert wird. Sie verfügt über eine einzelne Eingabe.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f12e7593f9cb0695a6adb7b955fb66b13c8d00b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949807"
---
# <a name="tint-effect"></a><span data-ttu-id="4c8ba-104">Tint-Effekt</span><span class="sxs-lookup"><span data-stu-id="4c8ba-104">Tint effect</span></span>

<span data-ttu-id="4c8ba-105">Dieser Effekt zeigt das Quell Bild, indem das Quell Bild mit der angegebenen Farbe multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="4c8ba-105">This effect tints the source image by multiplying the source image by the specified color.</span></span> <span data-ttu-id="4c8ba-106">Sie verfügt über eine einzelne Eingabe.</span><span class="sxs-lookup"><span data-stu-id="4c8ba-106">It has a single input.</span></span>

<span data-ttu-id="4c8ba-107">Die CLSID für diesen Effekt ist CLSID \_ D2D1Tint.</span><span class="sxs-lookup"><span data-stu-id="4c8ba-107">The CLSID for this effect is CLSID\_D2D1Tint.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="4c8ba-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4c8ba-108">Effect properties</span></span>



| <span data-ttu-id="4c8ba-109">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="4c8ba-109">Display name and index enumeration</span></span>                    | <span data-ttu-id="4c8ba-110">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="4c8ba-110">Type and default value</span></span>                              | <span data-ttu-id="4c8ba-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c8ba-111">Description</span></span>                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="4c8ba-112">ColorD2D1 \_ tint- \_ Prop- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="4c8ba-112">ColorD2D1\_TINT\_PROP\_COLOR</span></span><br/>               | <span data-ttu-id="4c8ba-113">D2D1 \_ Vector \_ 4f (1.0 f, 1.0 f, 1.0 f, 1.0 f)</span><span class="sxs-lookup"><span data-stu-id="4c8ba-113">D2D1\_VECTOR\_4F(1.0f, 1.0f, 1.0f, 1.0f)</span></span><br/> | <span data-ttu-id="4c8ba-114">Farben aus dem Quell Bild werden mit diesem Wert multipliziert.</span><span class="sxs-lookup"><span data-stu-id="4c8ba-114">Colors from the source image are multiplied by this value.</span></span>       |
| <span data-ttu-id="4c8ba-115">ClampOutputD2D1 \_ tint- \_ Prop- \_ \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="4c8ba-115">ClampOutputD2D1\_TINT\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="4c8ba-116">Boolfalse</span><span class="sxs-lookup"><span data-stu-id="4c8ba-116">BOOLFALSE</span></span><br/>                                | <span data-ttu-id="4c8ba-117">Gibt an, ob die Ausgabewerte mit dem Bereich \[ 0, 1, fixiert werden \] .</span><span class="sxs-lookup"><span data-stu-id="4c8ba-117">Whether or not to clamp the output values to the range \[0, 1\].</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="4c8ba-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c8ba-118">Requirements</span></span>



| <span data-ttu-id="4c8ba-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c8ba-119">Requirement</span></span> | <span data-ttu-id="4c8ba-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4c8ba-120">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="4c8ba-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c8ba-121">Minimum supported client</span></span> | <span data-ttu-id="4c8ba-122">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c8ba-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4c8ba-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c8ba-123">Minimum supported server</span></span> | <span data-ttu-id="4c8ba-124">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c8ba-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4c8ba-125">Header</span><span class="sxs-lookup"><span data-stu-id="4c8ba-125">Header</span></span>                   | <span data-ttu-id="4c8ba-126">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="4c8ba-126">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="4c8ba-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4c8ba-127">Library</span></span>                  | <span data-ttu-id="4c8ba-128">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="4c8ba-128">d2d1.lib, dxguid.lib</span></span>                              |



 ## <a name="related-topics"></a><span data-ttu-id="4c8ba-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4c8ba-129">Related topics</span></span>

* [<span data-ttu-id="4c8ba-130">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4c8ba-130">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
