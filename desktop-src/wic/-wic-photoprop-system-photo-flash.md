---
description: Die fotometadatenrichtlinie für die System. Photo. Flash-Eigenschaft.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: System. Photo. Flash-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0302e0f310d2f9a6a4390b0d4856578cc2f43e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373146"
---
# <a name="systemphotoflash-photo-metadata-policy"></a><span data-ttu-id="6f485-103">System. Photo. Flash-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="6f485-103">System.Photo.Flash Photo Metadata Policy</span></span>

<span data-ttu-id="6f485-104">Die fotometadatenrichtlinie für die [System. Photo. Flash](../properties/props-system-photo-exposuretime.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6f485-104">The photo metadata policy for the [System.Photo.Flash](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6f485-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="6f485-105">PKEY</span></span>

<span data-ttu-id="6f485-106">Pkey \_ Photo \_ Flash</span><span class="sxs-lookup"><span data-stu-id="6f485-106">PKEY\_Photo\_Flash</span></span>

### <a name="containers"></a><span data-ttu-id="6f485-107">Container</span><span class="sxs-lookup"><span data-stu-id="6f485-107">Containers</span></span>

<span data-ttu-id="6f485-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6f485-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6f485-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6f485-109">Read-Only</span></span>

<span data-ttu-id="6f485-110">Nein</span><span class="sxs-lookup"><span data-stu-id="6f485-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6f485-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="6f485-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6f485-112">VT \_ UI1 (wenn das Quell Schema XMP war) oder VT \_ UI2 (wenn das Quell Schema EXIF war)</span><span class="sxs-lookup"><span data-stu-id="6f485-112">VT\_UI1 (if the source schema was XMP), or VT\_UI2 (if the source schema was EXIF)</span></span>

<span data-ttu-id="6f485-113">\\lang1036</span><span class="sxs-lookup"><span data-stu-id="6f485-113">\\lang1036</span></span>

### <a name="input-type"></a><span data-ttu-id="6f485-114">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="6f485-114">Input Type</span></span>

<span data-ttu-id="6f485-115">VT \_ UI1, VTUI2, VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6f485-115">VT\_UI1, VTUI2, VT\_UI4</span></span>

<span data-ttu-id="6f485-116">\\lang1033</span><span class="sxs-lookup"><span data-stu-id="6f485-116">\\lang1033</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6f485-117">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="6f485-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="6f485-118">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="6f485-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6f485-119">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="6f485-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6f485-120">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="6f485-120">Read Paths</span></span>



| <span data-ttu-id="6f485-121">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6f485-121">Order</span></span> | <span data-ttu-id="6f485-122">Pfad</span><span class="sxs-lookup"><span data-stu-id="6f485-122">Path</span></span>                             | <span data-ttu-id="6f485-123">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="6f485-123">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="6f485-124">1</span><span class="sxs-lookup"><span data-stu-id="6f485-124">1</span></span>     | <span data-ttu-id="6f485-125">/App1/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="6f485-125">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="6f485-126">ushort</span><span class="sxs-lookup"><span data-stu-id="6f485-126">ushort</span></span>      |
| <span data-ttu-id="6f485-127">2</span><span class="sxs-lookup"><span data-stu-id="6f485-127">2</span></span>     | <span data-ttu-id="6f485-128">/XMP/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="6f485-128">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="6f485-129">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="6f485-129">Write Paths</span></span>



| <span data-ttu-id="6f485-130">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6f485-130">Order</span></span> | <span data-ttu-id="6f485-131">Pfad</span><span class="sxs-lookup"><span data-stu-id="6f485-131">Path</span></span>                             | <span data-ttu-id="6f485-132">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="6f485-132">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="6f485-133">1</span><span class="sxs-lookup"><span data-stu-id="6f485-133">1</span></span>     | <span data-ttu-id="6f485-134">/App1/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="6f485-134">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="6f485-135">ushort</span><span class="sxs-lookup"><span data-stu-id="6f485-135">ushort</span></span>      |
| <span data-ttu-id="6f485-136">2</span><span class="sxs-lookup"><span data-stu-id="6f485-136">2</span></span>     | <span data-ttu-id="6f485-137">/XMP/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="6f485-137">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="6f485-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="6f485-138">Remove Paths</span></span>



| <span data-ttu-id="6f485-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6f485-139">Order</span></span> | <span data-ttu-id="6f485-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="6f485-140">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="6f485-141">1</span><span class="sxs-lookup"><span data-stu-id="6f485-141">1</span></span>     | <span data-ttu-id="6f485-142">/App1/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="6f485-142">/app1/ifd/exif/{ushort=37385}</span></span>    |
| <span data-ttu-id="6f485-143">2</span><span class="sxs-lookup"><span data-stu-id="6f485-143">2</span></span>     | <span data-ttu-id="6f485-144">/XMP/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="6f485-144">/xmp/<xmpstruct>exif:flash</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="6f485-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="6f485-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6f485-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="6f485-146">Read Paths</span></span>



| <span data-ttu-id="6f485-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6f485-147">Order</span></span> | <span data-ttu-id="6f485-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="6f485-148">Path</span></span>                                 | <span data-ttu-id="6f485-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="6f485-149">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="6f485-150">1</span><span class="sxs-lookup"><span data-stu-id="6f485-150">1</span></span>     | <span data-ttu-id="6f485-151">/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="6f485-151">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="6f485-152">ushort</span><span class="sxs-lookup"><span data-stu-id="6f485-152">ushort</span></span>      |
| <span data-ttu-id="6f485-153">2</span><span class="sxs-lookup"><span data-stu-id="6f485-153">2</span></span>     | <span data-ttu-id="6f485-154">/IFD/XMP/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="6f485-154">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="6f485-155">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="6f485-155">Write Paths</span></span>



| <span data-ttu-id="6f485-156">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6f485-156">Order</span></span> | <span data-ttu-id="6f485-157">Pfad</span><span class="sxs-lookup"><span data-stu-id="6f485-157">Path</span></span>                                 | <span data-ttu-id="6f485-158">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="6f485-158">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="6f485-159">1</span><span class="sxs-lookup"><span data-stu-id="6f485-159">1</span></span>     | <span data-ttu-id="6f485-160">/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="6f485-160">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="6f485-161">ushort</span><span class="sxs-lookup"><span data-stu-id="6f485-161">ushort</span></span>      |
| <span data-ttu-id="6f485-162">2</span><span class="sxs-lookup"><span data-stu-id="6f485-162">2</span></span>     | <span data-ttu-id="6f485-163">/IFD/XMP/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="6f485-163">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="6f485-164">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="6f485-164">Remove Paths</span></span>



| <span data-ttu-id="6f485-165">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6f485-165">Order</span></span> | <span data-ttu-id="6f485-166">Pfad</span><span class="sxs-lookup"><span data-stu-id="6f485-166">Path</span></span>                                 |
|-------|--------------------------------------|
| <span data-ttu-id="6f485-167">1</span><span class="sxs-lookup"><span data-stu-id="6f485-167">1</span></span>     | <span data-ttu-id="6f485-168">/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="6f485-168">/ifd/exif/{ushort=37385}</span></span>             |
| <span data-ttu-id="6f485-169">2</span><span class="sxs-lookup"><span data-stu-id="6f485-169">2</span></span>     | <span data-ttu-id="6f485-170">/IFD/XMP/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="6f485-170">/ifd/xmp/<xmpstruct>exif:flash</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6f485-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f485-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f485-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6f485-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f485-173">System. Photo. Flash</span><span class="sxs-lookup"><span data-stu-id="6f485-173">System.Photo.Flash</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
