---
description: Die Richtlinie für Fotometadaten für die System.Photo.FNumber-Eigenschaft.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: System.Photo.FNumber-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85443b849d9f810709f3e75c3082738e5377092f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443621"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="099e6-103">System.Photo.FNumber-Richtlinie für Fotometadaten</span><span class="sxs-lookup"><span data-stu-id="099e6-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="099e6-104">Die Richtlinie für Fotometadaten für die [System.Photo.FNumber-Eigenschaft.](../properties/props-system-photo-fnumber.md)</span><span class="sxs-lookup"><span data-stu-id="099e6-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="099e6-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="099e6-105">PKEY</span></span>

<span data-ttu-id="099e6-106">PKEY \_ Photo \_ FNumber</span><span class="sxs-lookup"><span data-stu-id="099e6-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="099e6-107">Container</span><span class="sxs-lookup"><span data-stu-id="099e6-107">Containers</span></span>

<span data-ttu-id="099e6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="099e6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="099e6-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="099e6-109">Read-Only</span></span>

<span data-ttu-id="099e6-110">Ja</span><span class="sxs-lookup"><span data-stu-id="099e6-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="099e6-111">PROPVARIANT-Ausgabetyp</span><span class="sxs-lookup"><span data-stu-id="099e6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="099e6-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="099e6-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="099e6-113">Konfliktlösungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="099e6-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="099e6-114">Dieser Wert wird von System.Photo.FNumberNumerator und System.Photo.FNumberDenominator generiert.</span><span class="sxs-lookup"><span data-stu-id="099e6-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="099e6-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="099e6-115">It cannot be written directly.</span></span> <span data-ttu-id="099e6-116">Werte aus verschiedenen Schemas werden abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="099e6-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="099e6-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="099e6-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="099e6-118">Lesepfade</span><span class="sxs-lookup"><span data-stu-id="099e6-118">Read Paths</span></span>



| <span data-ttu-id="099e6-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="099e6-119">Order</span></span> | <span data-ttu-id="099e6-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="099e6-120">Path</span></span>                          | <span data-ttu-id="099e6-121">Datenträgerformat</span><span class="sxs-lookup"><span data-stu-id="099e6-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="099e6-122">1</span><span class="sxs-lookup"><span data-stu-id="099e6-122">1</span></span>     | <span data-ttu-id="099e6-123">/app1/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="099e6-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="099e6-124">2</span><span class="sxs-lookup"><span data-stu-id="099e6-124">2</span></span>     | <span data-ttu-id="099e6-125">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="099e6-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="099e6-126">Schreibpfade</span><span class="sxs-lookup"><span data-stu-id="099e6-126">Write Paths</span></span>



| <span data-ttu-id="099e6-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="099e6-127">Order</span></span> | <span data-ttu-id="099e6-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="099e6-128">Path</span></span>                          | <span data-ttu-id="099e6-129">Datenträgerformat</span><span class="sxs-lookup"><span data-stu-id="099e6-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="099e6-130">1</span><span class="sxs-lookup"><span data-stu-id="099e6-130">1</span></span>     | <span data-ttu-id="099e6-131">/app1/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="099e6-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="099e6-132">2</span><span class="sxs-lookup"><span data-stu-id="099e6-132">2</span></span>     | <span data-ttu-id="099e6-133">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="099e6-133">/xmp/exif:FNumber</span></span>             |             | 
 

### <a name="remove-paths"></a><span data-ttu-id="099e6-134">Entfernen von Pfaden</span><span class="sxs-lookup"><span data-stu-id="099e6-134">Remove Paths</span></span>



| <span data-ttu-id="099e6-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="099e6-135">Order</span></span> | <span data-ttu-id="099e6-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="099e6-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="099e6-137">1</span><span class="sxs-lookup"><span data-stu-id="099e6-137">1</span></span>     | <span data-ttu-id="099e6-138">/app1/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="099e6-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="099e6-139">2</span><span class="sxs-lookup"><span data-stu-id="099e6-139">2</span></span>     | <span data-ttu-id="099e6-140">/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="099e6-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="099e6-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="099e6-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="099e6-142">Lesepfade</span><span class="sxs-lookup"><span data-stu-id="099e6-142">Read Paths</span></span>



| <span data-ttu-id="099e6-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="099e6-143">Order</span></span> | <span data-ttu-id="099e6-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="099e6-144">Path</span></span>                     | <span data-ttu-id="099e6-145">Datenträgerformat</span><span class="sxs-lookup"><span data-stu-id="099e6-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="099e6-146">1</span><span class="sxs-lookup"><span data-stu-id="099e6-146">1</span></span>     | <span data-ttu-id="099e6-147">/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="099e6-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="099e6-148">2</span><span class="sxs-lookup"><span data-stu-id="099e6-148">2</span></span>     | <span data-ttu-id="099e6-149">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="099e6-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="099e6-150">Schreibpfade</span><span class="sxs-lookup"><span data-stu-id="099e6-150">Write Paths</span></span>



| <span data-ttu-id="099e6-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="099e6-151">Order</span></span> | <span data-ttu-id="099e6-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="099e6-152">Path</span></span>                     | <span data-ttu-id="099e6-153">Datenträgerformat</span><span class="sxs-lookup"><span data-stu-id="099e6-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="099e6-154">1</span><span class="sxs-lookup"><span data-stu-id="099e6-154">1</span></span>     | <span data-ttu-id="099e6-155">/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="099e6-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="099e6-156">2</span><span class="sxs-lookup"><span data-stu-id="099e6-156">2</span></span>     | <span data-ttu-id="099e6-157">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="099e6-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="099e6-158">Entfernen von Pfaden</span><span class="sxs-lookup"><span data-stu-id="099e6-158">Remove Paths</span></span>



| <span data-ttu-id="099e6-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="099e6-159">Order</span></span> | <span data-ttu-id="099e6-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="099e6-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="099e6-161">1</span><span class="sxs-lookup"><span data-stu-id="099e6-161">1</span></span>     | <span data-ttu-id="099e6-162">/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="099e6-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="099e6-163">2</span><span class="sxs-lookup"><span data-stu-id="099e6-163">2</span></span>     | <span data-ttu-id="099e6-164">/ifd/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="099e6-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="099e6-165">Hinweise</span><span class="sxs-lookup"><span data-stu-id="099e6-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="099e6-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="099e6-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="099e6-167">System.Photo.FNumber</span><span class="sxs-lookup"><span data-stu-id="099e6-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
