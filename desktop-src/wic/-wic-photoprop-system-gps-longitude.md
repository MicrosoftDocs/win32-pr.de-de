---
description: Die fotometadatenrichtlinie für die System. GPS. Longitude-Eigenschaft.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: System. GPS. Längengrade Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25eb9869bc536f97adfc8f3c0f5b1f70c8bf030f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351062"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a><span data-ttu-id="10f0d-103">System. GPS. Längengrade Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="10f0d-103">System.GPS.Longitude Photo Metadata Policy</span></span>

<span data-ttu-id="10f0d-104">Die fotometadatenrichtlinie für die [System. GPS. Longitude](../properties/props-system-gps-longitude.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="10f0d-104">The photo metadata policy for the [System.GPS.Longitude](../properties/props-system-gps-longitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="10f0d-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="10f0d-105">PKEY</span></span>

<span data-ttu-id="10f0d-106">Pkey \_ GPS- \_ Längengrad</span><span class="sxs-lookup"><span data-stu-id="10f0d-106">PKEY\_GPS\_Longitude</span></span>

### <a name="containers"></a><span data-ttu-id="10f0d-107">Container</span><span class="sxs-lookup"><span data-stu-id="10f0d-107">Containers</span></span>

<span data-ttu-id="10f0d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="10f0d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="10f0d-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10f0d-109">Read-Only</span></span>

<span data-ttu-id="10f0d-110">Ja</span><span class="sxs-lookup"><span data-stu-id="10f0d-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="10f0d-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="10f0d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="10f0d-112">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="10f0d-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="10f0d-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="10f0d-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="10f0d-114">Sie können diesen Wert schreiben, indem Sie in System. GPS. in "System. GPS.................</span><span class="sxs-lookup"><span data-stu-id="10f0d-114">This value can be written by writing to System.GPS.LongitudeNumerator and System.GPS.LongitudeDenominator.</span></span> <span data-ttu-id="10f0d-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="10f0d-115">It cannot be written directly.</span></span> <span data-ttu-id="10f0d-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="10f0d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="10f0d-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="10f0d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="10f0d-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="10f0d-118">Read Paths</span></span>



| <span data-ttu-id="10f0d-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="10f0d-119">Order</span></span> | <span data-ttu-id="10f0d-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="10f0d-120">Path</span></span>                     | <span data-ttu-id="10f0d-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="10f0d-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="10f0d-122">1</span><span class="sxs-lookup"><span data-stu-id="10f0d-122">1</span></span>     | <span data-ttu-id="10f0d-123">/App1/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="10f0d-123">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="10f0d-124">2</span><span class="sxs-lookup"><span data-stu-id="10f0d-124">2</span></span>     | <span data-ttu-id="10f0d-125">/XMP/EXIF: gpslängen Grad</span><span class="sxs-lookup"><span data-stu-id="10f0d-125">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="10f0d-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="10f0d-126">Write Paths</span></span>



| <span data-ttu-id="10f0d-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="10f0d-127">Order</span></span> | <span data-ttu-id="10f0d-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="10f0d-128">Path</span></span>                     | <span data-ttu-id="10f0d-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="10f0d-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="10f0d-130">1</span><span class="sxs-lookup"><span data-stu-id="10f0d-130">1</span></span>     | <span data-ttu-id="10f0d-131">/App1/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="10f0d-131">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="10f0d-132">2</span><span class="sxs-lookup"><span data-stu-id="10f0d-132">2</span></span>     | <span data-ttu-id="10f0d-133">/XMP/EXIF: gpslängen Grad</span><span class="sxs-lookup"><span data-stu-id="10f0d-133">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="10f0d-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="10f0d-134">Remove Paths</span></span>



| <span data-ttu-id="10f0d-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="10f0d-135">Order</span></span> | <span data-ttu-id="10f0d-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="10f0d-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="10f0d-137">1</span><span class="sxs-lookup"><span data-stu-id="10f0d-137">1</span></span>     | <span data-ttu-id="10f0d-138">/App1/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="10f0d-138">/app1/ifd/gps/{ushort=4}</span></span> |
| <span data-ttu-id="10f0d-139">2</span><span class="sxs-lookup"><span data-stu-id="10f0d-139">2</span></span>     | <span data-ttu-id="10f0d-140">/XMP/EXIF: gpslängen Grad</span><span class="sxs-lookup"><span data-stu-id="10f0d-140">/xmp/exif:gpslongitude</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="10f0d-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="10f0d-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="10f0d-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="10f0d-142">Read Paths</span></span>



| <span data-ttu-id="10f0d-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="10f0d-143">Order</span></span> | <span data-ttu-id="10f0d-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="10f0d-144">Path</span></span>                       | <span data-ttu-id="10f0d-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="10f0d-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="10f0d-146">1</span><span class="sxs-lookup"><span data-stu-id="10f0d-146">1</span></span>     | <span data-ttu-id="10f0d-147">/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="10f0d-147">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="10f0d-148">2</span><span class="sxs-lookup"><span data-stu-id="10f0d-148">2</span></span>     | <span data-ttu-id="10f0d-149">/IFD/XMP/EXIF: gpslängen Grad</span><span class="sxs-lookup"><span data-stu-id="10f0d-149">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="10f0d-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="10f0d-150">Write Paths</span></span>



| <span data-ttu-id="10f0d-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="10f0d-151">Order</span></span> | <span data-ttu-id="10f0d-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="10f0d-152">Path</span></span>                       | <span data-ttu-id="10f0d-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="10f0d-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="10f0d-154">1</span><span class="sxs-lookup"><span data-stu-id="10f0d-154">1</span></span>     | <span data-ttu-id="10f0d-155">/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="10f0d-155">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="10f0d-156">2</span><span class="sxs-lookup"><span data-stu-id="10f0d-156">2</span></span>     | <span data-ttu-id="10f0d-157">/IFD/XMP/EXIF: gpslängen Grad</span><span class="sxs-lookup"><span data-stu-id="10f0d-157">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="10f0d-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="10f0d-158">Remove Paths</span></span>



| <span data-ttu-id="10f0d-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="10f0d-159">Order</span></span> | <span data-ttu-id="10f0d-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="10f0d-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="10f0d-161">1</span><span class="sxs-lookup"><span data-stu-id="10f0d-161">1</span></span>     | <span data-ttu-id="10f0d-162">/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="10f0d-162">/ifd/gps/{ushort=4}</span></span>        |
| <span data-ttu-id="10f0d-163">2</span><span class="sxs-lookup"><span data-stu-id="10f0d-163">2</span></span>     | <span data-ttu-id="10f0d-164">/IFD/XMP/EXIF: gpslängen Grad</span><span class="sxs-lookup"><span data-stu-id="10f0d-164">/ifd/xmp/exif:gpslongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="10f0d-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10f0d-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="10f0d-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="10f0d-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10f0d-167">System. GPS. Längengrad</span><span class="sxs-lookup"><span data-stu-id="10f0d-167">System.GPS.Longitude</span></span>](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
