---
description: Die fotometadatenrichtlinie für die System. Photo. WhiteBalance-Eigenschaft.
ms.assetid: 7b3a31e6-a929-41e4-b7f0-c5b3beac2519
title: System. Photo. WhiteBalance Photo-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc333cedcd4665ace37033452ec3c7f0336f13e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349596"
---
# <a name="systemphotowhitebalance-photo-metadata-policy"></a><span data-ttu-id="c17ea-103">System. Photo. WhiteBalance Photo-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="c17ea-103">System.Photo.WhiteBalance Photo Metadata Policy</span></span>

<span data-ttu-id="c17ea-104">Die fotometadatenrichtlinie für die [System. Photo. WhiteBalance](../properties/props-system-photo-whitebalance.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c17ea-104">The photo metadata policy for the [System.Photo.WhiteBalance](../properties/props-system-photo-whitebalance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c17ea-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="c17ea-105">PKEY</span></span>

<span data-ttu-id="c17ea-106">Pkey- \_ Foto- \_ WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="c17ea-106">PKEY\_Photo\_WhiteBalance</span></span>

### <a name="containers"></a><span data-ttu-id="c17ea-107">Container</span><span class="sxs-lookup"><span data-stu-id="c17ea-107">Containers</span></span>

<span data-ttu-id="c17ea-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c17ea-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c17ea-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c17ea-109">Read-Only</span></span>

<span data-ttu-id="c17ea-110">Nein</span><span class="sxs-lookup"><span data-stu-id="c17ea-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c17ea-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="c17ea-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c17ea-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="c17ea-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="c17ea-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="c17ea-113">Input Type</span></span>

<span data-ttu-id="c17ea-114">UShort</span><span class="sxs-lookup"><span data-stu-id="c17ea-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c17ea-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="c17ea-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c17ea-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="c17ea-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="c17ea-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="c17ea-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c17ea-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="c17ea-118">Read Paths</span></span>



| <span data-ttu-id="c17ea-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c17ea-119">Order</span></span> | <span data-ttu-id="c17ea-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="c17ea-120">Path</span></span>                          | <span data-ttu-id="c17ea-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="c17ea-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c17ea-122">1</span><span class="sxs-lookup"><span data-stu-id="c17ea-122">1</span></span>     | <span data-ttu-id="c17ea-123">/App1/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="c17ea-123">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="c17ea-124">ushort</span><span class="sxs-lookup"><span data-stu-id="c17ea-124">ushort</span></span>      |
| <span data-ttu-id="c17ea-125">2</span><span class="sxs-lookup"><span data-stu-id="c17ea-125">2</span></span>     | <span data-ttu-id="c17ea-126">/XMP/EXIF: WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="c17ea-126">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="c17ea-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="c17ea-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c17ea-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="c17ea-128">Write Paths</span></span>



| <span data-ttu-id="c17ea-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c17ea-129">Order</span></span> | <span data-ttu-id="c17ea-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="c17ea-130">Path</span></span>                          | <span data-ttu-id="c17ea-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="c17ea-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c17ea-132">1</span><span class="sxs-lookup"><span data-stu-id="c17ea-132">1</span></span>     | <span data-ttu-id="c17ea-133">/App1/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="c17ea-133">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="c17ea-134">ushort</span><span class="sxs-lookup"><span data-stu-id="c17ea-134">ushort</span></span>      |
| <span data-ttu-id="c17ea-135">2</span><span class="sxs-lookup"><span data-stu-id="c17ea-135">2</span></span>     | <span data-ttu-id="c17ea-136">/XMP/EXIF: WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="c17ea-136">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="c17ea-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="c17ea-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c17ea-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="c17ea-138">Remove Paths</span></span>



| <span data-ttu-id="c17ea-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c17ea-139">Order</span></span> | <span data-ttu-id="c17ea-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="c17ea-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="c17ea-141">1</span><span class="sxs-lookup"><span data-stu-id="c17ea-141">1</span></span>     | <span data-ttu-id="c17ea-142">/App1/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="c17ea-142">/app1/ifd/exif/{ushort=41987}</span></span> |
| <span data-ttu-id="c17ea-143">2</span><span class="sxs-lookup"><span data-stu-id="c17ea-143">2</span></span>     | <span data-ttu-id="c17ea-144">/XMP/EXIF: WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="c17ea-144">/xmp/exif:whitebalance</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="c17ea-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="c17ea-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c17ea-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="c17ea-146">Read Paths</span></span>



| <span data-ttu-id="c17ea-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c17ea-147">Order</span></span> | <span data-ttu-id="c17ea-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="c17ea-148">Path</span></span>                       | <span data-ttu-id="c17ea-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="c17ea-149">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="c17ea-150">1</span><span class="sxs-lookup"><span data-stu-id="c17ea-150">1</span></span>     | <span data-ttu-id="c17ea-151">/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="c17ea-151">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="c17ea-152">ushort</span><span class="sxs-lookup"><span data-stu-id="c17ea-152">ushort</span></span>      |
| <span data-ttu-id="c17ea-153">2</span><span class="sxs-lookup"><span data-stu-id="c17ea-153">2</span></span>     | <span data-ttu-id="c17ea-154">/IFD/XMP/EXIF: WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="c17ea-154">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="c17ea-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="c17ea-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c17ea-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="c17ea-156">Write Paths</span></span>



| <span data-ttu-id="c17ea-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c17ea-157">Order</span></span> | <span data-ttu-id="c17ea-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="c17ea-158">Path</span></span>                       | <span data-ttu-id="c17ea-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="c17ea-159">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="c17ea-160">1</span><span class="sxs-lookup"><span data-stu-id="c17ea-160">1</span></span>     | <span data-ttu-id="c17ea-161">/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="c17ea-161">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="c17ea-162">ushort</span><span class="sxs-lookup"><span data-stu-id="c17ea-162">ushort</span></span>      |
| <span data-ttu-id="c17ea-163">2</span><span class="sxs-lookup"><span data-stu-id="c17ea-163">2</span></span>     | <span data-ttu-id="c17ea-164">/IFD/XMP/EXIF: WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="c17ea-164">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="c17ea-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="c17ea-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c17ea-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="c17ea-166">Remove Paths</span></span>



| <span data-ttu-id="c17ea-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c17ea-167">Order</span></span> | <span data-ttu-id="c17ea-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="c17ea-168">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="c17ea-169">1</span><span class="sxs-lookup"><span data-stu-id="c17ea-169">1</span></span>     | <span data-ttu-id="c17ea-170">/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="c17ea-170">/ifd/exif/{ushort=41987}</span></span>   |
| <span data-ttu-id="c17ea-171">2</span><span class="sxs-lookup"><span data-stu-id="c17ea-171">2</span></span>     | <span data-ttu-id="c17ea-172">/IFD/XMP/EXIF: WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="c17ea-172">/ifd/xmp/exif:whitebalance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c17ea-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c17ea-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c17ea-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c17ea-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c17ea-175">System. Photo. WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="c17ea-175">System.Photo.WhiteBalance</span></span>](../properties/props-system-photo-whitebalance.md)
</dt> </dl>

 

 
