---
description: Die fotometadatenrichtlinie für die System. Photo. Contrast-Eigenschaft.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: System. Photo. Contrast Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d6ed34854b525e9eaac2ff5ac7339a75ad10e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530263"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a><span data-ttu-id="d1d07-103">System. Photo. Contrast Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d1d07-103">System.Photo.Contrast Photo Metadata Policy</span></span>

<span data-ttu-id="d1d07-104">Die fotometadatenrichtlinie für die [System. Photo. Contrast](../properties/props-system-photo-contrast.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d1d07-104">The photo metadata policy for the [System.Photo.Contrast](../properties/props-system-photo-contrast.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d1d07-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="d1d07-105">PKEY</span></span>

<span data-ttu-id="d1d07-106">Kontrast zum pkey- \_ Foto \_</span><span class="sxs-lookup"><span data-stu-id="d1d07-106">PKEY\_Photo\_Contrast</span></span>

### <a name="containers"></a><span data-ttu-id="d1d07-107">Container</span><span class="sxs-lookup"><span data-stu-id="d1d07-107">Containers</span></span>

<span data-ttu-id="d1d07-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d1d07-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d1d07-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1d07-109">Read-Only</span></span>

<span data-ttu-id="d1d07-110">Nein</span><span class="sxs-lookup"><span data-stu-id="d1d07-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d1d07-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="d1d07-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d1d07-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="d1d07-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="d1d07-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="d1d07-113">Input Type</span></span>

<span data-ttu-id="d1d07-114">UShort</span><span class="sxs-lookup"><span data-stu-id="d1d07-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d1d07-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="d1d07-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d1d07-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="d1d07-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d1d07-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d1d07-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d1d07-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="d1d07-118">Read Paths</span></span>



| <span data-ttu-id="d1d07-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="d1d07-119">Order</span></span> | <span data-ttu-id="d1d07-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="d1d07-120">Path</span></span>                          | <span data-ttu-id="d1d07-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="d1d07-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="d1d07-122">1</span><span class="sxs-lookup"><span data-stu-id="d1d07-122">1</span></span>     | <span data-ttu-id="d1d07-123">/App1/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="d1d07-123">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="d1d07-124">ushort</span><span class="sxs-lookup"><span data-stu-id="d1d07-124">ushort</span></span>      |
| <span data-ttu-id="d1d07-125">2</span><span class="sxs-lookup"><span data-stu-id="d1d07-125">2</span></span>     | <span data-ttu-id="d1d07-126">/XMP/EXIF: Kontrast</span><span class="sxs-lookup"><span data-stu-id="d1d07-126">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="d1d07-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="d1d07-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d1d07-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="d1d07-128">Write Paths</span></span>



| <span data-ttu-id="d1d07-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="d1d07-129">Order</span></span> | <span data-ttu-id="d1d07-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="d1d07-130">Path</span></span>                          | <span data-ttu-id="d1d07-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="d1d07-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="d1d07-132">1</span><span class="sxs-lookup"><span data-stu-id="d1d07-132">1</span></span>     | <span data-ttu-id="d1d07-133">/App1/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="d1d07-133">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="d1d07-134">ushort</span><span class="sxs-lookup"><span data-stu-id="d1d07-134">ushort</span></span>      |
| <span data-ttu-id="d1d07-135">2</span><span class="sxs-lookup"><span data-stu-id="d1d07-135">2</span></span>     | <span data-ttu-id="d1d07-136">/XMP/EXIF: Kontrast</span><span class="sxs-lookup"><span data-stu-id="d1d07-136">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="d1d07-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="d1d07-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d1d07-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="d1d07-138">Remove Paths</span></span>



| <span data-ttu-id="d1d07-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="d1d07-139">Order</span></span> | <span data-ttu-id="d1d07-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="d1d07-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="d1d07-141">1</span><span class="sxs-lookup"><span data-stu-id="d1d07-141">1</span></span>     | <span data-ttu-id="d1d07-142">/App1/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="d1d07-142">/app1/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="d1d07-143">2</span><span class="sxs-lookup"><span data-stu-id="d1d07-143">2</span></span>     | <span data-ttu-id="d1d07-144">/XMP/EXIF: Kontrast</span><span class="sxs-lookup"><span data-stu-id="d1d07-144">/xmp/exif:contrast</span></span>            |



 

### <a name="tiff-policies"></a><span data-ttu-id="d1d07-145">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d1d07-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="d1d07-146">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="d1d07-146">Read Paths</span></span>



| <span data-ttu-id="d1d07-147">Auftrag</span><span class="sxs-lookup"><span data-stu-id="d1d07-147">Order</span></span> | <span data-ttu-id="d1d07-148">Pfad</span><span class="sxs-lookup"><span data-stu-id="d1d07-148">Path</span></span>                     | <span data-ttu-id="d1d07-149">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="d1d07-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="d1d07-150">1</span><span class="sxs-lookup"><span data-stu-id="d1d07-150">1</span></span>     | <span data-ttu-id="d1d07-151">/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="d1d07-151">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="d1d07-152">ushort</span><span class="sxs-lookup"><span data-stu-id="d1d07-152">ushort</span></span>      |
| <span data-ttu-id="d1d07-153">2</span><span class="sxs-lookup"><span data-stu-id="d1d07-153">2</span></span>     | <span data-ttu-id="d1d07-154">/IFD/XMP/EXIF: Kontrast</span><span class="sxs-lookup"><span data-stu-id="d1d07-154">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="d1d07-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="d1d07-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d1d07-156">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="d1d07-156">Write Paths</span></span>



| <span data-ttu-id="d1d07-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="d1d07-157">Order</span></span> | <span data-ttu-id="d1d07-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="d1d07-158">Path</span></span>                     | <span data-ttu-id="d1d07-159">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="d1d07-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="d1d07-160">1</span><span class="sxs-lookup"><span data-stu-id="d1d07-160">1</span></span>     | <span data-ttu-id="d1d07-161">/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="d1d07-161">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="d1d07-162">ushort</span><span class="sxs-lookup"><span data-stu-id="d1d07-162">ushort</span></span>      |
| <span data-ttu-id="d1d07-163">2</span><span class="sxs-lookup"><span data-stu-id="d1d07-163">2</span></span>     | <span data-ttu-id="d1d07-164">/IFD/XMP/EXIF: Kontrast</span><span class="sxs-lookup"><span data-stu-id="d1d07-164">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="d1d07-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="d1d07-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d1d07-166">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="d1d07-166">Remove Paths</span></span>



| <span data-ttu-id="d1d07-167">Auftrag</span><span class="sxs-lookup"><span data-stu-id="d1d07-167">Order</span></span> | <span data-ttu-id="d1d07-168">Pfad</span><span class="sxs-lookup"><span data-stu-id="d1d07-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="d1d07-169">1</span><span class="sxs-lookup"><span data-stu-id="d1d07-169">1</span></span>     | <span data-ttu-id="d1d07-170">/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="d1d07-170">/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="d1d07-171">2</span><span class="sxs-lookup"><span data-stu-id="d1d07-171">2</span></span>     | <span data-ttu-id="d1d07-172">/IFD/XMP/EXIF: Kontrast</span><span class="sxs-lookup"><span data-stu-id="d1d07-172">/ifd/xmp/exif:contrast</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="d1d07-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1d07-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1d07-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d1d07-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1d07-175">System. Photo. Kontrast</span><span class="sxs-lookup"><span data-stu-id="d1d07-175">System.Photo.Contrast</span></span>](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
