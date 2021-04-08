---
description: Die fotometadatenrichtlinie für die System. GPS. destlongitude-Eigenschaft.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: System. GPS. destlongitude-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e0a4f56e49dfbb3397b96cf7fae35a6065b7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050302"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a><span data-ttu-id="9599b-103">System. GPS. destlongitude-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="9599b-103">System.GPS.DestLongitude Photo Metadata Policy</span></span>

<span data-ttu-id="9599b-104">Die fotometadatenrichtlinie für die [System. GPS. destlongitude](../properties/props-system-gps-destlongitude.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9599b-104">The photo metadata policy for the [System.GPS.DestLongitude](../properties/props-system-gps-destlongitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9599b-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="9599b-105">PKEY</span></span>

<span data-ttu-id="9599b-106">Pkey \_ GPS \_ destlängen Grade</span><span class="sxs-lookup"><span data-stu-id="9599b-106">PKEY\_GPS\_DestLongitude</span></span>

### <a name="containers"></a><span data-ttu-id="9599b-107">Container</span><span class="sxs-lookup"><span data-stu-id="9599b-107">Containers</span></span>

<span data-ttu-id="9599b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9599b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9599b-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9599b-109">Read-Only</span></span>

<span data-ttu-id="9599b-110">Ja</span><span class="sxs-lookup"><span data-stu-id="9599b-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9599b-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="9599b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9599b-112">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="9599b-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="9599b-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="9599b-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="9599b-114">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="9599b-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9599b-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="9599b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="9599b-116">Dieser Wert wird von "System. GPS. destlängs denenumerator" und "System. GPS. dest-Debug" generiert.</span><span class="sxs-lookup"><span data-stu-id="9599b-116">This value is generated from System.GPS.DestLongitudeNumerator and System.GPS.DestLongitudeDenominator.</span></span> <span data-ttu-id="9599b-117">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9599b-117">It cannot be written directly.</span></span> <span data-ttu-id="9599b-118">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="9599b-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9599b-119">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="9599b-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9599b-120">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="9599b-120">Read Paths</span></span>



| <span data-ttu-id="9599b-121">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9599b-121">Order</span></span> | <span data-ttu-id="9599b-122">Pfad</span><span class="sxs-lookup"><span data-stu-id="9599b-122">Path</span></span>                       | <span data-ttu-id="9599b-123">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9599b-123">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="9599b-124">1</span><span class="sxs-lookup"><span data-stu-id="9599b-124">1</span></span>     | <span data-ttu-id="9599b-125">/App1/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="9599b-125">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="9599b-126">2</span><span class="sxs-lookup"><span data-stu-id="9599b-126">2</span></span>     | <span data-ttu-id="9599b-127">/XMP/EXIF: gpsdestlängen Grad</span><span class="sxs-lookup"><span data-stu-id="9599b-127">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="9599b-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="9599b-128">Write Paths</span></span>



| <span data-ttu-id="9599b-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9599b-129">Order</span></span> | <span data-ttu-id="9599b-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="9599b-130">Path</span></span>                       | <span data-ttu-id="9599b-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9599b-131">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="9599b-132">1</span><span class="sxs-lookup"><span data-stu-id="9599b-132">1</span></span>     | <span data-ttu-id="9599b-133">/App1/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="9599b-133">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="9599b-134">2</span><span class="sxs-lookup"><span data-stu-id="9599b-134">2</span></span>     | <span data-ttu-id="9599b-135">/XMP/EXIF: gpsdestlängen Grad</span><span class="sxs-lookup"><span data-stu-id="9599b-135">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9599b-136">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="9599b-136">Remove Paths</span></span>



| <span data-ttu-id="9599b-137">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9599b-137">Order</span></span> | <span data-ttu-id="9599b-138">Pfad</span><span class="sxs-lookup"><span data-stu-id="9599b-138">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="9599b-139">1</span><span class="sxs-lookup"><span data-stu-id="9599b-139">1</span></span>     | <span data-ttu-id="9599b-140">/App1/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="9599b-140">/app1/ifd/gps/{ushort=22}</span></span>  |
| <span data-ttu-id="9599b-141">2</span><span class="sxs-lookup"><span data-stu-id="9599b-141">2</span></span>     | <span data-ttu-id="9599b-142">/XMP/EXIF: gpsdestlängen Grad</span><span class="sxs-lookup"><span data-stu-id="9599b-142">/xmp/exif:gpsdestlongitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="9599b-143">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="9599b-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9599b-144">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="9599b-144">Read Paths</span></span>



| <span data-ttu-id="9599b-145">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9599b-145">Order</span></span> | <span data-ttu-id="9599b-146">Pfad</span><span class="sxs-lookup"><span data-stu-id="9599b-146">Path</span></span>                           | <span data-ttu-id="9599b-147">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9599b-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="9599b-148">1</span><span class="sxs-lookup"><span data-stu-id="9599b-148">1</span></span>     | <span data-ttu-id="9599b-149">/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="9599b-149">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="9599b-150">2</span><span class="sxs-lookup"><span data-stu-id="9599b-150">2</span></span>     | <span data-ttu-id="9599b-151">/IFD/XMP/EXIF: gpsdestlängen Grad</span><span class="sxs-lookup"><span data-stu-id="9599b-151">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="9599b-152">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="9599b-152">Write Paths</span></span>



| <span data-ttu-id="9599b-153">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9599b-153">Order</span></span> | <span data-ttu-id="9599b-154">Pfad</span><span class="sxs-lookup"><span data-stu-id="9599b-154">Path</span></span>                           | <span data-ttu-id="9599b-155">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9599b-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="9599b-156">1</span><span class="sxs-lookup"><span data-stu-id="9599b-156">1</span></span>     | <span data-ttu-id="9599b-157">/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="9599b-157">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="9599b-158">2</span><span class="sxs-lookup"><span data-stu-id="9599b-158">2</span></span>     | <span data-ttu-id="9599b-159">/IFD/XMP/EXIF: gpsdestlängen Grad</span><span class="sxs-lookup"><span data-stu-id="9599b-159">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9599b-160">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="9599b-160">Remove Paths</span></span>



| <span data-ttu-id="9599b-161">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9599b-161">Order</span></span> | <span data-ttu-id="9599b-162">Pfad</span><span class="sxs-lookup"><span data-stu-id="9599b-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="9599b-163">1</span><span class="sxs-lookup"><span data-stu-id="9599b-163">1</span></span>     | <span data-ttu-id="9599b-164">/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="9599b-164">/ifd/gps/{ushort=22}</span></span>           |
| <span data-ttu-id="9599b-165">2</span><span class="sxs-lookup"><span data-stu-id="9599b-165">2</span></span>     | <span data-ttu-id="9599b-166">/IFD/XMP/EXIF: gpsdestlängen Grad</span><span class="sxs-lookup"><span data-stu-id="9599b-166">/ifd/xmp/exif:gpsdestlongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9599b-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9599b-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9599b-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9599b-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9599b-169">System. GPS. destlongitude</span><span class="sxs-lookup"><span data-stu-id="9599b-169">System.GPS.DestLongitude</span></span>](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
