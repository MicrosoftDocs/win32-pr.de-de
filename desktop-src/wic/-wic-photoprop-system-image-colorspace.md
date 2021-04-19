---
description: Die fotometadatenrichtlinie für die System. Image. ColorSpace-Eigenschaft.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: System. Image. ColorSpace-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6ef2003d05fa19b958b28950f71ec2d5f73027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356197"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a><span data-ttu-id="53cee-103">System. Image. ColorSpace-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="53cee-103">System.Image.ColorSpace Photo Metadata Policy</span></span>

<span data-ttu-id="53cee-104">Die fotometadatenrichtlinie für die [System. Image. ColorSpace](../properties/props-system-image-colorspace.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="53cee-104">The photo metadata policy for the [System.Image.ColorSpace](../properties/props-system-image-colorspace.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="53cee-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="53cee-105">PKEY</span></span>

<span data-ttu-id="53cee-106">Pkey- \_ Image \_ Color Space</span><span class="sxs-lookup"><span data-stu-id="53cee-106">PKEY\_Image\_ColorSpace</span></span>

### <a name="containers"></a><span data-ttu-id="53cee-107">Container</span><span class="sxs-lookup"><span data-stu-id="53cee-107">Containers</span></span>

<span data-ttu-id="53cee-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="53cee-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="53cee-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53cee-109">Read-Only</span></span>

<span data-ttu-id="53cee-110">Ja</span><span class="sxs-lookup"><span data-stu-id="53cee-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="53cee-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="53cee-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="53cee-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="53cee-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="53cee-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="53cee-113">Input Type</span></span>

<span data-ttu-id="53cee-114">UShort</span><span class="sxs-lookup"><span data-stu-id="53cee-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="53cee-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="53cee-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="53cee-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="53cee-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="53cee-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="53cee-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="53cee-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="53cee-118">Read Paths</span></span>



| <span data-ttu-id="53cee-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="53cee-119">Order</span></span> | <span data-ttu-id="53cee-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="53cee-120">Path</span></span>                          | <span data-ttu-id="53cee-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="53cee-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="53cee-122">1</span><span class="sxs-lookup"><span data-stu-id="53cee-122">1</span></span>     | <span data-ttu-id="53cee-123">/App1/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="53cee-123">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="53cee-124">ushort</span><span class="sxs-lookup"><span data-stu-id="53cee-124">ushort</span></span>      |
| <span data-ttu-id="53cee-125">2</span><span class="sxs-lookup"><span data-stu-id="53cee-125">2</span></span>     | <span data-ttu-id="53cee-126">/XMP/EXIF: colorspace</span><span class="sxs-lookup"><span data-stu-id="53cee-126">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="53cee-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="53cee-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="53cee-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="53cee-128">Write Paths</span></span>



| <span data-ttu-id="53cee-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="53cee-129">Order</span></span> | <span data-ttu-id="53cee-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="53cee-130">Path</span></span>                          | <span data-ttu-id="53cee-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="53cee-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="53cee-132">1</span><span class="sxs-lookup"><span data-stu-id="53cee-132">1</span></span>     | <span data-ttu-id="53cee-133">/App1/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="53cee-133">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="53cee-134">ushort</span><span class="sxs-lookup"><span data-stu-id="53cee-134">ushort</span></span>      |
| <span data-ttu-id="53cee-135">2</span><span class="sxs-lookup"><span data-stu-id="53cee-135">2</span></span>     | <span data-ttu-id="53cee-136">/XMP/EXIF: colorspace</span><span class="sxs-lookup"><span data-stu-id="53cee-136">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="53cee-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="53cee-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="53cee-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="53cee-138">Remove Paths</span></span>



| <span data-ttu-id="53cee-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="53cee-139">Order</span></span> | <span data-ttu-id="53cee-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="53cee-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="53cee-141">1</span><span class="sxs-lookup"><span data-stu-id="53cee-141">1</span></span>     | <span data-ttu-id="53cee-142">/App1/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="53cee-142">/app1/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="53cee-143">2</span><span class="sxs-lookup"><span data-stu-id="53cee-143">2</span></span>     | <span data-ttu-id="53cee-144">/XMP/EXIF: colorspace</span><span class="sxs-lookup"><span data-stu-id="53cee-144">/xmp/exif:colorspace</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="53cee-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="53cee-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="53cee-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="53cee-146">Read Paths</span></span>



| <span data-ttu-id="53cee-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="53cee-147">Order</span></span> | <span data-ttu-id="53cee-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="53cee-148">Path</span></span>                     | <span data-ttu-id="53cee-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="53cee-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="53cee-150">1</span><span class="sxs-lookup"><span data-stu-id="53cee-150">1</span></span>     | <span data-ttu-id="53cee-151">/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="53cee-151">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="53cee-152">ushort</span><span class="sxs-lookup"><span data-stu-id="53cee-152">ushort</span></span>      |
| <span data-ttu-id="53cee-153">2</span><span class="sxs-lookup"><span data-stu-id="53cee-153">2</span></span>     | <span data-ttu-id="53cee-154">/IFD/XMP/EXIF: colorspace</span><span class="sxs-lookup"><span data-stu-id="53cee-154">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="53cee-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="53cee-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="53cee-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="53cee-156">Write Paths</span></span>



| <span data-ttu-id="53cee-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="53cee-157">Order</span></span> | <span data-ttu-id="53cee-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="53cee-158">Path</span></span>                     | <span data-ttu-id="53cee-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="53cee-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="53cee-160">1</span><span class="sxs-lookup"><span data-stu-id="53cee-160">1</span></span>     | <span data-ttu-id="53cee-161">/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="53cee-161">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="53cee-162">ushort</span><span class="sxs-lookup"><span data-stu-id="53cee-162">ushort</span></span>      |
| <span data-ttu-id="53cee-163">2</span><span class="sxs-lookup"><span data-stu-id="53cee-163">2</span></span>     | <span data-ttu-id="53cee-164">/IFD/XMP/EXIF: colorspace</span><span class="sxs-lookup"><span data-stu-id="53cee-164">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="53cee-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="53cee-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="53cee-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="53cee-166">Remove Paths</span></span>



| <span data-ttu-id="53cee-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="53cee-167">Order</span></span> | <span data-ttu-id="53cee-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="53cee-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="53cee-169">1</span><span class="sxs-lookup"><span data-stu-id="53cee-169">1</span></span>     | <span data-ttu-id="53cee-170">/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="53cee-170">/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="53cee-171">2</span><span class="sxs-lookup"><span data-stu-id="53cee-171">2</span></span>     | <span data-ttu-id="53cee-172">/IFD/XMP/EXIF: colorspace</span><span class="sxs-lookup"><span data-stu-id="53cee-172">/ifd/xmp/exif:colorspace</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="53cee-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53cee-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="53cee-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="53cee-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53cee-175">System. Image. ColorSpace</span><span class="sxs-lookup"><span data-stu-id="53cee-175">System.Image.ColorSpace</span></span>](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
