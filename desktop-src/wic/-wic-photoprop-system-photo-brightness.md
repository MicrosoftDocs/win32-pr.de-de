---
description: Die fotometadatenrichtlinie für die System. Photo. Brightness-Eigenschaft.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: System. Photo. Helligkeit Photo-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7328b4d40b8d1582dcc17b317b706b2695c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960580"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a><span data-ttu-id="f9521-103">System. Photo. Helligkeit Photo-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="f9521-103">System.Photo.Brightness Photo Metadata Policy</span></span>

<span data-ttu-id="f9521-104">Die fotometadatenrichtlinie für die [System. Photo. Brightness](../properties/props-system-photo-aperture.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f9521-104">The photo metadata policy for the [System.Photo.Brightness](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f9521-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="f9521-105">PKEY</span></span>

<span data-ttu-id="f9521-106">Pkey- \_ Foto \_ Helligkeit</span><span class="sxs-lookup"><span data-stu-id="f9521-106">PKEY\_Photo\_Brightness</span></span>

### <a name="containers"></a><span data-ttu-id="f9521-107">Container</span><span class="sxs-lookup"><span data-stu-id="f9521-107">Containers</span></span>

<span data-ttu-id="f9521-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f9521-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f9521-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9521-109">Read-Only</span></span>

<span data-ttu-id="f9521-110">Ja</span><span class="sxs-lookup"><span data-stu-id="f9521-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="f9521-111">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="f9521-111">Input Type</span></span>

<span data-ttu-id="f9521-112">Double</span><span class="sxs-lookup"><span data-stu-id="f9521-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f9521-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="f9521-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="f9521-114">Dieser Wert wird von "System. Photo. aperturenumerator" und "System. Photo. aperturenenner" generiert.</span><span class="sxs-lookup"><span data-stu-id="f9521-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="f9521-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f9521-115">It cannot be written directly.</span></span> <span data-ttu-id="f9521-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="f9521-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="f9521-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f9521-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f9521-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="f9521-118">Read Paths</span></span>



| <span data-ttu-id="f9521-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f9521-119">Order</span></span> | <span data-ttu-id="f9521-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="f9521-120">Path</span></span>                          | <span data-ttu-id="f9521-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="f9521-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f9521-122">1</span><span class="sxs-lookup"><span data-stu-id="f9521-122">1</span></span>     | <span data-ttu-id="f9521-123">/App1/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="f9521-123">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="f9521-124">2</span><span class="sxs-lookup"><span data-stu-id="f9521-124">2</span></span>     | <span data-ttu-id="f9521-125">/XMP/EXIF: brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="f9521-125">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="f9521-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="f9521-126">Write Paths</span></span>



| <span data-ttu-id="f9521-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f9521-127">Order</span></span> | <span data-ttu-id="f9521-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="f9521-128">Path</span></span>                          | <span data-ttu-id="f9521-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="f9521-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f9521-130">1</span><span class="sxs-lookup"><span data-stu-id="f9521-130">1</span></span>     | <span data-ttu-id="f9521-131">/App1/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="f9521-131">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="f9521-132">2</span><span class="sxs-lookup"><span data-stu-id="f9521-132">2</span></span>     | <span data-ttu-id="f9521-133">/XMP/EXIF: brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="f9521-133">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="f9521-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="f9521-134">Remove Paths</span></span>



| <span data-ttu-id="f9521-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f9521-135">Order</span></span> | <span data-ttu-id="f9521-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="f9521-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="f9521-137">1</span><span class="sxs-lookup"><span data-stu-id="f9521-137">1</span></span>     | <span data-ttu-id="f9521-138">/App1/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="f9521-138">/app1/ifd/exif/{ushort=37379}</span></span> |
| <span data-ttu-id="f9521-139">2</span><span class="sxs-lookup"><span data-stu-id="f9521-139">2</span></span>     | <span data-ttu-id="f9521-140">/XMP/EXIF: brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="f9521-140">/xmp/exif:brightnessvalue</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="f9521-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f9521-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f9521-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="f9521-142">Read Paths</span></span>



| <span data-ttu-id="f9521-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f9521-143">Order</span></span> | <span data-ttu-id="f9521-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="f9521-144">Path</span></span>                          | <span data-ttu-id="f9521-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="f9521-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f9521-146">1</span><span class="sxs-lookup"><span data-stu-id="f9521-146">1</span></span>     | <span data-ttu-id="f9521-147">/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="f9521-147">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="f9521-148">2</span><span class="sxs-lookup"><span data-stu-id="f9521-148">2</span></span>     | <span data-ttu-id="f9521-149">/IFD/XMP/EXIF: brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="f9521-149">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="f9521-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="f9521-150">Write Paths</span></span>



| <span data-ttu-id="f9521-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f9521-151">Order</span></span> | <span data-ttu-id="f9521-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="f9521-152">Path</span></span>                          | <span data-ttu-id="f9521-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="f9521-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f9521-154">1</span><span class="sxs-lookup"><span data-stu-id="f9521-154">1</span></span>     | <span data-ttu-id="f9521-155">/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="f9521-155">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="f9521-156">2</span><span class="sxs-lookup"><span data-stu-id="f9521-156">2</span></span>     | <span data-ttu-id="f9521-157">/IFD/XMP/EXIF: brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="f9521-157">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="f9521-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="f9521-158">Remove Paths</span></span>



| <span data-ttu-id="f9521-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f9521-159">Order</span></span> | <span data-ttu-id="f9521-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="f9521-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="f9521-161">1</span><span class="sxs-lookup"><span data-stu-id="f9521-161">1</span></span>     | <span data-ttu-id="f9521-162">/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="f9521-162">/ifd/exif/{ushort=37379}</span></span>      |
| <span data-ttu-id="f9521-163">2</span><span class="sxs-lookup"><span data-stu-id="f9521-163">2</span></span>     | <span data-ttu-id="f9521-164">/IFD/XMP/EXIF: brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="f9521-164">/ifd/xmp/exif:brightnessvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f9521-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9521-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9521-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9521-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9521-167">System. Photo. Helligkeit</span><span class="sxs-lookup"><span data-stu-id="f9521-167">System.Photo.Brightness</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
