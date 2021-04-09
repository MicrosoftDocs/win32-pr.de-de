---
description: Die fotometadatenrichtlinie für die System. Photo. Sättigung-Eigenschaft.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: System. Photo. Sättigung-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2b199458f063f2c28d7f6780a6ea907f76f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050296"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a><span data-ttu-id="3f243-103">System. Photo. Sättigung-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3f243-103">System.Photo.Saturation Photo Metadata Policy</span></span>

<span data-ttu-id="3f243-104">Die fotometadatenrichtlinie für die [System. Photo. Sättigung](../properties/props-system-photo-saturation.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3f243-104">The photo metadata policy for the [System.Photo.Saturation](../properties/props-system-photo-saturation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3f243-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="3f243-105">PKEY</span></span>

<span data-ttu-id="3f243-106">Pkey- \_ Foto \_ Sättigung</span><span class="sxs-lookup"><span data-stu-id="3f243-106">PKEY\_Photo\_Saturation</span></span>

### <a name="containers"></a><span data-ttu-id="3f243-107">Container</span><span class="sxs-lookup"><span data-stu-id="3f243-107">Containers</span></span>

<span data-ttu-id="3f243-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3f243-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3f243-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f243-109">Read-Only</span></span>

<span data-ttu-id="3f243-110">Nein</span><span class="sxs-lookup"><span data-stu-id="3f243-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3f243-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="3f243-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3f243-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="3f243-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="3f243-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="3f243-113">Input Type</span></span>

<span data-ttu-id="3f243-114">UShort</span><span class="sxs-lookup"><span data-stu-id="3f243-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3f243-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="3f243-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3f243-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="3f243-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="3f243-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="3f243-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3f243-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="3f243-118">Read Paths</span></span>



| <span data-ttu-id="3f243-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="3f243-119">Order</span></span> | <span data-ttu-id="3f243-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="3f243-120">Path</span></span>                          | <span data-ttu-id="3f243-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="3f243-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="3f243-122">1</span><span class="sxs-lookup"><span data-stu-id="3f243-122">1</span></span>     | <span data-ttu-id="3f243-123">/App1/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="3f243-123">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="3f243-124">ushort</span><span class="sxs-lookup"><span data-stu-id="3f243-124">ushort</span></span>      |
| <span data-ttu-id="3f243-125">2</span><span class="sxs-lookup"><span data-stu-id="3f243-125">2</span></span>     | <span data-ttu-id="3f243-126">/XMP/EXIF: Sättigung</span><span class="sxs-lookup"><span data-stu-id="3f243-126">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="3f243-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="3f243-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3f243-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="3f243-128">Write Paths</span></span>



| <span data-ttu-id="3f243-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="3f243-129">Order</span></span> | <span data-ttu-id="3f243-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="3f243-130">Path</span></span>                          | <span data-ttu-id="3f243-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="3f243-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="3f243-132">1</span><span class="sxs-lookup"><span data-stu-id="3f243-132">1</span></span>     | <span data-ttu-id="3f243-133">/App1/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="3f243-133">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="3f243-134">ushort</span><span class="sxs-lookup"><span data-stu-id="3f243-134">ushort</span></span>      |
| <span data-ttu-id="3f243-135">2</span><span class="sxs-lookup"><span data-stu-id="3f243-135">2</span></span>     | <span data-ttu-id="3f243-136">/XMP/EXIF: Sättigung</span><span class="sxs-lookup"><span data-stu-id="3f243-136">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="3f243-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="3f243-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3f243-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="3f243-138">Remove Paths</span></span>



| <span data-ttu-id="3f243-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="3f243-139">Order</span></span> | <span data-ttu-id="3f243-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="3f243-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="3f243-141">1</span><span class="sxs-lookup"><span data-stu-id="3f243-141">1</span></span>     | <span data-ttu-id="3f243-142">/App1/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="3f243-142">/app1/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="3f243-143">2</span><span class="sxs-lookup"><span data-stu-id="3f243-143">2</span></span>     | <span data-ttu-id="3f243-144">/XMP/EXIF: Sättigung</span><span class="sxs-lookup"><span data-stu-id="3f243-144">/xmp/exif:saturation</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="3f243-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="3f243-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3f243-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="3f243-146">Read Paths</span></span>



| <span data-ttu-id="3f243-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="3f243-147">Order</span></span> | <span data-ttu-id="3f243-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="3f243-148">Path</span></span>                     | <span data-ttu-id="3f243-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="3f243-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="3f243-150">1</span><span class="sxs-lookup"><span data-stu-id="3f243-150">1</span></span>     | <span data-ttu-id="3f243-151">/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="3f243-151">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="3f243-152">ushort</span><span class="sxs-lookup"><span data-stu-id="3f243-152">ushort</span></span>      |
| <span data-ttu-id="3f243-153">2</span><span class="sxs-lookup"><span data-stu-id="3f243-153">2</span></span>     | <span data-ttu-id="3f243-154">/IFD/XMP/EXIF: Sättigung</span><span class="sxs-lookup"><span data-stu-id="3f243-154">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="3f243-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="3f243-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3f243-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="3f243-156">Write Paths</span></span>



| <span data-ttu-id="3f243-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="3f243-157">Order</span></span> | <span data-ttu-id="3f243-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="3f243-158">Path</span></span>                     | <span data-ttu-id="3f243-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="3f243-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="3f243-160">1</span><span class="sxs-lookup"><span data-stu-id="3f243-160">1</span></span>     | <span data-ttu-id="3f243-161">/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="3f243-161">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="3f243-162">ushort</span><span class="sxs-lookup"><span data-stu-id="3f243-162">ushort</span></span>      |
| <span data-ttu-id="3f243-163">2</span><span class="sxs-lookup"><span data-stu-id="3f243-163">2</span></span>     | <span data-ttu-id="3f243-164">/IFD/XMP/EXIF: Sättigung</span><span class="sxs-lookup"><span data-stu-id="3f243-164">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="3f243-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="3f243-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3f243-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="3f243-166">Remove Paths</span></span>



| <span data-ttu-id="3f243-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="3f243-167">Order</span></span> | <span data-ttu-id="3f243-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="3f243-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="3f243-169">1</span><span class="sxs-lookup"><span data-stu-id="3f243-169">1</span></span>     | <span data-ttu-id="3f243-170">/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="3f243-170">/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="3f243-171">2</span><span class="sxs-lookup"><span data-stu-id="3f243-171">2</span></span>     | <span data-ttu-id="3f243-172">/IFD/XMP/EXIF: Sättigung</span><span class="sxs-lookup"><span data-stu-id="3f243-172">/ifd/xmp/exif:saturation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3f243-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f243-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f243-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f243-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f243-175">System. Photo. Sättigung</span><span class="sxs-lookup"><span data-stu-id="3f243-175">System.Photo.Saturation</span></span>](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
