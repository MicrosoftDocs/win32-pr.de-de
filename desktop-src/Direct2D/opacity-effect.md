---
title: Deckkraft Effekt
description: Dadurch wird die Deckkraft eines Bilds angepasst, indem der Alphakanal der Eingabe mit dem angegebenen Deckkraft Wert multipliziert wird. Sie verfügt über eine einzelne Eingabe.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc12aa8545f2742561490a3ddce799d6a1aa62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341404"
---
# <a name="opacity-effect"></a><span data-ttu-id="b0467-104">Deckkraft Effekt</span><span class="sxs-lookup"><span data-stu-id="b0467-104">Opacity effect</span></span>

<span data-ttu-id="b0467-105">Dadurch wird die Deckkraft eines Bilds angepasst, indem der Alphakanal der Eingabe mit dem angegebenen Deckkraft Wert multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="b0467-105">This effect adjusts the opacity of an image by multiplying the alpha channel of the input by the specified opacity value.</span></span> <span data-ttu-id="b0467-106">Sie verfügt über eine einzelne Eingabe.</span><span class="sxs-lookup"><span data-stu-id="b0467-106">It has a single input.</span></span>

<span data-ttu-id="b0467-107">Die CLSID für diesen Effekt ist CLSID \_ D2D1Opacity.</span><span class="sxs-lookup"><span data-stu-id="b0467-107">The CLSID for this effect is CLSID\_D2D1Opacity.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="b0467-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b0467-108">Effect properties</span></span>



| <span data-ttu-id="b0467-109">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="b0467-109">Display name and index enumeration</span></span>              | <span data-ttu-id="b0467-110">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="b0467-110">Type and default value</span></span> | <span data-ttu-id="b0467-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0467-111">Description</span></span>                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0467-112">Deckkraft D2D1 \_ Deckkraft \_ \_</span><span class="sxs-lookup"><span data-stu-id="b0467-112">Opacity D2D1\_OPACITY\_PROP\_OPACITY</span></span><br/> | <span data-ttu-id="b0467-113">Float 1.0 f</span><span class="sxs-lookup"><span data-stu-id="b0467-113">FLOAT1.0f</span></span><br/>   | <span data-ttu-id="b0467-114">Der Multiplikator des Alphakanals des Eingabe Bilds.</span><span class="sxs-lookup"><span data-stu-id="b0467-114">The multiplier to the input image's alpha channel.</span></span> <span data-ttu-id="b0467-115">Der Minimalwert ist 0,0 f, und der Höchstwert ist 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="b0467-115">The minimum value is 0.0f and the maximum value is 1.0f.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b0467-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0467-116">Requirements</span></span>



| <span data-ttu-id="b0467-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0467-117">Requirement</span></span> | <span data-ttu-id="b0467-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b0467-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="b0467-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0467-119">Minimum supported client</span></span> | <span data-ttu-id="b0467-120">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0467-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b0467-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0467-121">Minimum supported server</span></span> | <span data-ttu-id="b0467-122">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0467-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b0467-123">Header</span><span class="sxs-lookup"><span data-stu-id="b0467-123">Header</span></span>                   | <span data-ttu-id="b0467-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="b0467-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="b0467-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b0467-125">Library</span></span>                  | <span data-ttu-id="b0467-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b0467-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="b0467-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0467-127">Related topics</span></span>

* [<span data-ttu-id="b0467-128">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b0467-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
