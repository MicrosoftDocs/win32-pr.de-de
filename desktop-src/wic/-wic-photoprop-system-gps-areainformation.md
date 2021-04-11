---
description: Die fotometadatenrichtlinie für die System. GPS. areainformation-Eigenschaft.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: System. GPS. areainformation-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e14837da9ffa8b688caf1a544e222043988cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346418"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a><span data-ttu-id="08c08-103">System. GPS. areainformation-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="08c08-103">System.GPS.AreaInformation Photo Metadata Policy</span></span>

<span data-ttu-id="08c08-104">Die fotometadatenrichtlinie für die [System. GPS. areainformation](../properties/props-system-gps-areainformation.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="08c08-104">The photo metadata policy for the [System.GPS.AreaInformation](../properties/props-system-gps-areainformation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="08c08-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="08c08-105">PKEY</span></span>

<span data-ttu-id="08c08-106">Pkey \_ GPS \_ areainformation</span><span class="sxs-lookup"><span data-stu-id="08c08-106">PKEY\_GPS\_AreaInformation</span></span>

### <a name="containers"></a><span data-ttu-id="08c08-107">Container</span><span class="sxs-lookup"><span data-stu-id="08c08-107">Containers</span></span>

<span data-ttu-id="08c08-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="08c08-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="08c08-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08c08-109">Read-Only</span></span>

<span data-ttu-id="08c08-110">Nein</span><span class="sxs-lookup"><span data-stu-id="08c08-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="08c08-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="08c08-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="08c08-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="08c08-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="08c08-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="08c08-113">Input Type</span></span>

<span data-ttu-id="08c08-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="08c08-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="08c08-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="08c08-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="08c08-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="08c08-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="08c08-117">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="08c08-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="08c08-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="08c08-118">Read Paths</span></span>



| <span data-ttu-id="08c08-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="08c08-119">Order</span></span> | <span data-ttu-id="08c08-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="08c08-120">Path</span></span>                         | <span data-ttu-id="08c08-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="08c08-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="08c08-122">1</span><span class="sxs-lookup"><span data-stu-id="08c08-122">1</span></span>     | <span data-ttu-id="08c08-123">/App1/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="08c08-123">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="08c08-124">2</span><span class="sxs-lookup"><span data-stu-id="08c08-124">2</span></span>     | <span data-ttu-id="08c08-125">/XMP/EXIF: gpsareainformation</span><span class="sxs-lookup"><span data-stu-id="08c08-125">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="08c08-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="08c08-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="08c08-127">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="08c08-127">Write Paths</span></span>



| <span data-ttu-id="08c08-128">Auftrag</span><span class="sxs-lookup"><span data-stu-id="08c08-128">Order</span></span> | <span data-ttu-id="08c08-129">Pfad</span><span class="sxs-lookup"><span data-stu-id="08c08-129">Path</span></span>                         | <span data-ttu-id="08c08-130">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="08c08-130">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="08c08-131">1</span><span class="sxs-lookup"><span data-stu-id="08c08-131">1</span></span>     | <span data-ttu-id="08c08-132">/App1/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="08c08-132">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="08c08-133">2</span><span class="sxs-lookup"><span data-stu-id="08c08-133">2</span></span>     | <span data-ttu-id="08c08-134">/XMP/EXIF: gpsareainformation</span><span class="sxs-lookup"><span data-stu-id="08c08-134">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="08c08-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="08c08-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="08c08-136">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="08c08-136">Remove Paths</span></span>



| <span data-ttu-id="08c08-137">Auftrag</span><span class="sxs-lookup"><span data-stu-id="08c08-137">Order</span></span> | <span data-ttu-id="08c08-138">Pfad</span><span class="sxs-lookup"><span data-stu-id="08c08-138">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="08c08-139">1</span><span class="sxs-lookup"><span data-stu-id="08c08-139">1</span></span>     | <span data-ttu-id="08c08-140">/App1/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="08c08-140">/app1/ifd/gps/{ushort=28}</span></span>    |
| <span data-ttu-id="08c08-141">2</span><span class="sxs-lookup"><span data-stu-id="08c08-141">2</span></span>     | <span data-ttu-id="08c08-142">/XMP/EXIF: gpsareainformation</span><span class="sxs-lookup"><span data-stu-id="08c08-142">/xmp/exif:GPSAreaInformation</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="08c08-143">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="08c08-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="08c08-144">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="08c08-144">Read Paths</span></span>



| <span data-ttu-id="08c08-145">Auftrag</span><span class="sxs-lookup"><span data-stu-id="08c08-145">Order</span></span> | <span data-ttu-id="08c08-146">Pfad</span><span class="sxs-lookup"><span data-stu-id="08c08-146">Path</span></span>                             | <span data-ttu-id="08c08-147">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="08c08-147">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="08c08-148">1</span><span class="sxs-lookup"><span data-stu-id="08c08-148">1</span></span>     | <span data-ttu-id="08c08-149">/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="08c08-149">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="08c08-150">2</span><span class="sxs-lookup"><span data-stu-id="08c08-150">2</span></span>     | <span data-ttu-id="08c08-151">/IFD/XMP/EXIF: gpsareainformation</span><span class="sxs-lookup"><span data-stu-id="08c08-151">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="08c08-152">Unicode</span><span class="sxs-lookup"><span data-stu-id="08c08-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="08c08-153">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="08c08-153">Write Paths</span></span>



| <span data-ttu-id="08c08-154">Auftrag</span><span class="sxs-lookup"><span data-stu-id="08c08-154">Order</span></span> | <span data-ttu-id="08c08-155">Pfad</span><span class="sxs-lookup"><span data-stu-id="08c08-155">Path</span></span>                             | <span data-ttu-id="08c08-156">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="08c08-156">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="08c08-157">1</span><span class="sxs-lookup"><span data-stu-id="08c08-157">1</span></span>     | <span data-ttu-id="08c08-158">/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="08c08-158">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="08c08-159">2</span><span class="sxs-lookup"><span data-stu-id="08c08-159">2</span></span>     | <span data-ttu-id="08c08-160">/IFD/XMP/EXIF: gpsareainformation</span><span class="sxs-lookup"><span data-stu-id="08c08-160">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="08c08-161">Unicode</span><span class="sxs-lookup"><span data-stu-id="08c08-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="08c08-162">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="08c08-162">Remove Paths</span></span>



| <span data-ttu-id="08c08-163">Auftrag</span><span class="sxs-lookup"><span data-stu-id="08c08-163">Order</span></span> | <span data-ttu-id="08c08-164">Pfad</span><span class="sxs-lookup"><span data-stu-id="08c08-164">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="08c08-165">1</span><span class="sxs-lookup"><span data-stu-id="08c08-165">1</span></span>     | <span data-ttu-id="08c08-166">/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="08c08-166">/ifd/gps/{ushort=28}</span></span>             |
| <span data-ttu-id="08c08-167">2</span><span class="sxs-lookup"><span data-stu-id="08c08-167">2</span></span>     | <span data-ttu-id="08c08-168">/IFD/XMP/EXIF: gpsareainformation</span><span class="sxs-lookup"><span data-stu-id="08c08-168">/ifd/xmp/exif:GPSAreaInformation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="08c08-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08c08-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="08c08-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08c08-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08c08-171">System. GPS. areainformation</span><span class="sxs-lookup"><span data-stu-id="08c08-171">System.GPS.AreaInformation</span></span>](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
