---
description: Die fotometadatenrichtlinie für die System. GPS. Latitude-Eigenschaft.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: System. GPS. Latitude-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5320869c1e8fd0d4b17bb17da455fc939bf44b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350825"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a><span data-ttu-id="1f53e-103">System. GPS. Latitude-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="1f53e-103">System.GPS.Latitude Photo Metadata Policy</span></span>

<span data-ttu-id="1f53e-104">Die fotometadatenrichtlinie für die [System. GPS. Latitude](../properties/props-system-gps-latitude.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1f53e-104">The photo metadata policy for the [System.GPS.Latitude](../properties/props-system-gps-latitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1f53e-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="1f53e-105">PKEY</span></span>

<span data-ttu-id="1f53e-106">Pkey \_ GPS- \_ Breite</span><span class="sxs-lookup"><span data-stu-id="1f53e-106">PKEY\_GPS\_Latitude</span></span>

### <a name="containers"></a><span data-ttu-id="1f53e-107">Container</span><span class="sxs-lookup"><span data-stu-id="1f53e-107">Containers</span></span>

<span data-ttu-id="1f53e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1f53e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1f53e-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f53e-109">Read-Only</span></span>

<span data-ttu-id="1f53e-110">Ja</span><span class="sxs-lookup"><span data-stu-id="1f53e-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1f53e-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="1f53e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1f53e-112">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="1f53e-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1f53e-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="1f53e-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="1f53e-114">Dieser Wert kann durch Schreiben in "System. GPS. latitudenumerator" und "System. GPS. latitudebug" geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1f53e-114">This value can be written by writing to System.GPS.LatitudeNumerator and System.GPS.LatitudeDenominator.</span></span> <span data-ttu-id="1f53e-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1f53e-115">It cannot be written directly.</span></span> <span data-ttu-id="1f53e-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="1f53e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="1f53e-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="1f53e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1f53e-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="1f53e-118">Read Paths</span></span>



| <span data-ttu-id="1f53e-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1f53e-119">Order</span></span> | <span data-ttu-id="1f53e-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="1f53e-120">Path</span></span>                     | <span data-ttu-id="1f53e-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="1f53e-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="1f53e-122">1</span><span class="sxs-lookup"><span data-stu-id="1f53e-122">1</span></span>     | <span data-ttu-id="1f53e-123">/App1/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="1f53e-123">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="1f53e-124">2</span><span class="sxs-lookup"><span data-stu-id="1f53e-124">2</span></span>     | <span data-ttu-id="1f53e-125">/XMP/EXIF: gpslatitude</span><span class="sxs-lookup"><span data-stu-id="1f53e-125">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="1f53e-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="1f53e-126">Write Paths</span></span>



| <span data-ttu-id="1f53e-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1f53e-127">Order</span></span> | <span data-ttu-id="1f53e-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="1f53e-128">Path</span></span>                     | <span data-ttu-id="1f53e-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="1f53e-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="1f53e-130">1</span><span class="sxs-lookup"><span data-stu-id="1f53e-130">1</span></span>     | <span data-ttu-id="1f53e-131">/App1/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="1f53e-131">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="1f53e-132">2</span><span class="sxs-lookup"><span data-stu-id="1f53e-132">2</span></span>     | <span data-ttu-id="1f53e-133">/XMP/EXIF: gpslatitude</span><span class="sxs-lookup"><span data-stu-id="1f53e-133">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="1f53e-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="1f53e-134">Remove Paths</span></span>



| <span data-ttu-id="1f53e-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1f53e-135">Order</span></span> | <span data-ttu-id="1f53e-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="1f53e-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="1f53e-137">1</span><span class="sxs-lookup"><span data-stu-id="1f53e-137">1</span></span>     | <span data-ttu-id="1f53e-138">/App1/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="1f53e-138">/app1/ifd/gps/{ushort=2}</span></span> |
| <span data-ttu-id="1f53e-139">2</span><span class="sxs-lookup"><span data-stu-id="1f53e-139">2</span></span>     | <span data-ttu-id="1f53e-140">/XMP/EXIF: gpslatitude</span><span class="sxs-lookup"><span data-stu-id="1f53e-140">/xmp/exif:gpslatitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="1f53e-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="1f53e-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1f53e-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="1f53e-142">Read Paths</span></span>



| <span data-ttu-id="1f53e-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1f53e-143">Order</span></span> | <span data-ttu-id="1f53e-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="1f53e-144">Path</span></span>                      | <span data-ttu-id="1f53e-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="1f53e-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="1f53e-146">1</span><span class="sxs-lookup"><span data-stu-id="1f53e-146">1</span></span>     | <span data-ttu-id="1f53e-147">/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="1f53e-147">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="1f53e-148">2</span><span class="sxs-lookup"><span data-stu-id="1f53e-148">2</span></span>     | <span data-ttu-id="1f53e-149">/IFD/XMP/EXIF: gpslatitude</span><span class="sxs-lookup"><span data-stu-id="1f53e-149">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="1f53e-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="1f53e-150">Write Paths</span></span>



| <span data-ttu-id="1f53e-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1f53e-151">Order</span></span> | <span data-ttu-id="1f53e-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="1f53e-152">Path</span></span>                      | <span data-ttu-id="1f53e-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="1f53e-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="1f53e-154">1</span><span class="sxs-lookup"><span data-stu-id="1f53e-154">1</span></span>     | <span data-ttu-id="1f53e-155">/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="1f53e-155">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="1f53e-156">2</span><span class="sxs-lookup"><span data-stu-id="1f53e-156">2</span></span>     | <span data-ttu-id="1f53e-157">/IFD/XMP/EXIF: gpslatitude</span><span class="sxs-lookup"><span data-stu-id="1f53e-157">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="1f53e-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="1f53e-158">Remove Paths</span></span>



| <span data-ttu-id="1f53e-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1f53e-159">Order</span></span> | <span data-ttu-id="1f53e-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="1f53e-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="1f53e-161">1</span><span class="sxs-lookup"><span data-stu-id="1f53e-161">1</span></span>     | <span data-ttu-id="1f53e-162">/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="1f53e-162">/ifd/gps/{ushort=2}</span></span>       |
| <span data-ttu-id="1f53e-163">2</span><span class="sxs-lookup"><span data-stu-id="1f53e-163">2</span></span>     | <span data-ttu-id="1f53e-164">/IFD/XMP/EXIF: gpslatitude</span><span class="sxs-lookup"><span data-stu-id="1f53e-164">/ifd/xmp/exif:gpslatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1f53e-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f53e-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f53e-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1f53e-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f53e-167">System. GPS. Latitude</span><span class="sxs-lookup"><span data-stu-id="1f53e-167">System.GPS.Latitude</span></span>](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
