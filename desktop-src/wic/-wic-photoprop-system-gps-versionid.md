---
description: Die fotometadatenrichtlinie für die System. GPS. versionID-Eigenschaft.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: System. GPS. versionID Photo-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ca5bd1885f0ac5c3dc14dbb5e859de3f8a26cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362266"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a><span data-ttu-id="fffe8-103">System. GPS. versionID Photo-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="fffe8-103">System.GPS.VersionID Photo Metadata Policy</span></span>

<span data-ttu-id="fffe8-104">Die fotometadatenrichtlinie für die [System. GPS. versionID](../properties/props-system-gps-versionid.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="fffe8-104">The photo metadata policy for the [System.GPS.VersionID](../properties/props-system-gps-versionid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="fffe8-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="fffe8-105">PKEY</span></span>

<span data-ttu-id="fffe8-106">Pkey \_ GPS \_ versionID</span><span class="sxs-lookup"><span data-stu-id="fffe8-106">PKEY\_GPS\_VersionID</span></span>

### <a name="containers"></a><span data-ttu-id="fffe8-107">Container</span><span class="sxs-lookup"><span data-stu-id="fffe8-107">Containers</span></span>

<span data-ttu-id="fffe8-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="fffe8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="fffe8-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fffe8-109">Read-Only</span></span>

<span data-ttu-id="fffe8-110">Nein</span><span class="sxs-lookup"><span data-stu-id="fffe8-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="fffe8-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="fffe8-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="fffe8-112">VT \_ Vector \| VT \_ UI</span><span class="sxs-lookup"><span data-stu-id="fffe8-112">VT\_VECTOR \| VT\_UI</span></span>

### <a name="input-type"></a><span data-ttu-id="fffe8-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="fffe8-113">Input Type</span></span>

<span data-ttu-id="fffe8-114">Buffer</span><span class="sxs-lookup"><span data-stu-id="fffe8-114">Buffer</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="fffe8-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="fffe8-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="fffe8-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="fffe8-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="fffe8-117">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="fffe8-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="fffe8-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="fffe8-118">Read Paths</span></span>



| <span data-ttu-id="fffe8-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fffe8-119">Order</span></span> | <span data-ttu-id="fffe8-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="fffe8-120">Path</span></span>                     | <span data-ttu-id="fffe8-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fffe8-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="fffe8-122">1</span><span class="sxs-lookup"><span data-stu-id="fffe8-122">1</span></span>     | <span data-ttu-id="fffe8-123">/App1/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="fffe8-123">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="fffe8-124">2</span><span class="sxs-lookup"><span data-stu-id="fffe8-124">2</span></span>     | <span data-ttu-id="fffe8-125">/XMP/EXIF: gpsversionid</span><span class="sxs-lookup"><span data-stu-id="fffe8-125">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="fffe8-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="fffe8-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="fffe8-127">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="fffe8-127">Write Paths</span></span>



| <span data-ttu-id="fffe8-128">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fffe8-128">Order</span></span> | <span data-ttu-id="fffe8-129">Pfad</span><span class="sxs-lookup"><span data-stu-id="fffe8-129">Path</span></span>                     | <span data-ttu-id="fffe8-130">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fffe8-130">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="fffe8-131">1</span><span class="sxs-lookup"><span data-stu-id="fffe8-131">1</span></span>     | <span data-ttu-id="fffe8-132">/App1/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="fffe8-132">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="fffe8-133">2</span><span class="sxs-lookup"><span data-stu-id="fffe8-133">2</span></span>     | <span data-ttu-id="fffe8-134">/XMP/EXIF: gpsversionid</span><span class="sxs-lookup"><span data-stu-id="fffe8-134">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="fffe8-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="fffe8-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="fffe8-136">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="fffe8-136">Remove Paths</span></span>



| <span data-ttu-id="fffe8-137">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fffe8-137">Order</span></span> | <span data-ttu-id="fffe8-138">Pfad</span><span class="sxs-lookup"><span data-stu-id="fffe8-138">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="fffe8-139">1</span><span class="sxs-lookup"><span data-stu-id="fffe8-139">1</span></span>     | <span data-ttu-id="fffe8-140">/App1/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="fffe8-140">/app1/ifd/gps/{ushort=0}</span></span> |
| <span data-ttu-id="fffe8-141">2</span><span class="sxs-lookup"><span data-stu-id="fffe8-141">2</span></span>     | <span data-ttu-id="fffe8-142">/XMP/EXIF: gpsversionid</span><span class="sxs-lookup"><span data-stu-id="fffe8-142">/xmp/exif:gpsversionid</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="fffe8-143">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="fffe8-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="fffe8-144">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="fffe8-144">Read Paths</span></span>



| <span data-ttu-id="fffe8-145">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fffe8-145">Order</span></span> | <span data-ttu-id="fffe8-146">Pfad</span><span class="sxs-lookup"><span data-stu-id="fffe8-146">Path</span></span>                       | <span data-ttu-id="fffe8-147">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fffe8-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="fffe8-148">1</span><span class="sxs-lookup"><span data-stu-id="fffe8-148">1</span></span>     | <span data-ttu-id="fffe8-149">/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="fffe8-149">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="fffe8-150">2</span><span class="sxs-lookup"><span data-stu-id="fffe8-150">2</span></span>     | <span data-ttu-id="fffe8-151">/IFD/XMP/EXIF: gpsversionid</span><span class="sxs-lookup"><span data-stu-id="fffe8-151">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="fffe8-152">Unicode</span><span class="sxs-lookup"><span data-stu-id="fffe8-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="fffe8-153">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="fffe8-153">Write Paths</span></span>



| <span data-ttu-id="fffe8-154">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fffe8-154">Order</span></span> | <span data-ttu-id="fffe8-155">Pfad</span><span class="sxs-lookup"><span data-stu-id="fffe8-155">Path</span></span>                       | <span data-ttu-id="fffe8-156">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fffe8-156">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="fffe8-157">1</span><span class="sxs-lookup"><span data-stu-id="fffe8-157">1</span></span>     | <span data-ttu-id="fffe8-158">/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="fffe8-158">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="fffe8-159">2</span><span class="sxs-lookup"><span data-stu-id="fffe8-159">2</span></span>     | <span data-ttu-id="fffe8-160">/IFD/XMP/EXIF: gpsversionid</span><span class="sxs-lookup"><span data-stu-id="fffe8-160">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="fffe8-161">Unicode</span><span class="sxs-lookup"><span data-stu-id="fffe8-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="fffe8-162">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="fffe8-162">Remove Paths</span></span>



| <span data-ttu-id="fffe8-163">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fffe8-163">Order</span></span> | <span data-ttu-id="fffe8-164">Pfad</span><span class="sxs-lookup"><span data-stu-id="fffe8-164">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="fffe8-165">1</span><span class="sxs-lookup"><span data-stu-id="fffe8-165">1</span></span>     | <span data-ttu-id="fffe8-166">/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="fffe8-166">/ifd/gps/{ushort=0}</span></span>        |
| <span data-ttu-id="fffe8-167">2</span><span class="sxs-lookup"><span data-stu-id="fffe8-167">2</span></span>     | <span data-ttu-id="fffe8-168">/IFD/XMP/EXIF: gpsversionid</span><span class="sxs-lookup"><span data-stu-id="fffe8-168">/ifd/xmp/exif:gpsversionid</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fffe8-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fffe8-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="fffe8-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fffe8-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fffe8-171">System. GPS. versionID</span><span class="sxs-lookup"><span data-stu-id="fffe8-171">System.GPS.VersionID</span></span>](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
