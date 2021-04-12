---
description: Die fotometadatenrichtlinie für die System. GPS. Date-Eigenschaft.
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: System. GPS. Date-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218033"
---
# <a name="systemgpsdate-photo-metadata-policy"></a><span data-ttu-id="47096-103">System. GPS. Date-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="47096-103">System.GPS.Date Photo Metadata Policy</span></span>

<span data-ttu-id="47096-104">Die fotometadatenrichtlinie für die [System. GPS. Date](../properties/props-system-gps-date.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="47096-104">The photo metadata policy for the [System.GPS.Date](../properties/props-system-gps-date.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="47096-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="47096-105">PKEY</span></span>

<span data-ttu-id="47096-106">Pkey \_ -GPS- \_ Datum</span><span class="sxs-lookup"><span data-stu-id="47096-106">PKEY\_GPS\_Date</span></span>

### <a name="containers"></a><span data-ttu-id="47096-107">Container</span><span class="sxs-lookup"><span data-stu-id="47096-107">Containers</span></span>

<span data-ttu-id="47096-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="47096-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="47096-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47096-109">Read-Only</span></span>

<span data-ttu-id="47096-110">Nein</span><span class="sxs-lookup"><span data-stu-id="47096-110">No</span></span>

### <a name="input-type"></a><span data-ttu-id="47096-111">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="47096-111">Input Type</span></span>

<span data-ttu-id="47096-112">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="47096-112">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="47096-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="47096-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="47096-114">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="47096-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="47096-115">JPEG-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="47096-115">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="47096-116">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="47096-116">Read Paths</span></span>



| <span data-ttu-id="47096-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="47096-117">Order</span></span> | <span data-ttu-id="47096-118">Pfad</span><span class="sxs-lookup"><span data-stu-id="47096-118">Path</span></span>                      | <span data-ttu-id="47096-119">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="47096-119">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="47096-120">1</span><span class="sxs-lookup"><span data-stu-id="47096-120">1</span></span>     | <span data-ttu-id="47096-121">/App1/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="47096-121">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="47096-122">ascii</span><span class="sxs-lookup"><span data-stu-id="47096-122">ascii</span></span>       |
| <span data-ttu-id="47096-123">2</span><span class="sxs-lookup"><span data-stu-id="47096-123">2</span></span>     | <span data-ttu-id="47096-124">/XMP/EXIF: gpstimestamp</span><span class="sxs-lookup"><span data-stu-id="47096-124">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="47096-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="47096-125">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="47096-126">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="47096-126">Write Paths</span></span>



| <span data-ttu-id="47096-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="47096-127">Order</span></span> | <span data-ttu-id="47096-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="47096-128">Path</span></span>                      | <span data-ttu-id="47096-129">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="47096-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="47096-130">1</span><span class="sxs-lookup"><span data-stu-id="47096-130">1</span></span>     | <span data-ttu-id="47096-131">/App1/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="47096-131">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="47096-132">ascii</span><span class="sxs-lookup"><span data-stu-id="47096-132">ascii</span></span>       |
| <span data-ttu-id="47096-133">2</span><span class="sxs-lookup"><span data-stu-id="47096-133">2</span></span>     | <span data-ttu-id="47096-134">/XMP/EXIF: gpstimestamp</span><span class="sxs-lookup"><span data-stu-id="47096-134">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="47096-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="47096-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="47096-136">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="47096-136">Remove Paths</span></span>



| <span data-ttu-id="47096-137">Auftrag</span><span class="sxs-lookup"><span data-stu-id="47096-137">Order</span></span> | <span data-ttu-id="47096-138">Pfad</span><span class="sxs-lookup"><span data-stu-id="47096-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="47096-139">1</span><span class="sxs-lookup"><span data-stu-id="47096-139">1</span></span>     | <span data-ttu-id="47096-140">/App1/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="47096-140">/app1/ifd/gps/{ushort=29}</span></span> |
| <span data-ttu-id="47096-141">2</span><span class="sxs-lookup"><span data-stu-id="47096-141">2</span></span>     | <span data-ttu-id="47096-142">/XMP/EXIF: gpstimestamp</span><span class="sxs-lookup"><span data-stu-id="47096-142">/xmp/exif:GPSTimeStamp</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="47096-143">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="47096-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="47096-144">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="47096-144">Read Paths</span></span>



| <span data-ttu-id="47096-145">Auftrag</span><span class="sxs-lookup"><span data-stu-id="47096-145">Order</span></span> | <span data-ttu-id="47096-146">Pfad</span><span class="sxs-lookup"><span data-stu-id="47096-146">Path</span></span>                       | <span data-ttu-id="47096-147">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="47096-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="47096-148">1</span><span class="sxs-lookup"><span data-stu-id="47096-148">1</span></span>     | <span data-ttu-id="47096-149">/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="47096-149">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="47096-150">ascii</span><span class="sxs-lookup"><span data-stu-id="47096-150">ascii</span></span>       |
| <span data-ttu-id="47096-151">2</span><span class="sxs-lookup"><span data-stu-id="47096-151">2</span></span>     | <span data-ttu-id="47096-152">/IFD/XMP/EXIF: gpstimestamp</span><span class="sxs-lookup"><span data-stu-id="47096-152">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="47096-153">Unicode</span><span class="sxs-lookup"><span data-stu-id="47096-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="47096-154">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="47096-154">Write Paths</span></span>



| <span data-ttu-id="47096-155">Auftrag</span><span class="sxs-lookup"><span data-stu-id="47096-155">Order</span></span> | <span data-ttu-id="47096-156">Pfad</span><span class="sxs-lookup"><span data-stu-id="47096-156">Path</span></span>                       | <span data-ttu-id="47096-157">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="47096-157">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="47096-158">1</span><span class="sxs-lookup"><span data-stu-id="47096-158">1</span></span>     | <span data-ttu-id="47096-159">/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="47096-159">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="47096-160">ascii</span><span class="sxs-lookup"><span data-stu-id="47096-160">ascii</span></span>       |
| <span data-ttu-id="47096-161">2</span><span class="sxs-lookup"><span data-stu-id="47096-161">2</span></span>     | <span data-ttu-id="47096-162">/IFD/XMP/EXIF: gpstimestamp</span><span class="sxs-lookup"><span data-stu-id="47096-162">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="47096-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="47096-163">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="47096-164">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="47096-164">Remove Paths</span></span>



| <span data-ttu-id="47096-165">Auftrag</span><span class="sxs-lookup"><span data-stu-id="47096-165">Order</span></span> | <span data-ttu-id="47096-166">Pfad</span><span class="sxs-lookup"><span data-stu-id="47096-166">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="47096-167">1</span><span class="sxs-lookup"><span data-stu-id="47096-167">1</span></span>     | <span data-ttu-id="47096-168">/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="47096-168">/ifd/gps/{ushort=29}</span></span>       |
| <span data-ttu-id="47096-169">2</span><span class="sxs-lookup"><span data-stu-id="47096-169">2</span></span>     | <span data-ttu-id="47096-170">/IFD/XMP/EXIF: gpstimestamp</span><span class="sxs-lookup"><span data-stu-id="47096-170">/ifd/xmp/exif:GPSTimeStamp</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="47096-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47096-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="47096-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47096-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47096-173">System. GPS. Date</span><span class="sxs-lookup"><span data-stu-id="47096-173">System.GPS.Date</span></span>](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
