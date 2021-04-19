---
description: Die fotometadatenrichtlinie für die System. GPS. destlatitude-Eigenschaft.
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: System. GPS. destlatitude-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192db0f8efc868e9457e86d283d9967e4692c95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351063"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a><span data-ttu-id="b3f12-103">System. GPS. destlatitude-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b3f12-103">System.GPS.DestLatitude Photo Metadata Policy</span></span>

<span data-ttu-id="b3f12-104">Die fotometadatenrichtlinie für die [System. GPS. destlatitude](../properties/props-system-gps-destlatitude.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b3f12-104">The photo metadata policy for the [System.GPS.DestLatitude](../properties/props-system-gps-destlatitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b3f12-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="b3f12-105">PKEY</span></span>

<span data-ttu-id="b3f12-106">Pkey \_ GPS \_ destlatitude</span><span class="sxs-lookup"><span data-stu-id="b3f12-106">PKEY\_GPS\_DestLatitude</span></span>

### <a name="containers"></a><span data-ttu-id="b3f12-107">Container</span><span class="sxs-lookup"><span data-stu-id="b3f12-107">Containers</span></span>

<span data-ttu-id="b3f12-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b3f12-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b3f12-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3f12-109">Read-Only</span></span>

<span data-ttu-id="b3f12-110">Ja</span><span class="sxs-lookup"><span data-stu-id="b3f12-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b3f12-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="b3f12-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b3f12-112">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="b3f12-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="b3f12-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="b3f12-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="b3f12-114">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="b3f12-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b3f12-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="b3f12-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b3f12-116">Dieser Wert wird von "System. GPS. destlatitudenenumerator" und "System. GPS. destlatitudebug" generiert.</span><span class="sxs-lookup"><span data-stu-id="b3f12-116">This value is generated from System.GPS.DestLatitudeNumerator and System.GPS.DestLatitudeDenominator.</span></span> <span data-ttu-id="b3f12-117">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b3f12-117">It cannot be written directly.</span></span> <span data-ttu-id="b3f12-118">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="b3f12-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b3f12-119">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b3f12-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b3f12-120">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="b3f12-120">Read Paths</span></span>



| <span data-ttu-id="b3f12-121">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b3f12-121">Order</span></span> | <span data-ttu-id="b3f12-122">Pfad</span><span class="sxs-lookup"><span data-stu-id="b3f12-122">Path</span></span>                      | <span data-ttu-id="b3f12-123">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b3f12-123">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b3f12-124">1</span><span class="sxs-lookup"><span data-stu-id="b3f12-124">1</span></span>     | <span data-ttu-id="b3f12-125">/App1/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="b3f12-125">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="b3f12-126">2</span><span class="sxs-lookup"><span data-stu-id="b3f12-126">2</span></span>     | <span data-ttu-id="b3f12-127">/XMP/EXIF: gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="b3f12-127">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b3f12-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="b3f12-128">Write Paths</span></span>



| <span data-ttu-id="b3f12-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b3f12-129">Order</span></span> | <span data-ttu-id="b3f12-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="b3f12-130">Path</span></span>                      | <span data-ttu-id="b3f12-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b3f12-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b3f12-132">1</span><span class="sxs-lookup"><span data-stu-id="b3f12-132">1</span></span>     | <span data-ttu-id="b3f12-133">/App1/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="b3f12-133">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="b3f12-134">2</span><span class="sxs-lookup"><span data-stu-id="b3f12-134">2</span></span>     | <span data-ttu-id="b3f12-135">/XMP/EXIF: gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="b3f12-135">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b3f12-136">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="b3f12-136">Remove Paths</span></span>



| <span data-ttu-id="b3f12-137">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b3f12-137">Order</span></span> | <span data-ttu-id="b3f12-138">Pfad</span><span class="sxs-lookup"><span data-stu-id="b3f12-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="b3f12-139">1</span><span class="sxs-lookup"><span data-stu-id="b3f12-139">1</span></span>     | <span data-ttu-id="b3f12-140">/App1/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="b3f12-140">/app1/ifd/gps/{ushort=20}</span></span> |
| <span data-ttu-id="b3f12-141">2</span><span class="sxs-lookup"><span data-stu-id="b3f12-141">2</span></span>     | <span data-ttu-id="b3f12-142">/XMP/EXIF: gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="b3f12-142">/xmp/exif:gpsdestlatitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="b3f12-143">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="b3f12-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b3f12-144">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="b3f12-144">Read Paths</span></span>



| <span data-ttu-id="b3f12-145">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b3f12-145">Order</span></span> | <span data-ttu-id="b3f12-146">Pfad</span><span class="sxs-lookup"><span data-stu-id="b3f12-146">Path</span></span>                          | <span data-ttu-id="b3f12-147">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b3f12-147">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b3f12-148">1</span><span class="sxs-lookup"><span data-stu-id="b3f12-148">1</span></span>     | <span data-ttu-id="b3f12-149">/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="b3f12-149">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="b3f12-150">2</span><span class="sxs-lookup"><span data-stu-id="b3f12-150">2</span></span>     | <span data-ttu-id="b3f12-151">/IFD/XMP/EXIF: gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="b3f12-151">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b3f12-152">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="b3f12-152">Write Paths</span></span>



| <span data-ttu-id="b3f12-153">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b3f12-153">Order</span></span> | <span data-ttu-id="b3f12-154">Pfad</span><span class="sxs-lookup"><span data-stu-id="b3f12-154">Path</span></span>                          | <span data-ttu-id="b3f12-155">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b3f12-155">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b3f12-156">1</span><span class="sxs-lookup"><span data-stu-id="b3f12-156">1</span></span>     | <span data-ttu-id="b3f12-157">/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="b3f12-157">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="b3f12-158">2</span><span class="sxs-lookup"><span data-stu-id="b3f12-158">2</span></span>     | <span data-ttu-id="b3f12-159">/IFD/XMP/EXIF: gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="b3f12-159">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b3f12-160">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="b3f12-160">Remove Paths</span></span>



| <span data-ttu-id="b3f12-161">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b3f12-161">Order</span></span> | <span data-ttu-id="b3f12-162">Pfad</span><span class="sxs-lookup"><span data-stu-id="b3f12-162">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="b3f12-163">1</span><span class="sxs-lookup"><span data-stu-id="b3f12-163">1</span></span>     | <span data-ttu-id="b3f12-164">/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="b3f12-164">/ifd/gps/{ushort=20}</span></span>          |
| <span data-ttu-id="b3f12-165">2</span><span class="sxs-lookup"><span data-stu-id="b3f12-165">2</span></span>     | <span data-ttu-id="b3f12-166">/IFD/XMP/EXIF: gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="b3f12-166">/ifd/xmp/exif:gpsdestlatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b3f12-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3f12-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3f12-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3f12-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3f12-169">System. GPS. destlatitude</span><span class="sxs-lookup"><span data-stu-id="b3f12-169">System.GPS.DestLatitude</span></span>](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
