---
description: Die fotometadatenrichtlinie für die System. Photo. Isospeed-Eigenschaft.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: System. Photo. Isospeed-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2988f774f70721ab1817ffaf605098ab1164316a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346599"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a><span data-ttu-id="39025-103">System. Photo. Isospeed-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="39025-103">System.Photo.ISOSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="39025-104">Die fotometadatenrichtlinie für die [System. Photo. Isospeed](../properties/props-system-photo-focallengthinfilm.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="39025-104">The photo metadata policy for the [System.Photo.ISOSpeed](../properties/props-system-photo-focallengthinfilm.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="39025-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="39025-105">PKEY</span></span>

<span data-ttu-id="39025-106">Pkey- \_ Foto- \_ Isospeed</span><span class="sxs-lookup"><span data-stu-id="39025-106">PKEY\_Photo\_ISOSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="39025-107">Container</span><span class="sxs-lookup"><span data-stu-id="39025-107">Containers</span></span>

<span data-ttu-id="39025-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="39025-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="39025-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39025-109">Read-Only</span></span>

<span data-ttu-id="39025-110">Nein</span><span class="sxs-lookup"><span data-stu-id="39025-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="39025-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="39025-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="39025-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="39025-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="39025-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="39025-113">Input Type</span></span>

<span data-ttu-id="39025-114">UShort</span><span class="sxs-lookup"><span data-stu-id="39025-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="39025-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="39025-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="39025-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="39025-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="39025-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="39025-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="39025-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="39025-118">Read Paths</span></span>



| <span data-ttu-id="39025-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="39025-119">Order</span></span> | <span data-ttu-id="39025-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="39025-120">Path</span></span>                                    | <span data-ttu-id="39025-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="39025-121">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="39025-122">1</span><span class="sxs-lookup"><span data-stu-id="39025-122">1</span></span>     | <span data-ttu-id="39025-123">/App1/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="39025-123">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="39025-124">ushort</span><span class="sxs-lookup"><span data-stu-id="39025-124">ushort</span></span>      |
| <span data-ttu-id="39025-125">2</span><span class="sxs-lookup"><span data-stu-id="39025-125">2</span></span>     | <span data-ttu-id="39025-126">/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="39025-126">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="39025-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="39025-127">unicode</span></span>     |
| <span data-ttu-id="39025-128">3</span><span class="sxs-lookup"><span data-stu-id="39025-128">3</span></span>     | <span data-ttu-id="39025-129">/XMP/EXIF: Isospeed</span><span class="sxs-lookup"><span data-stu-id="39025-129">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="39025-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="39025-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="39025-131">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="39025-131">Write Paths</span></span>



| <span data-ttu-id="39025-132">Auftrag</span><span class="sxs-lookup"><span data-stu-id="39025-132">Order</span></span> | <span data-ttu-id="39025-133">Pfad</span><span class="sxs-lookup"><span data-stu-id="39025-133">Path</span></span>                                    | <span data-ttu-id="39025-134">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="39025-134">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="39025-135">1</span><span class="sxs-lookup"><span data-stu-id="39025-135">1</span></span>     | <span data-ttu-id="39025-136">/App1/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="39025-136">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="39025-137">ushort</span><span class="sxs-lookup"><span data-stu-id="39025-137">ushort</span></span>      |
| <span data-ttu-id="39025-138">2</span><span class="sxs-lookup"><span data-stu-id="39025-138">2</span></span>     | <span data-ttu-id="39025-139">/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="39025-139">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="39025-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="39025-140">unicode</span></span>     |
| <span data-ttu-id="39025-141">3</span><span class="sxs-lookup"><span data-stu-id="39025-141">3</span></span>     | <span data-ttu-id="39025-142">/XMP/EXIF: Isospeed</span><span class="sxs-lookup"><span data-stu-id="39025-142">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="39025-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="39025-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="39025-144">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="39025-144">Remove Paths</span></span>



| <span data-ttu-id="39025-145">Auftrag</span><span class="sxs-lookup"><span data-stu-id="39025-145">Order</span></span> | <span data-ttu-id="39025-146">Pfad</span><span class="sxs-lookup"><span data-stu-id="39025-146">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="39025-147">1</span><span class="sxs-lookup"><span data-stu-id="39025-147">1</span></span>     | <span data-ttu-id="39025-148">/App1/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="39025-148">/app1/ifd/exif/{ushort=34855}</span></span>           |
| <span data-ttu-id="39025-149">2</span><span class="sxs-lookup"><span data-stu-id="39025-149">2</span></span>     | <span data-ttu-id="39025-150">/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="39025-150">/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="39025-151">3</span><span class="sxs-lookup"><span data-stu-id="39025-151">3</span></span>     | <span data-ttu-id="39025-152">/XMP/EXIF: Isospeed</span><span class="sxs-lookup"><span data-stu-id="39025-152">/xmp/exif:isospeed</span></span>                      |



 

