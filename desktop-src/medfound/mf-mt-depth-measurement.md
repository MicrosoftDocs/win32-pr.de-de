---
description: Ein-Wert, der das Messsystem für einen tiefen Wert in einem Videoframe definiert.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: MF_MT_DEPTH_MEASUREMENT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8be6c06ea09f4017ae65935081eaa81d1ad00cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567857"
---
# <a name="mf_mt_depth_measurement-attribute"></a><span data-ttu-id="cbc1d-103">MF \_ - \_ Attribut "Tiefe \_ Messung"</span><span class="sxs-lookup"><span data-stu-id="cbc1d-103">MF\_MT\_DEPTH\_MEASUREMENT attribute</span></span>

<span data-ttu-id="cbc1d-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cbc1d-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="cbc1d-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cbc1d-106">Ein-Wert, der das Messsystem für einen tiefen Wert in einem Videoframe definiert.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-106">A value that defines the measurement system for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="cbc1d-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cbc1d-107">Data type</span></span>

<span data-ttu-id="cbc1d-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cbc1d-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cbc1d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbc1d-109">Remarks</span></span>

<span data-ttu-id="cbc1d-110">Dieser Wert ist ein Member der [**\_ mfdepthmeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-110">This value is a member of the [**\_MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement) enumeration</span></span>

<span data-ttu-id="cbc1d-111">Wenn dieses Attribut nicht vorhanden ist, wird davon ausgegangen, dass es sich um **distanceyfocalplane** handelt.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-111">If this attribute is not present it is assumed to be **DistanceToFocalPlane**.</span></span> <span data-ttu-id="cbc1d-112">Die Entfernung zur Fokusebene ist in der Regel einfacher in einem 3D-euklidischen Koordinatensystem zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-112">The distance to focal plane is typically easier to consume in a 3D Euclidian coordinate system.</span></span>

![Abbildung von distancedefocalplane](images/distance-to-focal-plane.png)

<span data-ttu-id="cbc1d-114">Der Abstand zum Fokus Center-Format ist in der Regel Rohdaten des Sensors, wie z. b. Zeit von Flug Kameras.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-114">The distance to focal center format is typically raw data from sensor such as time of flight cameras.</span></span>

![Abbildung von distancegeopticalcenter](images/distance-to-optical-center.png)

<span data-ttu-id="cbc1d-116">Tiefen Kameras können die Tiefe aller Pixel nicht verstehen.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-116">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="cbc1d-117">Wenn die Zuverlässigkeit eines Pixels aufgrund von Material, Okklusion, außerhalb des gültigen Bereichs usw. gering ist, kann der tiefen Wert dieses Pixels ungültig sein.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-117">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="cbc1d-118">Wenn ein tiefen Pixel Wert 0 ist, ist das Pixel ungültig.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-118">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="cbc1d-119">Bei einigen tiefen Kameras werden Bitmasken Metadaten für jedes Pixel zusätzlich zum tiefen Wert anfügen, um den Grund für die Ungültigkeit der Pixel Tiefe aufgrund von Material, Okklusion oder außerhalb des gültigen Bereichs usw. darzustellen. Es wird empfohlen, solche Metadaten nicht als Bits im tiefen Wert anzufügen, da dies in der Regel zu Schwierigkeiten führt, wenn Sie solche Werte in Pixel-Shader verwenden.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-119">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="cbc1d-120">Stattdessen.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-120">Instead.</span></span> <span data-ttu-id="cbc1d-121">Es wird empfohlen, dass Sie einen separaten 8-Bit-Image Puffer mit derselben Auflösung verwenden und ihn als Attribut von [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)anfügen.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-121">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="cbc1d-122">Diese Metadaten sind für jeden Hersteller der Kamera unterschiedlich und werden nicht von der Plattform standardisiert.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-122">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="cbc1d-123">Wir empfehlen die Verwendung von vollständigen 16 Bits für den Tiefen Wert zur einfacheren Verarbeitung von downstreamvorgängen und die Verwendung eines Fixed-Werts wie 0 für die Invalidierung.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-123">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc1d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbc1d-124">Requirements</span></span>



| <span data-ttu-id="cbc1d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbc1d-125">Requirement</span></span> | <span data-ttu-id="cbc1d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="cbc1d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc1d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbc1d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cbc1d-128">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbc1d-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cbc1d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbc1d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cbc1d-130">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbc1d-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="cbc1d-131">Header</span><span class="sxs-lookup"><span data-stu-id="cbc1d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbc1d-132"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbc1d-132"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




