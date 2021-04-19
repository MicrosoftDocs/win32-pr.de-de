---
description: Die fotometadatenrichtlinie für die System. Photo. focalLength-Eigenschaft.
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: System. Photo. focalLength-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7b36240713782c98d52e4fbf4dae5c0c06082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364071"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a><span data-ttu-id="b870b-103">System. Photo. focalLength-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b870b-103">System.Photo.FocalLength Photo Metadata Policy</span></span>

<span data-ttu-id="b870b-104">Die fotometadatenrichtlinie für die [System. Photo. focalLength](../properties/props-system-photo-focallength.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b870b-104">The photo metadata policy for the [System.Photo.FocalLength](../properties/props-system-photo-focallength.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b870b-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="b870b-105">PKEY</span></span>

<span data-ttu-id="b870b-106">Pkey \_ Photo \_ focalLength</span><span class="sxs-lookup"><span data-stu-id="b870b-106">PKEY\_Photo\_FocalLength</span></span>

### <a name="containers"></a><span data-ttu-id="b870b-107">Container</span><span class="sxs-lookup"><span data-stu-id="b870b-107">Containers</span></span>

<span data-ttu-id="b870b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b870b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b870b-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b870b-109">Read-Only</span></span>

<span data-ttu-id="b870b-110">Ja</span><span class="sxs-lookup"><span data-stu-id="b870b-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b870b-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="b870b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b870b-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="b870b-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b870b-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="b870b-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="b870b-114">Dieser Wert wird von System. Photo. focallengthnumerator und System. Photo. focallengthnenner generiert.</span><span class="sxs-lookup"><span data-stu-id="b870b-114">This value is generated from System.Photo.FocalLengthNumerator and System.Photo.FocalLengthDenominator.</span></span> <span data-ttu-id="b870b-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b870b-115">It cannot be written directly.</span></span> <span data-ttu-id="b870b-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="b870b-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b870b-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b870b-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b870b-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="b870b-118">Read Paths</span></span>



| <span data-ttu-id="b870b-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b870b-119">Order</span></span> | <span data-ttu-id="b870b-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="b870b-120">Path</span></span>                          | <span data-ttu-id="b870b-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b870b-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b870b-122">1</span><span class="sxs-lookup"><span data-stu-id="b870b-122">1</span></span>     | <span data-ttu-id="b870b-123">/App1/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="b870b-123">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="b870b-124">2</span><span class="sxs-lookup"><span data-stu-id="b870b-124">2</span></span>     | <span data-ttu-id="b870b-125">/XMP/EXIF: focalLength</span><span class="sxs-lookup"><span data-stu-id="b870b-125">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="b870b-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="b870b-126">Write Paths</span></span>



| <span data-ttu-id="b870b-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b870b-127">Order</span></span> | <span data-ttu-id="b870b-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="b870b-128">Path</span></span>                          | <span data-ttu-id="b870b-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b870b-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b870b-130">1</span><span class="sxs-lookup"><span data-stu-id="b870b-130">1</span></span>     | <span data-ttu-id="b870b-131">/App1/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="b870b-131">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="b870b-132">2</span><span class="sxs-lookup"><span data-stu-id="b870b-132">2</span></span>     | <span data-ttu-id="b870b-133">/XMP/EXIF: focalLength</span><span class="sxs-lookup"><span data-stu-id="b870b-133">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b870b-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="b870b-134">Remove Paths</span></span>



| <span data-ttu-id="b870b-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b870b-135">Order</span></span> | <span data-ttu-id="b870b-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="b870b-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="b870b-137">1</span><span class="sxs-lookup"><span data-stu-id="b870b-137">1</span></span>     | <span data-ttu-id="b870b-138">/App1/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="b870b-138">/app1/ifd/exif/{ushort=37386}</span></span> |
| <span data-ttu-id="b870b-139">2</span><span class="sxs-lookup"><span data-stu-id="b870b-139">2</span></span>     | <span data-ttu-id="b870b-140">/XMP/EXIF: focalLength</span><span class="sxs-lookup"><span data-stu-id="b870b-140">/xmp/exif:focallength</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="b870b-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="b870b-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b870b-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="b870b-142">Read Paths</span></span>



| <span data-ttu-id="b870b-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b870b-143">Order</span></span> | <span data-ttu-id="b870b-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="b870b-144">Path</span></span>                      | <span data-ttu-id="b870b-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b870b-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b870b-146">1</span><span class="sxs-lookup"><span data-stu-id="b870b-146">1</span></span>     | <span data-ttu-id="b870b-147">/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="b870b-147">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="b870b-148">2</span><span class="sxs-lookup"><span data-stu-id="b870b-148">2</span></span>     | <span data-ttu-id="b870b-149">/IFD/XMP/EXIF: focalLength</span><span class="sxs-lookup"><span data-stu-id="b870b-149">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b870b-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="b870b-150">Write Paths</span></span>



| <span data-ttu-id="b870b-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b870b-151">Order</span></span> | <span data-ttu-id="b870b-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="b870b-152">Path</span></span>                      | <span data-ttu-id="b870b-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b870b-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b870b-154">1</span><span class="sxs-lookup"><span data-stu-id="b870b-154">1</span></span>     | <span data-ttu-id="b870b-155">/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="b870b-155">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="b870b-156">2</span><span class="sxs-lookup"><span data-stu-id="b870b-156">2</span></span>     | <span data-ttu-id="b870b-157">/IFD/XMP/EXIF: focalLength</span><span class="sxs-lookup"><span data-stu-id="b870b-157">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b870b-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="b870b-158">Remove Paths</span></span>



| <span data-ttu-id="b870b-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b870b-159">Order</span></span> | <span data-ttu-id="b870b-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="b870b-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="b870b-161">1</span><span class="sxs-lookup"><span data-stu-id="b870b-161">1</span></span>     | <span data-ttu-id="b870b-162">/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="b870b-162">/ifd/exif/{ushort=37386}</span></span>  |
| <span data-ttu-id="b870b-163">2</span><span class="sxs-lookup"><span data-stu-id="b870b-163">2</span></span>     | <span data-ttu-id="b870b-164">/IFD/XMP/EXIF: focalLength</span><span class="sxs-lookup"><span data-stu-id="b870b-164">/ifd/xmp/exif:focallength</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b870b-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b870b-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b870b-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b870b-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b870b-167">System. Photo. focalLength</span><span class="sxs-lookup"><span data-stu-id="b870b-167">System.Photo.FocalLength</span></span>](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
