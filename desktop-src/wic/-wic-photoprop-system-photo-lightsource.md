---
description: Die fotometadatenrichtlinie für die System. Photo. LightSource-Eigenschaft.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: System. Photo. LightSource-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9b3d31f01cdd2bea8d3fabbbc730a41f1fb0da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529936"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a><span data-ttu-id="9f4ba-103">System. Photo. LightSource-fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="9f4ba-103">System.Photo.LightSource Photo Metadata Policy</span></span>

<span data-ttu-id="9f4ba-104">Die fotometadatenrichtlinie für die [System. Photo. LightSource](../properties/props-system-photo-lightsource.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9f4ba-104">The photo metadata policy for the [System.Photo.LightSource](../properties/props-system-photo-lightsource.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9f4ba-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="9f4ba-105">PKEY</span></span>

<span data-ttu-id="9f4ba-106">Pkey \_ Photo \_ LightSource</span><span class="sxs-lookup"><span data-stu-id="9f4ba-106">PKEY\_Photo\_LightSource</span></span>

### <a name="containers"></a><span data-ttu-id="9f4ba-107">Container</span><span class="sxs-lookup"><span data-stu-id="9f4ba-107">Containers</span></span>

<span data-ttu-id="9f4ba-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9f4ba-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9f4ba-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f4ba-109">Read-Only</span></span>

<span data-ttu-id="9f4ba-110">Nein</span><span class="sxs-lookup"><span data-stu-id="9f4ba-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9f4ba-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="9f4ba-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9f4ba-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="9f4ba-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="9f4ba-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="9f4ba-113">Input Type</span></span>

<span data-ttu-id="9f4ba-114">UShort</span><span class="sxs-lookup"><span data-stu-id="9f4ba-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9f4ba-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="9f4ba-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="9f4ba-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="9f4ba-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9f4ba-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="9f4ba-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9f4ba-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="9f4ba-118">Read Paths</span></span>



| <span data-ttu-id="9f4ba-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9f4ba-119">Order</span></span> | <span data-ttu-id="9f4ba-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="9f4ba-120">Path</span></span>                          | <span data-ttu-id="9f4ba-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9f4ba-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9f4ba-122">1</span><span class="sxs-lookup"><span data-stu-id="9f4ba-122">1</span></span>     | <span data-ttu-id="9f4ba-123">/App1/IFD/EXIF/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="9f4ba-123">/app1/ifd/exif/{ushort=37384}</span></span> | <span data-ttu-id="9f4ba-124">ushort</span><span class="sxs-lookup"><span data-stu-id="9f4ba-124">ushort</span></span>      |
| <span data-ttu-id="9f4ba-125">2</span><span class="sxs-lookup"><span data-stu-id="9f4ba-125">2</span></span>     | <span data-ttu-id="9f4ba-126">/XMP/EXIF: LightSource</span><span class="sxs-lookup"><span data-stu-id="9f4ba-126">/xmp/exif:LightSource</span></span>         | <span data-ttu-id="9f4ba-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="9f4ba-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9f4ba-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="9f4ba-128">Write Paths</span></span>



| <span data-ttu-id="9f4ba-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9f4ba-129">Order</span></span> | <span data-ttu-id="9f4ba-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="9f4ba-130">Path</span></span>                          | <span data-ttu-id="9f4ba-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9f4ba-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9f4ba-132">1</span><span class="sxs-lookup"><span data-stu-id="9f4ba-132">1</span></span>     | <span data-ttu-id="9f4ba-133">/App1/IFD/EXIF/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="9f4ba-133">/app1/ifd/exif/{ushort=37384}</span></span> | <span data-ttu-id="9f4ba-134">ushort</span><span class="sxs-lookup"><span data-stu-id="9f4ba-134">ushort</span></span>      |
| <span data-ttu-id="9f4ba-135">2</span><span class="sxs-lookup"><span data-stu-id="9f4ba-135">2</span></span>     | <span data-ttu-id="9f4ba-136">/XMP/EXIF: LightSource</span><span class="sxs-lookup"><span data-stu-id="9f4ba-136">/xmp/exif:LightSource</span></span>         | <span data-ttu-id="9f4ba-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="9f4ba-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9f4ba-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="9f4ba-138">Remove Paths</span></span>



| <span data-ttu-id="9f4ba-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9f4ba-139">Order</span></span> | <span data-ttu-id="9f4ba-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="9f4ba-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="9f4ba-141">1</span><span class="sxs-lookup"><span data-stu-id="9f4ba-141">1</span></span>     | <span data-ttu-id="9f4ba-142">/App1/IFD/EXIF/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="9f4ba-142">/app1/ifd/exif/{ushort=37384}</span></span> |
| <span data-ttu-id="9f4ba-143">2</span><span class="sxs-lookup"><span data-stu-id="9f4ba-143">2</span></span>     | <span data-ttu-id="9f4ba-144">/XMP/EXIF: LightSource</span><span class="sxs-lookup"><span data-stu-id="9f4ba-144">/xmp/exif:lightsource</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="9f4ba-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="9f4ba-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9f4ba-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="9f4ba-146">Read Paths</span></span>



| <span data-ttu-id="9f4ba-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9f4ba-147">Order</span></span> | <span data-ttu-id="9f4ba-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="9f4ba-148">Path</span></span>                      | <span data-ttu-id="9f4ba-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9f4ba-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9f4ba-150">1</span><span class="sxs-lookup"><span data-stu-id="9f4ba-150">1</span></span>     | <span data-ttu-id="9f4ba-151">/IFD/EXIF/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="9f4ba-151">/ifd/exif/{ushort=37384}</span></span>  | <span data-ttu-id="9f4ba-152">ushort</span><span class="sxs-lookup"><span data-stu-id="9f4ba-152">ushort</span></span>      |
| <span data-ttu-id="9f4ba-153">2</span><span class="sxs-lookup"><span data-stu-id="9f4ba-153">2</span></span>     | <span data-ttu-id="9f4ba-154">/IFD/XMP/EXIF: LightSource</span><span class="sxs-lookup"><span data-stu-id="9f4ba-154">/ifd/xmp/exif:LightSource</span></span> | <span data-ttu-id="9f4ba-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="9f4ba-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9f4ba-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="9f4ba-156">Write Paths</span></span>



| <span data-ttu-id="9f4ba-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9f4ba-157">Order</span></span> | <span data-ttu-id="9f4ba-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="9f4ba-158">Path</span></span>                      | <span data-ttu-id="9f4ba-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9f4ba-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9f4ba-160">1</span><span class="sxs-lookup"><span data-stu-id="9f4ba-160">1</span></span>     | <span data-ttu-id="9f4ba-161">/IFD/EXIF/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="9f4ba-161">/ifd/exif/{ushort=37384}</span></span>  | <span data-ttu-id="9f4ba-162">ushort</span><span class="sxs-lookup"><span data-stu-id="9f4ba-162">ushort</span></span>      |
| <span data-ttu-id="9f4ba-163">2</span><span class="sxs-lookup"><span data-stu-id="9f4ba-163">2</span></span>     | <span data-ttu-id="9f4ba-164">/IFD/XMP/EXIF: LightSource</span><span class="sxs-lookup"><span data-stu-id="9f4ba-164">/ifd/xmp/exif:LightSource</span></span> | <span data-ttu-id="9f4ba-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="9f4ba-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9f4ba-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="9f4ba-166">Remove Paths</span></span>



| <span data-ttu-id="9f4ba-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9f4ba-167">Order</span></span> | <span data-ttu-id="9f4ba-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="9f4ba-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="9f4ba-169">1</span><span class="sxs-lookup"><span data-stu-id="9f4ba-169">1</span></span>     | <span data-ttu-id="9f4ba-170">/IFD/EXIF/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="9f4ba-170">/ifd/exif/{ushort=37384}</span></span>  |
| <span data-ttu-id="9f4ba-171">2</span><span class="sxs-lookup"><span data-stu-id="9f4ba-171">2</span></span>     | <span data-ttu-id="9f4ba-172">/IFD/XMP/EXIF: LightSource</span><span class="sxs-lookup"><span data-stu-id="9f4ba-172">/ifd/xmp/exif:lightsource</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9f4ba-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f4ba-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f4ba-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9f4ba-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f4ba-175">System. Photo. LightSource</span><span class="sxs-lookup"><span data-stu-id="9f4ba-175">System.Photo.LightSource</span></span>](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