### <a name="tiff-policies"></a><span data-ttu-id="39025-153">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="39025-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="39025-154">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="39025-154">Read Paths</span></span>



| <span data-ttu-id="39025-155">Auftrag</span><span class="sxs-lookup"><span data-stu-id="39025-155">Order</span></span> | <span data-ttu-id="39025-156">Pfad</span><span class="sxs-lookup"><span data-stu-id="39025-156">Path</span></span>                                        | <span data-ttu-id="39025-157">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="39025-157">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="39025-158">1</span><span class="sxs-lookup"><span data-stu-id="39025-158">1</span></span>     | <span data-ttu-id="39025-159">/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="39025-159">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="39025-160">ushort</span><span class="sxs-lookup"><span data-stu-id="39025-160">ushort</span></span>      |
| <span data-ttu-id="39025-161">2</span><span class="sxs-lookup"><span data-stu-id="39025-161">2</span></span>     | <span data-ttu-id="39025-162">/IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="39025-162">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="39025-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="39025-163">unicode</span></span>     |
| <span data-ttu-id="39025-164">3</span><span class="sxs-lookup"><span data-stu-id="39025-164">3</span></span>     | <span data-ttu-id="39025-165">/IFD/XMP/EXIF: Isospeed</span><span class="sxs-lookup"><span data-stu-id="39025-165">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="39025-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="39025-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="39025-167">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="39025-167">Write Paths</span></span>



| <span data-ttu-id="39025-168">Auftrag</span><span class="sxs-lookup"><span data-stu-id="39025-168">Order</span></span> | <span data-ttu-id="39025-169">Pfad</span><span class="sxs-lookup"><span data-stu-id="39025-169">Path</span></span>                                        | <span data-ttu-id="39025-170">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="39025-170">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="39025-171">1</span><span class="sxs-lookup"><span data-stu-id="39025-171">1</span></span>     | <span data-ttu-id="39025-172">/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="39025-172">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="39025-173">ushort</span><span class="sxs-lookup"><span data-stu-id="39025-173">ushort</span></span>      |
| <span data-ttu-id="39025-174">2</span><span class="sxs-lookup"><span data-stu-id="39025-174">2</span></span>     | <span data-ttu-id="39025-175">/IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="39025-175">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="39025-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="39025-176">unicode</span></span>     |
| <span data-ttu-id="39025-177">3</span><span class="sxs-lookup"><span data-stu-id="39025-177">3</span></span>     | <span data-ttu-id="39025-178">/IFD/XMP/EXIF: Isospeed</span><span class="sxs-lookup"><span data-stu-id="39025-178">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="39025-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="39025-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="39025-180">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="39025-180">Remove Paths</span></span>



| <span data-ttu-id="39025-181">Auftrag</span><span class="sxs-lookup"><span data-stu-id="39025-181">Order</span></span> | <span data-ttu-id="39025-182">Pfad</span><span class="sxs-lookup"><span data-stu-id="39025-182">Path</span></span>                                        |
|-------|---------------------------------------------|
| <span data-ttu-id="39025-183">1</span><span class="sxs-lookup"><span data-stu-id="39025-183">1</span></span>     | <span data-ttu-id="39025-184">/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="39025-184">/ifd/exif/{ushort=34855}</span></span>                    |
| <span data-ttu-id="39025-185">2</span><span class="sxs-lookup"><span data-stu-id="39025-185">2</span></span>     | <span data-ttu-id="39025-186">/IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="39025-186">/ifd/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="39025-187">3</span><span class="sxs-lookup"><span data-stu-id="39025-187">3</span></span>     | <span data-ttu-id="39025-188">/IFD/XMP/EXIF: Isospeed</span><span class="sxs-lookup"><span data-stu-id="39025-188">/ifd/xmp/exif:isospeed</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="39025-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39025-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="39025-190">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39025-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39025-191">System. Photo. Isospeed</span><span class="sxs-lookup"><span data-stu-id="39025-191">System.Photo.ISOSpeed</span></span>](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
