---
description: Die fotometadatenrichtlinie für die System. Photo. EXIF Version-Eigenschaft.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: System. Photo. exibversion-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb823db41cb54a06fba235df5be4bb4acd55ea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217828"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a><span data-ttu-id="6e1ba-103">System. Photo. exibversion-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="6e1ba-103">System.Photo.EXIFVersion Photo Metadata Policy</span></span>

<span data-ttu-id="6e1ba-104">Die fotometadatenrichtlinie für die [System. Photo. EXIF Version](../properties/props-system-photo-exifversion.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-104">The photo metadata policy for the [System.Photo.EXIFVersion](../properties/props-system-photo-exifversion.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6e1ba-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="6e1ba-105">PKEY</span></span>

<span data-ttu-id="6e1ba-106">Pkey- \_ Foto- \_ EXIF-Version</span><span class="sxs-lookup"><span data-stu-id="6e1ba-106">PKEY\_Photo\_EXIFVersion</span></span>

### <a name="containers"></a><span data-ttu-id="6e1ba-107">Container</span><span class="sxs-lookup"><span data-stu-id="6e1ba-107">Containers</span></span>

<span data-ttu-id="6e1ba-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6e1ba-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6e1ba-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e1ba-109">Read-Only</span></span>

<span data-ttu-id="6e1ba-110">Nein</span><span class="sxs-lookup"><span data-stu-id="6e1ba-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6e1ba-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="6e1ba-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6e1ba-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="6e1ba-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="6e1ba-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="6e1ba-113">Input Type</span></span>

<span data-ttu-id="6e1ba-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6e1ba-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="6e1ba-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="6e1ba-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6e1ba-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="6e1ba-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6e1ba-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="6e1ba-118">Read Paths</span></span>



| <span data-ttu-id="6e1ba-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6e1ba-119">Order</span></span> | <span data-ttu-id="6e1ba-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="6e1ba-120">Path</span></span>                          | <span data-ttu-id="6e1ba-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="6e1ba-121">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="6e1ba-122">1</span><span class="sxs-lookup"><span data-stu-id="6e1ba-122">1</span></span>     | <span data-ttu-id="6e1ba-123">/App1/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="6e1ba-123">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="6e1ba-124">EXIF- \_ Version</span><span class="sxs-lookup"><span data-stu-id="6e1ba-124">exif\_version</span></span> |
| <span data-ttu-id="6e1ba-125">2</span><span class="sxs-lookup"><span data-stu-id="6e1ba-125">2</span></span>     | <span data-ttu-id="6e1ba-126">/XMP/EXIF: EXIF-Version</span><span class="sxs-lookup"><span data-stu-id="6e1ba-126">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="6e1ba-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="6e1ba-127">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="6e1ba-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="6e1ba-128">Write Paths</span></span>



| <span data-ttu-id="6e1ba-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6e1ba-129">Order</span></span> | <span data-ttu-id="6e1ba-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="6e1ba-130">Path</span></span>                          | <span data-ttu-id="6e1ba-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="6e1ba-131">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="6e1ba-132">1</span><span class="sxs-lookup"><span data-stu-id="6e1ba-132">1</span></span>     | <span data-ttu-id="6e1ba-133">/App1/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="6e1ba-133">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="6e1ba-134">EXIF- \_ Version</span><span class="sxs-lookup"><span data-stu-id="6e1ba-134">exif\_version</span></span> |
| <span data-ttu-id="6e1ba-135">2</span><span class="sxs-lookup"><span data-stu-id="6e1ba-135">2</span></span>     | <span data-ttu-id="6e1ba-136">/XMP/EXIF: EXIF-Version</span><span class="sxs-lookup"><span data-stu-id="6e1ba-136">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="6e1ba-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="6e1ba-137">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="6e1ba-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="6e1ba-138">Remove Paths</span></span>



| <span data-ttu-id="6e1ba-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6e1ba-139">Order</span></span> | <span data-ttu-id="6e1ba-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="6e1ba-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="6e1ba-141">1</span><span class="sxs-lookup"><span data-stu-id="6e1ba-141">1</span></span>     | <span data-ttu-id="6e1ba-142">/App1/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="6e1ba-142">/app1/ifd/exif/{ushort=36864}</span></span> |
| <span data-ttu-id="6e1ba-143">2</span><span class="sxs-lookup"><span data-stu-id="6e1ba-143">2</span></span>     | <span data-ttu-id="6e1ba-144">/XMP/EXIF: EXIF-Version</span><span class="sxs-lookup"><span data-stu-id="6e1ba-144">/xmp/exif:ExifVersion</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="6e1ba-145">TIFF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="6e1ba-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6e1ba-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="6e1ba-146">Read Paths</span></span>



| <span data-ttu-id="6e1ba-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6e1ba-147">Order</span></span> | <span data-ttu-id="6e1ba-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="6e1ba-148">Path</span></span>                      | <span data-ttu-id="6e1ba-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="6e1ba-149">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="6e1ba-150">1</span><span class="sxs-lookup"><span data-stu-id="6e1ba-150">1</span></span>     | <span data-ttu-id="6e1ba-151">/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="6e1ba-151">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="6e1ba-152">EXIF- \_ Version</span><span class="sxs-lookup"><span data-stu-id="6e1ba-152">exif\_version</span></span> |
| <span data-ttu-id="6e1ba-153">2</span><span class="sxs-lookup"><span data-stu-id="6e1ba-153">2</span></span>     | <span data-ttu-id="6e1ba-154">/IFD/XMP/EXIF: EXIF-Version</span><span class="sxs-lookup"><span data-stu-id="6e1ba-154">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="6e1ba-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="6e1ba-155">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="6e1ba-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="6e1ba-156">Write Paths</span></span>



| <span data-ttu-id="6e1ba-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6e1ba-157">Order</span></span> | <span data-ttu-id="6e1ba-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="6e1ba-158">Path</span></span>                      | <span data-ttu-id="6e1ba-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="6e1ba-159">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="6e1ba-160">1</span><span class="sxs-lookup"><span data-stu-id="6e1ba-160">1</span></span>     | <span data-ttu-id="6e1ba-161">/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="6e1ba-161">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="6e1ba-162">EXIF- \_ Version</span><span class="sxs-lookup"><span data-stu-id="6e1ba-162">exif\_version</span></span> |
| <span data-ttu-id="6e1ba-163">2</span><span class="sxs-lookup"><span data-stu-id="6e1ba-163">2</span></span>     | <span data-ttu-id="6e1ba-164">/IFD/XMP/EXIF: EXIF-Version</span><span class="sxs-lookup"><span data-stu-id="6e1ba-164">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="6e1ba-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="6e1ba-165">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="6e1ba-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="6e1ba-166">Remove Paths</span></span>



| <span data-ttu-id="6e1ba-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6e1ba-167">Order</span></span> | <span data-ttu-id="6e1ba-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="6e1ba-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="6e1ba-169">1</span><span class="sxs-lookup"><span data-stu-id="6e1ba-169">1</span></span>     | <span data-ttu-id="6e1ba-170">/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="6e1ba-170">/ifd/exif/{ushort=36864}</span></span>  |
| <span data-ttu-id="6e1ba-171">2</span><span class="sxs-lookup"><span data-stu-id="6e1ba-171">2</span></span>     | <span data-ttu-id="6e1ba-172">/IFD/XMP/EXIF: EXIF-Version</span><span class="sxs-lookup"><span data-stu-id="6e1ba-172">/ifd/xmp/exif:ExifVersion</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6e1ba-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e1ba-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e1ba-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e1ba-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e1ba-175">System. Photo. EXIF Version</span><span class="sxs-lookup"><span data-stu-id="6e1ba-175">System.Photo.EXIFVersion</span></span>](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
