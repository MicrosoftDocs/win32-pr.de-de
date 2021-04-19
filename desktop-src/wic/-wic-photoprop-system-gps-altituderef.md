---
description: Die fotometadatenrichtlinie für die System. GPS. altituderef-Eigenschaft.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: System. GPS. altituderef-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db600d218d72014c49fd3f0a8b5eb11dd4c467d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355374"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a><span data-ttu-id="bddf0-103">System. GPS. altituderef-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="bddf0-103">System.GPS.AltitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="bddf0-104">Die fotometadatenrichtlinie für die [System. GPS. altituderef](../properties/props-system-gps-altituderef.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bddf0-104">The photo metadata policy for the [System.GPS.AltitudeRef](../properties/props-system-gps-altituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="bddf0-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="bddf0-105">PKEY</span></span>

<span data-ttu-id="bddf0-106">Pkey \_ GPS \_ altituderef</span><span class="sxs-lookup"><span data-stu-id="bddf0-106">PKEY\_GPS\_AltitudeRef</span></span>

### <a name="description"></a><span data-ttu-id="bddf0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bddf0-107">Description</span></span>

<span data-ttu-id="bddf0-108">Gibt die als Bezugs Höhe verwendete Höhe an.</span><span class="sxs-lookup"><span data-stu-id="bddf0-108">Indicates the altitude used as the reference altitude.</span></span> <span data-ttu-id="bddf0-109">Der Wert 0 gibt an, dass die Höhe oberhalb der sebene liegt.</span><span class="sxs-lookup"><span data-stu-id="bddf0-109">A value of 0 indicates the altitude is above sea level.</span></span> <span data-ttu-id="bddf0-110">Der Wert 1 gibt eine Höhe unterhalb der sebene an.</span><span class="sxs-lookup"><span data-stu-id="bddf0-110">A value of 1 indicates an altitude below sea level.</span></span>

### <a name="containers"></a><span data-ttu-id="bddf0-111">Container</span><span class="sxs-lookup"><span data-stu-id="bddf0-111">Containers</span></span>

<span data-ttu-id="bddf0-112">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="bddf0-112">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="bddf0-113">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bddf0-113">Read-Only</span></span>

<span data-ttu-id="bddf0-114">Nein</span><span class="sxs-lookup"><span data-stu-id="bddf0-114">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="bddf0-115">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="bddf0-115">Output PROPVARIANT Type</span></span>

<span data-ttu-id="bddf0-116">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="bddf0-116">VT\_UI1</span></span>

### <a name="input-type"></a><span data-ttu-id="bddf0-117">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="bddf0-117">Input Type</span></span>

<span data-ttu-id="bddf0-118">Hobby.</span><span class="sxs-lookup"><span data-stu-id="bddf0-118">Byte.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="bddf0-119">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="bddf0-119">Conflict Resolution Policy</span></span>

<span data-ttu-id="bddf0-120">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="bddf0-120">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="bddf0-121">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="bddf0-121">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="bddf0-122">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="bddf0-122">Read Paths</span></span>



| <span data-ttu-id="bddf0-123">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bddf0-123">Order</span></span> | <span data-ttu-id="bddf0-124">Pfad</span><span class="sxs-lookup"><span data-stu-id="bddf0-124">Path</span></span>                     | <span data-ttu-id="bddf0-125">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="bddf0-125">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="bddf0-126">1</span><span class="sxs-lookup"><span data-stu-id="bddf0-126">1</span></span>     | <span data-ttu-id="bddf0-127">/App1/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="bddf0-127">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="bddf0-128">byte</span><span class="sxs-lookup"><span data-stu-id="bddf0-128">byte</span></span>        |
| <span data-ttu-id="bddf0-129">2</span><span class="sxs-lookup"><span data-stu-id="bddf0-129">2</span></span>     | <span data-ttu-id="bddf0-130">/XMP/EXIF: gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="bddf0-130">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="bddf0-131">Unicode</span><span class="sxs-lookup"><span data-stu-id="bddf0-131">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="bddf0-132">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="bddf0-132">Write Paths</span></span>



| <span data-ttu-id="bddf0-133">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bddf0-133">Order</span></span> | <span data-ttu-id="bddf0-134">Pfad</span><span class="sxs-lookup"><span data-stu-id="bddf0-134">Path</span></span>                     | <span data-ttu-id="bddf0-135">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="bddf0-135">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="bddf0-136">1</span><span class="sxs-lookup"><span data-stu-id="bddf0-136">1</span></span>     | <span data-ttu-id="bddf0-137">/App1/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="bddf0-137">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="bddf0-138">byte</span><span class="sxs-lookup"><span data-stu-id="bddf0-138">byte</span></span>        |
| <span data-ttu-id="bddf0-139">2</span><span class="sxs-lookup"><span data-stu-id="bddf0-139">2</span></span>     | <span data-ttu-id="bddf0-140">/XMP/EXIF: gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="bddf0-140">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="bddf0-141">Unicode</span><span class="sxs-lookup"><span data-stu-id="bddf0-141">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="bddf0-142">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="bddf0-142">Remove Paths</span></span>



| <span data-ttu-id="bddf0-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bddf0-143">Order</span></span> | <span data-ttu-id="bddf0-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="bddf0-144">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="bddf0-145">1</span><span class="sxs-lookup"><span data-stu-id="bddf0-145">1</span></span>     | <span data-ttu-id="bddf0-146">/App1/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="bddf0-146">/app1/ifd/gps/{ushort=5}</span></span> |
| <span data-ttu-id="bddf0-147">2</span><span class="sxs-lookup"><span data-stu-id="bddf0-147">2</span></span>     | <span data-ttu-id="bddf0-148">/XMP/EXIF: gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="bddf0-148">/xmp/exif:gpsaltituderef</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="bddf0-149">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="bddf0-149">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="bddf0-150">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="bddf0-150">Read Paths</span></span>



| <span data-ttu-id="bddf0-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bddf0-151">Order</span></span> | <span data-ttu-id="bddf0-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="bddf0-152">Path</span></span>                         | <span data-ttu-id="bddf0-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="bddf0-153">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="bddf0-154">1</span><span class="sxs-lookup"><span data-stu-id="bddf0-154">1</span></span>     | <span data-ttu-id="bddf0-155">/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="bddf0-155">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="bddf0-156">byte</span><span class="sxs-lookup"><span data-stu-id="bddf0-156">byte</span></span>        |
| <span data-ttu-id="bddf0-157">2</span><span class="sxs-lookup"><span data-stu-id="bddf0-157">2</span></span>     | <span data-ttu-id="bddf0-158">/IFD/XMP/EXIF: gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="bddf0-158">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="bddf0-159">Unicode</span><span class="sxs-lookup"><span data-stu-id="bddf0-159">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="bddf0-160">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="bddf0-160">Write Paths</span></span>



| <span data-ttu-id="bddf0-161">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bddf0-161">Order</span></span> | <span data-ttu-id="bddf0-162">Pfad</span><span class="sxs-lookup"><span data-stu-id="bddf0-162">Path</span></span>                         | <span data-ttu-id="bddf0-163">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="bddf0-163">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="bddf0-164">1</span><span class="sxs-lookup"><span data-stu-id="bddf0-164">1</span></span>     | <span data-ttu-id="bddf0-165">/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="bddf0-165">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="bddf0-166">byte</span><span class="sxs-lookup"><span data-stu-id="bddf0-166">byte</span></span>        |
| <span data-ttu-id="bddf0-167">2</span><span class="sxs-lookup"><span data-stu-id="bddf0-167">2</span></span>     | <span data-ttu-id="bddf0-168">/IFD/XMP/EXIF: gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="bddf0-168">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="bddf0-169">Unicode</span><span class="sxs-lookup"><span data-stu-id="bddf0-169">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="bddf0-170">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="bddf0-170">Remove Paths</span></span>



| <span data-ttu-id="bddf0-171">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bddf0-171">Order</span></span> | <span data-ttu-id="bddf0-172">Pfad</span><span class="sxs-lookup"><span data-stu-id="bddf0-172">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="bddf0-173">1</span><span class="sxs-lookup"><span data-stu-id="bddf0-173">1</span></span>     | <span data-ttu-id="bddf0-174">/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="bddf0-174">/ifd/gps/{ushort=5}</span></span>          |
| <span data-ttu-id="bddf0-175">2</span><span class="sxs-lookup"><span data-stu-id="bddf0-175">2</span></span>     | <span data-ttu-id="bddf0-176">/IFD/XMP/EXIF: gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="bddf0-176">/ifd/xmp/exif:gpsaltituderef</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bddf0-177">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bddf0-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="bddf0-178">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bddf0-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bddf0-179">System. GPS. altituderef</span><span class="sxs-lookup"><span data-stu-id="bddf0-179">System.GPS.AltitudeRef</span></span>](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
