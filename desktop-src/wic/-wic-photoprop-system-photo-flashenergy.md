---
description: Die fotometadatenrichtlinie für die System. Photo. Flash Energy-Eigenschaft.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: System. Photo. Flash Energy-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c272b4d6d14bf2f2e81d0964a3dc4395ba62dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050438"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a><span data-ttu-id="a7490-103">System. Photo. Flash Energy-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="a7490-103">System.Photo.FlashEnergy Photo Metadata Policy</span></span>

<span data-ttu-id="a7490-104">Die fotometadatenrichtlinie für die [System. Photo. Flash Energy](../properties/props-system-photo-flashenergy.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a7490-104">The photo metadata policy for the [System.Photo.FlashEnergy](../properties/props-system-photo-flashenergy.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a7490-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="a7490-105">PKEY</span></span>

<span data-ttu-id="a7490-106">Pkey \_ Photo \_ Flash Energy</span><span class="sxs-lookup"><span data-stu-id="a7490-106">PKEY\_Photo\_FlashEnergy</span></span>

### <a name="containers"></a><span data-ttu-id="a7490-107">Container</span><span class="sxs-lookup"><span data-stu-id="a7490-107">Containers</span></span>

<span data-ttu-id="a7490-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a7490-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a7490-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a7490-109">Read-Only</span></span>

<span data-ttu-id="a7490-110">Ja</span><span class="sxs-lookup"><span data-stu-id="a7490-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="a7490-111">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="a7490-111">Input Type</span></span>

<span data-ttu-id="a7490-112">Double</span><span class="sxs-lookup"><span data-stu-id="a7490-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a7490-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="a7490-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="a7490-114">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="a7490-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a7490-115">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a7490-115">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a7490-116">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="a7490-116">Read Paths</span></span>



| <span data-ttu-id="a7490-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a7490-117">Order</span></span> | <span data-ttu-id="a7490-118">Pfad</span><span class="sxs-lookup"><span data-stu-id="a7490-118">Path</span></span>                          | <span data-ttu-id="a7490-119">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a7490-119">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a7490-120">1</span><span class="sxs-lookup"><span data-stu-id="a7490-120">1</span></span>     | <span data-ttu-id="a7490-121">/App1/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="a7490-121">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="a7490-122">2</span><span class="sxs-lookup"><span data-stu-id="a7490-122">2</span></span>     | <span data-ttu-id="a7490-123">/XMP/EXIF: Flash Energy</span><span class="sxs-lookup"><span data-stu-id="a7490-123">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="a7490-124">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="a7490-124">Write Paths</span></span>



| <span data-ttu-id="a7490-125">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a7490-125">Order</span></span> | <span data-ttu-id="a7490-126">Pfad</span><span class="sxs-lookup"><span data-stu-id="a7490-126">Path</span></span>                          | <span data-ttu-id="a7490-127">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a7490-127">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a7490-128">1</span><span class="sxs-lookup"><span data-stu-id="a7490-128">1</span></span>     | <span data-ttu-id="a7490-129">/App1/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="a7490-129">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="a7490-130">2</span><span class="sxs-lookup"><span data-stu-id="a7490-130">2</span></span>     | <span data-ttu-id="a7490-131">/XMP/EXIF: Flash Energy</span><span class="sxs-lookup"><span data-stu-id="a7490-131">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a7490-132">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="a7490-132">Remove Paths</span></span>



| <span data-ttu-id="a7490-133">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a7490-133">Order</span></span> | <span data-ttu-id="a7490-134">Pfad</span><span class="sxs-lookup"><span data-stu-id="a7490-134">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="a7490-135">1</span><span class="sxs-lookup"><span data-stu-id="a7490-135">1</span></span>     | <span data-ttu-id="a7490-136">/App1/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="a7490-136">/app1/ifd/exif/{ushort=41483}</span></span> |
| <span data-ttu-id="a7490-137">2</span><span class="sxs-lookup"><span data-stu-id="a7490-137">2</span></span>     | <span data-ttu-id="a7490-138">/XMP/EXIF: Flash Energy</span><span class="sxs-lookup"><span data-stu-id="a7490-138">/xmp/exif:flashenergy</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="a7490-139">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="a7490-139">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a7490-140">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="a7490-140">Read Paths</span></span>



| <span data-ttu-id="a7490-141">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a7490-141">Order</span></span> | <span data-ttu-id="a7490-142">Pfad</span><span class="sxs-lookup"><span data-stu-id="a7490-142">Path</span></span>                      | <span data-ttu-id="a7490-143">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a7490-143">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a7490-144">1</span><span class="sxs-lookup"><span data-stu-id="a7490-144">1</span></span>     | <span data-ttu-id="a7490-145">/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="a7490-145">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="a7490-146">2</span><span class="sxs-lookup"><span data-stu-id="a7490-146">2</span></span>     | <span data-ttu-id="a7490-147">/IFD/XMP/EXIF: Flash Energy</span><span class="sxs-lookup"><span data-stu-id="a7490-147">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="a7490-148">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="a7490-148">Write Paths</span></span>



| <span data-ttu-id="a7490-149">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a7490-149">Order</span></span> | <span data-ttu-id="a7490-150">Pfad</span><span class="sxs-lookup"><span data-stu-id="a7490-150">Path</span></span>                      | <span data-ttu-id="a7490-151">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a7490-151">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a7490-152">1</span><span class="sxs-lookup"><span data-stu-id="a7490-152">1</span></span>     | <span data-ttu-id="a7490-153">/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="a7490-153">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="a7490-154">2</span><span class="sxs-lookup"><span data-stu-id="a7490-154">2</span></span>     | <span data-ttu-id="a7490-155">/IFD/XMP/EXIF: Flash Energy</span><span class="sxs-lookup"><span data-stu-id="a7490-155">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a7490-156">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="a7490-156">Remove Paths</span></span>



| <span data-ttu-id="a7490-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a7490-157">Order</span></span> | <span data-ttu-id="a7490-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="a7490-158">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="a7490-159">1</span><span class="sxs-lookup"><span data-stu-id="a7490-159">1</span></span>     | <span data-ttu-id="a7490-160">/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="a7490-160">/ifd/exif/{ushort=41483}</span></span>  |
| <span data-ttu-id="a7490-161">2</span><span class="sxs-lookup"><span data-stu-id="a7490-161">2</span></span>     | <span data-ttu-id="a7490-162">/IFD/XMP/EXIF: Flash Energy</span><span class="sxs-lookup"><span data-stu-id="a7490-162">/ifd/xmp/exif:flashenergy</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a7490-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7490-163">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7490-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a7490-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7490-165">System. Photo. Flash Energy</span><span class="sxs-lookup"><span data-stu-id="a7490-165">System.Photo.FlashEnergy</span></span>](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
