---
description: Die fotometadatenrichtlinie für die System. GPS. imgdirection-Eigenschaft.
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: System. GPS. imgdirection-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013edd632f98f1359c4f3c04856b0409c70eaa56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349664"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a><span data-ttu-id="a3deb-103">System. GPS. imgdirection-fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="a3deb-103">System.GPS.ImgDirection Photo Metadata Policy</span></span>

<span data-ttu-id="a3deb-104">Die fotometadatenrichtlinie für die [System. GPS. imgdirection](../properties/props-system-gps-imgdirection.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a3deb-104">The photo metadata policy for the [System.GPS.ImgDirection](../properties/props-system-gps-imgdirection.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a3deb-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="a3deb-105">PKEY</span></span>

<span data-ttu-id="a3deb-106">Pkey \_ GPS \_ imgdirection</span><span class="sxs-lookup"><span data-stu-id="a3deb-106">PKEY\_GPS\_ImgDirection</span></span>

### <a name="containers"></a><span data-ttu-id="a3deb-107">Container</span><span class="sxs-lookup"><span data-stu-id="a3deb-107">Containers</span></span>

<span data-ttu-id="a3deb-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a3deb-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a3deb-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a3deb-109">Read-Only</span></span>

<span data-ttu-id="a3deb-110">Ja</span><span class="sxs-lookup"><span data-stu-id="a3deb-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a3deb-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="a3deb-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a3deb-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="a3deb-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a3deb-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="a3deb-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="a3deb-114">Dieser Wert kann durch Schreiben in System. GPS. imgdirectionnumerator und System. GPS. imgdirectionnenner geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a3deb-114">This value can be written by writing to System.GPS.ImgDirectionNumerator and System.GPS.ImgDirectionDenominator.</span></span> <span data-ttu-id="a3deb-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a3deb-115">It cannot be written directly.</span></span> <span data-ttu-id="a3deb-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="a3deb-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a3deb-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a3deb-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a3deb-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="a3deb-118">Read Paths</span></span>



| <span data-ttu-id="a3deb-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a3deb-119">Order</span></span> | <span data-ttu-id="a3deb-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="a3deb-120">Path</span></span>                      | <span data-ttu-id="a3deb-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a3deb-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a3deb-122">1</span><span class="sxs-lookup"><span data-stu-id="a3deb-122">1</span></span>     | <span data-ttu-id="a3deb-123">/App1/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="a3deb-123">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="a3deb-124">2</span><span class="sxs-lookup"><span data-stu-id="a3deb-124">2</span></span>     | <span data-ttu-id="a3deb-125">/XMP/EXIF: gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="a3deb-125">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="a3deb-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="a3deb-126">Write Paths</span></span>



| <span data-ttu-id="a3deb-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a3deb-127">Order</span></span> | <span data-ttu-id="a3deb-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="a3deb-128">Path</span></span>                      | <span data-ttu-id="a3deb-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a3deb-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a3deb-130">1</span><span class="sxs-lookup"><span data-stu-id="a3deb-130">1</span></span>     | <span data-ttu-id="a3deb-131">/App1/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="a3deb-131">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="a3deb-132">2</span><span class="sxs-lookup"><span data-stu-id="a3deb-132">2</span></span>     | <span data-ttu-id="a3deb-133">/XMP/EXIF: gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="a3deb-133">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a3deb-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="a3deb-134">Remove Paths</span></span>



| <span data-ttu-id="a3deb-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a3deb-135">Order</span></span> | <span data-ttu-id="a3deb-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="a3deb-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="a3deb-137">1</span><span class="sxs-lookup"><span data-stu-id="a3deb-137">1</span></span>     | <span data-ttu-id="a3deb-138">/App1/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="a3deb-138">/app1/ifd/gps/{ushort=17}</span></span> |
| <span data-ttu-id="a3deb-139">2</span><span class="sxs-lookup"><span data-stu-id="a3deb-139">2</span></span>     | <span data-ttu-id="a3deb-140">/XMP/EXIF: gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="a3deb-140">/xmp/exif:gpsimgdirection</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="a3deb-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="a3deb-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a3deb-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="a3deb-142">Read Paths</span></span>



| <span data-ttu-id="a3deb-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a3deb-143">Order</span></span> | <span data-ttu-id="a3deb-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="a3deb-144">Path</span></span>                          | <span data-ttu-id="a3deb-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a3deb-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a3deb-146">1</span><span class="sxs-lookup"><span data-stu-id="a3deb-146">1</span></span>     | <span data-ttu-id="a3deb-147">/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="a3deb-147">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="a3deb-148">2</span><span class="sxs-lookup"><span data-stu-id="a3deb-148">2</span></span>     | <span data-ttu-id="a3deb-149">/IFD/XMP/EXIF: gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="a3deb-149">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="a3deb-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="a3deb-150">Write Paths</span></span>



| <span data-ttu-id="a3deb-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a3deb-151">Order</span></span> | <span data-ttu-id="a3deb-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="a3deb-152">Path</span></span>                          | <span data-ttu-id="a3deb-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a3deb-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a3deb-154">1</span><span class="sxs-lookup"><span data-stu-id="a3deb-154">1</span></span>     | <span data-ttu-id="a3deb-155">/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="a3deb-155">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="a3deb-156">2</span><span class="sxs-lookup"><span data-stu-id="a3deb-156">2</span></span>     | <span data-ttu-id="a3deb-157">/IFD/XMP/EXIF: gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="a3deb-157">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a3deb-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="a3deb-158">Remove Paths</span></span>



| <span data-ttu-id="a3deb-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a3deb-159">Order</span></span> | <span data-ttu-id="a3deb-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="a3deb-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="a3deb-161">1</span><span class="sxs-lookup"><span data-stu-id="a3deb-161">1</span></span>     | <span data-ttu-id="a3deb-162">/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="a3deb-162">/ifd/gps/{ushort=17}</span></span>          |
| <span data-ttu-id="a3deb-163">2</span><span class="sxs-lookup"><span data-stu-id="a3deb-163">2</span></span>     | <span data-ttu-id="a3deb-164">/IFD/XMP/EXIF: gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="a3deb-164">/ifd/xmp/exif:gpsimgdirection</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a3deb-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3deb-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3deb-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a3deb-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3deb-167">System. GPS. imgdirection</span><span class="sxs-lookup"><span data-stu-id="a3deb-167">System.GPS.ImgDirection</span></span>](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
