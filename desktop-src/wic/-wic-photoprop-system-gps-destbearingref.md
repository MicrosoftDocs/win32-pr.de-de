---
description: Die fotometadatenrichtlinie für die System. GPS. destbearingref-Eigenschaft.
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: System. GPS. destbearingref Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f00d3083459fe365fc54e81dc485ddd26887a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216814"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a><span data-ttu-id="7db88-103">System. GPS. destbearingref Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="7db88-103">System.GPS.DestBearingRef Photo Metadata Policy</span></span>

<span data-ttu-id="7db88-104">Die fotometadatenrichtlinie für die [System. GPS. destbearingref](../properties/props-system-gps-destbearingref.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7db88-104">The photo metadata policy for the [System.GPS.DestBearingRef](../properties/props-system-gps-destbearingref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="7db88-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="7db88-105">PKEY</span></span>

<span data-ttu-id="7db88-106">Pkey \_ GPS \_ destbearingref</span><span class="sxs-lookup"><span data-stu-id="7db88-106">PKEY\_GPS\_DestBearingRef</span></span>

### <a name="containers"></a><span data-ttu-id="7db88-107">Container</span><span class="sxs-lookup"><span data-stu-id="7db88-107">Containers</span></span>

<span data-ttu-id="7db88-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7db88-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="7db88-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7db88-109">Read-Only</span></span>

<span data-ttu-id="7db88-110">Nein</span><span class="sxs-lookup"><span data-stu-id="7db88-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="7db88-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="7db88-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="7db88-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="7db88-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="7db88-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="7db88-113">Input Type</span></span>

<span data-ttu-id="7db88-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7db88-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="7db88-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="7db88-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="7db88-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="7db88-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="7db88-117">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="7db88-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="7db88-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="7db88-118">Read Paths</span></span>



| <span data-ttu-id="7db88-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7db88-119">Order</span></span> | <span data-ttu-id="7db88-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="7db88-120">Path</span></span>                        | <span data-ttu-id="7db88-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="7db88-121">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="7db88-122">1</span><span class="sxs-lookup"><span data-stu-id="7db88-122">1</span></span>     | <span data-ttu-id="7db88-123">/App1/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="7db88-123">/app1/ifd/gps/{ushort=23}</span></span>   | <span data-ttu-id="7db88-124">ascii</span><span class="sxs-lookup"><span data-stu-id="7db88-124">ascii</span></span>       |
| <span data-ttu-id="7db88-125">2</span><span class="sxs-lookup"><span data-stu-id="7db88-125">2</span></span>     | <span data-ttu-id="7db88-126">/XMP/EXIF: gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="7db88-126">/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="7db88-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="7db88-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7db88-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="7db88-128">Write Paths</span></span>



| <span data-ttu-id="7db88-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7db88-129">Order</span></span> | <span data-ttu-id="7db88-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="7db88-130">Path</span></span>                        | <span data-ttu-id="7db88-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="7db88-131">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="7db88-132">1</span><span class="sxs-lookup"><span data-stu-id="7db88-132">1</span></span>     | <span data-ttu-id="7db88-133">/App1/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="7db88-133">/app1/ifd/gps/{ushort=23}</span></span>   | <span data-ttu-id="7db88-134">ascii</span><span class="sxs-lookup"><span data-stu-id="7db88-134">ascii</span></span>       |
| <span data-ttu-id="7db88-135">2</span><span class="sxs-lookup"><span data-stu-id="7db88-135">2</span></span>     | <span data-ttu-id="7db88-136">/XMP/EXIF: gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="7db88-136">/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="7db88-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="7db88-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7db88-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="7db88-138">Remove Paths</span></span>



| <span data-ttu-id="7db88-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7db88-139">Order</span></span> | <span data-ttu-id="7db88-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="7db88-140">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="7db88-141">1</span><span class="sxs-lookup"><span data-stu-id="7db88-141">1</span></span>     | <span data-ttu-id="7db88-142">/App1/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="7db88-142">/app1/ifd/gps/{ushort=23}</span></span>   |
| <span data-ttu-id="7db88-143">2</span><span class="sxs-lookup"><span data-stu-id="7db88-143">2</span></span>     | <span data-ttu-id="7db88-144">/XMP/EXIF: gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="7db88-144">/xmp/exif:gpsdestbearingref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="7db88-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="7db88-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="7db88-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="7db88-146">Read Paths</span></span>



| <span data-ttu-id="7db88-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7db88-147">Order</span></span> | <span data-ttu-id="7db88-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="7db88-148">Path</span></span>                            | <span data-ttu-id="7db88-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="7db88-149">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="7db88-150">1</span><span class="sxs-lookup"><span data-stu-id="7db88-150">1</span></span>     | <span data-ttu-id="7db88-151">/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="7db88-151">/ifd/gps/{ushort=23}</span></span>            | <span data-ttu-id="7db88-152">ascii</span><span class="sxs-lookup"><span data-stu-id="7db88-152">ascii</span></span>       |
| <span data-ttu-id="7db88-153">2</span><span class="sxs-lookup"><span data-stu-id="7db88-153">2</span></span>     | <span data-ttu-id="7db88-154">/IFD/XMP/EXIF: gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="7db88-154">/ifd/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="7db88-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="7db88-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7db88-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="7db88-156">Write Paths</span></span>



| <span data-ttu-id="7db88-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7db88-157">Order</span></span> | <span data-ttu-id="7db88-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="7db88-158">Path</span></span>                            | <span data-ttu-id="7db88-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="7db88-159">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="7db88-160">1</span><span class="sxs-lookup"><span data-stu-id="7db88-160">1</span></span>     | <span data-ttu-id="7db88-161">/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="7db88-161">/ifd/gps/{ushort=23}</span></span>            | <span data-ttu-id="7db88-162">ascii</span><span class="sxs-lookup"><span data-stu-id="7db88-162">ascii</span></span>       |
| <span data-ttu-id="7db88-163">2</span><span class="sxs-lookup"><span data-stu-id="7db88-163">2</span></span>     | <span data-ttu-id="7db88-164">/IFD/XMP/EXIF: gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="7db88-164">/ifd/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="7db88-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="7db88-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7db88-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="7db88-166">Remove Paths</span></span>



| <span data-ttu-id="7db88-167">order</span><span class="sxs-lookup"><span data-stu-id="7db88-167">order</span></span> | <span data-ttu-id="7db88-168">path</span><span class="sxs-lookup"><span data-stu-id="7db88-168">path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="7db88-169">1</span><span class="sxs-lookup"><span data-stu-id="7db88-169">1</span></span>     | <span data-ttu-id="7db88-170">/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="7db88-170">/ifd/gps/{ushort=23}</span></span>            |
| <span data-ttu-id="7db88-171">2</span><span class="sxs-lookup"><span data-stu-id="7db88-171">2</span></span>     | <span data-ttu-id="7db88-172">/IFD/XMP/EXIF: gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="7db88-172">/ifd/xmp/exif:gpsdestbearingref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7db88-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7db88-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="7db88-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7db88-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7db88-175">System. GPS. destbearingref</span><span class="sxs-lookup"><span data-stu-id="7db88-175">System.GPS.DestBearingRef</span></span>](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
