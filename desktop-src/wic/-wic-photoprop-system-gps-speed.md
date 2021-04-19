---
description: Die fotometadatenrichtlinie für die System. GPS. Speed-Eigenschaft.
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: System. GPS. Speed Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363290"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a><span data-ttu-id="54802-103">System. GPS. Speed Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="54802-103">System.GPS.Speed Photo Metadata Policy</span></span>

<span data-ttu-id="54802-104">Die fotometadatenrichtlinie für die [System. GPS. Speed](../properties/props-system-gps-speed.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="54802-104">The photo metadata policy for the [System.GPS.Speed](../properties/props-system-gps-speed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="54802-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="54802-105">PKEY</span></span>

<span data-ttu-id="54802-106">Pkey \_ -GPS- \_ Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="54802-106">PKEY\_GPS\_Speed</span></span>

### <a name="containers"></a><span data-ttu-id="54802-107">Container</span><span class="sxs-lookup"><span data-stu-id="54802-107">Containers</span></span>

<span data-ttu-id="54802-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="54802-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="54802-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54802-109">Read-Only</span></span>

<span data-ttu-id="54802-110">Ja</span><span class="sxs-lookup"><span data-stu-id="54802-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="54802-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="54802-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="54802-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="54802-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="54802-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="54802-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="54802-114">Dieser Wert wird von "System. GPS. speednumerator" und "System. GPS. speednenner" generiert.</span><span class="sxs-lookup"><span data-stu-id="54802-114">This value is generated from System.GPS.SpeedNumerator and System.GPS.SpeedDenominator.</span></span> <span data-ttu-id="54802-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="54802-115">It cannot be written directly.</span></span> <span data-ttu-id="54802-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="54802-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="54802-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="54802-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="54802-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="54802-118">Read Paths</span></span>



| <span data-ttu-id="54802-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="54802-119">Order</span></span> | <span data-ttu-id="54802-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="54802-120">Path</span></span>                      | <span data-ttu-id="54802-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="54802-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="54802-122">1</span><span class="sxs-lookup"><span data-stu-id="54802-122">1</span></span>     | <span data-ttu-id="54802-123">/App1/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="54802-123">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="54802-124">2</span><span class="sxs-lookup"><span data-stu-id="54802-124">2</span></span>     | <span data-ttu-id="54802-125">/XMP/EXIF: gpsspeed</span><span class="sxs-lookup"><span data-stu-id="54802-125">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="54802-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="54802-126">Write Paths</span></span>



| <span data-ttu-id="54802-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="54802-127">Order</span></span> | <span data-ttu-id="54802-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="54802-128">Path</span></span>                      | <span data-ttu-id="54802-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="54802-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="54802-130">1</span><span class="sxs-lookup"><span data-stu-id="54802-130">1</span></span>     | <span data-ttu-id="54802-131">/App1/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="54802-131">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="54802-132">2</span><span class="sxs-lookup"><span data-stu-id="54802-132">2</span></span>     | <span data-ttu-id="54802-133">/XMP/EXIF: gpsspeed</span><span class="sxs-lookup"><span data-stu-id="54802-133">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="54802-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="54802-134">Remove Paths</span></span>



| <span data-ttu-id="54802-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="54802-135">Order</span></span> | <span data-ttu-id="54802-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="54802-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="54802-137">1</span><span class="sxs-lookup"><span data-stu-id="54802-137">1</span></span>     | <span data-ttu-id="54802-138">/App1/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="54802-138">/app1/ifd/gps/{ushort=13}</span></span> |
| <span data-ttu-id="54802-139">2</span><span class="sxs-lookup"><span data-stu-id="54802-139">2</span></span>     | <span data-ttu-id="54802-140">/XMP/EXIF: gpsspeed</span><span class="sxs-lookup"><span data-stu-id="54802-140">/xmp/exif:gpsspeed</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="54802-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="54802-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="54802-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="54802-142">Read Paths</span></span>



| <span data-ttu-id="54802-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="54802-143">Order</span></span> | <span data-ttu-id="54802-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="54802-144">Path</span></span>                   | <span data-ttu-id="54802-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="54802-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="54802-146">1</span><span class="sxs-lookup"><span data-stu-id="54802-146">1</span></span>     | <span data-ttu-id="54802-147">/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="54802-147">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="54802-148">2</span><span class="sxs-lookup"><span data-stu-id="54802-148">2</span></span>     | <span data-ttu-id="54802-149">/IFD/XMP/EXIF: gpsspeed</span><span class="sxs-lookup"><span data-stu-id="54802-149">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="54802-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="54802-150">Write Paths</span></span>



| <span data-ttu-id="54802-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="54802-151">Order</span></span> | <span data-ttu-id="54802-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="54802-152">Path</span></span>                   | <span data-ttu-id="54802-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="54802-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="54802-154">1</span><span class="sxs-lookup"><span data-stu-id="54802-154">1</span></span>     | <span data-ttu-id="54802-155">/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="54802-155">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="54802-156">2</span><span class="sxs-lookup"><span data-stu-id="54802-156">2</span></span>     | <span data-ttu-id="54802-157">/IFD/XMP/EXIF: gpsspeed</span><span class="sxs-lookup"><span data-stu-id="54802-157">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="54802-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="54802-158">Remove Paths</span></span>



| <span data-ttu-id="54802-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="54802-159">Order</span></span> | <span data-ttu-id="54802-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="54802-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="54802-161">1</span><span class="sxs-lookup"><span data-stu-id="54802-161">1</span></span>     | <span data-ttu-id="54802-162">/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="54802-162">/ifd/gps/{ushort=13}</span></span>   |
| <span data-ttu-id="54802-163">2</span><span class="sxs-lookup"><span data-stu-id="54802-163">2</span></span>     | <span data-ttu-id="54802-164">/IFD/XMP/EXIF: gpsspeed</span><span class="sxs-lookup"><span data-stu-id="54802-164">/ifd/xmp/exif:gpsspeed</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="54802-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54802-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="54802-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54802-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54802-167">System. GPS. Speed</span><span class="sxs-lookup"><span data-stu-id="54802-167">System.GPS.Speed</span></span>](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
