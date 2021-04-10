---
description: Die fotometadatenrichtlinie für die System. Photo. Orientation-Eigenschaft.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: System. Photo. Orientation-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f4f350cd1a4c24d71ec737b4679aea2f7cab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050297"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a><span data-ttu-id="50743-103">System. Photo. Orientation-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="50743-103">System.Photo.Orientation Photo Metadata Policy</span></span>

<span data-ttu-id="50743-104">Die fotometadatenrichtlinie für die [System. Photo. Orientation](../properties/props-system-photo-meteringmode.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="50743-104">The photo metadata policy for the [System.Photo.Orientation](../properties/props-system-photo-meteringmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="50743-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="50743-105">PKEY</span></span>

<span data-ttu-id="50743-106">Pkey- \_ Foto \_ Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="50743-106">PKEY\_Photo\_Orientation</span></span>

### <a name="containers"></a><span data-ttu-id="50743-107">Container</span><span class="sxs-lookup"><span data-stu-id="50743-107">Containers</span></span>

<span data-ttu-id="50743-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="50743-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="50743-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50743-109">Read-Only</span></span>

<span data-ttu-id="50743-110">Nein</span><span class="sxs-lookup"><span data-stu-id="50743-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="50743-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="50743-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="50743-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="50743-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="50743-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="50743-113">Input Type</span></span>

<span data-ttu-id="50743-114">UShort</span><span class="sxs-lookup"><span data-stu-id="50743-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="50743-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="50743-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="50743-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="50743-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="50743-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="50743-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="50743-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="50743-118">Read Paths</span></span>



| <span data-ttu-id="50743-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="50743-119">Order</span></span> | <span data-ttu-id="50743-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="50743-120">Path</span></span>                   | <span data-ttu-id="50743-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="50743-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="50743-122">1</span><span class="sxs-lookup"><span data-stu-id="50743-122">1</span></span>     | <span data-ttu-id="50743-123">/App1/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="50743-123">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="50743-124">ushort</span><span class="sxs-lookup"><span data-stu-id="50743-124">ushort</span></span>      |
| <span data-ttu-id="50743-125">2</span><span class="sxs-lookup"><span data-stu-id="50743-125">2</span></span>     | <span data-ttu-id="50743-126">/XMP/TIFF: Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="50743-126">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="50743-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="50743-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="50743-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="50743-128">Write Paths</span></span>



| <span data-ttu-id="50743-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="50743-129">Order</span></span> | <span data-ttu-id="50743-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="50743-130">Path</span></span>                   | <span data-ttu-id="50743-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="50743-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="50743-132">1</span><span class="sxs-lookup"><span data-stu-id="50743-132">1</span></span>     | <span data-ttu-id="50743-133">/App1/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="50743-133">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="50743-134">ushort</span><span class="sxs-lookup"><span data-stu-id="50743-134">ushort</span></span>      |
| <span data-ttu-id="50743-135">2</span><span class="sxs-lookup"><span data-stu-id="50743-135">2</span></span>     | <span data-ttu-id="50743-136">/XMP/TIFF: Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="50743-136">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="50743-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="50743-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="50743-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="50743-138">Remove Paths</span></span>



| <span data-ttu-id="50743-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="50743-139">Order</span></span> | <span data-ttu-id="50743-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="50743-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="50743-141">1</span><span class="sxs-lookup"><span data-stu-id="50743-141">1</span></span>     | <span data-ttu-id="50743-142">/App1/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="50743-142">/app1/ifd/{ushort=274}</span></span> |
| <span data-ttu-id="50743-143">2</span><span class="sxs-lookup"><span data-stu-id="50743-143">2</span></span>     | <span data-ttu-id="50743-144">/XMP/TIFF: Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="50743-144">/xmp/tiff:orientation</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="50743-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="50743-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="50743-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="50743-146">Read Paths</span></span>



| <span data-ttu-id="50743-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="50743-147">Order</span></span> | <span data-ttu-id="50743-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="50743-148">Path</span></span>                      | <span data-ttu-id="50743-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="50743-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="50743-150">1</span><span class="sxs-lookup"><span data-stu-id="50743-150">1</span></span>     | <span data-ttu-id="50743-151">/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="50743-151">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="50743-152">ushort</span><span class="sxs-lookup"><span data-stu-id="50743-152">ushort</span></span>      |
| <span data-ttu-id="50743-153">2</span><span class="sxs-lookup"><span data-stu-id="50743-153">2</span></span>     | <span data-ttu-id="50743-154">/IFD/XMP/TIFF: Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="50743-154">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="50743-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="50743-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="50743-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="50743-156">Write Paths</span></span>



| <span data-ttu-id="50743-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="50743-157">Order</span></span> | <span data-ttu-id="50743-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="50743-158">Path</span></span>                      | <span data-ttu-id="50743-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="50743-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="50743-160">1</span><span class="sxs-lookup"><span data-stu-id="50743-160">1</span></span>     | <span data-ttu-id="50743-161">/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="50743-161">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="50743-162">ushort</span><span class="sxs-lookup"><span data-stu-id="50743-162">ushort</span></span>      |
| <span data-ttu-id="50743-163">2</span><span class="sxs-lookup"><span data-stu-id="50743-163">2</span></span>     | <span data-ttu-id="50743-164">/IFD/XMP/TIFF: Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="50743-164">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="50743-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="50743-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="50743-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="50743-166">Remove Paths</span></span>



| <span data-ttu-id="50743-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="50743-167">Order</span></span> | <span data-ttu-id="50743-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="50743-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="50743-169">1</span><span class="sxs-lookup"><span data-stu-id="50743-169">1</span></span>     | <span data-ttu-id="50743-170">/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="50743-170">/ifd/{ushort=274}</span></span>         |
| <span data-ttu-id="50743-171">2</span><span class="sxs-lookup"><span data-stu-id="50743-171">2</span></span>     | <span data-ttu-id="50743-172">/IFD/XMP/TIFF: Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="50743-172">/ifd/xmp/tiff:orientation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="50743-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50743-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="50743-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50743-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50743-175">System. Photo. Orientation</span><span class="sxs-lookup"><span data-stu-id="50743-175">System.Photo.Orientation</span></span>](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
