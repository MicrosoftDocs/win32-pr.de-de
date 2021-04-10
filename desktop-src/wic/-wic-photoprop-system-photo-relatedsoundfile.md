---
description: Die fotometadatenrichtlinie für die System. Photo. relatedsound File-Eigenschaft.
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: System. Photo. relatedsound File-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a29adb71f572868f21b1b8427e71b09616b24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960363"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a><span data-ttu-id="06917-103">System. Photo. relatedsound File-fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="06917-103">System.Photo.RelatedSoundFile Photo Metadata Policy</span></span>

<span data-ttu-id="06917-104">Die fotometadatenrichtlinie für die [System. Photo. relatedsound File](../properties/props-system-photo-relatedsoundfile.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="06917-104">The photo metadata policy for the [System.Photo.RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="06917-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="06917-105">PKEY</span></span>

<span data-ttu-id="06917-106">Pkey- \_ Foto \_ relatedsound file</span><span class="sxs-lookup"><span data-stu-id="06917-106">PKEY\_Photo\_RelatedSoundFile</span></span>

### <a name="containers"></a><span data-ttu-id="06917-107">Container</span><span class="sxs-lookup"><span data-stu-id="06917-107">Containers</span></span>

<span data-ttu-id="06917-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="06917-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="06917-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06917-109">Read-Only</span></span>

<span data-ttu-id="06917-110">Nein</span><span class="sxs-lookup"><span data-stu-id="06917-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="06917-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="06917-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="06917-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="06917-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="06917-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="06917-113">Input Type</span></span>

<span data-ttu-id="06917-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="06917-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="06917-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="06917-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="06917-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="06917-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="06917-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="06917-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="06917-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="06917-118">Read Paths</span></span>



| <span data-ttu-id="06917-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="06917-119">Order</span></span> | <span data-ttu-id="06917-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="06917-120">Path</span></span>                          | <span data-ttu-id="06917-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="06917-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="06917-122">1</span><span class="sxs-lookup"><span data-stu-id="06917-122">1</span></span>     | <span data-ttu-id="06917-123">/App1/IFD/EXIF/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="06917-123">/app1/ifd/exif/{ushort=40964}</span></span> | <span data-ttu-id="06917-124">ascii</span><span class="sxs-lookup"><span data-stu-id="06917-124">ascii</span></span>       |
| <span data-ttu-id="06917-125">2</span><span class="sxs-lookup"><span data-stu-id="06917-125">2</span></span>     | <span data-ttu-id="06917-126">/XMP/EXIF: relatedsoundfile</span><span class="sxs-lookup"><span data-stu-id="06917-126">/xmp/exif:RelatedSoundFile</span></span>    | <span data-ttu-id="06917-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="06917-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="06917-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="06917-128">Write Paths</span></span>



| <span data-ttu-id="06917-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="06917-129">Order</span></span> | <span data-ttu-id="06917-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="06917-130">Path</span></span>                          | <span data-ttu-id="06917-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="06917-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="06917-132">1</span><span class="sxs-lookup"><span data-stu-id="06917-132">1</span></span>     | <span data-ttu-id="06917-133">/App1/IFD/EXIF/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="06917-133">/app1/ifd/exif/{ushort=40964}</span></span> | <span data-ttu-id="06917-134">ascii</span><span class="sxs-lookup"><span data-stu-id="06917-134">ascii</span></span>       |
| <span data-ttu-id="06917-135">2</span><span class="sxs-lookup"><span data-stu-id="06917-135">2</span></span>     | <span data-ttu-id="06917-136">/XMP/EXIF: relatedsoundfile</span><span class="sxs-lookup"><span data-stu-id="06917-136">/xmp/exif:RelatedSoundFile</span></span>    | <span data-ttu-id="06917-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="06917-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="06917-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="06917-138">Remove Paths</span></span>



| <span data-ttu-id="06917-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="06917-139">Order</span></span> | <span data-ttu-id="06917-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="06917-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="06917-141">1</span><span class="sxs-lookup"><span data-stu-id="06917-141">1</span></span>     | <span data-ttu-id="06917-142">/App1/IFD/EXIF/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="06917-142">/app1/ifd/exif/{ushort=40964}</span></span> |
| <span data-ttu-id="06917-143">2</span><span class="sxs-lookup"><span data-stu-id="06917-143">2</span></span>     | <span data-ttu-id="06917-144">/XMP/EXIF: relatedsoundfile</span><span class="sxs-lookup"><span data-stu-id="06917-144">/xmp/exif:RelatedSoundFile</span></span>    |



 

### <a name="tiff-policy"></a><span data-ttu-id="06917-145">TIFF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="06917-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="06917-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="06917-146">Read Paths</span></span>



| <span data-ttu-id="06917-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="06917-147">Order</span></span> | <span data-ttu-id="06917-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="06917-148">Path</span></span>                           | <span data-ttu-id="06917-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="06917-149">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="06917-150">1</span><span class="sxs-lookup"><span data-stu-id="06917-150">1</span></span>     | <span data-ttu-id="06917-151">/IFD/EXIF/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="06917-151">/ifd/exif/{ushort=40964}</span></span>       | <span data-ttu-id="06917-152">ascii</span><span class="sxs-lookup"><span data-stu-id="06917-152">ascii</span></span>       |
| <span data-ttu-id="06917-153">2</span><span class="sxs-lookup"><span data-stu-id="06917-153">2</span></span>     | <span data-ttu-id="06917-154">/IFD/XMP/EXIF: relatedsoundfile</span><span class="sxs-lookup"><span data-stu-id="06917-154">/ifd/xmp/exif:RelatedSoundFile</span></span> | <span data-ttu-id="06917-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="06917-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="06917-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="06917-156">Write Paths</span></span>



| <span data-ttu-id="06917-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="06917-157">Order</span></span> | <span data-ttu-id="06917-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="06917-158">Path</span></span>                           | <span data-ttu-id="06917-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="06917-159">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="06917-160">1</span><span class="sxs-lookup"><span data-stu-id="06917-160">1</span></span>     | <span data-ttu-id="06917-161">/IFD/EXIF/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="06917-161">/ifd/exif/{ushort=40964}</span></span>       | <span data-ttu-id="06917-162">ascii</span><span class="sxs-lookup"><span data-stu-id="06917-162">ascii</span></span>       |
| <span data-ttu-id="06917-163">2</span><span class="sxs-lookup"><span data-stu-id="06917-163">2</span></span>     | <span data-ttu-id="06917-164">/IFD/XMP/EXIF: relatedsoundfile</span><span class="sxs-lookup"><span data-stu-id="06917-164">/ifd/xmp/exif:RelatedSoundFile</span></span> | <span data-ttu-id="06917-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="06917-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="06917-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="06917-166">Remove Paths</span></span>



| <span data-ttu-id="06917-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="06917-167">Order</span></span> | <span data-ttu-id="06917-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="06917-168">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="06917-169">1</span><span class="sxs-lookup"><span data-stu-id="06917-169">1</span></span>     | <span data-ttu-id="06917-170">/IFD/EXIF/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="06917-170">/ifd/exif/{ushort=40964}</span></span>       |
| <span data-ttu-id="06917-171">2</span><span class="sxs-lookup"><span data-stu-id="06917-171">2</span></span>     | <span data-ttu-id="06917-172">/IFD/XMP/EXIF: relatedsoundfile</span><span class="sxs-lookup"><span data-stu-id="06917-172">/ifd/xmp/exif:RelatedSoundFile</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="06917-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06917-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="06917-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06917-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06917-175">System. Photo. relatedsound file</span><span class="sxs-lookup"><span data-stu-id="06917-175">System.Photo.RelatedSoundFile</span></span>](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
