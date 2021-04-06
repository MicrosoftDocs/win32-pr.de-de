---
description: Die fotometadatenrichtlinie für die System. ApplicationName-Eigenschaft.
ms.assetid: bf4b310a-7e63-45c5-a327-2638fb31d676
title: System. ApplicationName Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e36fac2a864cabfd7c1521d72357d187a8aea50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759505"
---
# <a name="systemapplicationname-photo-metadata-policy"></a><span data-ttu-id="a2b41-103">System. ApplicationName Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a2b41-103">System.ApplicationName Photo Metadata Policy</span></span>

<span data-ttu-id="a2b41-104">Die fotometadatenrichtlinie für die [System. ApplicationName](../properties/props-system-applicationname.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a2b41-104">The photo metadata policy for the [System.ApplicationName](../properties/props-system-applicationname.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a2b41-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="a2b41-105">PKEY</span></span>

<span data-ttu-id="a2b41-106">Pkey- \_ ApplicationName</span><span class="sxs-lookup"><span data-stu-id="a2b41-106">PKEY\_ApplicationName</span></span>

### <a name="containers"></a><span data-ttu-id="a2b41-107">Container</span><span class="sxs-lookup"><span data-stu-id="a2b41-107">Containers</span></span>

<span data-ttu-id="a2b41-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a2b41-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a2b41-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2b41-109">Read-Only</span></span>

<span data-ttu-id="a2b41-110">Nein</span><span class="sxs-lookup"><span data-stu-id="a2b41-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a2b41-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="a2b41-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a2b41-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a2b41-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="a2b41-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="a2b41-113">Input Type</span></span>

<span data-ttu-id="a2b41-114">String</span><span class="sxs-lookup"><span data-stu-id="a2b41-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a2b41-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="a2b41-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a2b41-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="a2b41-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a2b41-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a2b41-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a2b41-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="a2b41-118">Read Paths</span></span>



| <span data-ttu-id="a2b41-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a2b41-119">Order</span></span> | <span data-ttu-id="a2b41-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="a2b41-120">Path</span></span>                                         | <span data-ttu-id="a2b41-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a2b41-121">Disk Format</span></span> |
|-------|----------------------------------------------|-------------|
|       | <span data-ttu-id="a2b41-122">/App1/IFD/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="a2b41-122">/app1/ifd/{ushort=305}</span></span>                       | <span data-ttu-id="a2b41-123">ascii</span><span class="sxs-lookup"><span data-stu-id="a2b41-123">ascii</span></span>       |
|       | <span data-ttu-id="a2b41-124">/app13/IRB/8bimiptc/IPTC/Originating-Programm</span><span class="sxs-lookup"><span data-stu-id="a2b41-124">/app13/irb/8bimiptc/iptc/Originating Program</span></span> |             |
|       | <span data-ttu-id="a2b41-125">/XMP/XMP: kreatortool</span><span class="sxs-lookup"><span data-stu-id="a2b41-125">/xmp/xmp:CreatorTool</span></span>                         | <span data-ttu-id="a2b41-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-126">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-127">/XMP/XMP: kreatortool</span><span class="sxs-lookup"><span data-stu-id="a2b41-127">/xmp/xmp:creatortool</span></span>                         | <span data-ttu-id="a2b41-128">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-128">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-129">/XMP/TIFF: Software</span><span class="sxs-lookup"><span data-stu-id="a2b41-129">/xmp/tiff:Software</span></span>                           | <span data-ttu-id="a2b41-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-130">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-131">/XMP/TIFF: Software</span><span class="sxs-lookup"><span data-stu-id="a2b41-131">/xmp/tiff:software</span></span>                           | <span data-ttu-id="a2b41-132">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-132">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-133">/app13/IRB/8bimiptc/IPTC/Originating-Programm</span><span class="sxs-lookup"><span data-stu-id="a2b41-133">/app13/irb/8bimiptc/iptc/Originating Program</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="a2b41-134">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="a2b41-134">Write Paths</span></span>



| <span data-ttu-id="a2b41-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a2b41-135">Order</span></span> | <span data-ttu-id="a2b41-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="a2b41-136">Path</span></span>                                         | <span data-ttu-id="a2b41-137">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a2b41-137">Disk Format</span></span> |
|-------|----------------------------------------------|-------------|
|       | <span data-ttu-id="a2b41-138">/App1/IFD/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="a2b41-138">/app1/ifd/{ushort=305}</span></span>                       | <span data-ttu-id="a2b41-139">ascii</span><span class="sxs-lookup"><span data-stu-id="a2b41-139">ascii</span></span>       |
|       | <span data-ttu-id="a2b41-140">/XMP/XMP: kreatortool</span><span class="sxs-lookup"><span data-stu-id="a2b41-140">/xmp/xmp:CreatorTool</span></span>                         | <span data-ttu-id="a2b41-141">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-141">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-142">/XMP/XMP: kreatortool</span><span class="sxs-lookup"><span data-stu-id="a2b41-142">/xmp/xmp:creatortool</span></span>                         | <span data-ttu-id="a2b41-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-143">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-144">/XMP/TIFF: Software</span><span class="sxs-lookup"><span data-stu-id="a2b41-144">/xmp/tiff:Software</span></span>                           | <span data-ttu-id="a2b41-145">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-145">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-146">/XMP/TIFF: Software</span><span class="sxs-lookup"><span data-stu-id="a2b41-146">/xmp/tiff:software</span></span>                           | <span data-ttu-id="a2b41-147">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-147">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-148">/app13/IRB/8bimiptc/IPTC/Originating-Programm</span><span class="sxs-lookup"><span data-stu-id="a2b41-148">/app13/irb/8bimiptc/iptc/Originating Program</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a2b41-149">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="a2b41-149">Remove Paths</span></span>



| <span data-ttu-id="a2b41-150">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a2b41-150">Order</span></span> | <span data-ttu-id="a2b41-151">Pfad</span><span class="sxs-lookup"><span data-stu-id="a2b41-151">Path</span></span>                                         |
|-------|----------------------------------------------|
|       | <span data-ttu-id="a2b41-152">/App1/IFD/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="a2b41-152">/app1/ifd/{ushort=305}</span></span>                       |
|       | <span data-ttu-id="a2b41-153">/XMP/XMP: kreatortool</span><span class="sxs-lookup"><span data-stu-id="a2b41-153">/xmp/xmp:CreatorTool</span></span>                         |
|       | <span data-ttu-id="a2b41-154">/XMP/XMP: kreatortool</span><span class="sxs-lookup"><span data-stu-id="a2b41-154">/xmp/xmp:creatortool</span></span>                         |
|       | <span data-ttu-id="a2b41-155">/XMP/TIFF: Software</span><span class="sxs-lookup"><span data-stu-id="a2b41-155">/xmp/tiff:Software</span></span>                           |
|       | <span data-ttu-id="a2b41-156">/XMP/TIFF: Software</span><span class="sxs-lookup"><span data-stu-id="a2b41-156">/xmp/tiff:software</span></span>                           |
|       | <span data-ttu-id="a2b41-157">/app13/IRB/8bimiptc/IPTC/Originating-Programm</span><span class="sxs-lookup"><span data-stu-id="a2b41-157">/app13/irb/8bimiptc/iptc/Originating Program</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="a2b41-158">TIFF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a2b41-158">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a2b41-159">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="a2b41-159">Read Paths</span></span>



| <span data-ttu-id="a2b41-160">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a2b41-160">Order</span></span> | <span data-ttu-id="a2b41-161">Pfad</span><span class="sxs-lookup"><span data-stu-id="a2b41-161">Path</span></span>                                       | <span data-ttu-id="a2b41-162">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a2b41-162">Disk Format</span></span> |
|-------|--------------------------------------------|-------------|
|       | <span data-ttu-id="a2b41-163">/IFD/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="a2b41-163">/ifd/{ushort=305}</span></span>                          | <span data-ttu-id="a2b41-164">ascii</span><span class="sxs-lookup"><span data-stu-id="a2b41-164">ascii</span></span>       |
|       | <span data-ttu-id="a2b41-165">/IFD/IPTC/Originating-Programm</span><span class="sxs-lookup"><span data-stu-id="a2b41-165">/ifd/iptc/Originating Program</span></span>              |             |
|       | <span data-ttu-id="a2b41-166">/IFD/XMP/XMP: kreatortool</span><span class="sxs-lookup"><span data-stu-id="a2b41-166">/ifd/xmp/xmp:CreatorTool</span></span>                   | <span data-ttu-id="a2b41-167">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-167">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-168">/IFD/XMP/XMP: kreatortool</span><span class="sxs-lookup"><span data-stu-id="a2b41-168">/ifd/xmp/xmp:creatortool</span></span>                   | <span data-ttu-id="a2b41-169">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-169">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-170">/IFD/XMP/TIFF: Software</span><span class="sxs-lookup"><span data-stu-id="a2b41-170">/ifd/xmp/tiff:Software</span></span>                     | <span data-ttu-id="a2b41-171">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-171">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-172">/IFD/XMP/TIFF: Software</span><span class="sxs-lookup"><span data-stu-id="a2b41-172">/ifd/xmp/tiff:software</span></span>                     | <span data-ttu-id="a2b41-173">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-173">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-174">/IFD/IPTC/Originating-Programm</span><span class="sxs-lookup"><span data-stu-id="a2b41-174">/ifd/iptc/Originating Program</span></span>              |             |
|       | <span data-ttu-id="a2b41-175">/IFD/IRB/8bimiptc/IPTC/Originating-Programm</span><span class="sxs-lookup"><span data-stu-id="a2b41-175">/ifd/irb/8bimiptc/iptc/Originating Program</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="a2b41-176">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="a2b41-176">Write Paths</span></span>



| <span data-ttu-id="a2b41-177">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a2b41-177">Order</span></span> | <span data-ttu-id="a2b41-178">Pfad</span><span class="sxs-lookup"><span data-stu-id="a2b41-178">Path</span></span>                                       | <span data-ttu-id="a2b41-179">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="a2b41-179">Disk Format</span></span> |
|-------|--------------------------------------------|-------------|
|       | <span data-ttu-id="a2b41-180">/IFD/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="a2b41-180">/ifd/{ushort=305}</span></span>                          | <span data-ttu-id="a2b41-181">ascii</span><span class="sxs-lookup"><span data-stu-id="a2b41-181">ascii</span></span>       |
|       | <span data-ttu-id="a2b41-182">/IFD/XMP/XMP: kreatortool</span><span class="sxs-lookup"><span data-stu-id="a2b41-182">/ifd/xmp/xmp:CreatorTool</span></span>                   | <span data-ttu-id="a2b41-183">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-183">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-184">/IFD/XMP/XMP: kreatortool</span><span class="sxs-lookup"><span data-stu-id="a2b41-184">/ifd/xmp/xmp:creatortool</span></span>                   | <span data-ttu-id="a2b41-185">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-185">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-186">/IFD/XMP/TIFF: Software</span><span class="sxs-lookup"><span data-stu-id="a2b41-186">/ifd/xmp/tiff:Software</span></span>                     | <span data-ttu-id="a2b41-187">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-187">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-188">/IFD/XMP/TIFF: Software</span><span class="sxs-lookup"><span data-stu-id="a2b41-188">/ifd/xmp/tiff:software</span></span>                     | <span data-ttu-id="a2b41-189">Unicode</span><span class="sxs-lookup"><span data-stu-id="a2b41-189">unicode</span></span>     |
|       | <span data-ttu-id="a2b41-190">/IFD/IPTC/Originating-Programm</span><span class="sxs-lookup"><span data-stu-id="a2b41-190">/ifd/iptc/Originating Program</span></span>              |             |
|       | <span data-ttu-id="a2b41-191">/IFD/IRB/8bimiptc/IPTC/Originating-Programm</span><span class="sxs-lookup"><span data-stu-id="a2b41-191">/ifd/irb/8bimiptc/iptc/Originating Program</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a2b41-192">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="a2b41-192">Remove Paths</span></span>



| <span data-ttu-id="a2b41-193">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a2b41-193">Order</span></span> | <span data-ttu-id="a2b41-194">Pfad</span><span class="sxs-lookup"><span data-stu-id="a2b41-194">Path</span></span>                                       |
|-------|--------------------------------------------|
|       | <span data-ttu-id="a2b41-195">/IFD/{ushort = 305}</span><span class="sxs-lookup"><span data-stu-id="a2b41-195">/ifd/{ushort=305}</span></span>                          |
|       | <span data-ttu-id="a2b41-196">/IFD/XMP/XMP: kreatortool</span><span class="sxs-lookup"><span data-stu-id="a2b41-196">/ifd/xmp/xmp:CreatorTool</span></span>                   |
|       | <span data-ttu-id="a2b41-197">/IFD/XMP/XMP: kreatortool</span><span class="sxs-lookup"><span data-stu-id="a2b41-197">/ifd/xmp/xmp:creatortool</span></span>                   |
|       | <span data-ttu-id="a2b41-198">/IFD/XMP/TIFF: Software</span><span class="sxs-lookup"><span data-stu-id="a2b41-198">/ifd/xmp/tiff:Software</span></span>                     |
|       | <span data-ttu-id="a2b41-199">/IFD/XMP/TIFF: Software</span><span class="sxs-lookup"><span data-stu-id="a2b41-199">/ifd/xmp/tiff:software</span></span>                     |
|       | <span data-ttu-id="a2b41-200">/IFD/IPTC/Originating-Programm</span><span class="sxs-lookup"><span data-stu-id="a2b41-200">/ifd/iptc/Originating Program</span></span>              |
|       | <span data-ttu-id="a2b41-201">/IFD/IRB/8bimiptc/IPTC/Originating-Programm</span><span class="sxs-lookup"><span data-stu-id="a2b41-201">/ifd/irb/8bimiptc/iptc/Originating Program</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a2b41-202">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2b41-202">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2b41-203">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a2b41-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2b41-204">System. ApplicationName</span><span class="sxs-lookup"><span data-stu-id="a2b41-204">System.ApplicationName</span></span>](../properties/props-system-applicationname.md)
</dt> </dl>

 

 
