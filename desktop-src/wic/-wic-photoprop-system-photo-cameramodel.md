---
description: Die fotometadatenrichtlinie für die System. Photo. CameraModel-Eigenschaft.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: System. Photo. CameraModel Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf9cbb2906f15d02e8d72219862c607d0f515a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868004"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a><span data-ttu-id="e2726-103">System. Photo. CameraModel Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e2726-103">System.Photo.CameraModel Photo Metadata Policy</span></span>

<span data-ttu-id="e2726-104">Die fotometadatenrichtlinie für die [System. Photo. CameraModel](../properties/props-system-photo-cameramodel.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e2726-104">The photo metadata policy for the [System.Photo.CameraModel](../properties/props-system-photo-cameramodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e2726-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="e2726-105">PKEY</span></span>

<span data-ttu-id="e2726-106">Pkey- \_ Foto \_ CameraModel</span><span class="sxs-lookup"><span data-stu-id="e2726-106">PKEY\_Photo\_CameraModel</span></span>

### <a name="containers"></a><span data-ttu-id="e2726-107">Container</span><span class="sxs-lookup"><span data-stu-id="e2726-107">Containers</span></span>

<span data-ttu-id="e2726-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e2726-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e2726-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2726-109">Read-Only</span></span>

<span data-ttu-id="e2726-110">Nein</span><span class="sxs-lookup"><span data-stu-id="e2726-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e2726-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="e2726-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e2726-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e2726-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="e2726-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="e2726-113">Input Type</span></span>

<span data-ttu-id="e2726-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e2726-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e2726-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="e2726-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e2726-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="e2726-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e2726-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e2726-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e2726-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="e2726-118">Read Paths</span></span>



| <span data-ttu-id="e2726-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e2726-119">Order</span></span> | <span data-ttu-id="e2726-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="e2726-120">Path</span></span>                   | <span data-ttu-id="e2726-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="e2726-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="e2726-122">1</span><span class="sxs-lookup"><span data-stu-id="e2726-122">1</span></span>     | <span data-ttu-id="e2726-123">/App1/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="e2726-123">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="e2726-124">ascii</span><span class="sxs-lookup"><span data-stu-id="e2726-124">ascii</span></span>       |
| <span data-ttu-id="e2726-125">2</span><span class="sxs-lookup"><span data-stu-id="e2726-125">2</span></span>     | <span data-ttu-id="e2726-126">/XMP/TIFF: Modell</span><span class="sxs-lookup"><span data-stu-id="e2726-126">/xmp/tiff:Model</span></span>        | <span data-ttu-id="e2726-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="e2726-127">unicode</span></span>     |
| <span data-ttu-id="e2726-128">3</span><span class="sxs-lookup"><span data-stu-id="e2726-128">3</span></span>     | <span data-ttu-id="e2726-129">/XMP/TIFF: Modell</span><span class="sxs-lookup"><span data-stu-id="e2726-129">/xmp/tiff:model</span></span>        | <span data-ttu-id="e2726-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="e2726-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e2726-131">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="e2726-131">Write Paths</span></span>



| <span data-ttu-id="e2726-132">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e2726-132">Order</span></span> | <span data-ttu-id="e2726-133">Pfad</span><span class="sxs-lookup"><span data-stu-id="e2726-133">Path</span></span>                   | <span data-ttu-id="e2726-134">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="e2726-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="e2726-135">1</span><span class="sxs-lookup"><span data-stu-id="e2726-135">1</span></span>     | <span data-ttu-id="e2726-136">/App1/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="e2726-136">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="e2726-137">ascii</span><span class="sxs-lookup"><span data-stu-id="e2726-137">ascii</span></span>       |
| <span data-ttu-id="e2726-138">2</span><span class="sxs-lookup"><span data-stu-id="e2726-138">2</span></span>     | <span data-ttu-id="e2726-139">/XMP/TIFF: Modell</span><span class="sxs-lookup"><span data-stu-id="e2726-139">/xmp/tiff:Model</span></span>        | <span data-ttu-id="e2726-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="e2726-140">unicode</span></span>     |
| <span data-ttu-id="e2726-141">3</span><span class="sxs-lookup"><span data-stu-id="e2726-141">3</span></span>     | <span data-ttu-id="e2726-142">/XMP/TIFF: Modell</span><span class="sxs-lookup"><span data-stu-id="e2726-142">/xmp/tiff:model</span></span>        | <span data-ttu-id="e2726-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="e2726-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e2726-144">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="e2726-144">Remove Paths</span></span>



| <span data-ttu-id="e2726-145">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e2726-145">Order</span></span> | <span data-ttu-id="e2726-146">Pfad</span><span class="sxs-lookup"><span data-stu-id="e2726-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="e2726-147">1</span><span class="sxs-lookup"><span data-stu-id="e2726-147">1</span></span>     | <span data-ttu-id="e2726-148">/App1/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="e2726-148">/app1/ifd/{ushort=272}</span></span> |
| <span data-ttu-id="e2726-149">2</span><span class="sxs-lookup"><span data-stu-id="e2726-149">2</span></span>     | <span data-ttu-id="e2726-150">/XMP/TIFF: Modell</span><span class="sxs-lookup"><span data-stu-id="e2726-150">/xmp/tiff:Model</span></span>        |
| <span data-ttu-id="e2726-151">3</span><span class="sxs-lookup"><span data-stu-id="e2726-151">3</span></span>     | <span data-ttu-id="e2726-152">/XMP/TIFF: Modell</span><span class="sxs-lookup"><span data-stu-id="e2726-152">/xmp/tiff:model</span></span>        |



 

### <a name="tiff-policy"></a><span data-ttu-id="e2726-153">TIFF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e2726-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e2726-154">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="e2726-154">Read Paths</span></span>



| <span data-ttu-id="e2726-155">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e2726-155">Order</span></span> | <span data-ttu-id="e2726-156">Pfad</span><span class="sxs-lookup"><span data-stu-id="e2726-156">Path</span></span>                | <span data-ttu-id="e2726-157">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="e2726-157">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="e2726-158">1</span><span class="sxs-lookup"><span data-stu-id="e2726-158">1</span></span>     | <span data-ttu-id="e2726-159">/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="e2726-159">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="e2726-160">ascii</span><span class="sxs-lookup"><span data-stu-id="e2726-160">ascii</span></span>       |
| <span data-ttu-id="e2726-161">2</span><span class="sxs-lookup"><span data-stu-id="e2726-161">2</span></span>     | <span data-ttu-id="e2726-162">/IFD/XMP/TIFF: Modell</span><span class="sxs-lookup"><span data-stu-id="e2726-162">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="e2726-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="e2726-163">unicode</span></span>     |
| <span data-ttu-id="e2726-164">3</span><span class="sxs-lookup"><span data-stu-id="e2726-164">3</span></span>     | <span data-ttu-id="e2726-165">/IFD/XMP/TIFF: Modell</span><span class="sxs-lookup"><span data-stu-id="e2726-165">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="e2726-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="e2726-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e2726-167">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="e2726-167">Write Paths</span></span>



| <span data-ttu-id="e2726-168">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e2726-168">Order</span></span> | <span data-ttu-id="e2726-169">Pfad</span><span class="sxs-lookup"><span data-stu-id="e2726-169">Path</span></span>                | <span data-ttu-id="e2726-170">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="e2726-170">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="e2726-171">1</span><span class="sxs-lookup"><span data-stu-id="e2726-171">1</span></span>     | <span data-ttu-id="e2726-172">/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="e2726-172">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="e2726-173">ascii</span><span class="sxs-lookup"><span data-stu-id="e2726-173">ascii</span></span>       |
| <span data-ttu-id="e2726-174">2</span><span class="sxs-lookup"><span data-stu-id="e2726-174">2</span></span>     | <span data-ttu-id="e2726-175">/IFD/XMP/TIFF: Modell</span><span class="sxs-lookup"><span data-stu-id="e2726-175">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="e2726-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="e2726-176">unicode</span></span>     |
| <span data-ttu-id="e2726-177">3</span><span class="sxs-lookup"><span data-stu-id="e2726-177">3</span></span>     | <span data-ttu-id="e2726-178">/IFD/XMP/TIFF: Modell</span><span class="sxs-lookup"><span data-stu-id="e2726-178">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="e2726-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="e2726-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e2726-180">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="e2726-180">Remove Paths</span></span>



| <span data-ttu-id="e2726-181">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e2726-181">Order</span></span> | <span data-ttu-id="e2726-182">Pfad</span><span class="sxs-lookup"><span data-stu-id="e2726-182">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="e2726-183">1</span><span class="sxs-lookup"><span data-stu-id="e2726-183">1</span></span>     | <span data-ttu-id="e2726-184">/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="e2726-184">/ifd/{ushort=272}</span></span>   |
| <span data-ttu-id="e2726-185">2</span><span class="sxs-lookup"><span data-stu-id="e2726-185">2</span></span>     | <span data-ttu-id="e2726-186">/IFD/XMP/TIFF: Modell</span><span class="sxs-lookup"><span data-stu-id="e2726-186">/ifd/xmp/tiff:Model</span></span> |
| <span data-ttu-id="e2726-187">3</span><span class="sxs-lookup"><span data-stu-id="e2726-187">3</span></span>     | <span data-ttu-id="e2726-188">/IFD/XMP/TIFF: Modell</span><span class="sxs-lookup"><span data-stu-id="e2726-188">/ifd/xmp/tiff:model</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e2726-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2726-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2726-190">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2726-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2726-191">System. Photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="e2726-191">System.Photo.CameraModel</span></span>](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
