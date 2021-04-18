---
description: Die fotometadatenrichtlinie für die System. Photo. photomezcinterpretation-Eigenschaft.
ms.assetid: ff36b2c3-8763-4640-a049-b5880fd26929
title: System. Photo. photomezcinterpretation-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b371ce9257d526f941f3fdb33949e8788a7112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352615"
---
# <a name="systemphotophotometricinterpretation-photo-metadata-policy"></a><span data-ttu-id="360ed-103">System. Photo. photomezcinterpretation-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="360ed-103">System.Photo.PhotometricInterpretation Photo Metadata Policy</span></span>

<span data-ttu-id="360ed-104">Die fotometadatenrichtlinie für die [System. Photo. photomezcinterpretation](../properties/props-system-photo-photometricinterpretation.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="360ed-104">The photo metadata policy for the [System.Photo.PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="360ed-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="360ed-105">PKEY</span></span>

<span data-ttu-id="360ed-106">Pkey- \_ Foto- \_ foequcinterpretation</span><span class="sxs-lookup"><span data-stu-id="360ed-106">PKEY\_Photo\_PhotometricInterpretation</span></span>

### <a name="containers"></a><span data-ttu-id="360ed-107">Container</span><span class="sxs-lookup"><span data-stu-id="360ed-107">Containers</span></span>

<span data-ttu-id="360ed-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="360ed-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="360ed-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="360ed-109">Read-Only</span></span>

<span data-ttu-id="360ed-110">Ja</span><span class="sxs-lookup"><span data-stu-id="360ed-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="360ed-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="360ed-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="360ed-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="360ed-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="360ed-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="360ed-113">Input Type</span></span>

<span data-ttu-id="360ed-114">UShort</span><span class="sxs-lookup"><span data-stu-id="360ed-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="360ed-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="360ed-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="360ed-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="360ed-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="360ed-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="360ed-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="360ed-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="360ed-118">Read Paths</span></span>



| <span data-ttu-id="360ed-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="360ed-119">Order</span></span> | <span data-ttu-id="360ed-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="360ed-120">Path</span></span>                                | <span data-ttu-id="360ed-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="360ed-121">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="360ed-122">1</span><span class="sxs-lookup"><span data-stu-id="360ed-122">1</span></span>     | <span data-ttu-id="360ed-123">/App1/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="360ed-123">/app1/ifd/{ushort=262}</span></span>              | <span data-ttu-id="360ed-124">ushort</span><span class="sxs-lookup"><span data-stu-id="360ed-124">ushort</span></span>      |
| <span data-ttu-id="360ed-125">2</span><span class="sxs-lookup"><span data-stu-id="360ed-125">2</span></span>     | <span data-ttu-id="360ed-126">/XMP/TIFF: photomezcinterpretation</span><span class="sxs-lookup"><span data-stu-id="360ed-126">/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="360ed-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="360ed-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="360ed-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="360ed-128">Write Paths</span></span>



| <span data-ttu-id="360ed-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="360ed-129">Order</span></span> | <span data-ttu-id="360ed-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="360ed-130">Path</span></span>                                | <span data-ttu-id="360ed-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="360ed-131">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="360ed-132">1</span><span class="sxs-lookup"><span data-stu-id="360ed-132">1</span></span>     | <span data-ttu-id="360ed-133">/App1/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="360ed-133">/app1/ifd/{ushort=262}</span></span>              | <span data-ttu-id="360ed-134">ushort</span><span class="sxs-lookup"><span data-stu-id="360ed-134">ushort</span></span>      |
| <span data-ttu-id="360ed-135">2</span><span class="sxs-lookup"><span data-stu-id="360ed-135">2</span></span>     | <span data-ttu-id="360ed-136">/XMP/TIFF: photomezcinterpretation</span><span class="sxs-lookup"><span data-stu-id="360ed-136">/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="360ed-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="360ed-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="360ed-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="360ed-138">Remove Paths</span></span>



| <span data-ttu-id="360ed-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="360ed-139">Order</span></span> | <span data-ttu-id="360ed-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="360ed-140">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="360ed-141">1</span><span class="sxs-lookup"><span data-stu-id="360ed-141">1</span></span>     | <span data-ttu-id="360ed-142">/App1/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="360ed-142">/app1/ifd/{ushort=262}</span></span>              |
| <span data-ttu-id="360ed-143">2</span><span class="sxs-lookup"><span data-stu-id="360ed-143">2</span></span>     | <span data-ttu-id="360ed-144">/XMP/TIFF: photomezcinterpretation</span><span class="sxs-lookup"><span data-stu-id="360ed-144">/xmp/tiff:photometricinterpretation</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="360ed-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="360ed-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="360ed-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="360ed-146">Read Paths</span></span>



| <span data-ttu-id="360ed-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="360ed-147">Order</span></span> | <span data-ttu-id="360ed-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="360ed-148">Path</span></span>                                    | <span data-ttu-id="360ed-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="360ed-149">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="360ed-150">1</span><span class="sxs-lookup"><span data-stu-id="360ed-150">1</span></span>     | <span data-ttu-id="360ed-151">/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="360ed-151">/ifd/{ushort=262}</span></span>                       | <span data-ttu-id="360ed-152">ushort</span><span class="sxs-lookup"><span data-stu-id="360ed-152">ushort</span></span>      |
| <span data-ttu-id="360ed-153">2</span><span class="sxs-lookup"><span data-stu-id="360ed-153">2</span></span>     | <span data-ttu-id="360ed-154">/IFD/XMP/TIFF: photomezcinterpretation</span><span class="sxs-lookup"><span data-stu-id="360ed-154">/ifd/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="360ed-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="360ed-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="360ed-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="360ed-156">Write Paths</span></span>



| <span data-ttu-id="360ed-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="360ed-157">Order</span></span> | <span data-ttu-id="360ed-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="360ed-158">Path</span></span>                                    | <span data-ttu-id="360ed-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="360ed-159">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="360ed-160">1</span><span class="sxs-lookup"><span data-stu-id="360ed-160">1</span></span>     | <span data-ttu-id="360ed-161">/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="360ed-161">/ifd/{ushort=262}</span></span>                       | <span data-ttu-id="360ed-162">ushort</span><span class="sxs-lookup"><span data-stu-id="360ed-162">ushort</span></span>      |
| <span data-ttu-id="360ed-163">2</span><span class="sxs-lookup"><span data-stu-id="360ed-163">2</span></span>     | <span data-ttu-id="360ed-164">/IFD/XMP/TIFF: photomezcinterpretation</span><span class="sxs-lookup"><span data-stu-id="360ed-164">/ifd/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="360ed-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="360ed-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="360ed-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="360ed-166">Remove Paths</span></span>



| <span data-ttu-id="360ed-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="360ed-167">Order</span></span> | <span data-ttu-id="360ed-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="360ed-168">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="360ed-169">1</span><span class="sxs-lookup"><span data-stu-id="360ed-169">1</span></span>     | <span data-ttu-id="360ed-170">/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="360ed-170">/ifd/{ushort=262}</span></span>                       |
| <span data-ttu-id="360ed-171">2</span><span class="sxs-lookup"><span data-stu-id="360ed-171">2</span></span>     | <span data-ttu-id="360ed-172">/IFD/XMP/TIFF: photomezcinterpretation</span><span class="sxs-lookup"><span data-stu-id="360ed-172">/ifd/xmp/tiff:photometricinterpretation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="360ed-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="360ed-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="360ed-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="360ed-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="360ed-175">System. Photo. photomezcinterpretation</span><span class="sxs-lookup"><span data-stu-id="360ed-175">System.Photo.PhotometricInterpretation</span></span>](../properties/props-system-photo-photometricinterpretation.md)
</dt> </dl>

 

 
