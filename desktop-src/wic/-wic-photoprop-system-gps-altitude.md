---
description: Die fotometadatenrichtlinie für die System. GPS. Altitude-Eigenschaft.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: System. GPS. Altitude-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003d39d135c625a01035c023b5d7dc8d890b3b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357022"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a><span data-ttu-id="4a101-103">System. GPS. Altitude-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="4a101-103">System.GPS.Altitude Photo Metadata Policy</span></span>

<span data-ttu-id="4a101-104">Die fotometadatenrichtlinie für die [System. GPS. Altitude](../properties/props-system-gps-altitude.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4a101-104">The photo metadata policy for the [System.GPS.Altitude](../properties/props-system-gps-altitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4a101-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="4a101-105">PKEY</span></span>

<span data-ttu-id="4a101-106">Pkey \_ GPS- \_ Höhe</span><span class="sxs-lookup"><span data-stu-id="4a101-106">PKEY\_GPS\_Altitude</span></span>

### <a name="description"></a><span data-ttu-id="4a101-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a101-107">Description</span></span>

<span data-ttu-id="4a101-108">Die Höhe wird als absoluter Wert angegeben, auf den in Meter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4a101-108">The altitude is indicated as an absolute value referenced in meters.</span></span>

### <a name="containers"></a><span data-ttu-id="4a101-109">Container</span><span class="sxs-lookup"><span data-stu-id="4a101-109">Containers</span></span>

<span data-ttu-id="4a101-110">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4a101-110">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4a101-111">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4a101-111">Read-Only</span></span>

<span data-ttu-id="4a101-112">Ja</span><span class="sxs-lookup"><span data-stu-id="4a101-112">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4a101-113">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="4a101-113">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4a101-114">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="4a101-114">VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="4a101-115">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="4a101-115">Input PROPVARIANT Type</span></span>

<span data-ttu-id="4a101-116">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="4a101-116">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4a101-117">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="4a101-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="4a101-118">Dieser Wert kann durch Schreiben in "System. GPS. Altitude. Numerator" und "System. GPS. Altitude. Nenner" geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4a101-118">This value can be written by writing to System.GPS.Altitude.Numerator and System.GPS.Altitude.Denominator.</span></span> <span data-ttu-id="4a101-119">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4a101-119">It cannot be written directly.</span></span> <span data-ttu-id="4a101-120">Die Schreib Pfade in den folgenden Tabellen geben an, wo der Wert möglicherweise beim Generieren gespeichert wird, nicht, wenn er direkt geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="4a101-120">The write paths in the following tables indicate where the value may be saved when it is generated, not when it is written directly.</span></span> <span data-ttu-id="4a101-121">Wenn der Wert gelesen wird, werden Werte aus unterschiedlichen Schemas abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="4a101-121">When the value is read, values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4a101-122">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="4a101-122">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4a101-123">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="4a101-123">Read Paths</span></span>



| <span data-ttu-id="4a101-124">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4a101-124">Order</span></span> | <span data-ttu-id="4a101-125">Pfad</span><span class="sxs-lookup"><span data-stu-id="4a101-125">Path</span></span>                     | <span data-ttu-id="4a101-126">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="4a101-126">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4a101-127">1</span><span class="sxs-lookup"><span data-stu-id="4a101-127">1</span></span>     | <span data-ttu-id="4a101-128">/App1/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="4a101-128">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="4a101-129">2</span><span class="sxs-lookup"><span data-stu-id="4a101-129">2</span></span>     | <span data-ttu-id="4a101-130">/XMP/EXIF: gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="4a101-130">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="4a101-131">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="4a101-131">Write Paths</span></span>



| <span data-ttu-id="4a101-132">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4a101-132">Order</span></span> | <span data-ttu-id="4a101-133">Pfad</span><span class="sxs-lookup"><span data-stu-id="4a101-133">Path</span></span>                     | <span data-ttu-id="4a101-134">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="4a101-134">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4a101-135">1</span><span class="sxs-lookup"><span data-stu-id="4a101-135">1</span></span>     | <span data-ttu-id="4a101-136">/App1/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="4a101-136">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="4a101-137">2</span><span class="sxs-lookup"><span data-stu-id="4a101-137">2</span></span>     | <span data-ttu-id="4a101-138">/XMP/EXIF: gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="4a101-138">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="4a101-139">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="4a101-139">Remove Paths</span></span>



| <span data-ttu-id="4a101-140">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4a101-140">Order</span></span> | <span data-ttu-id="4a101-141">Pfad</span><span class="sxs-lookup"><span data-stu-id="4a101-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="4a101-142">1</span><span class="sxs-lookup"><span data-stu-id="4a101-142">1</span></span>     | <span data-ttu-id="4a101-143">/App1/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="4a101-143">/app1/ifd/gps/{ushort=6}</span></span> |
| <span data-ttu-id="4a101-144">2</span><span class="sxs-lookup"><span data-stu-id="4a101-144">2</span></span>     | <span data-ttu-id="4a101-145">/XMP/EXIF: gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="4a101-145">/xmp/exif:gpsaltitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="4a101-146">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="4a101-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4a101-147">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="4a101-147">Read Paths</span></span>



| <span data-ttu-id="4a101-148">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4a101-148">Order</span></span> | <span data-ttu-id="4a101-149">Pfad</span><span class="sxs-lookup"><span data-stu-id="4a101-149">Path</span></span>                      | <span data-ttu-id="4a101-150">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="4a101-150">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4a101-151">1</span><span class="sxs-lookup"><span data-stu-id="4a101-151">1</span></span>     | <span data-ttu-id="4a101-152">/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="4a101-152">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="4a101-153">2</span><span class="sxs-lookup"><span data-stu-id="4a101-153">2</span></span>     | <span data-ttu-id="4a101-154">/IFD/XMP/EXIF: gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="4a101-154">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="4a101-155">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="4a101-155">Write Paths</span></span>



| <span data-ttu-id="4a101-156">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4a101-156">Order</span></span> | <span data-ttu-id="4a101-157">Pfad</span><span class="sxs-lookup"><span data-stu-id="4a101-157">Path</span></span>                      | <span data-ttu-id="4a101-158">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="4a101-158">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4a101-159">1</span><span class="sxs-lookup"><span data-stu-id="4a101-159">1</span></span>     | <span data-ttu-id="4a101-160">/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="4a101-160">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="4a101-161">2</span><span class="sxs-lookup"><span data-stu-id="4a101-161">2</span></span>     | <span data-ttu-id="4a101-162">/IFD/XMP/EXIF: gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="4a101-162">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="4a101-163">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="4a101-163">Remove Paths</span></span>



| <span data-ttu-id="4a101-164">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4a101-164">Order</span></span> | <span data-ttu-id="4a101-165">Pfad</span><span class="sxs-lookup"><span data-stu-id="4a101-165">Path</span></span>                      |     |
|-------|---------------------------|-----|
| <span data-ttu-id="4a101-166">1</span><span class="sxs-lookup"><span data-stu-id="4a101-166">1</span></span>     | <span data-ttu-id="4a101-167">/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="4a101-167">/ifd/gps/{ushort=6}</span></span>       |     |
| <span data-ttu-id="4a101-168">2</span><span class="sxs-lookup"><span data-stu-id="4a101-168">2</span></span>     | <span data-ttu-id="4a101-169">/IFD/XMP/EXIF: gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="4a101-169">/ifd/xmp/exif:gpsaltitude</span></span> |     |



 

## <a name="remarks"></a><span data-ttu-id="4a101-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a101-170">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a101-171">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a101-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a101-172">System. GPS. Altitude</span><span class="sxs-lookup"><span data-stu-id="4a101-172">System.GPS.Altitude</span></span>](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
