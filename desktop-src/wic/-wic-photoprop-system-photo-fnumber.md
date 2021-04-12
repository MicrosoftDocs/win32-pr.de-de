---
description: Die fotometadatenrichtlinie für die System. Photo. f Number-Eigenschaft.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: System. Photo. f Number-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c518ef2a05dde8fd7e812d1d76a79cbe3efb4217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216810"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="453c0-103">System. Photo. f Number-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="453c0-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="453c0-104">Die fotometadatenrichtlinie für die [System. Photo. f Number](../properties/props-system-photo-fnumber.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="453c0-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="453c0-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="453c0-105">PKEY</span></span>

<span data-ttu-id="453c0-106">Pkey- \_ Foto- \_ f-Nummer</span><span class="sxs-lookup"><span data-stu-id="453c0-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="453c0-107">Container</span><span class="sxs-lookup"><span data-stu-id="453c0-107">Containers</span></span>

<span data-ttu-id="453c0-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="453c0-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="453c0-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="453c0-109">Read-Only</span></span>

<span data-ttu-id="453c0-110">Ja</span><span class="sxs-lookup"><span data-stu-id="453c0-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="453c0-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="453c0-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="453c0-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="453c0-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="453c0-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="453c0-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="453c0-114">Dieser Wert wird von "System. Photo. vnumzähler" und "System. Photo. f-Nenner" generiert.</span><span class="sxs-lookup"><span data-stu-id="453c0-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="453c0-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="453c0-115">It cannot be written directly.</span></span> <span data-ttu-id="453c0-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="453c0-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="453c0-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="453c0-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="453c0-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="453c0-118">Read Paths</span></span>



| <span data-ttu-id="453c0-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="453c0-119">Order</span></span> | <span data-ttu-id="453c0-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="453c0-120">Path</span></span>                          | <span data-ttu-id="453c0-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="453c0-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="453c0-122">1</span><span class="sxs-lookup"><span data-stu-id="453c0-122">1</span></span>     | <span data-ttu-id="453c0-123">/App1/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="453c0-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="453c0-124">2</span><span class="sxs-lookup"><span data-stu-id="453c0-124">2</span></span>     | <span data-ttu-id="453c0-125">/XMP/EXIF: f-Nummer</span><span class="sxs-lookup"><span data-stu-id="453c0-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="453c0-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="453c0-126">Write Paths</span></span>



|       |                               |             |     |
|-------|-------------------------------|-------------|-----|
| <span data-ttu-id="453c0-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="453c0-127">Order</span></span> | <span data-ttu-id="453c0-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="453c0-128">Path</span></span>                          | <span data-ttu-id="453c0-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="453c0-129">Disk Format</span></span> |     |
| <span data-ttu-id="453c0-130">1</span><span class="sxs-lookup"><span data-stu-id="453c0-130">1</span></span>     | <span data-ttu-id="453c0-131">/App1/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="453c0-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |     |
| <span data-ttu-id="453c0-132">2</span><span class="sxs-lookup"><span data-stu-id="453c0-132">2</span></span>     | <span data-ttu-id="453c0-133">/XMP/EXIF: f-Nummer</span><span class="sxs-lookup"><span data-stu-id="453c0-133">/xmp/exif:FNumber</span></span>             |             |     |



 

### <a name="remove-paths"></a><span data-ttu-id="453c0-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="453c0-134">Remove Paths</span></span>



| <span data-ttu-id="453c0-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="453c0-135">Order</span></span> | <span data-ttu-id="453c0-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="453c0-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="453c0-137">1</span><span class="sxs-lookup"><span data-stu-id="453c0-137">1</span></span>     | <span data-ttu-id="453c0-138">/App1/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="453c0-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="453c0-139">2</span><span class="sxs-lookup"><span data-stu-id="453c0-139">2</span></span>     | <span data-ttu-id="453c0-140">/XMP/EXIF: f-Nummer</span><span class="sxs-lookup"><span data-stu-id="453c0-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="453c0-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="453c0-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="453c0-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="453c0-142">Read Paths</span></span>



| <span data-ttu-id="453c0-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="453c0-143">Order</span></span> | <span data-ttu-id="453c0-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="453c0-144">Path</span></span>                     | <span data-ttu-id="453c0-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="453c0-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="453c0-146">1</span><span class="sxs-lookup"><span data-stu-id="453c0-146">1</span></span>     | <span data-ttu-id="453c0-147">/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="453c0-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="453c0-148">2</span><span class="sxs-lookup"><span data-stu-id="453c0-148">2</span></span>     | <span data-ttu-id="453c0-149">/IFD/XMP/EXIF: f-Nummer</span><span class="sxs-lookup"><span data-stu-id="453c0-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="453c0-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="453c0-150">Write Paths</span></span>



| <span data-ttu-id="453c0-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="453c0-151">Order</span></span> | <span data-ttu-id="453c0-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="453c0-152">Path</span></span>                     | <span data-ttu-id="453c0-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="453c0-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="453c0-154">1</span><span class="sxs-lookup"><span data-stu-id="453c0-154">1</span></span>     | <span data-ttu-id="453c0-155">/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="453c0-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="453c0-156">2</span><span class="sxs-lookup"><span data-stu-id="453c0-156">2</span></span>     | <span data-ttu-id="453c0-157">/IFD/XMP/EXIF: f-Nummer</span><span class="sxs-lookup"><span data-stu-id="453c0-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="453c0-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="453c0-158">Remove Paths</span></span>



| <span data-ttu-id="453c0-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="453c0-159">Order</span></span> | <span data-ttu-id="453c0-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="453c0-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="453c0-161">1</span><span class="sxs-lookup"><span data-stu-id="453c0-161">1</span></span>     | <span data-ttu-id="453c0-162">/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="453c0-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="453c0-163">2</span><span class="sxs-lookup"><span data-stu-id="453c0-163">2</span></span>     | <span data-ttu-id="453c0-164">/IFD/XMP/EXIF: f-Nummer</span><span class="sxs-lookup"><span data-stu-id="453c0-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="453c0-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="453c0-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="453c0-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="453c0-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="453c0-167">System. Photo. f Number</span><span class="sxs-lookup"><span data-stu-id="453c0-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
