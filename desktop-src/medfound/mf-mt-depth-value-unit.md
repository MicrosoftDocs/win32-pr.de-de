---
description: Ein-Wert, der die Einheiten für einen tiefen Wert in einem Videoframe definiert.
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: MF_MT_DEPTH_VALUE_UNIT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f6086a34f62c26b3fe1fa611318792c9056a50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356602"
---
# <a name="mf_mt_depth_value_unit-attribute"></a><span data-ttu-id="c090c-103">Einheiten Attribut des MF- \_ MT- \_ tiefen \_ Werts \_</span><span class="sxs-lookup"><span data-stu-id="c090c-103">MF\_MT\_DEPTH\_VALUE\_UNIT attribute</span></span>

<span data-ttu-id="c090c-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="c090c-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c090c-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="c090c-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c090c-106">Ein-Wert, der die Einheiten für einen tiefen Wert in einem Videoframe definiert.</span><span class="sxs-lookup"><span data-stu-id="c090c-106">A value that defines the units for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="c090c-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c090c-107">Data type</span></span>

<span data-ttu-id="c090c-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="c090c-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="c090c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c090c-109">Remarks</span></span>

<span data-ttu-id="c090c-110">Der Einheits Wert ist ein UINT64-Wert in Nanometer im Bereich von 1E-9-Meter.</span><span class="sxs-lookup"><span data-stu-id="c090c-110">The unit value is a UINT64 value in nanometers, in the range 1e - 9 meters.</span></span> <span data-ttu-id="c090c-111">Wenn dieser Wert nicht vorhanden ist, ist der Standardwert der Einheit 1E-3, was bedeutet, dass jede Pixelebene in einem physischen Raum in 1 Millimeter gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="c090c-111">If this value is not present, the default value of the unit is 1e-3, which indicates each pixel level is measured in 1 millimeter in physical space.</span></span>

<span data-ttu-id="c090c-112">Tiefen Kameras können die Tiefe aller Pixel nicht verstehen.</span><span class="sxs-lookup"><span data-stu-id="c090c-112">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="c090c-113">Wenn die Zuverlässigkeit eines Pixels aufgrund von Material, Okklusion, außerhalb des gültigen Bereichs usw. gering ist, kann der tiefen Wert dieses Pixels ungültig sein.</span><span class="sxs-lookup"><span data-stu-id="c090c-113">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="c090c-114">Wenn ein tiefen Pixel Wert 0 ist, ist das Pixel ungültig.</span><span class="sxs-lookup"><span data-stu-id="c090c-114">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="c090c-115">Bei einigen tiefen Kameras werden Bitmasken Metadaten für jedes Pixel zusätzlich zum tiefen Wert anfügen, um den Grund für die Ungültigkeit der Pixel Tiefe aufgrund von Material, Okklusion oder außerhalb des gültigen Bereichs usw. darzustellen. Es wird empfohlen, solche Metadaten nicht als Bits im tiefen Wert anzufügen, da dies in der Regel zu Schwierigkeiten führt, wenn Sie solche Werte in Pixel-Shader verwenden.</span><span class="sxs-lookup"><span data-stu-id="c090c-115">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="c090c-116">Stattdessen.</span><span class="sxs-lookup"><span data-stu-id="c090c-116">Instead.</span></span> <span data-ttu-id="c090c-117">Es wird empfohlen, dass Sie einen separaten 8-Bit-Image Puffer mit derselben Auflösung verwenden und ihn als Attribut von [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)anfügen.</span><span class="sxs-lookup"><span data-stu-id="c090c-117">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="c090c-118">Diese Metadaten sind für jeden Hersteller der Kamera unterschiedlich und werden nicht von der Plattform standardisiert.</span><span class="sxs-lookup"><span data-stu-id="c090c-118">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="c090c-119">Wir empfehlen die Verwendung von vollständigen 16 Bits für den Tiefen Wert zur einfacheren Verarbeitung von downstreamvorgängen und die Verwendung eines Fixed-Werts wie 0 für die Invalidierung.</span><span class="sxs-lookup"><span data-stu-id="c090c-119">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c090c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c090c-120">Requirements</span></span>



| <span data-ttu-id="c090c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c090c-121">Requirement</span></span> | <span data-ttu-id="c090c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c090c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c090c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c090c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c090c-124">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c090c-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c090c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c090c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c090c-126">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c090c-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="c090c-127">Header</span><span class="sxs-lookup"><span data-stu-id="c090c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c090c-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c090c-128"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




