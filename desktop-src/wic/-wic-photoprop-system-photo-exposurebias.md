---
description: Die fotometadatenrichtlinie für die System. Photo. exposurebias-Eigenschaft.
ms.assetid: 00ebe037-0116-4d75-868b-d75b3e58a84d
title: System. Photo. exposurebias-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709aa21da7cec56d36b5de643681a592873717bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360659"
---
# <a name="systemphotoexposurebias-photo-metadata-policy"></a><span data-ttu-id="555b5-103">System. Photo. exposurebias-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="555b5-103">System.Photo.ExposureBias Photo Metadata Policy</span></span>

<span data-ttu-id="555b5-104">Die fotometadatenrichtlinie für die [System. Photo. exposurebias](../properties/props-system-photo-exposurebias.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="555b5-104">The photo metadata policy for the [System.Photo.ExposureBias](../properties/props-system-photo-exposurebias.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="555b5-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="555b5-105">PKEY</span></span>

<span data-ttu-id="555b5-106">Pkey- \_ Foto \_ exposurebias</span><span class="sxs-lookup"><span data-stu-id="555b5-106">PKEY\_Photo\_ExposureBias</span></span>

### <a name="containers"></a><span data-ttu-id="555b5-107">Container</span><span class="sxs-lookup"><span data-stu-id="555b5-107">Containers</span></span>

<span data-ttu-id="555b5-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="555b5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="555b5-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="555b5-109">Read-Only</span></span>

<span data-ttu-id="555b5-110">Ja</span><span class="sxs-lookup"><span data-stu-id="555b5-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="555b5-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="555b5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="555b5-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="555b5-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="555b5-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="555b5-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="555b5-114">Dieser Wert wird von "System. Photo. exposurebiasnumerator" und "System. Photo. exposurebiasnenner" generiert.</span><span class="sxs-lookup"><span data-stu-id="555b5-114">This value is generated from System.Photo.ExposureBiasNumerator and System.Photo.ExposureBiasDenominator.</span></span> <span data-ttu-id="555b5-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="555b5-115">It cannot be written directly.</span></span> <span data-ttu-id="555b5-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="555b5-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="555b5-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="555b5-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="555b5-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="555b5-118">Read Paths</span></span>



| <span data-ttu-id="555b5-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="555b5-119">Order</span></span> | <span data-ttu-id="555b5-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="555b5-120">Path</span></span>                          | <span data-ttu-id="555b5-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="555b5-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="555b5-122">1</span><span class="sxs-lookup"><span data-stu-id="555b5-122">1</span></span>     | <span data-ttu-id="555b5-123">/App1/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="555b5-123">/app1/ifd/exif/{ushort=37380}</span></span> |             |
| <span data-ttu-id="555b5-124">2</span><span class="sxs-lookup"><span data-stu-id="555b5-124">2</span></span>     | <span data-ttu-id="555b5-125">/XMP/EXIF: ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="555b5-125">/xmp/exif:ExposureBiasValue</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="555b5-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="555b5-126">Write Paths</span></span>



| <span data-ttu-id="555b5-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="555b5-127">Order</span></span> | <span data-ttu-id="555b5-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="555b5-128">Path</span></span>                          | <span data-ttu-id="555b5-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="555b5-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="555b5-130">1</span><span class="sxs-lookup"><span data-stu-id="555b5-130">1</span></span>     | <span data-ttu-id="555b5-131">/App1/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="555b5-131">/app1/ifd/exif/{ushort=37380}</span></span> |             |
| <span data-ttu-id="555b5-132">2</span><span class="sxs-lookup"><span data-stu-id="555b5-132">2</span></span>     | <span data-ttu-id="555b5-133">/XMP/EXIF: ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="555b5-133">/xmp/exif:ExposureBiasValue</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="555b5-134">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="555b5-134">Remove Paths</span></span>



| <span data-ttu-id="555b5-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="555b5-135">Order</span></span> | <span data-ttu-id="555b5-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="555b5-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="555b5-137">1</span><span class="sxs-lookup"><span data-stu-id="555b5-137">1</span></span>     | <span data-ttu-id="555b5-138">/App1/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="555b5-138">/app1/ifd/exif/{ushort=37380}</span></span> |
| <span data-ttu-id="555b5-139">2</span><span class="sxs-lookup"><span data-stu-id="555b5-139">2</span></span>     | <span data-ttu-id="555b5-140">/XMP/EXIF: ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="555b5-140">/xmp/exif:exposurebiasvalue</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="555b5-141">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="555b5-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="555b5-142">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="555b5-142">Read Paths</span></span>



| <span data-ttu-id="555b5-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="555b5-143">Order</span></span> | <span data-ttu-id="555b5-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="555b5-144">Path</span></span>                            | <span data-ttu-id="555b5-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="555b5-145">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="555b5-146">1</span><span class="sxs-lookup"><span data-stu-id="555b5-146">1</span></span>     | <span data-ttu-id="555b5-147">/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="555b5-147">/ifd/exif/{ushort=37380}</span></span>        |             |
| <span data-ttu-id="555b5-148">2</span><span class="sxs-lookup"><span data-stu-id="555b5-148">2</span></span>     | <span data-ttu-id="555b5-149">/IFD/XMP/EXIF: ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="555b5-149">/ifd/xmp/exif:ExposureBiasValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="555b5-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="555b5-150">Write Paths</span></span>



| <span data-ttu-id="555b5-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="555b5-151">Order</span></span> | <span data-ttu-id="555b5-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="555b5-152">Path</span></span>                            | <span data-ttu-id="555b5-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="555b5-153">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="555b5-154">1</span><span class="sxs-lookup"><span data-stu-id="555b5-154">1</span></span>     | <span data-ttu-id="555b5-155">/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="555b5-155">/ifd/exif/{ushort=37380}</span></span>        |             |
| <span data-ttu-id="555b5-156">2</span><span class="sxs-lookup"><span data-stu-id="555b5-156">2</span></span>     | <span data-ttu-id="555b5-157">/IFD/XMP/EXIF: ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="555b5-157">/ifd/xmp/exif:ExposureBiasValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="555b5-158">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="555b5-158">Remove Paths</span></span>



| <span data-ttu-id="555b5-159">Auftrag</span><span class="sxs-lookup"><span data-stu-id="555b5-159">Order</span></span> | <span data-ttu-id="555b5-160">Pfad</span><span class="sxs-lookup"><span data-stu-id="555b5-160">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="555b5-161">1</span><span class="sxs-lookup"><span data-stu-id="555b5-161">1</span></span>     | <span data-ttu-id="555b5-162">/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="555b5-162">/ifd/exif/{ushort=37380}</span></span>        |
| <span data-ttu-id="555b5-163">2</span><span class="sxs-lookup"><span data-stu-id="555b5-163">2</span></span>     | <span data-ttu-id="555b5-164">/IFD/XMP/EXIF: ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="555b5-164">/ifd/xmp/exif:exposurebiasvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="555b5-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="555b5-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="555b5-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="555b5-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="555b5-167">System. Photo. exposurebias</span><span class="sxs-lookup"><span data-stu-id="555b5-167">System.Photo.ExposureBias</span></span>](../properties/props-system-photo-exposurebias.md)
</dt> </dl>

 

 
