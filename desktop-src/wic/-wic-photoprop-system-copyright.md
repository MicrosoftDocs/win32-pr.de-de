---
description: Die fotometadatenrichtlinie für die System. Copyright-Eigenschaft.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: System. Copyright Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc65024458d88088e3c0cbeccc3bc9ea0211910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364230"
---
# <a name="systemcopyright-photo-metadata-policy"></a><span data-ttu-id="540ba-103">System. Copyright Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="540ba-103">System.Copyright Photo Metadata Policy</span></span>

<span data-ttu-id="540ba-104">Die fotometadatenrichtlinie für die [System. Copyright](../properties/props-system-copyright.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="540ba-104">The photo metadata policy for the [System.Copyright](../properties/props-system-copyright.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="540ba-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="540ba-105">PKEY</span></span>

<span data-ttu-id="540ba-106">Pkey- \_ Copyright</span><span class="sxs-lookup"><span data-stu-id="540ba-106">PKEY\_Copyright</span></span>

### <a name="containers"></a><span data-ttu-id="540ba-107">Container</span><span class="sxs-lookup"><span data-stu-id="540ba-107">Containers</span></span>

<span data-ttu-id="540ba-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="540ba-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="540ba-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="540ba-109">Read-Only</span></span>

<span data-ttu-id="540ba-110">Nein</span><span class="sxs-lookup"><span data-stu-id="540ba-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="540ba-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="540ba-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="540ba-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="540ba-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="540ba-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="540ba-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="540ba-114">String</span><span class="sxs-lookup"><span data-stu-id="540ba-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="540ba-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="540ba-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="540ba-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="540ba-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="540ba-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="540ba-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="540ba-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="540ba-118">Read Paths</span></span>



| <span data-ttu-id="540ba-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="540ba-119">Order</span></span> | <span data-ttu-id="540ba-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="540ba-120">Path</span></span>                                      | <span data-ttu-id="540ba-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="540ba-121">Disk Format</span></span> |
|-------|-------------------------------------------|-------------|
|       | <span data-ttu-id="540ba-122">/App1/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="540ba-122">/app1/ifd/{ushort=33432}</span></span>                  | <span data-ttu-id="540ba-123">ascii</span><span class="sxs-lookup"><span data-stu-id="540ba-123">ascii</span></span>       |
|       | <span data-ttu-id="540ba-124">/app13/IRB/8bimiptc/IPTC/Copyright Hinweis</span><span class="sxs-lookup"><span data-stu-id="540ba-124">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |             |
|       | <span data-ttu-id="540ba-125">/XMP/ <xmpalt> DC: Rechte</span><span class="sxs-lookup"><span data-stu-id="540ba-125">/xmp/<xmpalt>dc:rights</span></span>              | <span data-ttu-id="540ba-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="540ba-126">unicode</span></span>     |
|       | <span data-ttu-id="540ba-127">/XMP/DC: Rechte</span><span class="sxs-lookup"><span data-stu-id="540ba-127">/xmp/dc:rights</span></span>                            | <span data-ttu-id="540ba-128">Unicode</span><span class="sxs-lookup"><span data-stu-id="540ba-128">unicode</span></span>     |
|       | <span data-ttu-id="540ba-129">/app13/IRB/8bimiptc/IPTC/Copyright Hinweis</span><span class="sxs-lookup"><span data-stu-id="540ba-129">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="540ba-130">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="540ba-130">Write Paths</span></span>



| <span data-ttu-id="540ba-131">Auftrag</span><span class="sxs-lookup"><span data-stu-id="540ba-131">Order</span></span> | <span data-ttu-id="540ba-132">Pfad</span><span class="sxs-lookup"><span data-stu-id="540ba-132">Path</span></span>                                      | <span data-ttu-id="540ba-133">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="540ba-133">Disk Format</span></span> |
|-------|-------------------------------------------|-------------|
|       | <span data-ttu-id="540ba-134">/XMP/DC: Rechte</span><span class="sxs-lookup"><span data-stu-id="540ba-134">/xmp/dc:rights</span></span>                            | <span data-ttu-id="540ba-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="540ba-135">unicode</span></span>     |
|       | <span data-ttu-id="540ba-136">/XMP/ <xmpalt> DC: Rechte</span><span class="sxs-lookup"><span data-stu-id="540ba-136">/xmp/<xmpalt>dc:rights</span></span>              | <span data-ttu-id="540ba-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="540ba-137">unicode</span></span>     |
|       | <span data-ttu-id="540ba-138">/app13/IRB/8bimiptc/IPTC/Copyright Hinweis</span><span class="sxs-lookup"><span data-stu-id="540ba-138">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |             |
|       | <span data-ttu-id="540ba-139">/App1/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="540ba-139">/app1/ifd/{ushort=33432}</span></span>                  | <span data-ttu-id="540ba-140">ascii</span><span class="sxs-lookup"><span data-stu-id="540ba-140">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="540ba-141">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="540ba-141">Remove Paths</span></span>



| <span data-ttu-id="540ba-142">Auftrag</span><span class="sxs-lookup"><span data-stu-id="540ba-142">Order</span></span> | <span data-ttu-id="540ba-143">Pfad</span><span class="sxs-lookup"><span data-stu-id="540ba-143">Path</span></span>                                      |
|-------|-------------------------------------------|
|       | <span data-ttu-id="540ba-144">/XMP/DC: Rechte</span><span class="sxs-lookup"><span data-stu-id="540ba-144">/xmp/dc:rights</span></span>                            |
|       | <span data-ttu-id="540ba-145">/app13/IRB/8bimiptc/IPTC/Copyright Hinweis</span><span class="sxs-lookup"><span data-stu-id="540ba-145">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |
|       | <span data-ttu-id="540ba-146">/App1/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="540ba-146">/app1/ifd/{ushort=33432}</span></span>                  |



 

### <a name="tiff-policy"></a><span data-ttu-id="540ba-147">TIFF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="540ba-147">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="540ba-148">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="540ba-148">Read Paths</span></span>



| <span data-ttu-id="540ba-149">Auftrag</span><span class="sxs-lookup"><span data-stu-id="540ba-149">Order</span></span> | <span data-ttu-id="540ba-150">Pfad</span><span class="sxs-lookup"><span data-stu-id="540ba-150">Path</span></span>                                    | <span data-ttu-id="540ba-151">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="540ba-151">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
|       | <span data-ttu-id="540ba-152">/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="540ba-152">/ifd/{ushort=33432}</span></span>                     | <span data-ttu-id="540ba-153">ascii</span><span class="sxs-lookup"><span data-stu-id="540ba-153">ascii</span></span>       |
|       | <span data-ttu-id="540ba-154">/IFD/IPTC/Copyright Hinweis</span><span class="sxs-lookup"><span data-stu-id="540ba-154">/ifd/iptc/copyright notice</span></span>              |             |
|       | <span data-ttu-id="540ba-155">/IFD/XMP/ <xmpalt> DC: Rechte</span><span class="sxs-lookup"><span data-stu-id="540ba-155">/ifd/xmp/<xmpalt>dc:rights</span></span>        | <span data-ttu-id="540ba-156">Unicode</span><span class="sxs-lookup"><span data-stu-id="540ba-156">unicode</span></span>     |
|       | <span data-ttu-id="540ba-157">/IFD/XMP/DC: Rechte</span><span class="sxs-lookup"><span data-stu-id="540ba-157">/ifd/xmp/dc:rights</span></span>                      | <span data-ttu-id="540ba-158">Unicode</span><span class="sxs-lookup"><span data-stu-id="540ba-158">unicode</span></span>     |
|       | <span data-ttu-id="540ba-159">/IFD/IPTC/Copyright Hinweis</span><span class="sxs-lookup"><span data-stu-id="540ba-159">/ifd/iptc/copyright notice</span></span>              |             |
|       | <span data-ttu-id="540ba-160">/IFD/IRB/8bimiptc/IPTC/Copyright Hinweis</span><span class="sxs-lookup"><span data-stu-id="540ba-160">/ifd/irb/8bimiptc/iptc/copyright notice</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="540ba-161">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="540ba-161">Write Paths</span></span>



| <span data-ttu-id="540ba-162">Auftrag</span><span class="sxs-lookup"><span data-stu-id="540ba-162">Order</span></span> | <span data-ttu-id="540ba-163">Pfad</span><span class="sxs-lookup"><span data-stu-id="540ba-163">Path</span></span>                                    | <span data-ttu-id="540ba-164">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="540ba-164">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
|       | <span data-ttu-id="540ba-165">/IFD/XMP/DC: Rechte</span><span class="sxs-lookup"><span data-stu-id="540ba-165">/ifd/xmp/dc:rights</span></span>                      | <span data-ttu-id="540ba-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="540ba-166">unicode</span></span>     |
|       | <span data-ttu-id="540ba-167">/IFD/XMP/ <xmpalt> DC: Rechte</span><span class="sxs-lookup"><span data-stu-id="540ba-167">/ifd/xmp/<xmpalt>dc:rights</span></span>        | <span data-ttu-id="540ba-168">Unicode</span><span class="sxs-lookup"><span data-stu-id="540ba-168">unicode</span></span>     |
|       | <span data-ttu-id="540ba-169">/IFD/IPTC/Copyright Hinweis</span><span class="sxs-lookup"><span data-stu-id="540ba-169">/ifd/iptc/copyright notice</span></span>              |             |
|       | <span data-ttu-id="540ba-170">/IFD/IRB/8bimiptc/IPTC/Copyright Hinweis</span><span class="sxs-lookup"><span data-stu-id="540ba-170">/ifd/irb/8bimiptc/iptc/copyright notice</span></span> |             |
|       | <span data-ttu-id="540ba-171">/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="540ba-171">/ifd/{ushort=33432}</span></span>                     | <span data-ttu-id="540ba-172">ascii</span><span class="sxs-lookup"><span data-stu-id="540ba-172">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="540ba-173">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="540ba-173">Remove Paths</span></span>



| <span data-ttu-id="540ba-174">Auftrag</span><span class="sxs-lookup"><span data-stu-id="540ba-174">Order</span></span> | <span data-ttu-id="540ba-175">Pfad</span><span class="sxs-lookup"><span data-stu-id="540ba-175">Path</span></span>                                    |
|-------|-----------------------------------------|
|       | <span data-ttu-id="540ba-176">/IFD/XMP/DC: Rechte</span><span class="sxs-lookup"><span data-stu-id="540ba-176">/ifd/xmp/dc:rights</span></span>                      |
|       | <span data-ttu-id="540ba-177">/IFD/IPTC/Copyright Hinweis</span><span class="sxs-lookup"><span data-stu-id="540ba-177">/ifd/iptc/copyright notice</span></span>              |
|       | <span data-ttu-id="540ba-178">/IFD/IRB/8bimiptc/IPTC/Copyright Hinweis</span><span class="sxs-lookup"><span data-stu-id="540ba-178">/ifd/irb/8bimiptc/iptc/copyright notice</span></span> |
|       | <span data-ttu-id="540ba-179">/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="540ba-179">/ifd/{ushort=33432}</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="540ba-180">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="540ba-180">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="540ba-181">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="540ba-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="540ba-182">System. Copyright</span><span class="sxs-lookup"><span data-stu-id="540ba-182">System.Copyright</span></span>](../properties/props-system-copyright.md)
</dt> </dl>

 

 
