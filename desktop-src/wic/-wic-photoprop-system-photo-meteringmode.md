---
description: Die fotometadatenrichtlinie für die System. Photo. meteringmode-Eigenschaft.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: System. Photo. meteringmode Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a4443521c84113e4e2a6f4c2b9b2b3f822ae90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373217"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a><span data-ttu-id="1bb6e-103">System. Photo. meteringmode Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="1bb6e-103">System.Photo.MeteringMode Photo Metadata Policy</span></span>

<span data-ttu-id="1bb6e-104">Die fotometadatenrichtlinie für die [System. Photo. meteringmode](../properties/props-system-photo-meteringmode.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1bb6e-104">The photo metadata policy for the [System.Photo.MeteringMode](../properties/props-system-photo-meteringmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1bb6e-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="1bb6e-105">PKEY</span></span>

<span data-ttu-id="1bb6e-106">Pkey- \_ Foto ( \_ meteringmode)</span><span class="sxs-lookup"><span data-stu-id="1bb6e-106">PKEY\_Photo\_MeteringMode</span></span>

### <a name="containers"></a><span data-ttu-id="1bb6e-107">Container</span><span class="sxs-lookup"><span data-stu-id="1bb6e-107">Containers</span></span>

<span data-ttu-id="1bb6e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1bb6e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1bb6e-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1bb6e-109">Read-Only</span></span>

<span data-ttu-id="1bb6e-110">Nein</span><span class="sxs-lookup"><span data-stu-id="1bb6e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1bb6e-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="1bb6e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1bb6e-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="1bb6e-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="1bb6e-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="1bb6e-113">Input Type</span></span>

<span data-ttu-id="1bb6e-114">UShort</span><span class="sxs-lookup"><span data-stu-id="1bb6e-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1bb6e-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="1bb6e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="1bb6e-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="1bb6e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="1bb6e-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="1bb6e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1bb6e-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="1bb6e-118">Read Paths</span></span>



| <span data-ttu-id="1bb6e-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1bb6e-119">Order</span></span> | <span data-ttu-id="1bb6e-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="1bb6e-120">Path</span></span>                          | <span data-ttu-id="1bb6e-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="1bb6e-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1bb6e-122">1</span><span class="sxs-lookup"><span data-stu-id="1bb6e-122">1</span></span>     | <span data-ttu-id="1bb6e-123">/App1/IFD/EXIF/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="1bb6e-123">/app1/ifd/exif/{ushort=37383}</span></span> | <span data-ttu-id="1bb6e-124">ushort</span><span class="sxs-lookup"><span data-stu-id="1bb6e-124">ushort</span></span>      |
| <span data-ttu-id="1bb6e-125">2</span><span class="sxs-lookup"><span data-stu-id="1bb6e-125">2</span></span>     | <span data-ttu-id="1bb6e-126">/XMP/EXIF: meteringmode</span><span class="sxs-lookup"><span data-stu-id="1bb6e-126">/xmp/exif:MeteringMode</span></span>        | <span data-ttu-id="1bb6e-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="1bb6e-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1bb6e-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="1bb6e-128">Write Paths</span></span>



| <span data-ttu-id="1bb6e-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1bb6e-129">Order</span></span> | <span data-ttu-id="1bb6e-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="1bb6e-130">Path</span></span>                          | <span data-ttu-id="1bb6e-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="1bb6e-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1bb6e-132">1</span><span class="sxs-lookup"><span data-stu-id="1bb6e-132">1</span></span>     | <span data-ttu-id="1bb6e-133">/App1/IFD/EXIF/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="1bb6e-133">/app1/ifd/exif/{ushort=37383}</span></span> | <span data-ttu-id="1bb6e-134">ushort</span><span class="sxs-lookup"><span data-stu-id="1bb6e-134">ushort</span></span>      |
| <span data-ttu-id="1bb6e-135">2</span><span class="sxs-lookup"><span data-stu-id="1bb6e-135">2</span></span>     | <span data-ttu-id="1bb6e-136">/XMP/EXIF: meteringmode</span><span class="sxs-lookup"><span data-stu-id="1bb6e-136">/xmp/exif:MeteringMode</span></span>        | <span data-ttu-id="1bb6e-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="1bb6e-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1bb6e-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="1bb6e-138">Remove Paths</span></span>



| <span data-ttu-id="1bb6e-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1bb6e-139">Order</span></span> | <span data-ttu-id="1bb6e-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="1bb6e-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="1bb6e-141">1</span><span class="sxs-lookup"><span data-stu-id="1bb6e-141">1</span></span>     | <span data-ttu-id="1bb6e-142">/App1/IFD/EXIF/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="1bb6e-142">/app1/ifd/exif/{ushort=37383}</span></span> |
| <span data-ttu-id="1bb6e-143">2</span><span class="sxs-lookup"><span data-stu-id="1bb6e-143">2</span></span>     | <span data-ttu-id="1bb6e-144">/XMP/EXIF: meteringmode</span><span class="sxs-lookup"><span data-stu-id="1bb6e-144">/xmp/exif:meteringmode</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="1bb6e-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="1bb6e-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1bb6e-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="1bb6e-146">Read Paths</span></span>



| <span data-ttu-id="1bb6e-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1bb6e-147">Order</span></span> | <span data-ttu-id="1bb6e-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="1bb6e-148">Path</span></span>                       | <span data-ttu-id="1bb6e-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="1bb6e-149">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="1bb6e-150">1</span><span class="sxs-lookup"><span data-stu-id="1bb6e-150">1</span></span>     | <span data-ttu-id="1bb6e-151">/IFD/EXIF/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="1bb6e-151">/ifd/exif/{ushort=37383}</span></span>   | <span data-ttu-id="1bb6e-152">ushort</span><span class="sxs-lookup"><span data-stu-id="1bb6e-152">ushort</span></span>      |
| <span data-ttu-id="1bb6e-153">2</span><span class="sxs-lookup"><span data-stu-id="1bb6e-153">2</span></span>     | <span data-ttu-id="1bb6e-154">/IFD/XMP/EXIF: meteringmode</span><span class="sxs-lookup"><span data-stu-id="1bb6e-154">/ifd/xmp/exif:MeteringMode</span></span> | <span data-ttu-id="1bb6e-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="1bb6e-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1bb6e-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="1bb6e-156">Write Paths</span></span>



| <span data-ttu-id="1bb6e-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1bb6e-157">Order</span></span> | <span data-ttu-id="1bb6e-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="1bb6e-158">Path</span></span>                       | <span data-ttu-id="1bb6e-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="1bb6e-159">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="1bb6e-160">1</span><span class="sxs-lookup"><span data-stu-id="1bb6e-160">1</span></span>     | <span data-ttu-id="1bb6e-161">/IFD/EXIF/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="1bb6e-161">/ifd/exif/{ushort=37383}</span></span>   | <span data-ttu-id="1bb6e-162">ushort</span><span class="sxs-lookup"><span data-stu-id="1bb6e-162">ushort</span></span>      |
| <span data-ttu-id="1bb6e-163">2</span><span class="sxs-lookup"><span data-stu-id="1bb6e-163">2</span></span>     | <span data-ttu-id="1bb6e-164">/IFD/XMP/EXIF: meteringmode</span><span class="sxs-lookup"><span data-stu-id="1bb6e-164">/ifd/xmp/exif:MeteringMode</span></span> | <span data-ttu-id="1bb6e-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="1bb6e-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1bb6e-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="1bb6e-166">Remove Paths</span></span>



| <span data-ttu-id="1bb6e-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1bb6e-167">Order</span></span> | <span data-ttu-id="1bb6e-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="1bb6e-168">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="1bb6e-169">1</span><span class="sxs-lookup"><span data-stu-id="1bb6e-169">1</span></span>     | <span data-ttu-id="1bb6e-170">/IFD/EXIF/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="1bb6e-170">/ifd/exif/{ushort=37383}</span></span>   |
| <span data-ttu-id="1bb6e-171">2</span><span class="sxs-lookup"><span data-stu-id="1bb6e-171">2</span></span>     | <span data-ttu-id="1bb6e-172">/IFD/XMP/EXIF: meteringmode</span><span class="sxs-lookup"><span data-stu-id="1bb6e-172">/ifd/xmp/exif:meteringmode</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1bb6e-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1bb6e-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bb6e-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1bb6e-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bb6e-175">System. Photo. meteringmode</span><span class="sxs-lookup"><span data-stu-id="1bb6e-175">System.Photo.MeteringMode</span></span>](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
