---
description: Die fotometadatenrichtlinie für die System. Photo. focallengthinfilm-Eigenschaft.
ms.assetid: 3ad63a7a-5ced-4e7f-a4a0-e1463f3d3fa3
title: System. Photo. focallengthinfilm-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df46f3e52c447cb7902fe3cce2da201dae16d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485702"
---
# <a name="systemphotofocallengthinfilm-photo-metadata-policy"></a><span data-ttu-id="0e123-103">System. Photo. focallengthinfilm-fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="0e123-103">System.Photo.FocalLengthInFilm Photo Metadata Policy</span></span>

<span data-ttu-id="0e123-104">Die fotometadatenrichtlinie für die [System. Photo. focallengthinfilm](../properties/props-system-photo-focallengthinfilm.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0e123-104">The photo metadata policy for the [System.Photo.FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0e123-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="0e123-105">PKEY</span></span>

<span data-ttu-id="0e123-106">Pkey \_ focallengthinfilm</span><span class="sxs-lookup"><span data-stu-id="0e123-106">PKEY\_FocalLengthInFilm</span></span>

### <a name="containers"></a><span data-ttu-id="0e123-107">Container</span><span class="sxs-lookup"><span data-stu-id="0e123-107">Containers</span></span>

<span data-ttu-id="0e123-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="0e123-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0e123-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0e123-109">Read-Only</span></span>

<span data-ttu-id="0e123-110">Nein</span><span class="sxs-lookup"><span data-stu-id="0e123-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="0e123-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="0e123-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="0e123-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="0e123-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="0e123-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="0e123-113">Input Type</span></span>

<span data-ttu-id="0e123-114">UShort</span><span class="sxs-lookup"><span data-stu-id="0e123-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0e123-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="0e123-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="0e123-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="0e123-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="0e123-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="0e123-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="0e123-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="0e123-118">Read Paths</span></span>



| <span data-ttu-id="0e123-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0e123-119">Order</span></span> | <span data-ttu-id="0e123-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="0e123-120">Path</span></span>                            | <span data-ttu-id="0e123-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="0e123-121">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="0e123-122">1</span><span class="sxs-lookup"><span data-stu-id="0e123-122">1</span></span>     | <span data-ttu-id="0e123-123">/App1/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="0e123-123">/app1/ifd/exif/{ushort=41989}</span></span>   | <span data-ttu-id="0e123-124">ushort</span><span class="sxs-lookup"><span data-stu-id="0e123-124">ushort</span></span>      |
| <span data-ttu-id="0e123-125">2</span><span class="sxs-lookup"><span data-stu-id="0e123-125">2</span></span>     | <span data-ttu-id="0e123-126">/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="0e123-126">/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="0e123-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="0e123-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0e123-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="0e123-128">Write Paths</span></span>



| <span data-ttu-id="0e123-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0e123-129">Order</span></span> | <span data-ttu-id="0e123-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="0e123-130">Path</span></span>                            | <span data-ttu-id="0e123-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="0e123-131">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="0e123-132">1</span><span class="sxs-lookup"><span data-stu-id="0e123-132">1</span></span>     | <span data-ttu-id="0e123-133">/App1/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="0e123-133">/app1/ifd/exif/{ushort=41989}</span></span>   | <span data-ttu-id="0e123-134">ushort</span><span class="sxs-lookup"><span data-stu-id="0e123-134">ushort</span></span>      |
| <span data-ttu-id="0e123-135">2</span><span class="sxs-lookup"><span data-stu-id="0e123-135">2</span></span>     | <span data-ttu-id="0e123-136">/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="0e123-136">/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="0e123-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="0e123-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0e123-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="0e123-138">Remove Paths</span></span>



| <span data-ttu-id="0e123-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0e123-139">Order</span></span> | <span data-ttu-id="0e123-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="0e123-140">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="0e123-141">1</span><span class="sxs-lookup"><span data-stu-id="0e123-141">1</span></span>     | <span data-ttu-id="0e123-142">/App1/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="0e123-142">/app1/ifd/exif/{ushort=41989}</span></span>   |
| <span data-ttu-id="0e123-143">2</span><span class="sxs-lookup"><span data-stu-id="0e123-143">2</span></span>     | <span data-ttu-id="0e123-144">/xmp/exif:focallengthin35mmfilm</span><span class="sxs-lookup"><span data-stu-id="0e123-144">/xmp/exif:focallengthin35mmfilm</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="0e123-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="0e123-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0e123-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="0e123-146">Read Paths</span></span>



| <span data-ttu-id="0e123-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0e123-147">Order</span></span> | <span data-ttu-id="0e123-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="0e123-148">Path</span></span>                                | <span data-ttu-id="0e123-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="0e123-149">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="0e123-150">1</span><span class="sxs-lookup"><span data-stu-id="0e123-150">1</span></span>     | <span data-ttu-id="0e123-151">/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="0e123-151">/ifd/exif/{ushort=41989}</span></span>            | <span data-ttu-id="0e123-152">ushort</span><span class="sxs-lookup"><span data-stu-id="0e123-152">ushort</span></span>      |
| <span data-ttu-id="0e123-153">2</span><span class="sxs-lookup"><span data-stu-id="0e123-153">2</span></span>     | <span data-ttu-id="0e123-154">/ifd/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="0e123-154">/ifd/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="0e123-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="0e123-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0e123-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="0e123-156">Write Paths</span></span>



| <span data-ttu-id="0e123-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0e123-157">Order</span></span> | <span data-ttu-id="0e123-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="0e123-158">Path</span></span>                                | <span data-ttu-id="0e123-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="0e123-159">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="0e123-160">1</span><span class="sxs-lookup"><span data-stu-id="0e123-160">1</span></span>     | <span data-ttu-id="0e123-161">/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="0e123-161">/ifd/exif/{ushort=41989}</span></span>            | <span data-ttu-id="0e123-162">ushort</span><span class="sxs-lookup"><span data-stu-id="0e123-162">ushort</span></span>      |
| <span data-ttu-id="0e123-163">2</span><span class="sxs-lookup"><span data-stu-id="0e123-163">2</span></span>     | <span data-ttu-id="0e123-164">/ifd/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="0e123-164">/ifd/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="0e123-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="0e123-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0e123-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="0e123-166">Remove Paths</span></span>



| <span data-ttu-id="0e123-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0e123-167">Order</span></span> | <span data-ttu-id="0e123-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="0e123-168">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="0e123-169">1</span><span class="sxs-lookup"><span data-stu-id="0e123-169">1</span></span>     | <span data-ttu-id="0e123-170">/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="0e123-170">/ifd/exif/{ushort=41989}</span></span>            |
| <span data-ttu-id="0e123-171">2</span><span class="sxs-lookup"><span data-stu-id="0e123-171">2</span></span>     | <span data-ttu-id="0e123-172">/ifd/xmp/exif:focallengthin35mmfilm</span><span class="sxs-lookup"><span data-stu-id="0e123-172">/ifd/xmp/exif:focallengthin35mmfilm</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0e123-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e123-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e123-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e123-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e123-175">System. Photo. focallengthinfilm</span><span class="sxs-lookup"><span data-stu-id="0e123-175">System.Photo.FocalLengthInFilm</span></span>](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
