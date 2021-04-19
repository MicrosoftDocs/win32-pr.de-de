---
description: Die fotometadatenrichtlinie für die System. Image. Compression-Eigenschaft.
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: System. Image. Compression-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362265"
---
# <a name="systemimagecompression-photo-metadata-policy"></a><span data-ttu-id="90876-103">System. Image. Compression-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="90876-103">System.Image.Compression Photo Metadata Policy</span></span>

<span data-ttu-id="90876-104">Die fotometadatenrichtlinie für die [System. Image. Compression](../properties/props-system-image-compression.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="90876-104">The photo metadata policy for the [System.Image.Compression](../properties/props-system-image-compression.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="90876-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="90876-105">PKEY</span></span>

<span data-ttu-id="90876-106">Pkey- \_ Bild \_ Komprimierung</span><span class="sxs-lookup"><span data-stu-id="90876-106">PKEY\_Image\_Compression</span></span>

### <a name="containers"></a><span data-ttu-id="90876-107">Container</span><span class="sxs-lookup"><span data-stu-id="90876-107">Containers</span></span>

<span data-ttu-id="90876-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="90876-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="90876-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90876-109">Read-Only</span></span>

<span data-ttu-id="90876-110">Ja</span><span class="sxs-lookup"><span data-stu-id="90876-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="90876-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="90876-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="90876-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="90876-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="90876-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="90876-113">Input Type</span></span>

<span data-ttu-id="90876-114">UShort</span><span class="sxs-lookup"><span data-stu-id="90876-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="90876-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="90876-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="90876-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="90876-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="90876-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="90876-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="90876-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="90876-118">Read Paths</span></span>



| <span data-ttu-id="90876-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="90876-119">Order</span></span> | <span data-ttu-id="90876-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="90876-120">Path</span></span>                   | <span data-ttu-id="90876-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="90876-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="90876-122">1</span><span class="sxs-lookup"><span data-stu-id="90876-122">1</span></span>     | <span data-ttu-id="90876-123">/App1/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="90876-123">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="90876-124">ushort</span><span class="sxs-lookup"><span data-stu-id="90876-124">ushort</span></span>      |
| <span data-ttu-id="90876-125">2</span><span class="sxs-lookup"><span data-stu-id="90876-125">2</span></span>     | <span data-ttu-id="90876-126">/XMP/TIFF: Komprimierung</span><span class="sxs-lookup"><span data-stu-id="90876-126">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="90876-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="90876-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="90876-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="90876-128">Write Paths</span></span>



| <span data-ttu-id="90876-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="90876-129">Order</span></span> | <span data-ttu-id="90876-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="90876-130">Path</span></span>                   | <span data-ttu-id="90876-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="90876-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="90876-132">1</span><span class="sxs-lookup"><span data-stu-id="90876-132">1</span></span>     | <span data-ttu-id="90876-133">/App1/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="90876-133">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="90876-134">ushort</span><span class="sxs-lookup"><span data-stu-id="90876-134">ushort</span></span>      |
| <span data-ttu-id="90876-135">2</span><span class="sxs-lookup"><span data-stu-id="90876-135">2</span></span>     | <span data-ttu-id="90876-136">/XMP/TIFF: Komprimierung</span><span class="sxs-lookup"><span data-stu-id="90876-136">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="90876-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="90876-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="90876-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="90876-138">Remove Paths</span></span>



| <span data-ttu-id="90876-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="90876-139">Order</span></span> | <span data-ttu-id="90876-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="90876-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="90876-141">1</span><span class="sxs-lookup"><span data-stu-id="90876-141">1</span></span>     | <span data-ttu-id="90876-142">/App1/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="90876-142">/app1/ifd/{ushort=259}</span></span> |
| <span data-ttu-id="90876-143">2</span><span class="sxs-lookup"><span data-stu-id="90876-143">2</span></span>     | <span data-ttu-id="90876-144">/XMP/TIFF: Komprimierung</span><span class="sxs-lookup"><span data-stu-id="90876-144">/xmp/tiff:compression</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="90876-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="90876-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="90876-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="90876-146">Read Paths</span></span>



| <span data-ttu-id="90876-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="90876-147">Order</span></span> | <span data-ttu-id="90876-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="90876-148">Path</span></span>                      | <span data-ttu-id="90876-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="90876-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="90876-150">1</span><span class="sxs-lookup"><span data-stu-id="90876-150">1</span></span>     | <span data-ttu-id="90876-151">/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="90876-151">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="90876-152">ushort</span><span class="sxs-lookup"><span data-stu-id="90876-152">ushort</span></span>      |
| <span data-ttu-id="90876-153">2</span><span class="sxs-lookup"><span data-stu-id="90876-153">2</span></span>     | <span data-ttu-id="90876-154">/IFD/XMP/TIFF: Komprimierung</span><span class="sxs-lookup"><span data-stu-id="90876-154">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="90876-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="90876-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="90876-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="90876-156">Write Paths</span></span>



| <span data-ttu-id="90876-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="90876-157">Order</span></span> | <span data-ttu-id="90876-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="90876-158">Path</span></span>                      | <span data-ttu-id="90876-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="90876-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="90876-160">1</span><span class="sxs-lookup"><span data-stu-id="90876-160">1</span></span>     | <span data-ttu-id="90876-161">/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="90876-161">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="90876-162">ushort</span><span class="sxs-lookup"><span data-stu-id="90876-162">ushort</span></span>      |
| <span data-ttu-id="90876-163">2</span><span class="sxs-lookup"><span data-stu-id="90876-163">2</span></span>     | <span data-ttu-id="90876-164">/IFD/XMP/TIFF: Komprimierung</span><span class="sxs-lookup"><span data-stu-id="90876-164">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="90876-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="90876-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="90876-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="90876-166">Remove Paths</span></span>



| <span data-ttu-id="90876-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="90876-167">Order</span></span> | <span data-ttu-id="90876-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="90876-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="90876-169">1</span><span class="sxs-lookup"><span data-stu-id="90876-169">1</span></span>     | <span data-ttu-id="90876-170">/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="90876-170">/ifd/{ushort=259}</span></span>         |
| <span data-ttu-id="90876-171">2</span><span class="sxs-lookup"><span data-stu-id="90876-171">2</span></span>     | <span data-ttu-id="90876-172">/IFD/XMP/TIFF: Komprimierung</span><span class="sxs-lookup"><span data-stu-id="90876-172">/ifd/xmp/tiff:compression</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="90876-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90876-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="90876-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90876-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90876-175">System. Image. Compression</span><span class="sxs-lookup"><span data-stu-id="90876-175">System.Image.Compression</span></span>](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
