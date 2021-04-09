---
description: Die fotometadatenrichtlinie für die System. Photo. Program Mode-Eigenschaft.
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: System. Photo. Program Mode-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f5dffa822454509134c485e4792f4be4270912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960364"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a><span data-ttu-id="564af-103">System. Photo. Program Mode-fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="564af-103">System.Photo.ProgramMode Photo Metadata Policy</span></span>

<span data-ttu-id="564af-104">Die fotometadatenrichtlinie für die [System. Photo. Program Mode](../properties/props-system-photo-programmode.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="564af-104">The photo metadata policy for the [System.Photo.ProgramMode](../properties/props-system-photo-programmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="564af-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="564af-105">PKEY</span></span>

<span data-ttu-id="564af-106">Pkey- \_ Foto \_ Programmmodus</span><span class="sxs-lookup"><span data-stu-id="564af-106">PKEY\_Photo\_ProgramMode</span></span>

### <a name="containers"></a><span data-ttu-id="564af-107">Container</span><span class="sxs-lookup"><span data-stu-id="564af-107">Containers</span></span>

<span data-ttu-id="564af-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="564af-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="564af-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="564af-109">Read-Only</span></span>

<span data-ttu-id="564af-110">Nein</span><span class="sxs-lookup"><span data-stu-id="564af-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="564af-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="564af-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="564af-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="564af-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="564af-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="564af-113">Input Type</span></span>

<span data-ttu-id="564af-114">UShort</span><span class="sxs-lookup"><span data-stu-id="564af-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="564af-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="564af-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="564af-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="564af-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="564af-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="564af-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="564af-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="564af-118">Read Paths</span></span>



| <span data-ttu-id="564af-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="564af-119">Order</span></span> | <span data-ttu-id="564af-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="564af-120">Path</span></span>                          | <span data-ttu-id="564af-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="564af-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="564af-122">1</span><span class="sxs-lookup"><span data-stu-id="564af-122">1</span></span>     | <span data-ttu-id="564af-123">/App1/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="564af-123">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="564af-124">ushort</span><span class="sxs-lookup"><span data-stu-id="564af-124">ushort</span></span>      |
| <span data-ttu-id="564af-125">2</span><span class="sxs-lookup"><span data-stu-id="564af-125">2</span></span>     | <span data-ttu-id="564af-126">/XMP/EXIF: ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="564af-126">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="564af-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="564af-127">unicode</span></span>     |
| <span data-ttu-id="564af-128">3</span><span class="sxs-lookup"><span data-stu-id="564af-128">3</span></span>     | <span data-ttu-id="564af-129">/XMP/EXIF: Programm Mode</span><span class="sxs-lookup"><span data-stu-id="564af-129">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="564af-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="564af-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="564af-131">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="564af-131">Write Paths</span></span>



| <span data-ttu-id="564af-132">Auftrag</span><span class="sxs-lookup"><span data-stu-id="564af-132">Order</span></span> | <span data-ttu-id="564af-133">Pfad</span><span class="sxs-lookup"><span data-stu-id="564af-133">Path</span></span>                          | <span data-ttu-id="564af-134">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="564af-134">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="564af-135">1</span><span class="sxs-lookup"><span data-stu-id="564af-135">1</span></span>     | <span data-ttu-id="564af-136">/App1/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="564af-136">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="564af-137">ushort</span><span class="sxs-lookup"><span data-stu-id="564af-137">ushort</span></span>      |
| <span data-ttu-id="564af-138">2</span><span class="sxs-lookup"><span data-stu-id="564af-138">2</span></span>     | <span data-ttu-id="564af-139">/XMP/EXIF: ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="564af-139">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="564af-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="564af-140">unicode</span></span>     |
| <span data-ttu-id="564af-141">3</span><span class="sxs-lookup"><span data-stu-id="564af-141">3</span></span>     | <span data-ttu-id="564af-142">/XMP/EXIF: Programm Mode</span><span class="sxs-lookup"><span data-stu-id="564af-142">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="564af-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="564af-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="564af-144">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="564af-144">Remove Paths</span></span>



| <span data-ttu-id="564af-145">Auftrag</span><span class="sxs-lookup"><span data-stu-id="564af-145">Order</span></span> | <span data-ttu-id="564af-146">Pfad</span><span class="sxs-lookup"><span data-stu-id="564af-146">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="564af-147">1</span><span class="sxs-lookup"><span data-stu-id="564af-147">1</span></span>     | <span data-ttu-id="564af-148">/App1/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="564af-148">/app1/ifd/exif/{ushort=34850}</span></span> |
| <span data-ttu-id="564af-149">2</span><span class="sxs-lookup"><span data-stu-id="564af-149">2</span></span>     | <span data-ttu-id="564af-150">/XMP/EXIF: ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="564af-150">/xmp/exif:exposureprogram</span></span>     |
| <span data-ttu-id="564af-151">3</span><span class="sxs-lookup"><span data-stu-id="564af-151">3</span></span>     | <span data-ttu-id="564af-152">/XMP/EXIF: Programm Mode</span><span class="sxs-lookup"><span data-stu-id="564af-152">/xmp/exif:programmode</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="564af-153">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="564af-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="564af-154">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="564af-154">Read Paths</span></span>



| <span data-ttu-id="564af-155">Auftrag</span><span class="sxs-lookup"><span data-stu-id="564af-155">Order</span></span> | <span data-ttu-id="564af-156">Pfad</span><span class="sxs-lookup"><span data-stu-id="564af-156">Path</span></span>                          | <span data-ttu-id="564af-157">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="564af-157">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="564af-158">1</span><span class="sxs-lookup"><span data-stu-id="564af-158">1</span></span>     | <span data-ttu-id="564af-159">/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="564af-159">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="564af-160">ushort</span><span class="sxs-lookup"><span data-stu-id="564af-160">ushort</span></span>      |
| <span data-ttu-id="564af-161">2</span><span class="sxs-lookup"><span data-stu-id="564af-161">2</span></span>     | <span data-ttu-id="564af-162">/IFD/XMP/EXIF: ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="564af-162">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="564af-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="564af-163">unicode</span></span>     |
| <span data-ttu-id="564af-164">3</span><span class="sxs-lookup"><span data-stu-id="564af-164">3</span></span>     | <span data-ttu-id="564af-165">/IFD/XMP/EXIF: Programm Mode</span><span class="sxs-lookup"><span data-stu-id="564af-165">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="564af-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="564af-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="564af-167">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="564af-167">Write Paths</span></span>



| <span data-ttu-id="564af-168">Auftrag</span><span class="sxs-lookup"><span data-stu-id="564af-168">Order</span></span> | <span data-ttu-id="564af-169">Pfad</span><span class="sxs-lookup"><span data-stu-id="564af-169">Path</span></span>                          | <span data-ttu-id="564af-170">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="564af-170">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="564af-171">1</span><span class="sxs-lookup"><span data-stu-id="564af-171">1</span></span>     | <span data-ttu-id="564af-172">/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="564af-172">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="564af-173">ushort</span><span class="sxs-lookup"><span data-stu-id="564af-173">ushort</span></span>      |
| <span data-ttu-id="564af-174">2</span><span class="sxs-lookup"><span data-stu-id="564af-174">2</span></span>     | <span data-ttu-id="564af-175">/IFD/XMP/EXIF: ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="564af-175">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="564af-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="564af-176">unicode</span></span>     |
| <span data-ttu-id="564af-177">3</span><span class="sxs-lookup"><span data-stu-id="564af-177">3</span></span>     | <span data-ttu-id="564af-178">/IFD/XMP/EXIF: Programm Mode</span><span class="sxs-lookup"><span data-stu-id="564af-178">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="564af-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="564af-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="564af-180">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="564af-180">Remove Paths</span></span>



| <span data-ttu-id="564af-181">Auftrag</span><span class="sxs-lookup"><span data-stu-id="564af-181">Order</span></span> | <span data-ttu-id="564af-182">Pfad</span><span class="sxs-lookup"><span data-stu-id="564af-182">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="564af-183">1</span><span class="sxs-lookup"><span data-stu-id="564af-183">1</span></span>     | <span data-ttu-id="564af-184">/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="564af-184">/ifd/exif/{ushort=34850}</span></span>      |
| <span data-ttu-id="564af-185">2</span><span class="sxs-lookup"><span data-stu-id="564af-185">2</span></span>     | <span data-ttu-id="564af-186">/IFD/XMP/EXIF: ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="564af-186">/ifd/xmp/exif:exposureprogram</span></span> |
| <span data-ttu-id="564af-187">3</span><span class="sxs-lookup"><span data-stu-id="564af-187">3</span></span>     | <span data-ttu-id="564af-188">/IFD/XMP/EXIF: Programm Mode</span><span class="sxs-lookup"><span data-stu-id="564af-188">/ifd/xmp/exif:programmode</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="564af-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="564af-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="564af-190">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="564af-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="564af-191">System. Photo. Program Mode</span><span class="sxs-lookup"><span data-stu-id="564af-191">System.Photo.ProgramMode</span></span>](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
