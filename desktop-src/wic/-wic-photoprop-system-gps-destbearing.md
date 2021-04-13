---
description: Die fotometadatenrichtlinie für die System. GPS. destbearing-Eigenschaft.
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: System. GPS. destbearing-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a084a0633579afe646403fb4dcad0ca8a1b9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348588"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a><span data-ttu-id="fd57e-103">System. GPS. destbearing-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="fd57e-103">System.GPS.DestBearing Photo Metadata Policy</span></span>

<span data-ttu-id="fd57e-104">Die fotometadatenrichtlinie für die [System. GPS. destbearing](../properties/props-system-gps-destbearing.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="fd57e-104">The photo metadata policy for the [System.GPS.DestBearing](../properties/props-system-gps-destbearing.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="fd57e-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="fd57e-105">PKEY</span></span>

<span data-ttu-id="fd57e-106">Pkey \_ GPS- \_ destbearing</span><span class="sxs-lookup"><span data-stu-id="fd57e-106">PKEY\_GPS\_DestBearing</span></span>

### <a name="containers"></a><span data-ttu-id="fd57e-107">Container</span><span class="sxs-lookup"><span data-stu-id="fd57e-107">Containers</span></span>

<span data-ttu-id="fd57e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="fd57e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="fd57e-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd57e-109">Read-Only</span></span>

<span data-ttu-id="fd57e-110">Ja</span><span class="sxs-lookup"><span data-stu-id="fd57e-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="fd57e-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="fd57e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="fd57e-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="fd57e-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="fd57e-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="fd57e-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="fd57e-114">Dieser Wert kann durch Schreiben in System. GPS. destbearingnumerator und System. GPS. destbearingnenner geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fd57e-114">This value can be written by writing to System.GPS.DestBearingNumerator and System.GPS.DestBearingDenominator.</span></span> <span data-ttu-id="fd57e-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fd57e-115">It cannot be written directly.</span></span> <span data-ttu-id="fd57e-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="fd57e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="fd57e-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="fd57e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="fd57e-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="fd57e-118">Read Paths</span></span>



| <span data-ttu-id="fd57e-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fd57e-119">Order</span></span> | <span data-ttu-id="fd57e-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="fd57e-120">Path</span></span>                      | <span data-ttu-id="fd57e-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fd57e-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="fd57e-122">1</span><span class="sxs-lookup"><span data-stu-id="fd57e-122">1</span></span>     | <span data-ttu-id="fd57e-123">/App1/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="fd57e-123">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="fd57e-124">2</span><span class="sxs-lookup"><span data-stu-id="fd57e-124">2</span></span>     | <span data-ttu-id="fd57e-125">/XMP/EXIF: gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="fd57e-125">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="write-paths"></a><span data-ttu-id="fd57e-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="fd57e-126">Write Paths</span></span>



| <span data-ttu-id="fd57e-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fd57e-127">Order</span></span> | <span data-ttu-id="fd57e-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="fd57e-128">Path</span></span>                      | <span data-ttu-id="fd57e-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fd57e-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="fd57e-130">1</span><span class="sxs-lookup"><span data-stu-id="fd57e-130">1</span></span>     | <span data-ttu-id="fd57e-131">/App1/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="fd57e-131">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="fd57e-132">2</span><span class="sxs-lookup"><span data-stu-id="fd57e-132">2</span></span>     | <span data-ttu-id="fd57e-133">/XMP/EXIF: gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="fd57e-133">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="remove-paths"></a><span data-ttu-id="fd57e-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="fd57e-134">Remove Paths</span></span>



| <span data-ttu-id="fd57e-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fd57e-135">Order</span></span> | <span data-ttu-id="fd57e-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="fd57e-136">Path</span></span>                      | <span data-ttu-id="fd57e-137">Datenträgerformat</span><span class="sxs-lookup"><span data-stu-id="fd57e-137">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="fd57e-138">1</span><span class="sxs-lookup"><span data-stu-id="fd57e-138">1</span></span>     | <span data-ttu-id="fd57e-139">/App1/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="fd57e-139">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="fd57e-140">2</span><span class="sxs-lookup"><span data-stu-id="fd57e-140">2</span></span>     | <span data-ttu-id="fd57e-141">/XMP/EXIF: gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="fd57e-141">/xmp/exif:gpsdestbearing</span></span>  |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="fd57e-142">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="fd57e-142">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="fd57e-143">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="fd57e-143">Read Paths</span></span>



| <span data-ttu-id="fd57e-144">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fd57e-144">Order</span></span> | <span data-ttu-id="fd57e-145">Pfad</span><span class="sxs-lookup"><span data-stu-id="fd57e-145">Path</span></span>                         | <span data-ttu-id="fd57e-146">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fd57e-146">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="fd57e-147">1</span><span class="sxs-lookup"><span data-stu-id="fd57e-147">1</span></span>     | <span data-ttu-id="fd57e-148">/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="fd57e-148">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="fd57e-149">2</span><span class="sxs-lookup"><span data-stu-id="fd57e-149">2</span></span>     | <span data-ttu-id="fd57e-150">/IFD/XMP/EXIF: gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="fd57e-150">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="fd57e-151">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="fd57e-151">Write Paths</span></span>



| <span data-ttu-id="fd57e-152">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fd57e-152">Order</span></span> | <span data-ttu-id="fd57e-153">Pfad</span><span class="sxs-lookup"><span data-stu-id="fd57e-153">Path</span></span>                         | <span data-ttu-id="fd57e-154">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fd57e-154">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="fd57e-155">1</span><span class="sxs-lookup"><span data-stu-id="fd57e-155">1</span></span>     | <span data-ttu-id="fd57e-156">/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="fd57e-156">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="fd57e-157">2</span><span class="sxs-lookup"><span data-stu-id="fd57e-157">2</span></span>     | <span data-ttu-id="fd57e-158">/IFD/XMP/EXIF: gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="fd57e-158">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="fd57e-159">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="fd57e-159">Remove Paths</span></span>



| <span data-ttu-id="fd57e-160">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fd57e-160">Order</span></span> | <span data-ttu-id="fd57e-161">Pfad</span><span class="sxs-lookup"><span data-stu-id="fd57e-161">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="fd57e-162">1</span><span class="sxs-lookup"><span data-stu-id="fd57e-162">1</span></span>     | <span data-ttu-id="fd57e-163">/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="fd57e-163">/ifd/gps/{ushort=24}</span></span>         |
| <span data-ttu-id="fd57e-164">2</span><span class="sxs-lookup"><span data-stu-id="fd57e-164">2</span></span>     | <span data-ttu-id="fd57e-165">/IFD/XMP/EXIF: gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="fd57e-165">/ifd/xmp/exif:gpsdestbearing</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fd57e-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd57e-166">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd57e-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd57e-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd57e-168">System. GPS. destbearing</span><span class="sxs-lookup"><span data-stu-id="fd57e-168">System.GPS.DestBearing</span></span>](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
