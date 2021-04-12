---
description: Die fotometadatenrichtlinie für die System. Image. ImageID-Eigenschaft.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: System. Image. ImageID-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529270"
---
# <a name="systemimageimageid-photo-metadata-policy"></a><span data-ttu-id="c7546-103">System. Image. ImageID-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="c7546-103">System.Image.ImageID Photo Metadata Policy</span></span>

<span data-ttu-id="c7546-104">Die fotometadatenrichtlinie für die [System. Image. ImageID](../properties/props-system-image-imageid.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c7546-104">The photo metadata policy for the [System.Image.ImageID](../properties/props-system-image-imageid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c7546-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="c7546-105">PKEY</span></span>

<span data-ttu-id="c7546-106">Pkey- \_ Image- \_ ImageID</span><span class="sxs-lookup"><span data-stu-id="c7546-106">PKEY\_Image\_ImageID</span></span>

### <a name="containers"></a><span data-ttu-id="c7546-107">Container</span><span class="sxs-lookup"><span data-stu-id="c7546-107">Containers</span></span>

<span data-ttu-id="c7546-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c7546-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c7546-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7546-109">Read-Only</span></span>

<span data-ttu-id="c7546-110">Nein</span><span class="sxs-lookup"><span data-stu-id="c7546-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c7546-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="c7546-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c7546-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="c7546-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="c7546-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="c7546-113">Input Type</span></span>

<span data-ttu-id="c7546-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c7546-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c7546-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="c7546-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c7546-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="c7546-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="c7546-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="c7546-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c7546-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="c7546-118">Read Paths</span></span>



| <span data-ttu-id="c7546-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c7546-119">Order</span></span> | <span data-ttu-id="c7546-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="c7546-120">Path</span></span>                          | <span data-ttu-id="c7546-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="c7546-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c7546-122">1</span><span class="sxs-lookup"><span data-stu-id="c7546-122">1</span></span>     | <span data-ttu-id="c7546-123">/App1/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="c7546-123">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="c7546-124">ascii</span><span class="sxs-lookup"><span data-stu-id="c7546-124">ascii</span></span>       |
| <span data-ttu-id="c7546-125">2</span><span class="sxs-lookup"><span data-stu-id="c7546-125">2</span></span>     | <span data-ttu-id="c7546-126">/XMP/EXIF: imageuniqueid</span><span class="sxs-lookup"><span data-stu-id="c7546-126">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="c7546-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="c7546-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c7546-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="c7546-128">Write Paths</span></span>



| <span data-ttu-id="c7546-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c7546-129">Order</span></span> | <span data-ttu-id="c7546-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="c7546-130">Path</span></span>                          | <span data-ttu-id="c7546-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="c7546-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c7546-132">1</span><span class="sxs-lookup"><span data-stu-id="c7546-132">1</span></span>     | <span data-ttu-id="c7546-133">/App1/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="c7546-133">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="c7546-134">ascii</span><span class="sxs-lookup"><span data-stu-id="c7546-134">ascii</span></span>       |
| <span data-ttu-id="c7546-135">2</span><span class="sxs-lookup"><span data-stu-id="c7546-135">2</span></span>     | <span data-ttu-id="c7546-136">/XMP/EXIF: imageuniqueid</span><span class="sxs-lookup"><span data-stu-id="c7546-136">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="c7546-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="c7546-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c7546-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="c7546-138">Remove Paths</span></span>



| <span data-ttu-id="c7546-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c7546-139">Order</span></span> | <span data-ttu-id="c7546-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="c7546-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="c7546-141">1</span><span class="sxs-lookup"><span data-stu-id="c7546-141">1</span></span>     | <span data-ttu-id="c7546-142">/App1/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="c7546-142">/app1/ifd/exif/{ushort=42016}</span></span> |
| <span data-ttu-id="c7546-143">2</span><span class="sxs-lookup"><span data-stu-id="c7546-143">2</span></span>     | <span data-ttu-id="c7546-144">/XMP/EXIF: imageuniqueid</span><span class="sxs-lookup"><span data-stu-id="c7546-144">/xmp/exif:ImageUniqueID</span></span>       |



 

### <a name="tiff-policy"></a><span data-ttu-id="c7546-145">TIFF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="c7546-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c7546-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="c7546-146">Read Paths</span></span>



| <span data-ttu-id="c7546-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c7546-147">Order</span></span> | <span data-ttu-id="c7546-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="c7546-148">Path</span></span>                        | <span data-ttu-id="c7546-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="c7546-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="c7546-150">/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="c7546-150">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="c7546-151">ascii</span><span class="sxs-lookup"><span data-stu-id="c7546-151">ascii</span></span>       |
|       | <span data-ttu-id="c7546-152">/IFD/XMP/EXIF: imageuniqueid</span><span class="sxs-lookup"><span data-stu-id="c7546-152">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="c7546-153">Unicode</span><span class="sxs-lookup"><span data-stu-id="c7546-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c7546-154">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="c7546-154">Write Paths</span></span>



| <span data-ttu-id="c7546-155">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c7546-155">Order</span></span> | <span data-ttu-id="c7546-156">Pfad</span><span class="sxs-lookup"><span data-stu-id="c7546-156">Path</span></span>                        | <span data-ttu-id="c7546-157">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="c7546-157">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="c7546-158">/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="c7546-158">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="c7546-159">ascii</span><span class="sxs-lookup"><span data-stu-id="c7546-159">ascii</span></span>       |
|       | <span data-ttu-id="c7546-160">/IFD/XMP/EXIF: imageuniqueid</span><span class="sxs-lookup"><span data-stu-id="c7546-160">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="c7546-161">Unicode</span><span class="sxs-lookup"><span data-stu-id="c7546-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c7546-162">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="c7546-162">Remove Paths</span></span>



| <span data-ttu-id="c7546-163">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c7546-163">Order</span></span> | <span data-ttu-id="c7546-164">Pfad</span><span class="sxs-lookup"><span data-stu-id="c7546-164">Path</span></span>                        |
|-------|-----------------------------|
|       | <span data-ttu-id="c7546-165">/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="c7546-165">/ifd/exif/{ushort=42016}</span></span>    |
|       | <span data-ttu-id="c7546-166">/IFD/XMP/EXIF: imageuniqueid</span><span class="sxs-lookup"><span data-stu-id="c7546-166">/ifd/xmp/exif:ImageUniqueID</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c7546-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7546-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7546-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7546-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7546-169">System. Image. ImageID</span><span class="sxs-lookup"><span data-stu-id="c7546-169">System.Image.ImageID</span></span>](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
