---
description: Die fotometadatenrichtlinie für die System. GPS. processingmethod-Eigenschaft.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: System. GPS. processingmethod-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bf1484eb8e8a53c65a9cd43c54b076e418d4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359582"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a><span data-ttu-id="5ed5e-103">System. GPS. processingmethod-fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="5ed5e-103">System.GPS.ProcessingMethod Photo Metadata Policy</span></span>

<span data-ttu-id="5ed5e-104">Die fotometadatenrichtlinie für die [System. GPS. processingmethod](../properties/props-system-gps-processingmethod.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5ed5e-104">The photo metadata policy for the [System.GPS.ProcessingMethod](../properties/props-system-gps-processingmethod.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5ed5e-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="5ed5e-105">PKEY</span></span>

<span data-ttu-id="5ed5e-106">Pkey \_ GPS \_ processingmethod</span><span class="sxs-lookup"><span data-stu-id="5ed5e-106">PKEY\_GPS\_ProcessingMethod</span></span>

### <a name="containers"></a><span data-ttu-id="5ed5e-107">Container</span><span class="sxs-lookup"><span data-stu-id="5ed5e-107">Containers</span></span>

<span data-ttu-id="5ed5e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5ed5e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5ed5e-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5ed5e-109">Read-Only</span></span>

<span data-ttu-id="5ed5e-110">Nein</span><span class="sxs-lookup"><span data-stu-id="5ed5e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5ed5e-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="5ed5e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5ed5e-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5ed5e-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="5ed5e-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="5ed5e-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="5ed5e-114">VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird ebenfalls akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="5ed5e-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5ed5e-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="5ed5e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="5ed5e-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="5ed5e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="5ed5e-117">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="5ed5e-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5ed5e-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="5ed5e-118">Read Paths</span></span>



| <span data-ttu-id="5ed5e-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="5ed5e-119">Order</span></span> | <span data-ttu-id="5ed5e-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="5ed5e-120">Path</span></span>                          | <span data-ttu-id="5ed5e-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="5ed5e-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="5ed5e-122">1</span><span class="sxs-lookup"><span data-stu-id="5ed5e-122">1</span></span>     | <span data-ttu-id="5ed5e-123">/App1/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="5ed5e-123">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="5ed5e-124">2</span><span class="sxs-lookup"><span data-stu-id="5ed5e-124">2</span></span>     | <span data-ttu-id="5ed5e-125">/XMP/EXIF: gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="5ed5e-125">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="5ed5e-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="5ed5e-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="5ed5e-127">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="5ed5e-127">Write Paths</span></span>



| <span data-ttu-id="5ed5e-128">Auftrag</span><span class="sxs-lookup"><span data-stu-id="5ed5e-128">Order</span></span> | <span data-ttu-id="5ed5e-129">Pfad</span><span class="sxs-lookup"><span data-stu-id="5ed5e-129">Path</span></span>                          | <span data-ttu-id="5ed5e-130">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="5ed5e-130">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="5ed5e-131">1</span><span class="sxs-lookup"><span data-stu-id="5ed5e-131">1</span></span>     | <span data-ttu-id="5ed5e-132">/App1/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="5ed5e-132">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="5ed5e-133">2</span><span class="sxs-lookup"><span data-stu-id="5ed5e-133">2</span></span>     | <span data-ttu-id="5ed5e-134">/XMP/EXIF: gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="5ed5e-134">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="5ed5e-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="5ed5e-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="5ed5e-136">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="5ed5e-136">Remove Paths</span></span>



| <span data-ttu-id="5ed5e-137">Auftrag</span><span class="sxs-lookup"><span data-stu-id="5ed5e-137">Order</span></span> | <span data-ttu-id="5ed5e-138">Pfad</span><span class="sxs-lookup"><span data-stu-id="5ed5e-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="5ed5e-139">1</span><span class="sxs-lookup"><span data-stu-id="5ed5e-139">1</span></span>     | <span data-ttu-id="5ed5e-140">/App1/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="5ed5e-140">/app1/ifd/gps/{ushort=27}</span></span>     |
| <span data-ttu-id="5ed5e-141">2</span><span class="sxs-lookup"><span data-stu-id="5ed5e-141">2</span></span>     | <span data-ttu-id="5ed5e-142">/XMP/EXIF: gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="5ed5e-142">/xmp/exif:gpsprocessingmethod</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="5ed5e-143">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="5ed5e-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5ed5e-144">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="5ed5e-144">Read Paths</span></span>



| <span data-ttu-id="5ed5e-145">Auftrag</span><span class="sxs-lookup"><span data-stu-id="5ed5e-145">Order</span></span> | <span data-ttu-id="5ed5e-146">Pfad</span><span class="sxs-lookup"><span data-stu-id="5ed5e-146">Path</span></span>                              | <span data-ttu-id="5ed5e-147">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="5ed5e-147">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="5ed5e-148">1</span><span class="sxs-lookup"><span data-stu-id="5ed5e-148">1</span></span>     | <span data-ttu-id="5ed5e-149">/IFD/XMP/EXIF: gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="5ed5e-149">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="5ed5e-150">Unicode</span><span class="sxs-lookup"><span data-stu-id="5ed5e-150">unicode</span></span>     |
| <span data-ttu-id="5ed5e-151">2</span><span class="sxs-lookup"><span data-stu-id="5ed5e-151">2</span></span>     | <span data-ttu-id="5ed5e-152">/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="5ed5e-152">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="write-paths"></a><span data-ttu-id="5ed5e-153">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="5ed5e-153">Write Paths</span></span>



| <span data-ttu-id="5ed5e-154">Auftrag</span><span class="sxs-lookup"><span data-stu-id="5ed5e-154">Order</span></span> | <span data-ttu-id="5ed5e-155">Pfad</span><span class="sxs-lookup"><span data-stu-id="5ed5e-155">Path</span></span>                              | <span data-ttu-id="5ed5e-156">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="5ed5e-156">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="5ed5e-157">1</span><span class="sxs-lookup"><span data-stu-id="5ed5e-157">1</span></span>     | <span data-ttu-id="5ed5e-158">/IFD/XMP/EXIF: gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="5ed5e-158">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="5ed5e-159">Unicode</span><span class="sxs-lookup"><span data-stu-id="5ed5e-159">unicode</span></span>     |
| <span data-ttu-id="5ed5e-160">2</span><span class="sxs-lookup"><span data-stu-id="5ed5e-160">2</span></span>     | <span data-ttu-id="5ed5e-161">/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="5ed5e-161">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="remove-paths"></a><span data-ttu-id="5ed5e-162">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="5ed5e-162">Remove Paths</span></span>



| <span data-ttu-id="5ed5e-163">Auftrag</span><span class="sxs-lookup"><span data-stu-id="5ed5e-163">Order</span></span> | <span data-ttu-id="5ed5e-164">Pfad</span><span class="sxs-lookup"><span data-stu-id="5ed5e-164">Path</span></span>                              |
|-------|-----------------------------------|
| <span data-ttu-id="5ed5e-165">1</span><span class="sxs-lookup"><span data-stu-id="5ed5e-165">1</span></span>     | <span data-ttu-id="5ed5e-166">/IFD/XMP/EXIF: gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="5ed5e-166">/ifd/xmp/exif:gpsprocessingmethod</span></span> |
| <span data-ttu-id="5ed5e-167">2</span><span class="sxs-lookup"><span data-stu-id="5ed5e-167">2</span></span>     | <span data-ttu-id="5ed5e-168">/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="5ed5e-168">/ifd/gps/{ushort=27}</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="5ed5e-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ed5e-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ed5e-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5ed5e-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ed5e-171">System. GPS. processingmethod</span><span class="sxs-lookup"><span data-stu-id="5ed5e-171">System.GPS.ProcessingMethod</span></span>](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
