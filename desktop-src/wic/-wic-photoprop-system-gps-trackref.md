---
description: Die fotometadatenrichtlinie für die System. GPS. trackref-Eigenschaft.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: System. GPS. trackref-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95fc63de6eaffd697798c08ff74a46c3d15c7818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218569"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a><span data-ttu-id="700fc-103">System. GPS. trackref-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="700fc-103">System.GPS.TrackRef Photo Metadata Policy</span></span>

<span data-ttu-id="700fc-104">Die fotometadatenrichtlinie für die [System. GPS. trackref](../properties/props-system-gps-trackref.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="700fc-104">The photo metadata policy for the [System.GPS.TrackRef](../properties/props-system-gps-trackref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="700fc-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="700fc-105">PKEY</span></span>

<span data-ttu-id="700fc-106">Pkey \_ GPS \_ trackref</span><span class="sxs-lookup"><span data-stu-id="700fc-106">PKEY\_GPS\_TrackRef</span></span>

### <a name="containers"></a><span data-ttu-id="700fc-107">Container</span><span class="sxs-lookup"><span data-stu-id="700fc-107">Containers</span></span>

<span data-ttu-id="700fc-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="700fc-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="700fc-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="700fc-109">Read-Only</span></span>

<span data-ttu-id="700fc-110">Nein</span><span class="sxs-lookup"><span data-stu-id="700fc-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="700fc-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="700fc-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="700fc-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="700fc-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="700fc-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="700fc-113">Input Type</span></span>

<span data-ttu-id="700fc-114">String</span><span class="sxs-lookup"><span data-stu-id="700fc-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="700fc-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="700fc-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="700fc-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="700fc-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="700fc-117">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="700fc-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="700fc-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="700fc-118">Read Paths</span></span>



| <span data-ttu-id="700fc-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="700fc-119">Order</span></span> | <span data-ttu-id="700fc-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="700fc-120">Path</span></span>                      | <span data-ttu-id="700fc-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="700fc-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="700fc-122">1</span><span class="sxs-lookup"><span data-stu-id="700fc-122">1</span></span>     | <span data-ttu-id="700fc-123">/App1/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="700fc-123">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="700fc-124">ascii</span><span class="sxs-lookup"><span data-stu-id="700fc-124">ascii</span></span>       |
| <span data-ttu-id="700fc-125">2</span><span class="sxs-lookup"><span data-stu-id="700fc-125">2</span></span>     | <span data-ttu-id="700fc-126">/XMP/EXIF: gpstrackref</span><span class="sxs-lookup"><span data-stu-id="700fc-126">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="700fc-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="700fc-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="700fc-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="700fc-128">Write Paths</span></span>



| <span data-ttu-id="700fc-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="700fc-129">Order</span></span> | <span data-ttu-id="700fc-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="700fc-130">Path</span></span>                      | <span data-ttu-id="700fc-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="700fc-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="700fc-132">1</span><span class="sxs-lookup"><span data-stu-id="700fc-132">1</span></span>     | <span data-ttu-id="700fc-133">/App1/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="700fc-133">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="700fc-134">ascii</span><span class="sxs-lookup"><span data-stu-id="700fc-134">ascii</span></span>       |
| <span data-ttu-id="700fc-135">2</span><span class="sxs-lookup"><span data-stu-id="700fc-135">2</span></span>     | <span data-ttu-id="700fc-136">/XMP/EXIF: gpstrackref</span><span class="sxs-lookup"><span data-stu-id="700fc-136">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="700fc-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="700fc-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="700fc-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="700fc-138">Remove Paths</span></span>



| <span data-ttu-id="700fc-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="700fc-139">Order</span></span> | <span data-ttu-id="700fc-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="700fc-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="700fc-141">1</span><span class="sxs-lookup"><span data-stu-id="700fc-141">1</span></span>     | <span data-ttu-id="700fc-142">/App1/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="700fc-142">/app1/ifd/gps/{ushort=14}</span></span> |
| <span data-ttu-id="700fc-143">2</span><span class="sxs-lookup"><span data-stu-id="700fc-143">2</span></span>     | <span data-ttu-id="700fc-144">/XMP/EXIF: gpstrackref</span><span class="sxs-lookup"><span data-stu-id="700fc-144">/xmp/exif:gpstrackref</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="700fc-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="700fc-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="700fc-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="700fc-146">Read Paths</span></span>



| <span data-ttu-id="700fc-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="700fc-147">Order</span></span> | <span data-ttu-id="700fc-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="700fc-148">Path</span></span>                      | <span data-ttu-id="700fc-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="700fc-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="700fc-150">1</span><span class="sxs-lookup"><span data-stu-id="700fc-150">1</span></span>     | <span data-ttu-id="700fc-151">/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="700fc-151">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="700fc-152">ascii</span><span class="sxs-lookup"><span data-stu-id="700fc-152">ascii</span></span>       |
| <span data-ttu-id="700fc-153">2</span><span class="sxs-lookup"><span data-stu-id="700fc-153">2</span></span>     | <span data-ttu-id="700fc-154">/IFD/XMP/EXIF: gpstrackref</span><span class="sxs-lookup"><span data-stu-id="700fc-154">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="700fc-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="700fc-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="700fc-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="700fc-156">Write Paths</span></span>



| <span data-ttu-id="700fc-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="700fc-157">Order</span></span> | <span data-ttu-id="700fc-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="700fc-158">Path</span></span>                      | <span data-ttu-id="700fc-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="700fc-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="700fc-160">1</span><span class="sxs-lookup"><span data-stu-id="700fc-160">1</span></span>     | <span data-ttu-id="700fc-161">/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="700fc-161">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="700fc-162">ascii</span><span class="sxs-lookup"><span data-stu-id="700fc-162">ascii</span></span>       |
| <span data-ttu-id="700fc-163">2</span><span class="sxs-lookup"><span data-stu-id="700fc-163">2</span></span>     | <span data-ttu-id="700fc-164">/IFD/XMP/EXIF: gpstrackref</span><span class="sxs-lookup"><span data-stu-id="700fc-164">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="700fc-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="700fc-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="700fc-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="700fc-166">Remove Paths</span></span>



| <span data-ttu-id="700fc-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="700fc-167">Order</span></span> | <span data-ttu-id="700fc-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="700fc-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="700fc-169">1</span><span class="sxs-lookup"><span data-stu-id="700fc-169">1</span></span>     | <span data-ttu-id="700fc-170">/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="700fc-170">/ifd/gps/{ushort=14}</span></span>      |
| <span data-ttu-id="700fc-171">2</span><span class="sxs-lookup"><span data-stu-id="700fc-171">2</span></span>     | <span data-ttu-id="700fc-172">/IFD/XMP/EXIF: gpstrackref</span><span class="sxs-lookup"><span data-stu-id="700fc-172">/ifd/xmp/exif:gpstrackref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="700fc-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="700fc-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="700fc-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="700fc-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="700fc-175">System. GPS. trackref</span><span class="sxs-lookup"><span data-stu-id="700fc-175">System.GPS.TrackRef</span></span>](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
