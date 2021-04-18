---
description: Die fotometadatenrichtlinie für die System. GPS. Status-Eigenschaft.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: System. GPS. Status Photo-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac08139a267052f8d6dd3dc463e2a2768309a41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358936"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a><span data-ttu-id="fb986-103">System. GPS. Status Photo-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="fb986-103">System.GPS.Status Photo Metadata Policy</span></span>

<span data-ttu-id="fb986-104">Die fotometadatenrichtlinie für die [System. GPS. Status](../properties/props-system-gps-status.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="fb986-104">The photo metadata policy for the [System.GPS.Status](../properties/props-system-gps-status.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="fb986-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="fb986-105">PKEY</span></span>

<span data-ttu-id="fb986-106">Pkey \_ GPS- \_ Status</span><span class="sxs-lookup"><span data-stu-id="fb986-106">PKEY\_GPS\_Status</span></span>

### <a name="containers"></a><span data-ttu-id="fb986-107">Container</span><span class="sxs-lookup"><span data-stu-id="fb986-107">Containers</span></span>

<span data-ttu-id="fb986-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="fb986-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="fb986-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb986-109">Read-Only</span></span>

<span data-ttu-id="fb986-110">Nein</span><span class="sxs-lookup"><span data-stu-id="fb986-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="fb986-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="fb986-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="fb986-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="fb986-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="fb986-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="fb986-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="fb986-114">VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird ebenfalls akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="fb986-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="fb986-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="fb986-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="fb986-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="fb986-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="fb986-117">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="fb986-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="fb986-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="fb986-118">Read Paths</span></span>



| <span data-ttu-id="fb986-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fb986-119">Order</span></span> | <span data-ttu-id="fb986-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="fb986-120">Path</span></span>                     | <span data-ttu-id="fb986-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fb986-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="fb986-122">1</span><span class="sxs-lookup"><span data-stu-id="fb986-122">1</span></span>     | <span data-ttu-id="fb986-123">/App1/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="fb986-123">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="fb986-124">ascii</span><span class="sxs-lookup"><span data-stu-id="fb986-124">ascii</span></span>       |
| <span data-ttu-id="fb986-125">2</span><span class="sxs-lookup"><span data-stu-id="fb986-125">2</span></span>     | <span data-ttu-id="fb986-126">/XMP/EXIF: gpsstatus</span><span class="sxs-lookup"><span data-stu-id="fb986-126">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="fb986-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="fb986-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="fb986-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="fb986-128">Write Paths</span></span>



| <span data-ttu-id="fb986-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fb986-129">Order</span></span> | <span data-ttu-id="fb986-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="fb986-130">Path</span></span>                     | <span data-ttu-id="fb986-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fb986-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="fb986-132">1</span><span class="sxs-lookup"><span data-stu-id="fb986-132">1</span></span>     | <span data-ttu-id="fb986-133">/App1/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="fb986-133">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="fb986-134">ascii</span><span class="sxs-lookup"><span data-stu-id="fb986-134">ascii</span></span>       |
| <span data-ttu-id="fb986-135">2</span><span class="sxs-lookup"><span data-stu-id="fb986-135">2</span></span>     | <span data-ttu-id="fb986-136">/XMP/EXIF: gpsstatus</span><span class="sxs-lookup"><span data-stu-id="fb986-136">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="fb986-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="fb986-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="fb986-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="fb986-138">Remove Paths</span></span>



| <span data-ttu-id="fb986-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fb986-139">Order</span></span> | <span data-ttu-id="fb986-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="fb986-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="fb986-141">1</span><span class="sxs-lookup"><span data-stu-id="fb986-141">1</span></span>     | <span data-ttu-id="fb986-142">/App1/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="fb986-142">/app1/ifd/gps/{ushort=9}</span></span> |
| <span data-ttu-id="fb986-143">2</span><span class="sxs-lookup"><span data-stu-id="fb986-143">2</span></span>     | <span data-ttu-id="fb986-144">/XMP/EXIF: gpsstatus</span><span class="sxs-lookup"><span data-stu-id="fb986-144">/xmp/exif:gpsstatus</span></span>      |



 

### <a name="tiff-policies"></a><span data-ttu-id="fb986-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="fb986-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="fb986-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="fb986-146">Read Paths</span></span>



| <span data-ttu-id="fb986-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fb986-147">Order</span></span> | <span data-ttu-id="fb986-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="fb986-148">Path</span></span>                    | <span data-ttu-id="fb986-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fb986-149">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="fb986-150">1</span><span class="sxs-lookup"><span data-stu-id="fb986-150">1</span></span>     | <span data-ttu-id="fb986-151">/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="fb986-151">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="fb986-152">ascii</span><span class="sxs-lookup"><span data-stu-id="fb986-152">ascii</span></span>       |
| <span data-ttu-id="fb986-153">2</span><span class="sxs-lookup"><span data-stu-id="fb986-153">2</span></span>     | <span data-ttu-id="fb986-154">/IFD/XMP/EXIF: gpsstatus</span><span class="sxs-lookup"><span data-stu-id="fb986-154">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="fb986-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="fb986-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="fb986-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="fb986-156">Write Paths</span></span>



| <span data-ttu-id="fb986-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fb986-157">Order</span></span> | <span data-ttu-id="fb986-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="fb986-158">Path</span></span>                    | <span data-ttu-id="fb986-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fb986-159">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="fb986-160">1</span><span class="sxs-lookup"><span data-stu-id="fb986-160">1</span></span>     | <span data-ttu-id="fb986-161">/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="fb986-161">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="fb986-162">ascii</span><span class="sxs-lookup"><span data-stu-id="fb986-162">ascii</span></span>       |
| <span data-ttu-id="fb986-163">2</span><span class="sxs-lookup"><span data-stu-id="fb986-163">2</span></span>     | <span data-ttu-id="fb986-164">/IFD/XMP/EXIF: gpsstatus</span><span class="sxs-lookup"><span data-stu-id="fb986-164">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="fb986-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="fb986-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="fb986-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="fb986-166">Remove Paths</span></span>



| <span data-ttu-id="fb986-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fb986-167">Order</span></span> | <span data-ttu-id="fb986-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="fb986-168">Path</span></span>                    |
|-------|-------------------------|
| <span data-ttu-id="fb986-169">1</span><span class="sxs-lookup"><span data-stu-id="fb986-169">1</span></span>     | <span data-ttu-id="fb986-170">/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="fb986-170">/ifd/gps/{ushort=9}</span></span>     |
| <span data-ttu-id="fb986-171">2</span><span class="sxs-lookup"><span data-stu-id="fb986-171">2</span></span>     | <span data-ttu-id="fb986-172">/IFD/XMP/EXIF: gpsstatus</span><span class="sxs-lookup"><span data-stu-id="fb986-172">/ifd/xmp/exif:gpsstatus</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fb986-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb986-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb986-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fb986-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb986-175">System. GPS. Status</span><span class="sxs-lookup"><span data-stu-id="fb986-175">System.GPS.Status</span></span>](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
