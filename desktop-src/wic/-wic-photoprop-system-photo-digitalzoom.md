---
description: Die fotometadatenrichtlinie für die System. Photo. Digitalzoom-Eigenschaft.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: System. Photo. Digitalzoom-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf440e92243eb2102ac6abaa349ea83e58d9a2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347428"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a><span data-ttu-id="dd7cb-103">System. Photo. Digitalzoom-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="dd7cb-103">System.Photo.DigitalZoom Photo Metadata Policy</span></span>

<span data-ttu-id="dd7cb-104">Die fotometadatenrichtlinie für die [System. Photo. Digitalzoom](../properties/props-system-photo-digitalzoom.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dd7cb-104">The photo metadata policy for the [System.Photo.DigitalZoom](../properties/props-system-photo-digitalzoom.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="dd7cb-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="dd7cb-105">PKEY</span></span>

<span data-ttu-id="dd7cb-106">Pkey- \_ Foto \_ Digitalzoom</span><span class="sxs-lookup"><span data-stu-id="dd7cb-106">PKEY\_Photo\_DigitalZoom</span></span>

### <a name="containers"></a><span data-ttu-id="dd7cb-107">Container</span><span class="sxs-lookup"><span data-stu-id="dd7cb-107">Containers</span></span>

<span data-ttu-id="dd7cb-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="dd7cb-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="dd7cb-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd7cb-109">Read-Only</span></span>

<span data-ttu-id="dd7cb-110">Ja</span><span class="sxs-lookup"><span data-stu-id="dd7cb-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="dd7cb-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="dd7cb-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="dd7cb-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="dd7cb-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="dd7cb-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="dd7cb-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="dd7cb-114">Dieser Wert wird von System. Photo. digitalzoomzähler und System. Photo. digitalzoomnenner generiert.</span><span class="sxs-lookup"><span data-stu-id="dd7cb-114">This value is generated from System.Photo.DigitalZoomNumerator and System.Photo.DigitalZoomDenominator.</span></span> <span data-ttu-id="dd7cb-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dd7cb-115">It cannot be written directly.</span></span> <span data-ttu-id="dd7cb-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="dd7cb-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="dd7cb-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="dd7cb-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="dd7cb-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="dd7cb-118">Read Paths</span></span>



| <span data-ttu-id="dd7cb-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="dd7cb-119">Order</span></span> | <span data-ttu-id="dd7cb-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="dd7cb-120">Path</span></span>                          | <span data-ttu-id="dd7cb-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="dd7cb-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="dd7cb-122">1</span><span class="sxs-lookup"><span data-stu-id="dd7cb-122">1</span></span>     | <span data-ttu-id="dd7cb-123">/App1/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="dd7cb-123">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="dd7cb-124">2</span><span class="sxs-lookup"><span data-stu-id="dd7cb-124">2</span></span>     | <span data-ttu-id="dd7cb-125">/XMP/EXIF: DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="dd7cb-125">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="dd7cb-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="dd7cb-126">Write Paths</span></span>



| <span data-ttu-id="dd7cb-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="dd7cb-127">Order</span></span> | <span data-ttu-id="dd7cb-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="dd7cb-128">Path</span></span>                          | <span data-ttu-id="dd7cb-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="dd7cb-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="dd7cb-130">1</span><span class="sxs-lookup"><span data-stu-id="dd7cb-130">1</span></span>     | <span data-ttu-id="dd7cb-131">/App1/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="dd7cb-131">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="dd7cb-132">2</span><span class="sxs-lookup"><span data-stu-id="dd7cb-132">2</span></span>     | <span data-ttu-id="dd7cb-133">/XMP/EXIF: DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="dd7cb-133">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="dd7cb-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="dd7cb-134">Remove Paths</span></span>



| <span data-ttu-id="dd7cb-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="dd7cb-135">Order</span></span> | <span data-ttu-id="dd7cb-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="dd7cb-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="dd7cb-137">1</span><span class="sxs-lookup"><span data-stu-id="dd7cb-137">1</span></span>     | <span data-ttu-id="dd7cb-138">/App1/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="dd7cb-138">/app1/ifd/exif/{ushort=41988}</span></span> |
| <span data-ttu-id="dd7cb-139">2</span><span class="sxs-lookup"><span data-stu-id="dd7cb-139">2</span></span>     | <span data-ttu-id="dd7cb-140">/XMP/EXIF: DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="dd7cb-140">/xmp/exif:digitalzoomratio</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="dd7cb-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="dd7cb-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="dd7cb-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="dd7cb-142">Read Paths</span></span>



| <span data-ttu-id="dd7cb-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="dd7cb-143">Order</span></span> | <span data-ttu-id="dd7cb-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="dd7cb-144">Path</span></span>                           | <span data-ttu-id="dd7cb-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="dd7cb-145">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="dd7cb-146">1</span><span class="sxs-lookup"><span data-stu-id="dd7cb-146">1</span></span>     | <span data-ttu-id="dd7cb-147">/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="dd7cb-147">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="dd7cb-148">2</span><span class="sxs-lookup"><span data-stu-id="dd7cb-148">2</span></span>     | <span data-ttu-id="dd7cb-149">/IFD/XMP/EXIF: DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="dd7cb-149">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="dd7cb-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="dd7cb-150">Write Paths</span></span>



| <span data-ttu-id="dd7cb-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="dd7cb-151">Order</span></span> | <span data-ttu-id="dd7cb-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="dd7cb-152">Path</span></span>                           | <span data-ttu-id="dd7cb-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="dd7cb-153">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="dd7cb-154">1</span><span class="sxs-lookup"><span data-stu-id="dd7cb-154">1</span></span>     | <span data-ttu-id="dd7cb-155">/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="dd7cb-155">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="dd7cb-156">2</span><span class="sxs-lookup"><span data-stu-id="dd7cb-156">2</span></span>     | <span data-ttu-id="dd7cb-157">/IFD/XMP/EXIF: DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="dd7cb-157">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="dd7cb-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="dd7cb-158">Remove Paths</span></span>



| <span data-ttu-id="dd7cb-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="dd7cb-159">Order</span></span> | <span data-ttu-id="dd7cb-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="dd7cb-160">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="dd7cb-161">1</span><span class="sxs-lookup"><span data-stu-id="dd7cb-161">1</span></span>     | <span data-ttu-id="dd7cb-162">/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="dd7cb-162">/ifd/exif/{ushort=41988}</span></span>       |
| <span data-ttu-id="dd7cb-163">2</span><span class="sxs-lookup"><span data-stu-id="dd7cb-163">2</span></span>     | <span data-ttu-id="dd7cb-164">/IFD/XMP/EXIF: DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="dd7cb-164">/ifd/xmp/exif:digitalzoomratio</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="dd7cb-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd7cb-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd7cb-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd7cb-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd7cb-167">System. Photo. Digitalzoom</span><span class="sxs-lookup"><span data-stu-id="dd7cb-167">System.Photo.DigitalZoom</span></span>](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
