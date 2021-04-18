---
description: Die fotometadatenrichtlinie für die System. GPS. Satellites-Eigenschaft.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: System. GPS. Satellites-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980393accdb1bee3d2a44dd539f3c9fb169c648b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368790"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a><span data-ttu-id="7ecf6-103">System. GPS. Satellites-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="7ecf6-103">System.GPS.Satellites Photo Metadata Policy</span></span>

<span data-ttu-id="7ecf6-104">Die fotometadatenrichtlinie für die [System. GPS. Satellites](../properties/props-system-gps-satellites.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7ecf6-104">The photo metadata policy for the [System.GPS.Satellites](../properties/props-system-gps-satellites.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="7ecf6-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="7ecf6-105">PKEY</span></span>

<span data-ttu-id="7ecf6-106">Pkey \_ GPS- \_ Satelliten</span><span class="sxs-lookup"><span data-stu-id="7ecf6-106">PKEY\_GPS\_Satellites</span></span>

### <a name="containers"></a><span data-ttu-id="7ecf6-107">Container</span><span class="sxs-lookup"><span data-stu-id="7ecf6-107">Containers</span></span>

<span data-ttu-id="7ecf6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7ecf6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="7ecf6-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ecf6-109">Read-Only</span></span>

<span data-ttu-id="7ecf6-110">Nein</span><span class="sxs-lookup"><span data-stu-id="7ecf6-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="7ecf6-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="7ecf6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="7ecf6-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="7ecf6-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="7ecf6-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="7ecf6-113">Input Type</span></span>

<span data-ttu-id="7ecf6-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7ecf6-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="7ecf6-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="7ecf6-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="7ecf6-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="7ecf6-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="7ecf6-117">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="7ecf6-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="7ecf6-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="7ecf6-118">Read Paths</span></span>



| <span data-ttu-id="7ecf6-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7ecf6-119">Order</span></span> | <span data-ttu-id="7ecf6-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="7ecf6-120">Path</span></span>                     | <span data-ttu-id="7ecf6-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="7ecf6-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="7ecf6-122">1</span><span class="sxs-lookup"><span data-stu-id="7ecf6-122">1</span></span>     | <span data-ttu-id="7ecf6-123">/App1/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="7ecf6-123">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="7ecf6-124">ascii</span><span class="sxs-lookup"><span data-stu-id="7ecf6-124">ascii</span></span>       |
| <span data-ttu-id="7ecf6-125">2</span><span class="sxs-lookup"><span data-stu-id="7ecf6-125">2</span></span>     | <span data-ttu-id="7ecf6-126">/XMP/EXIF: gpssatellites</span><span class="sxs-lookup"><span data-stu-id="7ecf6-126">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="7ecf6-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="7ecf6-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7ecf6-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="7ecf6-128">Write Paths</span></span>



| <span data-ttu-id="7ecf6-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7ecf6-129">Order</span></span> | <span data-ttu-id="7ecf6-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="7ecf6-130">Path</span></span>                     | <span data-ttu-id="7ecf6-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="7ecf6-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="7ecf6-132">1</span><span class="sxs-lookup"><span data-stu-id="7ecf6-132">1</span></span>     | <span data-ttu-id="7ecf6-133">/App1/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="7ecf6-133">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="7ecf6-134">ascii</span><span class="sxs-lookup"><span data-stu-id="7ecf6-134">ascii</span></span>       |
| <span data-ttu-id="7ecf6-135">2</span><span class="sxs-lookup"><span data-stu-id="7ecf6-135">2</span></span>     | <span data-ttu-id="7ecf6-136">/XMP/EXIF: gpssatellites</span><span class="sxs-lookup"><span data-stu-id="7ecf6-136">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="7ecf6-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="7ecf6-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7ecf6-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="7ecf6-138">Remove Paths</span></span>



| <span data-ttu-id="7ecf6-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7ecf6-139">Order</span></span> | <span data-ttu-id="7ecf6-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="7ecf6-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="7ecf6-141">1</span><span class="sxs-lookup"><span data-stu-id="7ecf6-141">1</span></span>     | <span data-ttu-id="7ecf6-142">/App1/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="7ecf6-142">/app1/ifd/gps/{ushort=8}</span></span> |
| <span data-ttu-id="7ecf6-143">2</span><span class="sxs-lookup"><span data-stu-id="7ecf6-143">2</span></span>     | <span data-ttu-id="7ecf6-144">/XMP/EXIF: gpssatellites</span><span class="sxs-lookup"><span data-stu-id="7ecf6-144">/xmp/exif:gpssatellites</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="7ecf6-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="7ecf6-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="7ecf6-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="7ecf6-146">Read Paths</span></span>



| <span data-ttu-id="7ecf6-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7ecf6-147">Order</span></span> | <span data-ttu-id="7ecf6-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="7ecf6-148">Path</span></span>                        | <span data-ttu-id="7ecf6-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="7ecf6-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="7ecf6-150">1</span><span class="sxs-lookup"><span data-stu-id="7ecf6-150">1</span></span>     | <span data-ttu-id="7ecf6-151">/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="7ecf6-151">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="7ecf6-152">ascii</span><span class="sxs-lookup"><span data-stu-id="7ecf6-152">ascii</span></span>       |
| <span data-ttu-id="7ecf6-153">2</span><span class="sxs-lookup"><span data-stu-id="7ecf6-153">2</span></span>     | <span data-ttu-id="7ecf6-154">/IFD/XMP/EXIF: gpssatellites</span><span class="sxs-lookup"><span data-stu-id="7ecf6-154">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="7ecf6-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="7ecf6-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7ecf6-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="7ecf6-156">Write Paths</span></span>



| <span data-ttu-id="7ecf6-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7ecf6-157">Order</span></span> | <span data-ttu-id="7ecf6-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="7ecf6-158">Path</span></span>                        | <span data-ttu-id="7ecf6-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="7ecf6-159">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="7ecf6-160">1</span><span class="sxs-lookup"><span data-stu-id="7ecf6-160">1</span></span>     | <span data-ttu-id="7ecf6-161">/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="7ecf6-161">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="7ecf6-162">ascii</span><span class="sxs-lookup"><span data-stu-id="7ecf6-162">ascii</span></span>       |
| <span data-ttu-id="7ecf6-163">2</span><span class="sxs-lookup"><span data-stu-id="7ecf6-163">2</span></span>     | <span data-ttu-id="7ecf6-164">/IFD/XMP/EXIF: gpssatellites</span><span class="sxs-lookup"><span data-stu-id="7ecf6-164">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="7ecf6-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="7ecf6-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7ecf6-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="7ecf6-166">Remove Paths</span></span>



| <span data-ttu-id="7ecf6-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7ecf6-167">Order</span></span> | <span data-ttu-id="7ecf6-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="7ecf6-168">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="7ecf6-169">1</span><span class="sxs-lookup"><span data-stu-id="7ecf6-169">1</span></span>     | <span data-ttu-id="7ecf6-170">/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="7ecf6-170">/ifd/gps/{ushort=8}</span></span>         |
| <span data-ttu-id="7ecf6-171">2</span><span class="sxs-lookup"><span data-stu-id="7ecf6-171">2</span></span>     | <span data-ttu-id="7ecf6-172">/IFD/XMP/EXIF: gpssatellites</span><span class="sxs-lookup"><span data-stu-id="7ecf6-172">/ifd/xmp/exif:gpssatellites</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7ecf6-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ecf6-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ecf6-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7ecf6-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ecf6-175">System. GPS. Satelliten</span><span class="sxs-lookup"><span data-stu-id="7ecf6-175">System.GPS.Satellites</span></span>](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
