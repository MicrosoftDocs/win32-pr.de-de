---
description: Die fotometadatenrichtlinie für die System. Photo. shutterspeed-Eigenschaft.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: System. Photo. shutterspeed Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363289"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a><span data-ttu-id="b52c5-103">System. Photo. shutterspeed Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b52c5-103">System.Photo.ShutterSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="b52c5-104">Die fotometadatenrichtlinie für die [System. Photo. shutterspeed](../properties/props-system-photo-shutterspeed.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b52c5-104">The photo metadata policy for the [System.Photo.ShutterSpeed](../properties/props-system-photo-shutterspeed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b52c5-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="b52c5-105">PKEY</span></span>

<span data-ttu-id="b52c5-106">Pkey \_ Photo \_ shutterspeed</span><span class="sxs-lookup"><span data-stu-id="b52c5-106">PKEY\_Photo\_ShutterSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="b52c5-107">Container</span><span class="sxs-lookup"><span data-stu-id="b52c5-107">Containers</span></span>

<span data-ttu-id="b52c5-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b52c5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b52c5-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b52c5-109">Read-Only</span></span>

<span data-ttu-id="b52c5-110">Ja</span><span class="sxs-lookup"><span data-stu-id="b52c5-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b52c5-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="b52c5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b52c5-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="b52c5-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b52c5-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="b52c5-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="b52c5-114">Dieser Wert wird von "System. Photo. shutterspeednumerator" und "System. Photo. shutterspeednenner" generiert.</span><span class="sxs-lookup"><span data-stu-id="b52c5-114">This value is generated from System.Photo.ShutterSpeedNumerator and System.Photo.ShutterSpeedDenominator.</span></span> <span data-ttu-id="b52c5-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b52c5-115">It cannot be written directly.</span></span> <span data-ttu-id="b52c5-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="b52c5-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b52c5-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b52c5-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b52c5-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="b52c5-118">Read Paths</span></span>



| <span data-ttu-id="b52c5-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b52c5-119">Order</span></span> | <span data-ttu-id="b52c5-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="b52c5-120">Path</span></span>                          | <span data-ttu-id="b52c5-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b52c5-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b52c5-122">1</span><span class="sxs-lookup"><span data-stu-id="b52c5-122">1</span></span>     | <span data-ttu-id="b52c5-123">/App1/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="b52c5-123">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="b52c5-124">2</span><span class="sxs-lookup"><span data-stu-id="b52c5-124">2</span></span>     | <span data-ttu-id="b52c5-125">/XMP/EXIF: shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="b52c5-125">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="b52c5-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="b52c5-126">Write Paths</span></span>



| <span data-ttu-id="b52c5-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b52c5-127">Order</span></span> | <span data-ttu-id="b52c5-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="b52c5-128">Path</span></span>                          | <span data-ttu-id="b52c5-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b52c5-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b52c5-130">1</span><span class="sxs-lookup"><span data-stu-id="b52c5-130">1</span></span>     | <span data-ttu-id="b52c5-131">/App1/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="b52c5-131">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="b52c5-132">2</span><span class="sxs-lookup"><span data-stu-id="b52c5-132">2</span></span>     | <span data-ttu-id="b52c5-133">/XMP/EXIF: shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="b52c5-133">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b52c5-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="b52c5-134">Remove Paths</span></span>



| <span data-ttu-id="b52c5-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b52c5-135">Order</span></span> | <span data-ttu-id="b52c5-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="b52c5-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="b52c5-137">1</span><span class="sxs-lookup"><span data-stu-id="b52c5-137">1</span></span>     | <span data-ttu-id="b52c5-138">/App1/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="b52c5-138">/app1/ifd/exif/{ushort=37377}</span></span> |
| <span data-ttu-id="b52c5-139">2</span><span class="sxs-lookup"><span data-stu-id="b52c5-139">2</span></span>     | <span data-ttu-id="b52c5-140">/XMP/EXIF: shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="b52c5-140">/xmp/exif:shutterspeedvalue</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="b52c5-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="b52c5-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b52c5-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="b52c5-142">Read Paths</span></span>



| <span data-ttu-id="b52c5-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b52c5-143">Order</span></span> | <span data-ttu-id="b52c5-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="b52c5-144">Path</span></span>                            | <span data-ttu-id="b52c5-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b52c5-145">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="b52c5-146">1</span><span class="sxs-lookup"><span data-stu-id="b52c5-146">1</span></span>     | <span data-ttu-id="b52c5-147">/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="b52c5-147">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="b52c5-148">2</span><span class="sxs-lookup"><span data-stu-id="b52c5-148">2</span></span>     | <span data-ttu-id="b52c5-149">/IFD/XMP/EXIF: shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="b52c5-149">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b52c5-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="b52c5-150">Write Paths</span></span>



| <span data-ttu-id="b52c5-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b52c5-151">Order</span></span> | <span data-ttu-id="b52c5-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="b52c5-152">Path</span></span>                            | <span data-ttu-id="b52c5-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b52c5-153">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="b52c5-154">1</span><span class="sxs-lookup"><span data-stu-id="b52c5-154">1</span></span>     | <span data-ttu-id="b52c5-155">/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="b52c5-155">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="b52c5-156">2</span><span class="sxs-lookup"><span data-stu-id="b52c5-156">2</span></span>     | <span data-ttu-id="b52c5-157">/IFD/XMP/EXIF: shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="b52c5-157">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b52c5-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="b52c5-158">Remove Paths</span></span>



| <span data-ttu-id="b52c5-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b52c5-159">Order</span></span> | <span data-ttu-id="b52c5-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="b52c5-160">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="b52c5-161">1</span><span class="sxs-lookup"><span data-stu-id="b52c5-161">1</span></span>     | <span data-ttu-id="b52c5-162">/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="b52c5-162">/ifd/exif/{ushort=37377}</span></span>        |
| <span data-ttu-id="b52c5-163">2</span><span class="sxs-lookup"><span data-stu-id="b52c5-163">2</span></span>     | <span data-ttu-id="b52c5-164">/IFD/XMP/EXIF: shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="b52c5-164">/ifd/xmp/exif:shutterspeedvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b52c5-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b52c5-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b52c5-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b52c5-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b52c5-167">System. Photo. shutterspeed</span><span class="sxs-lookup"><span data-stu-id="b52c5-167">System.Photo.ShutterSpeed</span></span>](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
