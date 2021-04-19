---
description: Die fotometadatenrichtlinie für die System. GPS. destdistanceref-Eigenschaft.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: System. GPS. destdistanceref-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349665"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a><span data-ttu-id="c8c99-103">System. GPS. destdistanceref-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="c8c99-103">System.GPS.DestDistanceRef Photo Metadata Policy</span></span>

<span data-ttu-id="c8c99-104">Die fotometadatenrichtlinie für die [System. GPS. destdistanceref](../properties/props-system-gps-destdistanceref.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c8c99-104">The photo metadata policy for the [System.GPS.DestDistanceRef](../properties/props-system-gps-destdistanceref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c8c99-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="c8c99-105">PKEY</span></span>

<span data-ttu-id="c8c99-106">Pkey \_ destdistanceref</span><span class="sxs-lookup"><span data-stu-id="c8c99-106">PKEY\_DestDistanceRef</span></span>

### <a name="containers"></a><span data-ttu-id="c8c99-107">Container</span><span class="sxs-lookup"><span data-stu-id="c8c99-107">Containers</span></span>

<span data-ttu-id="c8c99-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c8c99-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c8c99-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8c99-109">Read-Only</span></span>

<span data-ttu-id="c8c99-110">Nein</span><span class="sxs-lookup"><span data-stu-id="c8c99-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c8c99-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="c8c99-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c8c99-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="c8c99-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="c8c99-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="c8c99-113">Input Type</span></span>

<span data-ttu-id="c8c99-114">VT \_ LPWSTR oder VT \_ LPSTR wird akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c8c99-114">VT\_LPWSTR or VT\_LPSTR are accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c8c99-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="c8c99-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c8c99-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="c8c99-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="c8c99-117">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="c8c99-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c8c99-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="c8c99-118">Read Paths</span></span>



| <span data-ttu-id="c8c99-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c8c99-119">Order</span></span> | <span data-ttu-id="c8c99-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="c8c99-120">Path</span></span>                         | <span data-ttu-id="c8c99-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="c8c99-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="c8c99-122">1</span><span class="sxs-lookup"><span data-stu-id="c8c99-122">1</span></span>     | <span data-ttu-id="c8c99-123">/App1/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="c8c99-123">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="c8c99-124">ascii</span><span class="sxs-lookup"><span data-stu-id="c8c99-124">ascii</span></span>       |
| <span data-ttu-id="c8c99-125">2</span><span class="sxs-lookup"><span data-stu-id="c8c99-125">2</span></span>     | <span data-ttu-id="c8c99-126">/XMP/EXIF: gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="c8c99-126">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="c8c99-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="c8c99-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c8c99-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="c8c99-128">Write Paths</span></span>



| <span data-ttu-id="c8c99-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c8c99-129">Order</span></span> | <span data-ttu-id="c8c99-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="c8c99-130">Path</span></span>                         | <span data-ttu-id="c8c99-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="c8c99-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="c8c99-132">1</span><span class="sxs-lookup"><span data-stu-id="c8c99-132">1</span></span>     | <span data-ttu-id="c8c99-133">/App1/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="c8c99-133">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="c8c99-134">ascii</span><span class="sxs-lookup"><span data-stu-id="c8c99-134">ascii</span></span>       |
| <span data-ttu-id="c8c99-135">2</span><span class="sxs-lookup"><span data-stu-id="c8c99-135">2</span></span>     | <span data-ttu-id="c8c99-136">/XMP/EXIF: gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="c8c99-136">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="c8c99-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="c8c99-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c8c99-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="c8c99-138">Remove Paths</span></span>



| <span data-ttu-id="c8c99-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c8c99-139">Order</span></span> | <span data-ttu-id="c8c99-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="c8c99-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="c8c99-141">1</span><span class="sxs-lookup"><span data-stu-id="c8c99-141">1</span></span>     | <span data-ttu-id="c8c99-142">/App1/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="c8c99-142">/app1/ifd/gps/{ushort=25}</span></span>    |
| <span data-ttu-id="c8c99-143">2</span><span class="sxs-lookup"><span data-stu-id="c8c99-143">2</span></span>     | <span data-ttu-id="c8c99-144">/XMP/EXIF: gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="c8c99-144">/xmp/exif:gpsdestdistanceref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="c8c99-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="c8c99-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c8c99-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="c8c99-146">Read Paths</span></span>



| <span data-ttu-id="c8c99-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c8c99-147">Order</span></span> | <span data-ttu-id="c8c99-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="c8c99-148">Path</span></span>                             | <span data-ttu-id="c8c99-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="c8c99-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="c8c99-150">1</span><span class="sxs-lookup"><span data-stu-id="c8c99-150">1</span></span>     | <span data-ttu-id="c8c99-151">/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="c8c99-151">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="c8c99-152">ascii</span><span class="sxs-lookup"><span data-stu-id="c8c99-152">ascii</span></span>       |
| <span data-ttu-id="c8c99-153">2</span><span class="sxs-lookup"><span data-stu-id="c8c99-153">2</span></span>     | <span data-ttu-id="c8c99-154">/IFD/XMP/EXIF: gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="c8c99-154">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="c8c99-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="c8c99-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c8c99-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="c8c99-156">Write Paths</span></span>



| <span data-ttu-id="c8c99-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c8c99-157">Order</span></span> | <span data-ttu-id="c8c99-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="c8c99-158">Path</span></span>                             | <span data-ttu-id="c8c99-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="c8c99-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="c8c99-160">1</span><span class="sxs-lookup"><span data-stu-id="c8c99-160">1</span></span>     | <span data-ttu-id="c8c99-161">/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="c8c99-161">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="c8c99-162">ascii</span><span class="sxs-lookup"><span data-stu-id="c8c99-162">ascii</span></span>       |
| <span data-ttu-id="c8c99-163">2</span><span class="sxs-lookup"><span data-stu-id="c8c99-163">2</span></span>     | <span data-ttu-id="c8c99-164">/IFD/XMP/EXIF: gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="c8c99-164">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="c8c99-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="c8c99-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c8c99-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="c8c99-166">Remove Paths</span></span>



| <span data-ttu-id="c8c99-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c8c99-167">Order</span></span> | <span data-ttu-id="c8c99-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="c8c99-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="c8c99-169">1</span><span class="sxs-lookup"><span data-stu-id="c8c99-169">1</span></span>     | <span data-ttu-id="c8c99-170">/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="c8c99-170">/ifd/gps/{ushort=25}</span></span>             |
| <span data-ttu-id="c8c99-171">2</span><span class="sxs-lookup"><span data-stu-id="c8c99-171">2</span></span>     | <span data-ttu-id="c8c99-172">/IFD/XMP/EXIF: gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="c8c99-172">/ifd/xmp/exif:gpsdestdistanceref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c8c99-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8c99-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8c99-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c8c99-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8c99-175">System. GPS. destdistanceref</span><span class="sxs-lookup"><span data-stu-id="c8c99-175">System.GPS.DestDistanceRef</span></span>](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
