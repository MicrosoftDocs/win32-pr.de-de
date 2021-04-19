---
description: Die fotometadatenrichtlinie für die System. GPS. speedref-Eigenschaft.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: System. GPS. speedref-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363636"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a><span data-ttu-id="6d733-103">System. GPS. speedref-fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="6d733-103">System.GPS.SpeedRef Photo Metadata Policy</span></span>

<span data-ttu-id="6d733-104">Die fotometadatenrichtlinie für die [System. GPS. speedref](../properties/props-system-gps-speedref.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6d733-104">The photo metadata policy for the [System.GPS.SpeedRef](../properties/props-system-gps-speedref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6d733-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="6d733-105">PKEY</span></span>

<span data-ttu-id="6d733-106">Pkey \_ GPS- \_ speedref</span><span class="sxs-lookup"><span data-stu-id="6d733-106">PKEY\_GPS\_SpeedRef</span></span>

### <a name="containers"></a><span data-ttu-id="6d733-107">Container</span><span class="sxs-lookup"><span data-stu-id="6d733-107">Containers</span></span>

<span data-ttu-id="6d733-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6d733-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6d733-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6d733-109">Read-Only</span></span>

<span data-ttu-id="6d733-110">Nein</span><span class="sxs-lookup"><span data-stu-id="6d733-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6d733-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="6d733-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6d733-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="6d733-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="6d733-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="6d733-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="6d733-114">VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird ebenfalls akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="6d733-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted..</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6d733-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="6d733-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="6d733-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="6d733-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="6d733-117">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="6d733-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6d733-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="6d733-118">Read Paths</span></span>



| <span data-ttu-id="6d733-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6d733-119">Order</span></span> | <span data-ttu-id="6d733-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="6d733-120">Path</span></span>                      | <span data-ttu-id="6d733-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="6d733-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="6d733-122">1</span><span class="sxs-lookup"><span data-stu-id="6d733-122">1</span></span>     | <span data-ttu-id="6d733-123">/App1/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="6d733-123">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="6d733-124">ascii</span><span class="sxs-lookup"><span data-stu-id="6d733-124">ascii</span></span>       |
| <span data-ttu-id="6d733-125">2</span><span class="sxs-lookup"><span data-stu-id="6d733-125">2</span></span>     | <span data-ttu-id="6d733-126">/XMP/EXIF: gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="6d733-126">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="6d733-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="6d733-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="6d733-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="6d733-128">Write Paths</span></span>



| <span data-ttu-id="6d733-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6d733-129">Order</span></span> | <span data-ttu-id="6d733-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="6d733-130">Path</span></span>                      | <span data-ttu-id="6d733-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="6d733-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="6d733-132">1</span><span class="sxs-lookup"><span data-stu-id="6d733-132">1</span></span>     | <span data-ttu-id="6d733-133">/App1/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="6d733-133">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="6d733-134">ascii</span><span class="sxs-lookup"><span data-stu-id="6d733-134">ascii</span></span>       |
| <span data-ttu-id="6d733-135">2</span><span class="sxs-lookup"><span data-stu-id="6d733-135">2</span></span>     | <span data-ttu-id="6d733-136">/XMP/EXIF: gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="6d733-136">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="6d733-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="6d733-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="6d733-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="6d733-138">Remove Paths</span></span>



| <span data-ttu-id="6d733-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6d733-139">Order</span></span> | <span data-ttu-id="6d733-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="6d733-140">Path</span></span>                      | <span data-ttu-id="6d733-141">Datenträgerformat</span><span class="sxs-lookup"><span data-stu-id="6d733-141">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="6d733-142">1</span><span class="sxs-lookup"><span data-stu-id="6d733-142">1</span></span>     | <span data-ttu-id="6d733-143">/App1/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="6d733-143">/app1/ifd/gps/{ushort=12}</span></span> |             |
| <span data-ttu-id="6d733-144">2</span><span class="sxs-lookup"><span data-stu-id="6d733-144">2</span></span>     | <span data-ttu-id="6d733-145">/XMP/EXIF: gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="6d733-145">/xmp/exif:gpsspeedref</span></span>     |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="6d733-146">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="6d733-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6d733-147">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="6d733-147">Read Paths</span></span>



| <span data-ttu-id="6d733-148">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6d733-148">Order</span></span> | <span data-ttu-id="6d733-149">Pfad</span><span class="sxs-lookup"><span data-stu-id="6d733-149">Path</span></span>                      |         |
|-------|---------------------------|---------|
| <span data-ttu-id="6d733-150">1</span><span class="sxs-lookup"><span data-stu-id="6d733-150">1</span></span>     | <span data-ttu-id="6d733-151">/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="6d733-151">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="6d733-152">ascii</span><span class="sxs-lookup"><span data-stu-id="6d733-152">ascii</span></span>   |
| <span data-ttu-id="6d733-153">2</span><span class="sxs-lookup"><span data-stu-id="6d733-153">2</span></span>     | <span data-ttu-id="6d733-154">/IFD/XMP/EXIF: gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="6d733-154">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="6d733-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="6d733-155">unicode</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="6d733-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="6d733-156">Write Paths</span></span>



| <span data-ttu-id="6d733-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6d733-157">Order</span></span> | <span data-ttu-id="6d733-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="6d733-158">Path</span></span>                      | <span data-ttu-id="6d733-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="6d733-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="6d733-160">1</span><span class="sxs-lookup"><span data-stu-id="6d733-160">1</span></span>     | <span data-ttu-id="6d733-161">/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="6d733-161">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="6d733-162">ascii</span><span class="sxs-lookup"><span data-stu-id="6d733-162">ascii</span></span>       |
| <span data-ttu-id="6d733-163">2</span><span class="sxs-lookup"><span data-stu-id="6d733-163">2</span></span>     | <span data-ttu-id="6d733-164">/IFD/XMP/EXIF: gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="6d733-164">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="6d733-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="6d733-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="6d733-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="6d733-166">Remove Paths</span></span>



| <span data-ttu-id="6d733-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6d733-167">Order</span></span> | <span data-ttu-id="6d733-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="6d733-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="6d733-169">1</span><span class="sxs-lookup"><span data-stu-id="6d733-169">1</span></span>     | <span data-ttu-id="6d733-170">/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="6d733-170">/ifd/gps/{ushort=12}</span></span>      |
| <span data-ttu-id="6d733-171">2</span><span class="sxs-lookup"><span data-stu-id="6d733-171">2</span></span>     | <span data-ttu-id="6d733-172">/IFD/XMP/EXIF: gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="6d733-172">/ifd/xmp/exif:gpsspeedref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6d733-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d733-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d733-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d733-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d733-175">System. GPS. speedref</span><span class="sxs-lookup"><span data-stu-id="6d733-175">System.GPS.SpeedRef</span></span>](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
