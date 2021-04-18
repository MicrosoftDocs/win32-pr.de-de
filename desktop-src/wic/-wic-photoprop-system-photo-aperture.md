---
description: Die fotometadatenrichtlinie für die System. Photo. Aperture-Eigenschaft.
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: System. Photo. Aperture-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352674"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a><span data-ttu-id="a56a3-103">System. Photo. Aperture-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="a56a3-103">System.Photo.Aperture Photo Metadata Policy</span></span>

<span data-ttu-id="a56a3-104">Die fotometadatenrichtlinie für die [System. Photo. Aperture](../properties/props-system-photo-aperture.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a56a3-104">The photo metadata policy for the [System.Photo.Aperture](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a56a3-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="a56a3-105">PKEY</span></span>

<span data-ttu-id="a56a3-106">Pkey- \_ Foto- \_ Aperture</span><span class="sxs-lookup"><span data-stu-id="a56a3-106">PKEY\_Photo\_Aperture</span></span>

### <a name="containers"></a><span data-ttu-id="a56a3-107">Container</span><span class="sxs-lookup"><span data-stu-id="a56a3-107">Containers</span></span>

<span data-ttu-id="a56a3-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a56a3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a56a3-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a56a3-109">Read-Only</span></span>

<span data-ttu-id="a56a3-110">Ja</span><span class="sxs-lookup"><span data-stu-id="a56a3-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a56a3-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="a56a3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a56a3-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="a56a3-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a56a3-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="a56a3-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="a56a3-114">Dieser Wert wird von "System. Photo. aperturenumerator" und "System. Photo. aperturenenner" generiert.</span><span class="sxs-lookup"><span data-stu-id="a56a3-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="a56a3-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a56a3-115">It cannot be written directly.</span></span> <span data-ttu-id="a56a3-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="a56a3-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a56a3-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a56a3-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a56a3-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="a56a3-118">Read Paths</span></span>



| <span data-ttu-id="a56a3-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a56a3-119">Order</span></span> | <span data-ttu-id="a56a3-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="a56a3-120">Path</span></span>                          | <span data-ttu-id="a56a3-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a56a3-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a56a3-122">1</span><span class="sxs-lookup"><span data-stu-id="a56a3-122">1</span></span>     | <span data-ttu-id="a56a3-123">/App1/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="a56a3-123">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="a56a3-124">2</span><span class="sxs-lookup"><span data-stu-id="a56a3-124">2</span></span>     | <span data-ttu-id="a56a3-125">/XMP/EXIF: aperturevalue</span><span class="sxs-lookup"><span data-stu-id="a56a3-125">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="write-paths"></a><span data-ttu-id="a56a3-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="a56a3-126">Write Paths</span></span>



| <span data-ttu-id="a56a3-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a56a3-127">Order</span></span> | <span data-ttu-id="a56a3-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="a56a3-128">Path</span></span>                          | <span data-ttu-id="a56a3-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a56a3-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a56a3-130">1</span><span class="sxs-lookup"><span data-stu-id="a56a3-130">1</span></span>     | <span data-ttu-id="a56a3-131">/App1/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="a56a3-131">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="a56a3-132">2</span><span class="sxs-lookup"><span data-stu-id="a56a3-132">2</span></span>     | <span data-ttu-id="a56a3-133">/XMP/EXIF: aperturevalue</span><span class="sxs-lookup"><span data-stu-id="a56a3-133">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a56a3-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="a56a3-134">Remove Paths</span></span>



| <span data-ttu-id="a56a3-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a56a3-135">Order</span></span> | <span data-ttu-id="a56a3-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="a56a3-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="a56a3-137">1</span><span class="sxs-lookup"><span data-stu-id="a56a3-137">1</span></span>     | <span data-ttu-id="a56a3-138">/App1/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="a56a3-138">/app1/ifd/exif/{ushort=37378}</span></span> |
| <span data-ttu-id="a56a3-139">2</span><span class="sxs-lookup"><span data-stu-id="a56a3-139">2</span></span>     | <span data-ttu-id="a56a3-140">/XMP/EXIF: aperturevalue</span><span class="sxs-lookup"><span data-stu-id="a56a3-140">/xmp/exif:aperturevalue</span></span>       |



 

### <a name="tiff-policies"></a><span data-ttu-id="a56a3-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="a56a3-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a56a3-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="a56a3-142">Read Paths</span></span>



| <span data-ttu-id="a56a3-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a56a3-143">Order</span></span> | <span data-ttu-id="a56a3-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="a56a3-144">Path</span></span>                        | <span data-ttu-id="a56a3-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a56a3-145">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="a56a3-146">1</span><span class="sxs-lookup"><span data-stu-id="a56a3-146">1</span></span>     | <span data-ttu-id="a56a3-147">/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="a56a3-147">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="a56a3-148">2</span><span class="sxs-lookup"><span data-stu-id="a56a3-148">2</span></span>     | <span data-ttu-id="a56a3-149">/IFD/XMP/EXIF: aperturevalue</span><span class="sxs-lookup"><span data-stu-id="a56a3-149">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="a56a3-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="a56a3-150">Write Paths</span></span>



| <span data-ttu-id="a56a3-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a56a3-151">Order</span></span> | <span data-ttu-id="a56a3-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="a56a3-152">Path</span></span>                        | <span data-ttu-id="a56a3-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a56a3-153">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="a56a3-154">1</span><span class="sxs-lookup"><span data-stu-id="a56a3-154">1</span></span>     | <span data-ttu-id="a56a3-155">/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="a56a3-155">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="a56a3-156">2</span><span class="sxs-lookup"><span data-stu-id="a56a3-156">2</span></span>     | <span data-ttu-id="a56a3-157">/IFD/XMP/EXIF: aperturevalue</span><span class="sxs-lookup"><span data-stu-id="a56a3-157">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a56a3-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="a56a3-158">Remove Paths</span></span>



| <span data-ttu-id="a56a3-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a56a3-159">Order</span></span> | <span data-ttu-id="a56a3-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="a56a3-160">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="a56a3-161">1</span><span class="sxs-lookup"><span data-stu-id="a56a3-161">1</span></span>     | <span data-ttu-id="a56a3-162">/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="a56a3-162">/ifd/exif/{ushort=37378}</span></span>    |
| <span data-ttu-id="a56a3-163">2</span><span class="sxs-lookup"><span data-stu-id="a56a3-163">2</span></span>     | <span data-ttu-id="a56a3-164">/IFD/XMP/EXIF: aperturevalue</span><span class="sxs-lookup"><span data-stu-id="a56a3-164">/ifd/xmp/exif:aperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a56a3-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a56a3-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a56a3-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a56a3-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a56a3-167">System. Photo. Aperture</span><span class="sxs-lookup"><span data-stu-id="a56a3-167">System.Photo.Aperture</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
