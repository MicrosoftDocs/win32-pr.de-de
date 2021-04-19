---
description: Die fotometadatenrichtlinie für die System. Photo. cameramanufakturer-Eigenschaft.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: System. Photo. cameramanufakturer Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1d2765b6c787b7d7ad421300f1c3492669830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364192"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a><span data-ttu-id="f1400-103">System. Photo. cameramanufakturer Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f1400-103">System.Photo.CameraManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="f1400-104">Die fotometadatenrichtlinie für die [System. Photo. cameramanufakturer](../properties/props-system-photo-cameramanufacturer.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f1400-104">The photo metadata policy for the [System.Photo.CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f1400-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="f1400-105">PKEY</span></span>

<span data-ttu-id="f1400-106">Pkey- \_ Foto \_ cameramanufakturer</span><span class="sxs-lookup"><span data-stu-id="f1400-106">PKEY\_Photo\_CameraManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="f1400-107">Container</span><span class="sxs-lookup"><span data-stu-id="f1400-107">Containers</span></span>

<span data-ttu-id="f1400-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f1400-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f1400-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1400-109">Read-Only</span></span>

<span data-ttu-id="f1400-110">Nein</span><span class="sxs-lookup"><span data-stu-id="f1400-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f1400-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="f1400-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f1400-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="f1400-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="f1400-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="f1400-113">Input Type</span></span>

<span data-ttu-id="f1400-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f1400-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f1400-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="f1400-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f1400-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="f1400-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="f1400-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f1400-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f1400-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="f1400-118">Read Paths</span></span>



| <span data-ttu-id="f1400-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f1400-119">Order</span></span> | <span data-ttu-id="f1400-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="f1400-120">Path</span></span>                   | <span data-ttu-id="f1400-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="f1400-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="f1400-122">1</span><span class="sxs-lookup"><span data-stu-id="f1400-122">1</span></span>     | <span data-ttu-id="f1400-123">/App1/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="f1400-123">/app1/ifd/{ushort=271}</span></span> | <span data-ttu-id="f1400-124">ascii</span><span class="sxs-lookup"><span data-stu-id="f1400-124">ascii</span></span>       |
| <span data-ttu-id="f1400-125">2</span><span class="sxs-lookup"><span data-stu-id="f1400-125">2</span></span>     | <span data-ttu-id="f1400-126">/XMP/TIFF: Erstellen</span><span class="sxs-lookup"><span data-stu-id="f1400-126">/xmp/tiff:Make</span></span>         | <span data-ttu-id="f1400-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="f1400-127">unicode</span></span>     |
| <span data-ttu-id="f1400-128">3</span><span class="sxs-lookup"><span data-stu-id="f1400-128">3</span></span>     | <span data-ttu-id="f1400-129">/XMP/TIFF: Erstellen</span><span class="sxs-lookup"><span data-stu-id="f1400-129">/xmp/tiff:make</span></span>         | <span data-ttu-id="f1400-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="f1400-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f1400-131">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="f1400-131">Write Paths</span></span>



| <span data-ttu-id="f1400-132">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f1400-132">Order</span></span> | <span data-ttu-id="f1400-133">Pfad</span><span class="sxs-lookup"><span data-stu-id="f1400-133">Path</span></span>                   | <span data-ttu-id="f1400-134">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="f1400-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="f1400-135">1</span><span class="sxs-lookup"><span data-stu-id="f1400-135">1</span></span>     | <span data-ttu-id="f1400-136">/App1/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="f1400-136">/app1/ifd/{ushort=271}</span></span> | <span data-ttu-id="f1400-137">ascii</span><span class="sxs-lookup"><span data-stu-id="f1400-137">ascii</span></span>       |
| <span data-ttu-id="f1400-138">2</span><span class="sxs-lookup"><span data-stu-id="f1400-138">2</span></span>     | <span data-ttu-id="f1400-139">/XMP/TIFF: Erstellen</span><span class="sxs-lookup"><span data-stu-id="f1400-139">/xmp/tiff:Make</span></span>         | <span data-ttu-id="f1400-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="f1400-140">unicode</span></span>     |
| <span data-ttu-id="f1400-141">3</span><span class="sxs-lookup"><span data-stu-id="f1400-141">3</span></span>     | <span data-ttu-id="f1400-142">/XMP/TIFF: Erstellen</span><span class="sxs-lookup"><span data-stu-id="f1400-142">/xmp/tiff:make</span></span>         | <span data-ttu-id="f1400-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="f1400-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f1400-144">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="f1400-144">Remove Paths</span></span>



| <span data-ttu-id="f1400-145">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f1400-145">Order</span></span> | <span data-ttu-id="f1400-146">Pfad</span><span class="sxs-lookup"><span data-stu-id="f1400-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="f1400-147">1</span><span class="sxs-lookup"><span data-stu-id="f1400-147">1</span></span>     | <span data-ttu-id="f1400-148">/App1/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="f1400-148">/app1/ifd/{ushort=271}</span></span> |
| <span data-ttu-id="f1400-149">2</span><span class="sxs-lookup"><span data-stu-id="f1400-149">2</span></span>     | <span data-ttu-id="f1400-150">/XMP/TIFF: Erstellen</span><span class="sxs-lookup"><span data-stu-id="f1400-150">/xmp/tiff:Make</span></span>         |
| <span data-ttu-id="f1400-151">3</span><span class="sxs-lookup"><span data-stu-id="f1400-151">3</span></span>     | <span data-ttu-id="f1400-152">/XMP/TIFF: Erstellen</span><span class="sxs-lookup"><span data-stu-id="f1400-152">/xmp/tiff:make</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="f1400-153">TIFF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f1400-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f1400-154">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="f1400-154">Read Paths</span></span>



| <span data-ttu-id="f1400-155">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f1400-155">Order</span></span> | <span data-ttu-id="f1400-156">Pfad</span><span class="sxs-lookup"><span data-stu-id="f1400-156">Path</span></span>               | <span data-ttu-id="f1400-157">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="f1400-157">Disk Format</span></span> |
|-------|--------------------|-------------|
| <span data-ttu-id="f1400-158">1</span><span class="sxs-lookup"><span data-stu-id="f1400-158">1</span></span>     | <span data-ttu-id="f1400-159">/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="f1400-159">/ifd/{ushort=271}</span></span>  | <span data-ttu-id="f1400-160">ascii</span><span class="sxs-lookup"><span data-stu-id="f1400-160">ascii</span></span>       |
| <span data-ttu-id="f1400-161">2</span><span class="sxs-lookup"><span data-stu-id="f1400-161">2</span></span>     | <span data-ttu-id="f1400-162">/IFD/XMP/TIFF: Erstellen</span><span class="sxs-lookup"><span data-stu-id="f1400-162">/ifd/xmp/tiff:Make</span></span> | <span data-ttu-id="f1400-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="f1400-163">unicode</span></span>     |
| <span data-ttu-id="f1400-164">3</span><span class="sxs-lookup"><span data-stu-id="f1400-164">3</span></span>     | <span data-ttu-id="f1400-165">/IFD/XMP/TIFF: Erstellen</span><span class="sxs-lookup"><span data-stu-id="f1400-165">/ifd/xmp/tiff:make</span></span> | <span data-ttu-id="f1400-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="f1400-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f1400-167">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="f1400-167">Write Paths</span></span>



| <span data-ttu-id="f1400-168">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f1400-168">Order</span></span> | <span data-ttu-id="f1400-169">Pfad</span><span class="sxs-lookup"><span data-stu-id="f1400-169">Path</span></span>               | <span data-ttu-id="f1400-170">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="f1400-170">Disk Format</span></span> |
|-------|--------------------|-------------|
| <span data-ttu-id="f1400-171">1</span><span class="sxs-lookup"><span data-stu-id="f1400-171">1</span></span>     | <span data-ttu-id="f1400-172">/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="f1400-172">/ifd/{ushort=271}</span></span>  | <span data-ttu-id="f1400-173">ascii</span><span class="sxs-lookup"><span data-stu-id="f1400-173">ascii</span></span>       |
| <span data-ttu-id="f1400-174">2</span><span class="sxs-lookup"><span data-stu-id="f1400-174">2</span></span>     | <span data-ttu-id="f1400-175">/IFD/XMP/TIFF: Erstellen</span><span class="sxs-lookup"><span data-stu-id="f1400-175">/ifd/xmp/tiff:Make</span></span> | <span data-ttu-id="f1400-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="f1400-176">unicode</span></span>     |
| <span data-ttu-id="f1400-177">3</span><span class="sxs-lookup"><span data-stu-id="f1400-177">3</span></span>     | <span data-ttu-id="f1400-178">/IFD/XMP/TIFF: Erstellen</span><span class="sxs-lookup"><span data-stu-id="f1400-178">/ifd/xmp/tiff:make</span></span> | <span data-ttu-id="f1400-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="f1400-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f1400-180">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="f1400-180">Remove Paths</span></span>



| <span data-ttu-id="f1400-181">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f1400-181">Order</span></span> | <span data-ttu-id="f1400-182">Pfad</span><span class="sxs-lookup"><span data-stu-id="f1400-182">Path</span></span>               |
|-------|--------------------|
| <span data-ttu-id="f1400-183">1</span><span class="sxs-lookup"><span data-stu-id="f1400-183">1</span></span>     | <span data-ttu-id="f1400-184">/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="f1400-184">/ifd/{ushort=271}</span></span>  |
| <span data-ttu-id="f1400-185">2</span><span class="sxs-lookup"><span data-stu-id="f1400-185">2</span></span>     | <span data-ttu-id="f1400-186">/IFD/XMP/TIFF: Erstellen</span><span class="sxs-lookup"><span data-stu-id="f1400-186">/ifd/xmp/tiff:Make</span></span> |
| <span data-ttu-id="f1400-187">3</span><span class="sxs-lookup"><span data-stu-id="f1400-187">3</span></span>     | <span data-ttu-id="f1400-188">/IFD/XMP/TIFF: Erstellen</span><span class="sxs-lookup"><span data-stu-id="f1400-188">/ifd/xmp/tiff:make</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f1400-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1400-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1400-190">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f1400-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1400-191">System. Photo. cameramanufakturer</span><span class="sxs-lookup"><span data-stu-id="f1400-191">System.Photo.CameraManufacturer</span></span>](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
