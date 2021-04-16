---
description: Die fotometadatenrichtlinie für die System. GPS. Differential-Eigenschaft.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: System. GPS. differenzielle fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc3f114683d324a067fe4ce4034e2de5cfc88da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348578"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a><span data-ttu-id="9a7d3-103">System. GPS. differenzielle fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="9a7d3-103">System.GPS.Differential Photo Metadata Policy</span></span>

<span data-ttu-id="9a7d3-104">Die fotometadatenrichtlinie für die [System. GPS. Differential](../properties/props-system-gps-differential.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9a7d3-104">The photo metadata policy for the [System.GPS.Differential](../properties/props-system-gps-differential.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9a7d3-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="9a7d3-105">PKEY</span></span>

<span data-ttu-id="9a7d3-106">Pkey \_ -GPS- \_ differenziell</span><span class="sxs-lookup"><span data-stu-id="9a7d3-106">PKEY\_GPS\_Differential</span></span>

### <a name="containers"></a><span data-ttu-id="9a7d3-107">Container</span><span class="sxs-lookup"><span data-stu-id="9a7d3-107">Containers</span></span>

<span data-ttu-id="9a7d3-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9a7d3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9a7d3-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a7d3-109">Read-Only</span></span>

<span data-ttu-id="9a7d3-110">Nein</span><span class="sxs-lookup"><span data-stu-id="9a7d3-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9a7d3-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="9a7d3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9a7d3-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="9a7d3-112">VT\_UI2</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="9a7d3-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="9a7d3-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="9a7d3-114">VT \_ UI1, VT \_ UI2 und VT \_ UI4 werden alle akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="9a7d3-114">VT\_UI1, VT\_UI2, and VT\_UI4 are all accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9a7d3-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="9a7d3-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="9a7d3-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="9a7d3-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="9a7d3-117">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="9a7d3-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9a7d3-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="9a7d3-118">Read Paths</span></span>



| <span data-ttu-id="9a7d3-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9a7d3-119">Order</span></span> | <span data-ttu-id="9a7d3-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="9a7d3-120">Path</span></span>                      | <span data-ttu-id="9a7d3-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9a7d3-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9a7d3-122">1</span><span class="sxs-lookup"><span data-stu-id="9a7d3-122">1</span></span>     | <span data-ttu-id="9a7d3-123">/App1/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="9a7d3-123">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="9a7d3-124">ushort</span><span class="sxs-lookup"><span data-stu-id="9a7d3-124">ushort</span></span>      |
| <span data-ttu-id="9a7d3-125">2</span><span class="sxs-lookup"><span data-stu-id="9a7d3-125">2</span></span>     | <span data-ttu-id="9a7d3-126">/XMP/EXIF: gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="9a7d3-126">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="9a7d3-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="9a7d3-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9a7d3-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="9a7d3-128">Write Paths</span></span>



| <span data-ttu-id="9a7d3-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9a7d3-129">Order</span></span> | <span data-ttu-id="9a7d3-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="9a7d3-130">Path</span></span>                      | <span data-ttu-id="9a7d3-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9a7d3-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9a7d3-132">1</span><span class="sxs-lookup"><span data-stu-id="9a7d3-132">1</span></span>     | <span data-ttu-id="9a7d3-133">/App1/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="9a7d3-133">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="9a7d3-134">ushort</span><span class="sxs-lookup"><span data-stu-id="9a7d3-134">ushort</span></span>      |
| <span data-ttu-id="9a7d3-135">2</span><span class="sxs-lookup"><span data-stu-id="9a7d3-135">2</span></span>     | <span data-ttu-id="9a7d3-136">/XMP/EXIF: gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="9a7d3-136">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="9a7d3-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="9a7d3-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9a7d3-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="9a7d3-138">Remove Paths</span></span>



| <span data-ttu-id="9a7d3-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9a7d3-139">Order</span></span> | <span data-ttu-id="9a7d3-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="9a7d3-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="9a7d3-141">1</span><span class="sxs-lookup"><span data-stu-id="9a7d3-141">1</span></span>     | <span data-ttu-id="9a7d3-142">/App1/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="9a7d3-142">/app1/ifd/gps/{ushort=30}</span></span> |
| <span data-ttu-id="9a7d3-143">2</span><span class="sxs-lookup"><span data-stu-id="9a7d3-143">2</span></span>     | <span data-ttu-id="9a7d3-144">/XMP/EXIF: gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="9a7d3-144">/xmp/exif:gpsdifferential</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="9a7d3-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="9a7d3-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9a7d3-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="9a7d3-146">Read Paths</span></span>



| <span data-ttu-id="9a7d3-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9a7d3-147">Order</span></span> | <span data-ttu-id="9a7d3-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="9a7d3-148">Path</span></span>                          | <span data-ttu-id="9a7d3-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9a7d3-149">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9a7d3-150">1</span><span class="sxs-lookup"><span data-stu-id="9a7d3-150">1</span></span>     | <span data-ttu-id="9a7d3-151">/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="9a7d3-151">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="9a7d3-152">ushort</span><span class="sxs-lookup"><span data-stu-id="9a7d3-152">ushort</span></span>      |
| <span data-ttu-id="9a7d3-153">2</span><span class="sxs-lookup"><span data-stu-id="9a7d3-153">2</span></span>     | <span data-ttu-id="9a7d3-154">/IFD/XMP/EXIF: gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="9a7d3-154">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="9a7d3-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="9a7d3-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9a7d3-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="9a7d3-156">Write Paths</span></span>



| <span data-ttu-id="9a7d3-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9a7d3-157">Order</span></span> | <span data-ttu-id="9a7d3-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="9a7d3-158">Path</span></span>                          | <span data-ttu-id="9a7d3-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9a7d3-159">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9a7d3-160">1</span><span class="sxs-lookup"><span data-stu-id="9a7d3-160">1</span></span>     | <span data-ttu-id="9a7d3-161">/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="9a7d3-161">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="9a7d3-162">ushort</span><span class="sxs-lookup"><span data-stu-id="9a7d3-162">ushort</span></span>      |
| <span data-ttu-id="9a7d3-163">2</span><span class="sxs-lookup"><span data-stu-id="9a7d3-163">2</span></span>     | <span data-ttu-id="9a7d3-164">/IFD/XMP/EXIF: gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="9a7d3-164">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="9a7d3-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="9a7d3-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9a7d3-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="9a7d3-166">Remove Paths</span></span>



| <span data-ttu-id="9a7d3-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9a7d3-167">Order</span></span> | <span data-ttu-id="9a7d3-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="9a7d3-168">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="9a7d3-169">1</span><span class="sxs-lookup"><span data-stu-id="9a7d3-169">1</span></span>     | <span data-ttu-id="9a7d3-170">/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="9a7d3-170">/ifd/gps/{ushort=30}</span></span>          |
| <span data-ttu-id="9a7d3-171">2</span><span class="sxs-lookup"><span data-stu-id="9a7d3-171">2</span></span>     | <span data-ttu-id="9a7d3-172">/IFD/XMP/EXIF: gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="9a7d3-172">/ifd/xmp/exif:gpsdifferential</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9a7d3-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a7d3-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a7d3-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9a7d3-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a7d3-175">System. GPS. Differential</span><span class="sxs-lookup"><span data-stu-id="9a7d3-175">System.GPS.Differential</span></span>](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
