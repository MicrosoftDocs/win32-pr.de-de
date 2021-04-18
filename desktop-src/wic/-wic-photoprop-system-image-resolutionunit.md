---
description: Die fotometadatenrichtlinie für die System. Image. ResolutionUnit-Eigenschaft.
ms.assetid: b8b744bd-976b-4648-a04b-33607467d6ac
title: System. Image. ResolutionUnit Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d954df0b7efe9501cf25c33a54cd4296fb03f3c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351718"
---
# <a name="systemimageresolutionunit-photo-metadata-policy"></a><span data-ttu-id="80987-103">System. Image. ResolutionUnit Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="80987-103">System.Image.ResolutionUnit Photo Metadata Policy</span></span>

<span data-ttu-id="80987-104">Die fotometadatenrichtlinie für die [System. Image. ResolutionUnit](../properties/props-system-image-resolutionunit.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="80987-104">The photo metadata policy for the [System.Image.ResolutionUnit](../properties/props-system-image-resolutionunit.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="80987-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="80987-105">PKEY</span></span>

<span data-ttu-id="80987-106">Pkey- \_ Image \_ ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="80987-106">PKEY\_Image\_ResolutionUnit</span></span>

### <a name="containers"></a><span data-ttu-id="80987-107">Container</span><span class="sxs-lookup"><span data-stu-id="80987-107">Containers</span></span>

<span data-ttu-id="80987-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="80987-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="80987-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80987-109">Read-Only</span></span>

<span data-ttu-id="80987-110">Ja.</span><span class="sxs-lookup"><span data-stu-id="80987-110">Yes.</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="80987-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="80987-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="80987-112">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="80987-112">VT\_I2</span></span>

### <a name="input-type"></a><span data-ttu-id="80987-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="80987-113">Input Type</span></span>

<span data-ttu-id="80987-114">UShort</span><span class="sxs-lookup"><span data-stu-id="80987-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="80987-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="80987-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="80987-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="80987-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="80987-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="80987-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="80987-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="80987-118">Read Paths</span></span>



| <span data-ttu-id="80987-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="80987-119">Order</span></span> | <span data-ttu-id="80987-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="80987-120">Path</span></span>                     | <span data-ttu-id="80987-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="80987-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="80987-122">1</span><span class="sxs-lookup"><span data-stu-id="80987-122">1</span></span>     | <span data-ttu-id="80987-123">/App1/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="80987-123">/app1/ifd/{ushort=296}</span></span>   | <span data-ttu-id="80987-124">ushort</span><span class="sxs-lookup"><span data-stu-id="80987-124">ushort</span></span>      |
| <span data-ttu-id="80987-125">2</span><span class="sxs-lookup"><span data-stu-id="80987-125">2</span></span>     | <span data-ttu-id="80987-126">/XMP/TIFF: ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="80987-126">/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="80987-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="80987-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="80987-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="80987-128">Write Paths</span></span>



| <span data-ttu-id="80987-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="80987-129">Order</span></span> | <span data-ttu-id="80987-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="80987-130">Path</span></span>                     | <span data-ttu-id="80987-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="80987-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="80987-132">1</span><span class="sxs-lookup"><span data-stu-id="80987-132">1</span></span>     | <span data-ttu-id="80987-133">/App1/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="80987-133">/app1/ifd/{ushort=296}</span></span>   | <span data-ttu-id="80987-134">ushort</span><span class="sxs-lookup"><span data-stu-id="80987-134">ushort</span></span>      |
| <span data-ttu-id="80987-135">2</span><span class="sxs-lookup"><span data-stu-id="80987-135">2</span></span>     | <span data-ttu-id="80987-136">/XMP/TIFF: ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="80987-136">/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="80987-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="80987-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="80987-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="80987-138">Remove Paths</span></span>



| <span data-ttu-id="80987-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="80987-139">Order</span></span> | <span data-ttu-id="80987-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="80987-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="80987-141">1</span><span class="sxs-lookup"><span data-stu-id="80987-141">1</span></span>     | <span data-ttu-id="80987-142">/App1/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="80987-142">/app1/ifd/{ushort=296}</span></span>   |
| <span data-ttu-id="80987-143">2</span><span class="sxs-lookup"><span data-stu-id="80987-143">2</span></span>     | <span data-ttu-id="80987-144">/XMP/TIFF: ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="80987-144">/xmp/tiff:resolutionunit</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="80987-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="80987-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="80987-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="80987-146">Read Paths</span></span>



| <span data-ttu-id="80987-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="80987-147">Order</span></span> | <span data-ttu-id="80987-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="80987-148">Path</span></span>                         | <span data-ttu-id="80987-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="80987-149">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="80987-150">1</span><span class="sxs-lookup"><span data-stu-id="80987-150">1</span></span>     | <span data-ttu-id="80987-151">/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="80987-151">/ifd/{ushort=296}</span></span>            | <span data-ttu-id="80987-152">ushort</span><span class="sxs-lookup"><span data-stu-id="80987-152">ushort</span></span>      |
| <span data-ttu-id="80987-153">2</span><span class="sxs-lookup"><span data-stu-id="80987-153">2</span></span>     | <span data-ttu-id="80987-154">/IFD/XMP/TIFF: ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="80987-154">/ifd/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="80987-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="80987-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="80987-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="80987-156">Write Paths</span></span>



| <span data-ttu-id="80987-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="80987-157">Order</span></span> | <span data-ttu-id="80987-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="80987-158">Path</span></span>                         | <span data-ttu-id="80987-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="80987-159">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="80987-160">1</span><span class="sxs-lookup"><span data-stu-id="80987-160">1</span></span>     | <span data-ttu-id="80987-161">/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="80987-161">/ifd/{ushort=296}</span></span>            | <span data-ttu-id="80987-162">ushort</span><span class="sxs-lookup"><span data-stu-id="80987-162">ushort</span></span>      |
| <span data-ttu-id="80987-163">2</span><span class="sxs-lookup"><span data-stu-id="80987-163">2</span></span>     | <span data-ttu-id="80987-164">/IFD/XMP/TIFF: ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="80987-164">/ifd/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="80987-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="80987-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="80987-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="80987-166">Remove Paths</span></span>



| <span data-ttu-id="80987-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="80987-167">Order</span></span> | <span data-ttu-id="80987-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="80987-168">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="80987-169">1</span><span class="sxs-lookup"><span data-stu-id="80987-169">1</span></span>     | <span data-ttu-id="80987-170">/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="80987-170">/ifd/{ushort=296}</span></span>            |
| <span data-ttu-id="80987-171">2</span><span class="sxs-lookup"><span data-stu-id="80987-171">2</span></span>     | <span data-ttu-id="80987-172">/IFD/XMP/TIFF: ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="80987-172">/ifd/xmp/tiff:resolutionunit</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="80987-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80987-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="80987-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="80987-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80987-175">System. Image. ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="80987-175">System.Image.ResolutionUnit</span></span>](../properties/props-system-image-resolutionunit.md)
</dt> </dl>

 

 
