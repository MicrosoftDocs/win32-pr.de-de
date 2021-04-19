---
description: Die fotometadatenrichtlinie für die System. GPS. Track-Eigenschaft.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: System. GPS. Track Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773c65eec8b165c51456f3871309644638c1e2da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369876"
---
# <a name="systemgpstrack-photo-metadata-policy"></a><span data-ttu-id="2baf2-103">System. GPS. Track Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="2baf2-103">System.GPS.Track Photo Metadata Policy</span></span>

<span data-ttu-id="2baf2-104">Die fotometadatenrichtlinie für die [System. GPS. Track](../properties/props-system-gps-track.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2baf2-104">The photo metadata policy for the [System.GPS.Track](../properties/props-system-gps-track.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="2baf2-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="2baf2-105">PKEY</span></span>

<span data-ttu-id="2baf2-106">Pkey \_ GPS- \_ Track</span><span class="sxs-lookup"><span data-stu-id="2baf2-106">PKEY\_GPS\_Track</span></span>

### <a name="containers"></a><span data-ttu-id="2baf2-107">Container</span><span class="sxs-lookup"><span data-stu-id="2baf2-107">Containers</span></span>

<span data-ttu-id="2baf2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="2baf2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="2baf2-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2baf2-109">Read-Only</span></span>

<span data-ttu-id="2baf2-110">Ja</span><span class="sxs-lookup"><span data-stu-id="2baf2-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="2baf2-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="2baf2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="2baf2-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="2baf2-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="2baf2-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="2baf2-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="2baf2-114">Dieser Wert wird von "System. GPS. tracknumerator" und "System. GPS. tracknenner" generiert.</span><span class="sxs-lookup"><span data-stu-id="2baf2-114">This value is generated from System.GPS.TrackNumerator and System.GPS.TrackDenominator.</span></span> <span data-ttu-id="2baf2-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2baf2-115">It cannot be written directly.</span></span> <span data-ttu-id="2baf2-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="2baf2-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="2baf2-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="2baf2-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="2baf2-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="2baf2-118">Read Paths</span></span>



| <span data-ttu-id="2baf2-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="2baf2-119">Order</span></span> | <span data-ttu-id="2baf2-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="2baf2-120">Path</span></span>                      | <span data-ttu-id="2baf2-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="2baf2-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="2baf2-122">1</span><span class="sxs-lookup"><span data-stu-id="2baf2-122">1</span></span>     | <span data-ttu-id="2baf2-123">/App1/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="2baf2-123">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="2baf2-124">2</span><span class="sxs-lookup"><span data-stu-id="2baf2-124">2</span></span>     | <span data-ttu-id="2baf2-125">/XMP/EXIF: gpstrack</span><span class="sxs-lookup"><span data-stu-id="2baf2-125">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="2baf2-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="2baf2-126">Write Paths</span></span>



| <span data-ttu-id="2baf2-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="2baf2-127">Order</span></span> | <span data-ttu-id="2baf2-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="2baf2-128">Path</span></span>                      | <span data-ttu-id="2baf2-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="2baf2-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="2baf2-130">1</span><span class="sxs-lookup"><span data-stu-id="2baf2-130">1</span></span>     | <span data-ttu-id="2baf2-131">/App1/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="2baf2-131">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="2baf2-132">2</span><span class="sxs-lookup"><span data-stu-id="2baf2-132">2</span></span>     | <span data-ttu-id="2baf2-133">/XMP/EXIF: gpstrack</span><span class="sxs-lookup"><span data-stu-id="2baf2-133">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="2baf2-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="2baf2-134">Remove Paths</span></span>



| <span data-ttu-id="2baf2-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="2baf2-135">Order</span></span> | <span data-ttu-id="2baf2-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="2baf2-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="2baf2-137">1</span><span class="sxs-lookup"><span data-stu-id="2baf2-137">1</span></span>     | <span data-ttu-id="2baf2-138">/App1/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="2baf2-138">/app1/ifd/gps/{ushort=15}</span></span> |
| <span data-ttu-id="2baf2-139">2</span><span class="sxs-lookup"><span data-stu-id="2baf2-139">2</span></span>     | <span data-ttu-id="2baf2-140">/XMP/EXIF: gpstrack</span><span class="sxs-lookup"><span data-stu-id="2baf2-140">/xmp/exif:gpstrack</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="2baf2-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="2baf2-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="2baf2-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="2baf2-142">Read Paths</span></span>



| <span data-ttu-id="2baf2-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="2baf2-143">Order</span></span> | <span data-ttu-id="2baf2-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="2baf2-144">Path</span></span>                   | <span data-ttu-id="2baf2-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="2baf2-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="2baf2-146">1</span><span class="sxs-lookup"><span data-stu-id="2baf2-146">1</span></span>     | <span data-ttu-id="2baf2-147">/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="2baf2-147">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="2baf2-148">2</span><span class="sxs-lookup"><span data-stu-id="2baf2-148">2</span></span>     | <span data-ttu-id="2baf2-149">/IFD/XMP/EXIF: gpstrack</span><span class="sxs-lookup"><span data-stu-id="2baf2-149">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="2baf2-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="2baf2-150">Write Paths</span></span>



| <span data-ttu-id="2baf2-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="2baf2-151">Order</span></span> | <span data-ttu-id="2baf2-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="2baf2-152">Path</span></span>                   | <span data-ttu-id="2baf2-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="2baf2-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="2baf2-154">1</span><span class="sxs-lookup"><span data-stu-id="2baf2-154">1</span></span>     | <span data-ttu-id="2baf2-155">/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="2baf2-155">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="2baf2-156">2</span><span class="sxs-lookup"><span data-stu-id="2baf2-156">2</span></span>     | <span data-ttu-id="2baf2-157">/IFD/XMP/EXIF: gpstrack</span><span class="sxs-lookup"><span data-stu-id="2baf2-157">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="2baf2-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="2baf2-158">Remove Paths</span></span>



| <span data-ttu-id="2baf2-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="2baf2-159">Order</span></span> | <span data-ttu-id="2baf2-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="2baf2-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="2baf2-161">1</span><span class="sxs-lookup"><span data-stu-id="2baf2-161">1</span></span>     | <span data-ttu-id="2baf2-162">/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="2baf2-162">/ifd/gps/{ushort=15}</span></span>   |
| <span data-ttu-id="2baf2-163">2</span><span class="sxs-lookup"><span data-stu-id="2baf2-163">2</span></span>     | <span data-ttu-id="2baf2-164">/IFD/XMP/EXIF: gpstrack</span><span class="sxs-lookup"><span data-stu-id="2baf2-164">/ifd/xmp/exif:gpstrack</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2baf2-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2baf2-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="2baf2-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2baf2-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2baf2-167">System. GPS. Track</span><span class="sxs-lookup"><span data-stu-id="2baf2-167">System.GPS.Track</span></span>](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
