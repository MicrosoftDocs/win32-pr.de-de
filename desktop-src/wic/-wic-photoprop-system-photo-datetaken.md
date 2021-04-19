---
description: Die fotometadatenrichtlinie für die System. Photo. DateTaken-Eigenschaft.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: System. Photo. DateTaken-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc1d3fb50a9a94e4bb13b35a0a5726572d78429f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366225"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a><span data-ttu-id="60688-103">System. Photo. DateTaken-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="60688-103">System.Photo.DateTaken Photo Metadata Policy</span></span>

<span data-ttu-id="60688-104">Die fotometadatenrichtlinie für die [System. Photo. DateTaken](../properties/props-system-photo-datetaken.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="60688-104">The photo metadata policy for the [System.Photo.DateTaken](../properties/props-system-photo-datetaken.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="60688-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="60688-105">PKEY</span></span>

<span data-ttu-id="60688-106">Pkey- \_ Foto, \_ DateTaken</span><span class="sxs-lookup"><span data-stu-id="60688-106">PKEY\_Photo\_DateTaken</span></span>

### <a name="containers"></a><span data-ttu-id="60688-107">Container</span><span class="sxs-lookup"><span data-stu-id="60688-107">Containers</span></span>

<span data-ttu-id="60688-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="60688-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="60688-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60688-109">Read-Only</span></span>

<span data-ttu-id="60688-110">Nein</span><span class="sxs-lookup"><span data-stu-id="60688-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="60688-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="60688-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="60688-112">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="60688-112">VT\_FILETIME</span></span>

### <a name="input-type"></a><span data-ttu-id="60688-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="60688-113">Input Type</span></span>

<span data-ttu-id="60688-114">Datetime</span><span class="sxs-lookup"><span data-stu-id="60688-114">DateTime</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="60688-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="60688-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="60688-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="60688-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="60688-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="60688-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="60688-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="60688-118">Read Paths</span></span>



| <span data-ttu-id="60688-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="60688-119">Order</span></span> | <span data-ttu-id="60688-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="60688-120">Path</span></span>                                  | <span data-ttu-id="60688-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="60688-121">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="60688-122">1</span><span class="sxs-lookup"><span data-stu-id="60688-122">1</span></span>     | <span data-ttu-id="60688-123">/App1/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="60688-123">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="60688-124">ascii</span><span class="sxs-lookup"><span data-stu-id="60688-124">ascii</span></span>       |
| <span data-ttu-id="60688-125">2</span><span class="sxs-lookup"><span data-stu-id="60688-125">2</span></span>     | <span data-ttu-id="60688-126">/app13/IRB/8bimiptc/IPTC/Date erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-126">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="60688-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-127">unicode</span></span>     |
| <span data-ttu-id="60688-128">3</span><span class="sxs-lookup"><span data-stu-id="60688-128">3</span></span>     | <span data-ttu-id="60688-129">/XMP/XMP: kreatedate</span><span class="sxs-lookup"><span data-stu-id="60688-129">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="60688-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-130">unicode</span></span>     |
| <span data-ttu-id="60688-131">4</span><span class="sxs-lookup"><span data-stu-id="60688-131">4</span></span>     | <span data-ttu-id="60688-132">/App1/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="60688-132">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="60688-133">ascii</span><span class="sxs-lookup"><span data-stu-id="60688-133">ascii</span></span>       |
| <span data-ttu-id="60688-134">5</span><span class="sxs-lookup"><span data-stu-id="60688-134">5</span></span>     | <span data-ttu-id="60688-135">/app13/IRB/8bimiptc/IPTC/Date erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-135">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="60688-136">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-136">unicode</span></span>     |
| <span data-ttu-id="60688-137">6</span><span class="sxs-lookup"><span data-stu-id="60688-137">6</span></span>     | <span data-ttu-id="60688-138">/XMP/EXIF: DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="60688-138">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="60688-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-139">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="60688-140">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="60688-140">Write Paths</span></span>



| <span data-ttu-id="60688-141">Auftrag</span><span class="sxs-lookup"><span data-stu-id="60688-141">Order</span></span> | <span data-ttu-id="60688-142">Pfad</span><span class="sxs-lookup"><span data-stu-id="60688-142">Path</span></span>                                  | <span data-ttu-id="60688-143">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="60688-143">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="60688-144">1</span><span class="sxs-lookup"><span data-stu-id="60688-144">1</span></span>     | <span data-ttu-id="60688-145">/App1/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="60688-145">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="60688-146">ascii</span><span class="sxs-lookup"><span data-stu-id="60688-146">ascii</span></span>       |
| <span data-ttu-id="60688-147">2</span><span class="sxs-lookup"><span data-stu-id="60688-147">2</span></span>     | <span data-ttu-id="60688-148">/app13/IRB/8bimiptc/IPTC/Date erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-148">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="60688-149">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-149">unicode</span></span>     |
| <span data-ttu-id="60688-150">3</span><span class="sxs-lookup"><span data-stu-id="60688-150">3</span></span>     | <span data-ttu-id="60688-151">/XMP/XMP: kreatedate</span><span class="sxs-lookup"><span data-stu-id="60688-151">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="60688-152">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-152">unicode</span></span>     |
| <span data-ttu-id="60688-153">4</span><span class="sxs-lookup"><span data-stu-id="60688-153">4</span></span>     | <span data-ttu-id="60688-154">/App1/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="60688-154">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="60688-155">ascii</span><span class="sxs-lookup"><span data-stu-id="60688-155">ascii</span></span>       |
| <span data-ttu-id="60688-156">5</span><span class="sxs-lookup"><span data-stu-id="60688-156">5</span></span>     | <span data-ttu-id="60688-157">/XMP/EXIF: DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="60688-157">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="60688-158">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-158">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="60688-159">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="60688-159">Remove Paths</span></span>



| <span data-ttu-id="60688-160">Auftrag</span><span class="sxs-lookup"><span data-stu-id="60688-160">Order</span></span> | <span data-ttu-id="60688-161">Pfad</span><span class="sxs-lookup"><span data-stu-id="60688-161">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="60688-162">1</span><span class="sxs-lookup"><span data-stu-id="60688-162">1</span></span>     | <span data-ttu-id="60688-163">/App1/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="60688-163">/app1/ifd/exif/{ushort=36867}</span></span>         |
| <span data-ttu-id="60688-164">2</span><span class="sxs-lookup"><span data-stu-id="60688-164">2</span></span>     | <span data-ttu-id="60688-165">/App1/IFD/EXIF/{ushort = 37521}</span><span class="sxs-lookup"><span data-stu-id="60688-165">/app1/ifd/exif/{ushort=37521}</span></span>         |
| <span data-ttu-id="60688-166">3</span><span class="sxs-lookup"><span data-stu-id="60688-166">3</span></span>     | <span data-ttu-id="60688-167">/App1/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="60688-167">/app1/ifd/exif/{ushort=36868}</span></span>         |
| <span data-ttu-id="60688-168">4</span><span class="sxs-lookup"><span data-stu-id="60688-168">4</span></span>     | <span data-ttu-id="60688-169">/App1/IFD/EXIF/{ushort = 37522}</span><span class="sxs-lookup"><span data-stu-id="60688-169">/app1/ifd/exif/{ushort=37522}</span></span>         |
| <span data-ttu-id="60688-170">5</span><span class="sxs-lookup"><span data-stu-id="60688-170">5</span></span>     | <span data-ttu-id="60688-171">/XMP/EXIF: DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="60688-171">/xmp/exif:DateTimeOriginal</span></span>            |
| <span data-ttu-id="60688-172">6</span><span class="sxs-lookup"><span data-stu-id="60688-172">6</span></span>     | <span data-ttu-id="60688-173">/XMP/XMP: kreatedate</span><span class="sxs-lookup"><span data-stu-id="60688-173">/xmp/xmp:CreateDate</span></span>                   |
| <span data-ttu-id="60688-174">7</span><span class="sxs-lookup"><span data-stu-id="60688-174">7</span></span>     | <span data-ttu-id="60688-175">/app13/IRB/8bimiptc/IPTC/Date erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-175">/app13/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="60688-176">8</span><span class="sxs-lookup"><span data-stu-id="60688-176">8</span></span>     | <span data-ttu-id="60688-177">/app13/IRB/8bimiptc/IPTC/Time erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-177">/app13/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="60688-178">TIFF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="60688-178">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="60688-179">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="60688-179">Read Paths</span></span>



| <span data-ttu-id="60688-180">Auftrag</span><span class="sxs-lookup"><span data-stu-id="60688-180">Order</span></span> | <span data-ttu-id="60688-181">Pfad</span><span class="sxs-lookup"><span data-stu-id="60688-181">Path</span></span>                                | <span data-ttu-id="60688-182">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="60688-182">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="60688-183">1</span><span class="sxs-lookup"><span data-stu-id="60688-183">1</span></span>     | <span data-ttu-id="60688-184">/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="60688-184">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="60688-185">ascii</span><span class="sxs-lookup"><span data-stu-id="60688-185">ascii</span></span>       |
| <span data-ttu-id="60688-186">2</span><span class="sxs-lookup"><span data-stu-id="60688-186">2</span></span>     | <span data-ttu-id="60688-187">/IFD/IPTC/Date erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-187">/ifd/iptc/date created</span></span>              | <span data-ttu-id="60688-188">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-188">unicode</span></span>     |
| <span data-ttu-id="60688-189">3</span><span class="sxs-lookup"><span data-stu-id="60688-189">3</span></span>     | <span data-ttu-id="60688-190">/IFD/XMP/XMP: kreatedate</span><span class="sxs-lookup"><span data-stu-id="60688-190">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="60688-191">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-191">unicode</span></span>     |
| <span data-ttu-id="60688-192">4</span><span class="sxs-lookup"><span data-stu-id="60688-192">4</span></span>     | <span data-ttu-id="60688-193">/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="60688-193">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="60688-194">ascii</span><span class="sxs-lookup"><span data-stu-id="60688-194">ascii</span></span>       |
| <span data-ttu-id="60688-195">5</span><span class="sxs-lookup"><span data-stu-id="60688-195">5</span></span>     | <span data-ttu-id="60688-196">/IFD/IPTC/Date erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-196">/ifd/iptc/date created</span></span>              | <span data-ttu-id="60688-197">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-197">unicode</span></span>     |
| <span data-ttu-id="60688-198">6</span><span class="sxs-lookup"><span data-stu-id="60688-198">6</span></span>     | <span data-ttu-id="60688-199">/IFD/IRB/8bimiptc/IPTC/Date erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-199">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="60688-200">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-200">unicode</span></span>     |
| <span data-ttu-id="60688-201">7</span><span class="sxs-lookup"><span data-stu-id="60688-201">7</span></span>     | <span data-ttu-id="60688-202">/IFD/XMP/EXIF: DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="60688-202">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="60688-203">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-203">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="60688-204">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="60688-204">Write Paths</span></span>



| <span data-ttu-id="60688-205">Auftrag</span><span class="sxs-lookup"><span data-stu-id="60688-205">Order</span></span> | <span data-ttu-id="60688-206">Pfad</span><span class="sxs-lookup"><span data-stu-id="60688-206">Path</span></span>                                | <span data-ttu-id="60688-207">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="60688-207">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="60688-208">1</span><span class="sxs-lookup"><span data-stu-id="60688-208">1</span></span>     | <span data-ttu-id="60688-209">/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="60688-209">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="60688-210">ascii</span><span class="sxs-lookup"><span data-stu-id="60688-210">ascii</span></span>       |
| <span data-ttu-id="60688-211">2</span><span class="sxs-lookup"><span data-stu-id="60688-211">2</span></span>     | <span data-ttu-id="60688-212">/IFD/IPTC/Date erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-212">/ifd/iptc/date created</span></span>              | <span data-ttu-id="60688-213">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-213">unicode</span></span>     |
| <span data-ttu-id="60688-214">3</span><span class="sxs-lookup"><span data-stu-id="60688-214">3</span></span>     | <span data-ttu-id="60688-215">/IFD/XMP/XMP: kreatedate</span><span class="sxs-lookup"><span data-stu-id="60688-215">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="60688-216">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-216">unicode</span></span>     |
| <span data-ttu-id="60688-217">4</span><span class="sxs-lookup"><span data-stu-id="60688-217">4</span></span>     | <span data-ttu-id="60688-218">/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="60688-218">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="60688-219">ascii</span><span class="sxs-lookup"><span data-stu-id="60688-219">ascii</span></span>       |
| <span data-ttu-id="60688-220">5</span><span class="sxs-lookup"><span data-stu-id="60688-220">5</span></span>     | <span data-ttu-id="60688-221">/IFD/IRB/8bimiptc/IPTC/Date erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-221">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="60688-222">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-222">unicode</span></span>     |
| <span data-ttu-id="60688-223">6</span><span class="sxs-lookup"><span data-stu-id="60688-223">6</span></span>     | <span data-ttu-id="60688-224">/IFD/XMP/EXIF: DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="60688-224">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="60688-225">Unicode</span><span class="sxs-lookup"><span data-stu-id="60688-225">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="60688-226">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="60688-226">Remove Paths</span></span>



| <span data-ttu-id="60688-227">Auftrag</span><span class="sxs-lookup"><span data-stu-id="60688-227">Order</span></span> | <span data-ttu-id="60688-228">Pfad</span><span class="sxs-lookup"><span data-stu-id="60688-228">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="60688-229">1</span><span class="sxs-lookup"><span data-stu-id="60688-229">1</span></span>     | <span data-ttu-id="60688-230">/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="60688-230">/ifd/exif/{ushort=36867}</span></span>            |
| <span data-ttu-id="60688-231">2</span><span class="sxs-lookup"><span data-stu-id="60688-231">2</span></span>     | <span data-ttu-id="60688-232">/IFD/EXIF/{ushort = 37521}</span><span class="sxs-lookup"><span data-stu-id="60688-232">/ifd/exif/{ushort=37521}</span></span>            |
| <span data-ttu-id="60688-233">3</span><span class="sxs-lookup"><span data-stu-id="60688-233">3</span></span>     | <span data-ttu-id="60688-234">/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="60688-234">/ifd/exif/{ushort=36868}</span></span>            |
| <span data-ttu-id="60688-235">4</span><span class="sxs-lookup"><span data-stu-id="60688-235">4</span></span>     | <span data-ttu-id="60688-236">/IFD/EXIF/{ushort = 37522}</span><span class="sxs-lookup"><span data-stu-id="60688-236">/ifd/exif/{ushort=37522}</span></span>            |
| <span data-ttu-id="60688-237">5</span><span class="sxs-lookup"><span data-stu-id="60688-237">5</span></span>     | <span data-ttu-id="60688-238">/IFD/XMP/EXIF: DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="60688-238">/ifd/xmp/exif:DateTimeOriginal</span></span>      |
| <span data-ttu-id="60688-239">6</span><span class="sxs-lookup"><span data-stu-id="60688-239">6</span></span>     | <span data-ttu-id="60688-240">/IFD/XMP/XMP: kreatedate</span><span class="sxs-lookup"><span data-stu-id="60688-240">/ifd/xmp/xmp:CreateDate</span></span>             |
| <span data-ttu-id="60688-241">7</span><span class="sxs-lookup"><span data-stu-id="60688-241">7</span></span>     | <span data-ttu-id="60688-242">/IFD/IPTC/Date erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-242">/ifd/iptc/date created</span></span>              |
| <span data-ttu-id="60688-243">8</span><span class="sxs-lookup"><span data-stu-id="60688-243">8</span></span>     | <span data-ttu-id="60688-244">/IFD/IPTC/Time erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-244">/ifd/iptc/time created</span></span>              |
| <span data-ttu-id="60688-245">9</span><span class="sxs-lookup"><span data-stu-id="60688-245">9</span></span>     | <span data-ttu-id="60688-246">/IFD/IRB/8bimiptc/IPTC/Date erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-246">/ifd/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="60688-247">10</span><span class="sxs-lookup"><span data-stu-id="60688-247">10</span></span>    | <span data-ttu-id="60688-248">/IFD/IRB/8bimiptc/IPTC/Time erstellt</span><span class="sxs-lookup"><span data-stu-id="60688-248">/ifd/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="png-policy"></a><span data-ttu-id="60688-249">PNG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="60688-249">PNG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="60688-250">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="60688-250">Read Paths</span></span>



| <span data-ttu-id="60688-251">Auftrag</span><span class="sxs-lookup"><span data-stu-id="60688-251">Order</span></span> | <span data-ttu-id="60688-252">Pfad</span><span class="sxs-lookup"><span data-stu-id="60688-252">Path</span></span>                      | <span data-ttu-id="60688-253">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="60688-253">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="60688-254">1</span><span class="sxs-lookup"><span data-stu-id="60688-254">1</span></span>     | <span data-ttu-id="60688-255">/\[\*\]Text/Erstellungszeit</span><span class="sxs-lookup"><span data-stu-id="60688-255">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="60688-256">ascii</span><span class="sxs-lookup"><span data-stu-id="60688-256">ascii</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="60688-257">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="60688-257">Write Paths</span></span>



| <span data-ttu-id="60688-258">Auftrag</span><span class="sxs-lookup"><span data-stu-id="60688-258">Order</span></span> | <span data-ttu-id="60688-259">Pfad</span><span class="sxs-lookup"><span data-stu-id="60688-259">Path</span></span>                      | <span data-ttu-id="60688-260">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="60688-260">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="60688-261">2</span><span class="sxs-lookup"><span data-stu-id="60688-261">2</span></span>     | <span data-ttu-id="60688-262">/\[\*\]Text/Erstellungszeit</span><span class="sxs-lookup"><span data-stu-id="60688-262">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="60688-263">ascii</span><span class="sxs-lookup"><span data-stu-id="60688-263">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="60688-264">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="60688-264">Remove Paths</span></span>



| <span data-ttu-id="60688-265">Auftrag</span><span class="sxs-lookup"><span data-stu-id="60688-265">Order</span></span> | <span data-ttu-id="60688-266">Pfad</span><span class="sxs-lookup"><span data-stu-id="60688-266">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="60688-267">3</span><span class="sxs-lookup"><span data-stu-id="60688-267">3</span></span>     | <span data-ttu-id="60688-268">/\[\*\]Text/Erstellungszeit</span><span class="sxs-lookup"><span data-stu-id="60688-268">/\[\*\]tEXt/Creation Time</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="60688-269">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60688-269">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="60688-270">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60688-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60688-271">System. Photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="60688-271">System.Photo.DateTaken</span></span>](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
