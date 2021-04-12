---
description: Die fotometadatenrichtlinie für die System. GPS. imgdirectionref-Eigenschaft.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: System. GPS. imgdirectionref-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80276ca8d1981935004dbec49fef588fcde330ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218031"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a><span data-ttu-id="0a86e-103">System. GPS. imgdirectionref-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="0a86e-103">System.GPS.ImgDirectionRef Photo Metadata Policy</span></span>

<span data-ttu-id="0a86e-104">Die fotometadatenrichtlinie für die [System. GPS. imgdirectionref](../properties/props-system-gps-imgdirectionref.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0a86e-104">The photo metadata policy for the [System.GPS.ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0a86e-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="0a86e-105">PKEY</span></span>

<span data-ttu-id="0a86e-106">pkey \_ GPS. Imgdirectionref</span><span class="sxs-lookup"><span data-stu-id="0a86e-106">PKEY\_GPS.ImgDirectionRef</span></span>

### <a name="containers"></a><span data-ttu-id="0a86e-107">Container</span><span class="sxs-lookup"><span data-stu-id="0a86e-107">Containers</span></span>

<span data-ttu-id="0a86e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="0a86e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0a86e-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a86e-109">Read-Only</span></span>

<span data-ttu-id="0a86e-110">Nein</span><span class="sxs-lookup"><span data-stu-id="0a86e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="0a86e-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="0a86e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="0a86e-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="0a86e-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="0a86e-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="0a86e-113">Input Type</span></span>

<span data-ttu-id="0a86e-114">VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird ebenfalls akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="0a86e-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0a86e-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="0a86e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="0a86e-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="0a86e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="0a86e-117">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="0a86e-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0a86e-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="0a86e-118">Read Paths</span></span>



| <span data-ttu-id="0a86e-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0a86e-119">Order</span></span> | <span data-ttu-id="0a86e-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="0a86e-120">Path</span></span>                         | <span data-ttu-id="0a86e-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="0a86e-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="0a86e-122">1</span><span class="sxs-lookup"><span data-stu-id="0a86e-122">1</span></span>     | <span data-ttu-id="0a86e-123">/App1/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="0a86e-123">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="0a86e-124">ascii</span><span class="sxs-lookup"><span data-stu-id="0a86e-124">ascii</span></span>       |
| <span data-ttu-id="0a86e-125">2</span><span class="sxs-lookup"><span data-stu-id="0a86e-125">2</span></span>     | <span data-ttu-id="0a86e-126">/XMP/EXIF: gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="0a86e-126">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="0a86e-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="0a86e-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0a86e-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="0a86e-128">Write Paths</span></span>



| <span data-ttu-id="0a86e-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0a86e-129">Order</span></span> | <span data-ttu-id="0a86e-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="0a86e-130">Path</span></span>                         | <span data-ttu-id="0a86e-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="0a86e-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="0a86e-132">1</span><span class="sxs-lookup"><span data-stu-id="0a86e-132">1</span></span>     | <span data-ttu-id="0a86e-133">/App1/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="0a86e-133">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="0a86e-134">ascii</span><span class="sxs-lookup"><span data-stu-id="0a86e-134">ascii</span></span>       |
| <span data-ttu-id="0a86e-135">2</span><span class="sxs-lookup"><span data-stu-id="0a86e-135">2</span></span>     | <span data-ttu-id="0a86e-136">/XMP/EXIF: gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="0a86e-136">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="0a86e-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="0a86e-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0a86e-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="0a86e-138">Remove Paths</span></span>



| <span data-ttu-id="0a86e-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0a86e-139">Order</span></span> | <span data-ttu-id="0a86e-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="0a86e-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="0a86e-141">1</span><span class="sxs-lookup"><span data-stu-id="0a86e-141">1</span></span>     | <span data-ttu-id="0a86e-142">/App1/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="0a86e-142">/app1/ifd/gps/{ushort=16}</span></span>    |
| <span data-ttu-id="0a86e-143">2</span><span class="sxs-lookup"><span data-stu-id="0a86e-143">2</span></span>     | <span data-ttu-id="0a86e-144">/XMP/EXIF: gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="0a86e-144">/xmp/exif:gpsimgdirectionref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="0a86e-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="0a86e-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0a86e-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="0a86e-146">Read Paths</span></span>



| <span data-ttu-id="0a86e-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0a86e-147">Order</span></span> | <span data-ttu-id="0a86e-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="0a86e-148">Path</span></span>                             | <span data-ttu-id="0a86e-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="0a86e-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="0a86e-150">1</span><span class="sxs-lookup"><span data-stu-id="0a86e-150">1</span></span>     | <span data-ttu-id="0a86e-151">/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="0a86e-151">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="0a86e-152">ascii</span><span class="sxs-lookup"><span data-stu-id="0a86e-152">ascii</span></span>       |
| <span data-ttu-id="0a86e-153">2</span><span class="sxs-lookup"><span data-stu-id="0a86e-153">2</span></span>     | <span data-ttu-id="0a86e-154">/IFD/XMP/EXIF: gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="0a86e-154">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="0a86e-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="0a86e-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0a86e-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="0a86e-156">Write Paths</span></span>



| <span data-ttu-id="0a86e-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0a86e-157">Order</span></span> | <span data-ttu-id="0a86e-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="0a86e-158">Path</span></span>                             | <span data-ttu-id="0a86e-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="0a86e-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="0a86e-160">1</span><span class="sxs-lookup"><span data-stu-id="0a86e-160">1</span></span>     | <span data-ttu-id="0a86e-161">/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="0a86e-161">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="0a86e-162">ascii</span><span class="sxs-lookup"><span data-stu-id="0a86e-162">ascii</span></span>       |
| <span data-ttu-id="0a86e-163">2</span><span class="sxs-lookup"><span data-stu-id="0a86e-163">2</span></span>     | <span data-ttu-id="0a86e-164">/IFD/XMP/EXIF: gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="0a86e-164">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="0a86e-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="0a86e-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0a86e-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="0a86e-166">Remove Paths</span></span>



| <span data-ttu-id="0a86e-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0a86e-167">Order</span></span> | <span data-ttu-id="0a86e-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="0a86e-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="0a86e-169">1</span><span class="sxs-lookup"><span data-stu-id="0a86e-169">1</span></span>     | <span data-ttu-id="0a86e-170">/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="0a86e-170">/ifd/gps/{ushort=16}</span></span>             |
| <span data-ttu-id="0a86e-171">2</span><span class="sxs-lookup"><span data-stu-id="0a86e-171">2</span></span>     | <span data-ttu-id="0a86e-172">/IFD/XMP/EXIF: gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="0a86e-172">/ifd/xmp/exif:gpsimgdirectionref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0a86e-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a86e-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a86e-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0a86e-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a86e-175">System. GPS. imgdirectionref</span><span class="sxs-lookup"><span data-stu-id="0a86e-175">System.GPS.ImgDirectionRef</span></span>](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
