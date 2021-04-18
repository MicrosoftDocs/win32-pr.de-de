---
description: Die fotometadatenrichtlinie für die System. Photo. maxaperture-Eigenschaft.
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: System. Photo. maxaperture-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3dab4d5ebf89033de03dfce887a7cea10fa11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347675"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a><span data-ttu-id="394b2-103">System. Photo. maxaperture-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="394b2-103">System.Photo.MaxAperture Photo Metadata Policy</span></span>

<span data-ttu-id="394b2-104">Die fotometadatenrichtlinie für die [System. Photo. maxaperture](../properties/props-system-photo-maxaperture.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="394b2-104">The photo metadata policy for the [System.Photo.MaxAperture](../properties/props-system-photo-maxaperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="394b2-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="394b2-105">PKEY</span></span>

<span data-ttu-id="394b2-106">Pkey- \_ Foto ( \_ maxaperture)</span><span class="sxs-lookup"><span data-stu-id="394b2-106">PKEY\_Photo\_MaxAperture</span></span>

### <a name="containers"></a><span data-ttu-id="394b2-107">Container</span><span class="sxs-lookup"><span data-stu-id="394b2-107">Containers</span></span>

<span data-ttu-id="394b2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="394b2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="394b2-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="394b2-109">Read-Only</span></span>

<span data-ttu-id="394b2-110">Ja</span><span class="sxs-lookup"><span data-stu-id="394b2-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="394b2-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="394b2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="394b2-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="394b2-112">VT\_R8</span></span>

### <a name="input-type"></a><span data-ttu-id="394b2-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="394b2-113">Input Type</span></span>

<span data-ttu-id="394b2-114">Double</span><span class="sxs-lookup"><span data-stu-id="394b2-114">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="394b2-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="394b2-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="394b2-116">Dieser Wert wird von "System. Photo. maxaperturenumerator" und "System. Photo. maxaperturenenner" generiert.</span><span class="sxs-lookup"><span data-stu-id="394b2-116">This value is generated from System.Photo.MaxApertureNumerator and System.Photo.MaxApertureDenominator.</span></span> <span data-ttu-id="394b2-117">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="394b2-117">It cannot be written directly.</span></span> <span data-ttu-id="394b2-118">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="394b2-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="394b2-119">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="394b2-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="394b2-120">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="394b2-120">Read Paths</span></span>



| <span data-ttu-id="394b2-121">Auftrag</span><span class="sxs-lookup"><span data-stu-id="394b2-121">Order</span></span> | <span data-ttu-id="394b2-122">Pfad</span><span class="sxs-lookup"><span data-stu-id="394b2-122">Path</span></span>                          | <span data-ttu-id="394b2-123">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="394b2-123">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="394b2-124">1</span><span class="sxs-lookup"><span data-stu-id="394b2-124">1</span></span>     | <span data-ttu-id="394b2-125">/App1/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="394b2-125">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="394b2-126">2</span><span class="sxs-lookup"><span data-stu-id="394b2-126">2</span></span>     | <span data-ttu-id="394b2-127">/XMP/EXIF: MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="394b2-127">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="394b2-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="394b2-128">Write Paths</span></span>



| <span data-ttu-id="394b2-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="394b2-129">Order</span></span> | <span data-ttu-id="394b2-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="394b2-130">Path</span></span>                          | <span data-ttu-id="394b2-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="394b2-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="394b2-132">1</span><span class="sxs-lookup"><span data-stu-id="394b2-132">1</span></span>     | <span data-ttu-id="394b2-133">/App1/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="394b2-133">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="394b2-134">2</span><span class="sxs-lookup"><span data-stu-id="394b2-134">2</span></span>     | <span data-ttu-id="394b2-135">/XMP/EXIF: MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="394b2-135">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="394b2-136">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="394b2-136">Remove Paths</span></span>



| <span data-ttu-id="394b2-137">Auftrag</span><span class="sxs-lookup"><span data-stu-id="394b2-137">Order</span></span> | <span data-ttu-id="394b2-138">Pfad</span><span class="sxs-lookup"><span data-stu-id="394b2-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="394b2-139">1</span><span class="sxs-lookup"><span data-stu-id="394b2-139">1</span></span>     | <span data-ttu-id="394b2-140">/App1/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="394b2-140">/app1/ifd/exif/{ushort=37381}</span></span> |
| <span data-ttu-id="394b2-141">2</span><span class="sxs-lookup"><span data-stu-id="394b2-141">2</span></span>     | <span data-ttu-id="394b2-142">/XMP/EXIF: MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="394b2-142">/xmp/exif:maxaperturevalue</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="394b2-143">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="394b2-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="394b2-144">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="394b2-144">Read Paths</span></span>



| <span data-ttu-id="394b2-145">Auftrag</span><span class="sxs-lookup"><span data-stu-id="394b2-145">Order</span></span> | <span data-ttu-id="394b2-146">Pfad</span><span class="sxs-lookup"><span data-stu-id="394b2-146">Path</span></span>                           | <span data-ttu-id="394b2-147">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="394b2-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="394b2-148">1</span><span class="sxs-lookup"><span data-stu-id="394b2-148">1</span></span>     | <span data-ttu-id="394b2-149">/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="394b2-149">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="394b2-150">2</span><span class="sxs-lookup"><span data-stu-id="394b2-150">2</span></span>     | <span data-ttu-id="394b2-151">/IFD/XMP/EXIF: MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="394b2-151">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="394b2-152">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="394b2-152">Write Paths</span></span>



| <span data-ttu-id="394b2-153">Auftrag</span><span class="sxs-lookup"><span data-stu-id="394b2-153">Order</span></span> | <span data-ttu-id="394b2-154">Pfad</span><span class="sxs-lookup"><span data-stu-id="394b2-154">Path</span></span>                           | <span data-ttu-id="394b2-155">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="394b2-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="394b2-156">1</span><span class="sxs-lookup"><span data-stu-id="394b2-156">1</span></span>     | <span data-ttu-id="394b2-157">/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="394b2-157">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="394b2-158">2</span><span class="sxs-lookup"><span data-stu-id="394b2-158">2</span></span>     | <span data-ttu-id="394b2-159">/IFD/XMP/EXIF: MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="394b2-159">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="394b2-160">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="394b2-160">Remove Paths</span></span>



| <span data-ttu-id="394b2-161">Auftrag</span><span class="sxs-lookup"><span data-stu-id="394b2-161">Order</span></span> | <span data-ttu-id="394b2-162">Pfad</span><span class="sxs-lookup"><span data-stu-id="394b2-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="394b2-163">1</span><span class="sxs-lookup"><span data-stu-id="394b2-163">1</span></span>     | <span data-ttu-id="394b2-164">/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="394b2-164">/ifd/exif/{ushort=37381}</span></span>       |
| <span data-ttu-id="394b2-165">2</span><span class="sxs-lookup"><span data-stu-id="394b2-165">2</span></span>     | <span data-ttu-id="394b2-166">/IFD/XMP/EXIF: MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="394b2-166">/ifd/xmp/exif:maxaperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="394b2-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="394b2-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="394b2-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="394b2-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="394b2-169">System. Photo. maxaperture</span><span class="sxs-lookup"><span data-stu-id="394b2-169">System.Photo.MaxAperture</span></span>](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
