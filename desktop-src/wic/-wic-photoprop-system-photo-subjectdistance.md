---
description: Die fotometadatenrichtlinie für die System. Photo. subjetdistance-Eigenschaft.
ms.assetid: 8d5acd7e-7227-4a79-890a-43e6dace3864
title: System. Photo. subjetdistance-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3335b17f45cce7dc60881dc7ea8d9ffecc711016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867328"
---
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a><span data-ttu-id="02f6d-103">System. Photo. subjetdistance-fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="02f6d-103">System.Photo.SubjectDistance Photo Metadata Policy</span></span>

<span data-ttu-id="02f6d-104">Die fotometadatenrichtlinie für die [System. Photo. subjetdistance](../properties/props-system-photo-subjectdistance.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="02f6d-104">The photo metadata policy for the [System.Photo.SubjectDistance](../properties/props-system-photo-subjectdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="02f6d-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="02f6d-105">PKEY</span></span>

<span data-ttu-id="02f6d-106">Pkey- \_ Foto ( \_ subjetdistance)</span><span class="sxs-lookup"><span data-stu-id="02f6d-106">PKEY\_Photo\_SubjectDistance</span></span>

### <a name="containers"></a><span data-ttu-id="02f6d-107">Container</span><span class="sxs-lookup"><span data-stu-id="02f6d-107">Containers</span></span>

<span data-ttu-id="02f6d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="02f6d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="02f6d-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02f6d-109">Read-Only</span></span>

<span data-ttu-id="02f6d-110">Ja</span><span class="sxs-lookup"><span data-stu-id="02f6d-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="02f6d-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="02f6d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="02f6d-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="02f6d-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="02f6d-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="02f6d-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="02f6d-114">Dieser Wert wird von "System. Photo. subjetdistancenenumerator" und "System. Photo. subjetdistancenenner" generiert.</span><span class="sxs-lookup"><span data-stu-id="02f6d-114">This value is generated from System.Photo.SubjectDistanceNumerator and System.Photo.SubjectDistanceDenominator.</span></span> <span data-ttu-id="02f6d-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="02f6d-115">It cannot be written directly.</span></span> <span data-ttu-id="02f6d-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="02f6d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="02f6d-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="02f6d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="02f6d-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="02f6d-118">Read Paths</span></span>



| <span data-ttu-id="02f6d-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="02f6d-119">Order</span></span> | <span data-ttu-id="02f6d-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="02f6d-120">Path</span></span>                          | <span data-ttu-id="02f6d-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="02f6d-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="02f6d-122">1</span><span class="sxs-lookup"><span data-stu-id="02f6d-122">1</span></span>     | <span data-ttu-id="02f6d-123">/App1/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="02f6d-123">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="02f6d-124">2</span><span class="sxs-lookup"><span data-stu-id="02f6d-124">2</span></span>     | <span data-ttu-id="02f6d-125">/XMP/EXIF: subjetdistance</span><span class="sxs-lookup"><span data-stu-id="02f6d-125">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="02f6d-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="02f6d-126">Write Paths</span></span>



| <span data-ttu-id="02f6d-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="02f6d-127">Order</span></span> | <span data-ttu-id="02f6d-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="02f6d-128">Path</span></span>                          | <span data-ttu-id="02f6d-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="02f6d-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="02f6d-130">1</span><span class="sxs-lookup"><span data-stu-id="02f6d-130">1</span></span>     | <span data-ttu-id="02f6d-131">/App1/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="02f6d-131">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="02f6d-132">2</span><span class="sxs-lookup"><span data-stu-id="02f6d-132">2</span></span>     | <span data-ttu-id="02f6d-133">/XMP/EXIF: subjetdistance</span><span class="sxs-lookup"><span data-stu-id="02f6d-133">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="02f6d-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="02f6d-134">Remove Paths</span></span>



| <span data-ttu-id="02f6d-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="02f6d-135">Order</span></span> | <span data-ttu-id="02f6d-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="02f6d-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="02f6d-137">1</span><span class="sxs-lookup"><span data-stu-id="02f6d-137">1</span></span>     | <span data-ttu-id="02f6d-138">/App1/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="02f6d-138">/app1/ifd/exif/{ushort=37382}</span></span> |
| <span data-ttu-id="02f6d-139">2</span><span class="sxs-lookup"><span data-stu-id="02f6d-139">2</span></span>     | <span data-ttu-id="02f6d-140">/XMP/EXIF: subjetdistance</span><span class="sxs-lookup"><span data-stu-id="02f6d-140">/xmp/exif:subjectdistance</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="02f6d-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="02f6d-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="02f6d-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="02f6d-142">Read Paths</span></span>



| <span data-ttu-id="02f6d-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="02f6d-143">Order</span></span> | <span data-ttu-id="02f6d-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="02f6d-144">Path</span></span>                          | <span data-ttu-id="02f6d-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="02f6d-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="02f6d-146">1</span><span class="sxs-lookup"><span data-stu-id="02f6d-146">1</span></span>     | <span data-ttu-id="02f6d-147">/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="02f6d-147">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="02f6d-148">2</span><span class="sxs-lookup"><span data-stu-id="02f6d-148">2</span></span>     | <span data-ttu-id="02f6d-149">/IFD/XMP/EXIF: subjetdistance</span><span class="sxs-lookup"><span data-stu-id="02f6d-149">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="02f6d-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="02f6d-150">Write Paths</span></span>



| <span data-ttu-id="02f6d-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="02f6d-151">Order</span></span> | <span data-ttu-id="02f6d-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="02f6d-152">Path</span></span>                          | <span data-ttu-id="02f6d-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="02f6d-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="02f6d-154">1</span><span class="sxs-lookup"><span data-stu-id="02f6d-154">1</span></span>     | <span data-ttu-id="02f6d-155">/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="02f6d-155">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="02f6d-156">2</span><span class="sxs-lookup"><span data-stu-id="02f6d-156">2</span></span>     | <span data-ttu-id="02f6d-157">/IFD/XMP/EXIF: subjetdistance</span><span class="sxs-lookup"><span data-stu-id="02f6d-157">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="02f6d-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="02f6d-158">Remove Paths</span></span>



| <span data-ttu-id="02f6d-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="02f6d-159">Order</span></span> | <span data-ttu-id="02f6d-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="02f6d-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="02f6d-161">1</span><span class="sxs-lookup"><span data-stu-id="02f6d-161">1</span></span>     | <span data-ttu-id="02f6d-162">/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="02f6d-162">/ifd/exif/{ushort=37382}</span></span>      |
| <span data-ttu-id="02f6d-163">2</span><span class="sxs-lookup"><span data-stu-id="02f6d-163">2</span></span>     | <span data-ttu-id="02f6d-164">/IFD/XMP/EXIF: subjetdistance</span><span class="sxs-lookup"><span data-stu-id="02f6d-164">/ifd/xmp/exif:subjectdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="02f6d-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02f6d-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="02f6d-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="02f6d-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02f6d-167">System. Photo. subjetdistance</span><span class="sxs-lookup"><span data-stu-id="02f6d-167">System.Photo.SubjectDistance</span></span>](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
