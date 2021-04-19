---
description: Die fotometadatenrichtlinie für die System. Photo. Schärding-Eigenschaft.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: System. Photo. Schärding-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362395"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a><span data-ttu-id="ed6c4-103">System. Photo. Schärding-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ed6c4-103">System.Photo.Sharpness Photo Metadata Policy</span></span>

<span data-ttu-id="ed6c4-104">Die fotometadatenrichtlinie für die [System. Photo. Schärding](../properties/props-system-photo-sharpness.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ed6c4-104">The photo metadata policy for the [System.Photo.Sharpness](../properties/props-system-photo-sharpness.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ed6c4-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="ed6c4-105">PKEY</span></span>

<span data-ttu-id="ed6c4-106">Pkey- \_ Foto \_ Schärfe</span><span class="sxs-lookup"><span data-stu-id="ed6c4-106">PKEY\_Photo\_Sharpness</span></span>

### <a name="containers"></a><span data-ttu-id="ed6c4-107">Container</span><span class="sxs-lookup"><span data-stu-id="ed6c4-107">Containers</span></span>

<span data-ttu-id="ed6c4-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ed6c4-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ed6c4-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed6c4-109">Read-Only</span></span>

<span data-ttu-id="ed6c4-110">Nein</span><span class="sxs-lookup"><span data-stu-id="ed6c4-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ed6c4-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="ed6c4-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ed6c4-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ed6c4-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="ed6c4-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="ed6c4-113">Input Type</span></span>

<span data-ttu-id="ed6c4-114">UShort</span><span class="sxs-lookup"><span data-stu-id="ed6c4-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ed6c4-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="ed6c4-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ed6c4-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="ed6c4-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ed6c4-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="ed6c4-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ed6c4-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="ed6c4-118">Read Paths</span></span>



| <span data-ttu-id="ed6c4-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="ed6c4-119">Order</span></span> | <span data-ttu-id="ed6c4-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="ed6c4-120">Path</span></span>                          | <span data-ttu-id="ed6c4-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="ed6c4-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="ed6c4-122">1</span><span class="sxs-lookup"><span data-stu-id="ed6c4-122">1</span></span>     | <span data-ttu-id="ed6c4-123">/App1/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="ed6c4-123">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="ed6c4-124">ushort</span><span class="sxs-lookup"><span data-stu-id="ed6c4-124">ushort</span></span>      |
| <span data-ttu-id="ed6c4-125">2</span><span class="sxs-lookup"><span data-stu-id="ed6c4-125">2</span></span>     | <span data-ttu-id="ed6c4-126">/XMP/EXIF: Schärfe</span><span class="sxs-lookup"><span data-stu-id="ed6c4-126">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="ed6c4-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="ed6c4-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ed6c4-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="ed6c4-128">Write Paths</span></span>



| <span data-ttu-id="ed6c4-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="ed6c4-129">Order</span></span> | <span data-ttu-id="ed6c4-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="ed6c4-130">Path</span></span>                          | <span data-ttu-id="ed6c4-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="ed6c4-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="ed6c4-132">1</span><span class="sxs-lookup"><span data-stu-id="ed6c4-132">1</span></span>     | <span data-ttu-id="ed6c4-133">/App1/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="ed6c4-133">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="ed6c4-134">ushort</span><span class="sxs-lookup"><span data-stu-id="ed6c4-134">ushort</span></span>      |
| <span data-ttu-id="ed6c4-135">2</span><span class="sxs-lookup"><span data-stu-id="ed6c4-135">2</span></span>     | <span data-ttu-id="ed6c4-136">/XMP/EXIF: Schärfe</span><span class="sxs-lookup"><span data-stu-id="ed6c4-136">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="ed6c4-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="ed6c4-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ed6c4-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="ed6c4-138">Remove Paths</span></span>



| <span data-ttu-id="ed6c4-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="ed6c4-139">Order</span></span> | <span data-ttu-id="ed6c4-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="ed6c4-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="ed6c4-141">1</span><span class="sxs-lookup"><span data-stu-id="ed6c4-141">1</span></span>     | <span data-ttu-id="ed6c4-142">/App1/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="ed6c4-142">/app1/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="ed6c4-143">2</span><span class="sxs-lookup"><span data-stu-id="ed6c4-143">2</span></span>     | <span data-ttu-id="ed6c4-144">/XMP/EXIF: Schärfe</span><span class="sxs-lookup"><span data-stu-id="ed6c4-144">/xmp/exif:sharpness</span></span>           |



 

### <a name="tiff-policies"></a><span data-ttu-id="ed6c4-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="ed6c4-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ed6c4-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="ed6c4-146">Read Paths</span></span>



| <span data-ttu-id="ed6c4-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="ed6c4-147">Order</span></span> | <span data-ttu-id="ed6c4-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="ed6c4-148">Path</span></span>                     | <span data-ttu-id="ed6c4-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="ed6c4-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="ed6c4-150">1</span><span class="sxs-lookup"><span data-stu-id="ed6c4-150">1</span></span>     | <span data-ttu-id="ed6c4-151">/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="ed6c4-151">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="ed6c4-152">ushort</span><span class="sxs-lookup"><span data-stu-id="ed6c4-152">ushort</span></span>      |
| <span data-ttu-id="ed6c4-153">2</span><span class="sxs-lookup"><span data-stu-id="ed6c4-153">2</span></span>     | <span data-ttu-id="ed6c4-154">/IFD/XMP/EXIF: Schärfe</span><span class="sxs-lookup"><span data-stu-id="ed6c4-154">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="ed6c4-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="ed6c4-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ed6c4-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="ed6c4-156">Write Paths</span></span>



| <span data-ttu-id="ed6c4-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="ed6c4-157">Order</span></span> | <span data-ttu-id="ed6c4-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="ed6c4-158">Path</span></span>                     | <span data-ttu-id="ed6c4-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="ed6c4-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="ed6c4-160">1</span><span class="sxs-lookup"><span data-stu-id="ed6c4-160">1</span></span>     | <span data-ttu-id="ed6c4-161">/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="ed6c4-161">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="ed6c4-162">ushort</span><span class="sxs-lookup"><span data-stu-id="ed6c4-162">ushort</span></span>      |
| <span data-ttu-id="ed6c4-163">2</span><span class="sxs-lookup"><span data-stu-id="ed6c4-163">2</span></span>     | <span data-ttu-id="ed6c4-164">/IFD/XMP/EXIF: Schärfe</span><span class="sxs-lookup"><span data-stu-id="ed6c4-164">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="ed6c4-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="ed6c4-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ed6c4-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="ed6c4-166">Remove Paths</span></span>



| <span data-ttu-id="ed6c4-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="ed6c4-167">Order</span></span> | <span data-ttu-id="ed6c4-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="ed6c4-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="ed6c4-169">1</span><span class="sxs-lookup"><span data-stu-id="ed6c4-169">1</span></span>     | <span data-ttu-id="ed6c4-170">/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="ed6c4-170">/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="ed6c4-171">2</span><span class="sxs-lookup"><span data-stu-id="ed6c4-171">2</span></span>     | <span data-ttu-id="ed6c4-172">/IFD/XMP/EXIF: Schärfe</span><span class="sxs-lookup"><span data-stu-id="ed6c4-172">/ifd/xmp/exif:sharpness</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="ed6c4-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed6c4-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed6c4-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed6c4-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed6c4-175">System. Photo. Schärding</span><span class="sxs-lookup"><span data-stu-id="ed6c4-175">System.Photo.Sharpness</span></span>](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
