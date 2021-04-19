---
description: Die fotometadatenrichtlinie für die System. GPS. destdistance-Eigenschaft.
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: System. GPS. destdistance-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc71c89ae6270f5babf08637f54baaf2cb57aae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363573"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a><span data-ttu-id="0b259-103">System. GPS. destdistance-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="0b259-103">System.GPS.DestDistance Photo Metadata Policy</span></span>

<span data-ttu-id="0b259-104">Die fotometadatenrichtlinie für die [System. GPS. destdistance](../properties/props-system-gps-destdistance.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0b259-104">The photo metadata policy for the [System.GPS.DestDistance](../properties/props-system-gps-destdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0b259-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="0b259-105">PKEY</span></span>

<span data-ttu-id="0b259-106">Pkey \_ GPS \_ destdistance</span><span class="sxs-lookup"><span data-stu-id="0b259-106">PKEY\_GPS\_DestDistance</span></span>

### <a name="containers"></a><span data-ttu-id="0b259-107">Container</span><span class="sxs-lookup"><span data-stu-id="0b259-107">Containers</span></span>

<span data-ttu-id="0b259-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="0b259-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0b259-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0b259-109">Read-Only</span></span>

<span data-ttu-id="0b259-110">Ja</span><span class="sxs-lookup"><span data-stu-id="0b259-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="0b259-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="0b259-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="0b259-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="0b259-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0b259-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="0b259-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="0b259-114">Dieser Wert wird von System. GPS. destdistancenenumerator und System. GPS. destdistancenenner generiert.</span><span class="sxs-lookup"><span data-stu-id="0b259-114">This value is generated from System.GPS.DestDistanceNumerator and System.GPS.DestDistanceDenominator.</span></span> <span data-ttu-id="0b259-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0b259-115">It cannot be written directly.</span></span> <span data-ttu-id="0b259-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="0b259-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="0b259-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="0b259-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="0b259-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="0b259-118">Read Paths</span></span>



| <span data-ttu-id="0b259-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0b259-119">Order</span></span> | <span data-ttu-id="0b259-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="0b259-120">Path</span></span>                      | <span data-ttu-id="0b259-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="0b259-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="0b259-122">1</span><span class="sxs-lookup"><span data-stu-id="0b259-122">1</span></span>     | <span data-ttu-id="0b259-123">/App1/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="0b259-123">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="0b259-124">2</span><span class="sxs-lookup"><span data-stu-id="0b259-124">2</span></span>     | <span data-ttu-id="0b259-125">/XMP/EXIF: gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="0b259-125">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="0b259-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="0b259-126">Write Paths</span></span>



| <span data-ttu-id="0b259-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0b259-127">Order</span></span> | <span data-ttu-id="0b259-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="0b259-128">Path</span></span>                      | <span data-ttu-id="0b259-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="0b259-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="0b259-130">1</span><span class="sxs-lookup"><span data-stu-id="0b259-130">1</span></span>     | <span data-ttu-id="0b259-131">/App1/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="0b259-131">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="0b259-132">2</span><span class="sxs-lookup"><span data-stu-id="0b259-132">2</span></span>     | <span data-ttu-id="0b259-133">/XMP/EXIF: gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="0b259-133">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="0b259-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="0b259-134">Remove Paths</span></span>



| <span data-ttu-id="0b259-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0b259-135">Order</span></span> | <span data-ttu-id="0b259-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="0b259-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="0b259-137">1</span><span class="sxs-lookup"><span data-stu-id="0b259-137">1</span></span>     | <span data-ttu-id="0b259-138">/App1/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="0b259-138">/app1/ifd/gps/{ushort=26}</span></span> |
| <span data-ttu-id="0b259-139">2</span><span class="sxs-lookup"><span data-stu-id="0b259-139">2</span></span>     | <span data-ttu-id="0b259-140">/XMP/EXIF: gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="0b259-140">/xmp/exif:gpsdestdistance</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="0b259-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="0b259-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0b259-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="0b259-142">Read Paths</span></span>



| <span data-ttu-id="0b259-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0b259-143">Order</span></span> | <span data-ttu-id="0b259-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="0b259-144">Path</span></span>                          | <span data-ttu-id="0b259-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="0b259-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0b259-146">1</span><span class="sxs-lookup"><span data-stu-id="0b259-146">1</span></span>     | <span data-ttu-id="0b259-147">/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="0b259-147">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="0b259-148">2</span><span class="sxs-lookup"><span data-stu-id="0b259-148">2</span></span>     | <span data-ttu-id="0b259-149">/IFD/XMP/EXIF: gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="0b259-149">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="0b259-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="0b259-150">Write Paths</span></span>



| <span data-ttu-id="0b259-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0b259-151">Order</span></span> | <span data-ttu-id="0b259-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="0b259-152">Path</span></span>                          | <span data-ttu-id="0b259-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="0b259-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0b259-154">1</span><span class="sxs-lookup"><span data-stu-id="0b259-154">1</span></span>     | <span data-ttu-id="0b259-155">/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="0b259-155">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="0b259-156">2</span><span class="sxs-lookup"><span data-stu-id="0b259-156">2</span></span>     | <span data-ttu-id="0b259-157">/IFD/XMP/EXIF: gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="0b259-157">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="0b259-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="0b259-158">Remove Paths</span></span>



| <span data-ttu-id="0b259-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0b259-159">Order</span></span> | <span data-ttu-id="0b259-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="0b259-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="0b259-161">1</span><span class="sxs-lookup"><span data-stu-id="0b259-161">1</span></span>     | <span data-ttu-id="0b259-162">/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="0b259-162">/ifd/gps/{ushort=26}</span></span>          |
| <span data-ttu-id="0b259-163">2</span><span class="sxs-lookup"><span data-stu-id="0b259-163">2</span></span>     | <span data-ttu-id="0b259-164">/IFD/XMP/EXIF: gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="0b259-164">/ifd/xmp/exif:gpsdestdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0b259-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b259-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b259-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b259-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b259-167">System. GPS. destdistance</span><span class="sxs-lookup"><span data-stu-id="0b259-167">System.GPS.DestDistance</span></span>](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
