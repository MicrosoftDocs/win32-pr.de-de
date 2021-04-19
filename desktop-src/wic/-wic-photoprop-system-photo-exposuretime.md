---
description: Die fotometadatenrichtlinie für die System. Photo. ExposureTime-Eigenschaft.
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: System. Photo. ExposureTime-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9078befd0cbc26272ff14ae023b1b22cb4f0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349952"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a><span data-ttu-id="330db-103">System. Photo. ExposureTime-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="330db-103">System.Photo.ExposureTime Photo Metadata Policy</span></span>

<span data-ttu-id="330db-104">Die fotometadatenrichtlinie für die [System. Photo. ExposureTime](../properties/props-system-photo-exposuretime.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="330db-104">The photo metadata policy for the [System.Photo.ExposureTime](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="330db-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="330db-105">PKEY</span></span>

<span data-ttu-id="330db-106">Pkey- \_ Foto- \_ ExposureTime</span><span class="sxs-lookup"><span data-stu-id="330db-106">PKEY\_Photo\_ExposureTime</span></span>

### <a name="containers"></a><span data-ttu-id="330db-107">Container</span><span class="sxs-lookup"><span data-stu-id="330db-107">Containers</span></span>

<span data-ttu-id="330db-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="330db-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="330db-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="330db-109">Read-Only</span></span>

<span data-ttu-id="330db-110">Ja</span><span class="sxs-lookup"><span data-stu-id="330db-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="330db-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="330db-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="330db-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="330db-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="330db-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="330db-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="330db-114">Dieser Wert wird von System. Photo. exposuretimenenumerator und System. Photo. exposuretimenenner generiert.</span><span class="sxs-lookup"><span data-stu-id="330db-114">This value is generated from System.Photo.ExposureTimeNumerator and System.Photo.ExposureTimeDenominator.</span></span> <span data-ttu-id="330db-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="330db-115">It cannot be written directly.</span></span> <span data-ttu-id="330db-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="330db-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="330db-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="330db-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="330db-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="330db-118">Read Paths</span></span>



| <span data-ttu-id="330db-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="330db-119">Order</span></span> | <span data-ttu-id="330db-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="330db-120">Path</span></span>                          | <span data-ttu-id="330db-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="330db-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="330db-122">1</span><span class="sxs-lookup"><span data-stu-id="330db-122">1</span></span>     | <span data-ttu-id="330db-123">/App1/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="330db-123">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="330db-124">2</span><span class="sxs-lookup"><span data-stu-id="330db-124">2</span></span>     | <span data-ttu-id="330db-125">/XMP/EXIF: ExposureTime</span><span class="sxs-lookup"><span data-stu-id="330db-125">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="330db-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="330db-126">Write Paths</span></span>



| <span data-ttu-id="330db-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="330db-127">Order</span></span> | <span data-ttu-id="330db-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="330db-128">Path</span></span>                          | <span data-ttu-id="330db-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="330db-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="330db-130">1</span><span class="sxs-lookup"><span data-stu-id="330db-130">1</span></span>     | <span data-ttu-id="330db-131">/App1/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="330db-131">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="330db-132">2</span><span class="sxs-lookup"><span data-stu-id="330db-132">2</span></span>     | <span data-ttu-id="330db-133">/XMP/EXIF: ExposureTime</span><span class="sxs-lookup"><span data-stu-id="330db-133">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="330db-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="330db-134">Remove Paths</span></span>



| <span data-ttu-id="330db-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="330db-135">Order</span></span> | <span data-ttu-id="330db-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="330db-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="330db-137">1</span><span class="sxs-lookup"><span data-stu-id="330db-137">1</span></span>     | <span data-ttu-id="330db-138">/App1/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="330db-138">/app1/ifd/exif/{ushort=33434}</span></span> |
| <span data-ttu-id="330db-139">2</span><span class="sxs-lookup"><span data-stu-id="330db-139">2</span></span>     | <span data-ttu-id="330db-140">/XMP/EXIF: ExposureTime</span><span class="sxs-lookup"><span data-stu-id="330db-140">/xmp/exif:exposuretime</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="330db-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="330db-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="330db-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="330db-142">Read Paths</span></span>



| <span data-ttu-id="330db-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="330db-143">Order</span></span> | <span data-ttu-id="330db-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="330db-144">Path</span></span>                       | <span data-ttu-id="330db-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="330db-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="330db-146">1</span><span class="sxs-lookup"><span data-stu-id="330db-146">1</span></span>     | <span data-ttu-id="330db-147">/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="330db-147">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="330db-148">2</span><span class="sxs-lookup"><span data-stu-id="330db-148">2</span></span>     | <span data-ttu-id="330db-149">/IFD/XMP/EXIF: ExposureTime</span><span class="sxs-lookup"><span data-stu-id="330db-149">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="330db-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="330db-150">Write Paths</span></span>



| <span data-ttu-id="330db-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="330db-151">Order</span></span> | <span data-ttu-id="330db-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="330db-152">Path</span></span>                       | <span data-ttu-id="330db-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="330db-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="330db-154">1</span><span class="sxs-lookup"><span data-stu-id="330db-154">1</span></span>     | <span data-ttu-id="330db-155">/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="330db-155">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="330db-156">2</span><span class="sxs-lookup"><span data-stu-id="330db-156">2</span></span>     | <span data-ttu-id="330db-157">/IFD/XMP/EXIF: ExposureTime</span><span class="sxs-lookup"><span data-stu-id="330db-157">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="330db-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="330db-158">Remove Paths</span></span>



| <span data-ttu-id="330db-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="330db-159">Order</span></span> | <span data-ttu-id="330db-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="330db-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="330db-161">1</span><span class="sxs-lookup"><span data-stu-id="330db-161">1</span></span>     | <span data-ttu-id="330db-162">/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="330db-162">/ifd/exif/{ushort=33434}</span></span>   |
| <span data-ttu-id="330db-163">2</span><span class="sxs-lookup"><span data-stu-id="330db-163">2</span></span>     | <span data-ttu-id="330db-164">/IFD/XMP/EXIF: ExposureTime</span><span class="sxs-lookup"><span data-stu-id="330db-164">/ifd/xmp/exif:exposuretime</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="330db-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="330db-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="330db-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="330db-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="330db-167">System. Photo. ExposureTime</span><span class="sxs-lookup"><span data-stu-id="330db-167">System.Photo.ExposureTime</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
