---
description: Die fotometadatenrichtlinie für die System. GPS. messremode-Eigenschaft.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: System. GPS. messremode Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9449ca9a7d1ee5ef213c37562392be2842a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959883"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a><span data-ttu-id="f2335-103">System. GPS. messremode Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f2335-103">System.GPS.MeasureMode Photo Metadata Policy</span></span>

<span data-ttu-id="f2335-104">Die fotometadatenrichtlinie für die [System. GPS. messremode](../properties/props-system-gps-measuremode.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f2335-104">The photo metadata policy for the [System.GPS.MeasureMode](../properties/props-system-gps-measuremode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f2335-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="f2335-105">PKEY</span></span>

<span data-ttu-id="f2335-106">Pkey \_ GPS \_ messremode</span><span class="sxs-lookup"><span data-stu-id="f2335-106">PKEY\_GPS\_MeasureMode</span></span>

### <a name="containers"></a><span data-ttu-id="f2335-107">Container</span><span class="sxs-lookup"><span data-stu-id="f2335-107">Containers</span></span>

<span data-ttu-id="f2335-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f2335-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f2335-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2335-109">Read-Only</span></span>

<span data-ttu-id="f2335-110">Nein</span><span class="sxs-lookup"><span data-stu-id="f2335-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f2335-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="f2335-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f2335-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="f2335-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="f2335-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="f2335-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="f2335-114">VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird ebenfalls akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="f2335-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f2335-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="f2335-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f2335-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="f2335-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="f2335-117">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f2335-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f2335-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="f2335-118">Read Paths</span></span>



| <span data-ttu-id="f2335-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f2335-119">Order</span></span> | <span data-ttu-id="f2335-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="f2335-120">Path</span></span>                      | <span data-ttu-id="f2335-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="f2335-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f2335-122">1</span><span class="sxs-lookup"><span data-stu-id="f2335-122">1</span></span>     | <span data-ttu-id="f2335-123">/App1/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="f2335-123">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="f2335-124">ascii</span><span class="sxs-lookup"><span data-stu-id="f2335-124">ascii</span></span>       |
| <span data-ttu-id="f2335-125">2</span><span class="sxs-lookup"><span data-stu-id="f2335-125">2</span></span>     | <span data-ttu-id="f2335-126">/XMP/EXIF: gpsmessremode</span><span class="sxs-lookup"><span data-stu-id="f2335-126">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="f2335-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="f2335-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f2335-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="f2335-128">Write Paths</span></span>



| <span data-ttu-id="f2335-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f2335-129">Order</span></span> | <span data-ttu-id="f2335-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="f2335-130">Path</span></span>                      | <span data-ttu-id="f2335-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="f2335-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f2335-132">1</span><span class="sxs-lookup"><span data-stu-id="f2335-132">1</span></span>     | <span data-ttu-id="f2335-133">/App1/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="f2335-133">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="f2335-134">ascii</span><span class="sxs-lookup"><span data-stu-id="f2335-134">ascii</span></span>       |
| <span data-ttu-id="f2335-135">2</span><span class="sxs-lookup"><span data-stu-id="f2335-135">2</span></span>     | <span data-ttu-id="f2335-136">/XMP/EXIF: gpsmessremode</span><span class="sxs-lookup"><span data-stu-id="f2335-136">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="f2335-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="f2335-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f2335-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="f2335-138">Remove Paths</span></span>



| <span data-ttu-id="f2335-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f2335-139">Order</span></span> | <span data-ttu-id="f2335-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="f2335-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="f2335-141">1</span><span class="sxs-lookup"><span data-stu-id="f2335-141">1</span></span>     | <span data-ttu-id="f2335-142">/App1/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="f2335-142">/app1/ifd/gps/{ushort=10}</span></span> |
| <span data-ttu-id="f2335-143">2</span><span class="sxs-lookup"><span data-stu-id="f2335-143">2</span></span>     | <span data-ttu-id="f2335-144">/XMP/EXIF: gpsmessremode</span><span class="sxs-lookup"><span data-stu-id="f2335-144">/xmp/exif:gpsmeasuremode</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="f2335-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f2335-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f2335-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="f2335-146">Read Paths</span></span>



| <span data-ttu-id="f2335-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f2335-147">Order</span></span> | <span data-ttu-id="f2335-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="f2335-148">Path</span></span>                         | <span data-ttu-id="f2335-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="f2335-149">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="f2335-150">1</span><span class="sxs-lookup"><span data-stu-id="f2335-150">1</span></span>     | <span data-ttu-id="f2335-151">/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="f2335-151">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="f2335-152">ascii</span><span class="sxs-lookup"><span data-stu-id="f2335-152">ascii</span></span>       |
| <span data-ttu-id="f2335-153">2</span><span class="sxs-lookup"><span data-stu-id="f2335-153">2</span></span>     | <span data-ttu-id="f2335-154">/IFD/XMP/EXIF: gpsmessremode</span><span class="sxs-lookup"><span data-stu-id="f2335-154">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="f2335-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="f2335-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f2335-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="f2335-156">Write Paths</span></span>



| <span data-ttu-id="f2335-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f2335-157">Order</span></span> | <span data-ttu-id="f2335-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="f2335-158">Path</span></span>                         | <span data-ttu-id="f2335-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="f2335-159">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="f2335-160">1</span><span class="sxs-lookup"><span data-stu-id="f2335-160">1</span></span>     | <span data-ttu-id="f2335-161">/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="f2335-161">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="f2335-162">ascii</span><span class="sxs-lookup"><span data-stu-id="f2335-162">ascii</span></span>       |
| <span data-ttu-id="f2335-163">2</span><span class="sxs-lookup"><span data-stu-id="f2335-163">2</span></span>     | <span data-ttu-id="f2335-164">/IFD/XMP/EXIF: gpsmessremode</span><span class="sxs-lookup"><span data-stu-id="f2335-164">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="f2335-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="f2335-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f2335-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="f2335-166">Remove Paths</span></span>



| <span data-ttu-id="f2335-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f2335-167">Order</span></span> | <span data-ttu-id="f2335-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="f2335-168">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="f2335-169">1</span><span class="sxs-lookup"><span data-stu-id="f2335-169">1</span></span>     | <span data-ttu-id="f2335-170">/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="f2335-170">/ifd/gps/{ushort=10}</span></span>         |
| <span data-ttu-id="f2335-171">2</span><span class="sxs-lookup"><span data-stu-id="f2335-171">2</span></span>     | <span data-ttu-id="f2335-172">/IFD/XMP/EXIF: gpsmessremode</span><span class="sxs-lookup"><span data-stu-id="f2335-172">/ifd/xmp/exif:gpsmeasuremode</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f2335-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2335-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2335-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2335-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2335-175">System. GPS. messremode</span><span class="sxs-lookup"><span data-stu-id="f2335-175">System.GPS.MeasureMode</span></span>](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
