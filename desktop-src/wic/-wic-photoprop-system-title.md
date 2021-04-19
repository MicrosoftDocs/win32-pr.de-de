---
description: Die fotometadatenrichtlinie für die System. Title-Eigenschaft.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: System. Title-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02513f3f566576999e83b09c156d36ac480c17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356948"
---
# <a name="systemtitle-photo-metadata-policy"></a><span data-ttu-id="23a7a-103">System. Title-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="23a7a-103">System.Title Photo Metadata Policy</span></span>

<span data-ttu-id="23a7a-104">Die fotometadatenrichtlinie für die [System. Title](../properties/props-system-title.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="23a7a-104">The photo metadata policy for the [System.Title](../properties/props-system-title.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="23a7a-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="23a7a-105">PKEY</span></span>

<span data-ttu-id="23a7a-106">Pkey- \_ Titel</span><span class="sxs-lookup"><span data-stu-id="23a7a-106">PKEY\_Title</span></span>

### <a name="containers"></a><span data-ttu-id="23a7a-107">Container</span><span class="sxs-lookup"><span data-stu-id="23a7a-107">Containers</span></span>

<span data-ttu-id="23a7a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="23a7a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="23a7a-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23a7a-109">Read-Only</span></span>

<span data-ttu-id="23a7a-110">Nein</span><span class="sxs-lookup"><span data-stu-id="23a7a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="23a7a-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="23a7a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="23a7a-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="23a7a-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="23a7a-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="23a7a-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="23a7a-114">Entweder VT \_ LPWSTR oder VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="23a7a-114">Either VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="23a7a-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="23a7a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="23a7a-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="23a7a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="23a7a-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="23a7a-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="23a7a-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="23a7a-118">Read Paths</span></span>



| <span data-ttu-id="23a7a-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="23a7a-119">Order</span></span> | <span data-ttu-id="23a7a-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="23a7a-120">Path</span></span>                                | <span data-ttu-id="23a7a-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="23a7a-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="23a7a-122">1</span><span class="sxs-lookup"><span data-stu-id="23a7a-122">1</span></span>     | <span data-ttu-id="23a7a-123">/App1/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="23a7a-123">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="23a7a-124">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="23a7a-124">unicode\_bytes</span></span> |
| <span data-ttu-id="23a7a-125">2</span><span class="sxs-lookup"><span data-stu-id="23a7a-125">2</span></span>     | <span data-ttu-id="23a7a-126">/XMP/ <xmpalt> DC: Title</span><span class="sxs-lookup"><span data-stu-id="23a7a-126">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="23a7a-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-127">unicode</span></span>        |
| <span data-ttu-id="23a7a-128">3</span><span class="sxs-lookup"><span data-stu-id="23a7a-128">3</span></span>     | <span data-ttu-id="23a7a-129">/XMP/DC: Title</span><span class="sxs-lookup"><span data-stu-id="23a7a-129">/xmp/dc:title</span></span>                       | <span data-ttu-id="23a7a-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-130">unicode</span></span>        |
| <span data-ttu-id="23a7a-131">4</span><span class="sxs-lookup"><span data-stu-id="23a7a-131">4</span></span>     | <span data-ttu-id="23a7a-132">/App1/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="23a7a-132">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="23a7a-133">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-133">unicode</span></span>        |
| <span data-ttu-id="23a7a-134">5</span><span class="sxs-lookup"><span data-stu-id="23a7a-134">5</span></span>     | <span data-ttu-id="23a7a-135">/App1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="23a7a-135">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="23a7a-136">ascii</span><span class="sxs-lookup"><span data-stu-id="23a7a-136">ascii</span></span>          |
| <span data-ttu-id="23a7a-137">6</span><span class="sxs-lookup"><span data-stu-id="23a7a-137">6</span></span>     | <span data-ttu-id="23a7a-138">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="23a7a-138">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="23a7a-139">7</span><span class="sxs-lookup"><span data-stu-id="23a7a-139">7</span></span>     | <span data-ttu-id="23a7a-140">/XMP/ <xmpalt> DC: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23a7a-140">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="23a7a-141">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-141">unicode</span></span>        |
| <span data-ttu-id="23a7a-142">8</span><span class="sxs-lookup"><span data-stu-id="23a7a-142">8</span></span>     | <span data-ttu-id="23a7a-143">/XMP/DC: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23a7a-143">/xmp/dc:description</span></span>                 | <span data-ttu-id="23a7a-144">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-144">unicode</span></span>        |
| <span data-ttu-id="23a7a-145">9</span><span class="sxs-lookup"><span data-stu-id="23a7a-145">9</span></span>     | <span data-ttu-id="23a7a-146">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="23a7a-146">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="23a7a-147">10</span><span class="sxs-lookup"><span data-stu-id="23a7a-147">10</span></span>    | <span data-ttu-id="23a7a-148">/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="23a7a-148">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="23a7a-149">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-149">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="23a7a-150">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="23a7a-150">Write Paths</span></span>



| <span data-ttu-id="23a7a-151">Auftrag</span><span class="sxs-lookup"><span data-stu-id="23a7a-151">Order</span></span> | <span data-ttu-id="23a7a-152">Pfad</span><span class="sxs-lookup"><span data-stu-id="23a7a-152">Path</span></span>                                | <span data-ttu-id="23a7a-153">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="23a7a-153">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="23a7a-154">1</span><span class="sxs-lookup"><span data-stu-id="23a7a-154">1</span></span>     | <span data-ttu-id="23a7a-155">/App1/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="23a7a-155">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="23a7a-156">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="23a7a-156">unicode\_bytes</span></span> |
| <span data-ttu-id="23a7a-157">2</span><span class="sxs-lookup"><span data-stu-id="23a7a-157">2</span></span>     | <span data-ttu-id="23a7a-158">/XMP/DC: Title</span><span class="sxs-lookup"><span data-stu-id="23a7a-158">/xmp/dc:title</span></span>                       | <span data-ttu-id="23a7a-159">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-159">unicode</span></span>        |
| <span data-ttu-id="23a7a-160">3</span><span class="sxs-lookup"><span data-stu-id="23a7a-160">3</span></span>     | <span data-ttu-id="23a7a-161">/XMP/ <xmpalt> DC: Title</span><span class="sxs-lookup"><span data-stu-id="23a7a-161">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="23a7a-162">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-162">unicode</span></span>        |
| <span data-ttu-id="23a7a-163">4</span><span class="sxs-lookup"><span data-stu-id="23a7a-163">4</span></span>     | <span data-ttu-id="23a7a-164">/App1/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="23a7a-164">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="23a7a-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-165">unicode</span></span>        |
| <span data-ttu-id="23a7a-166">5</span><span class="sxs-lookup"><span data-stu-id="23a7a-166">5</span></span>     | <span data-ttu-id="23a7a-167">/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="23a7a-167">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="23a7a-168">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-168">unicode</span></span>        |
| <span data-ttu-id="23a7a-169">6</span><span class="sxs-lookup"><span data-stu-id="23a7a-169">6</span></span>     | <span data-ttu-id="23a7a-170">/App1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="23a7a-170">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="23a7a-171">ascii</span><span class="sxs-lookup"><span data-stu-id="23a7a-171">ascii</span></span>          |
| <span data-ttu-id="23a7a-172">7</span><span class="sxs-lookup"><span data-stu-id="23a7a-172">7</span></span>     | <span data-ttu-id="23a7a-173">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="23a7a-173">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="23a7a-174">8</span><span class="sxs-lookup"><span data-stu-id="23a7a-174">8</span></span>     | <span data-ttu-id="23a7a-175">/XMP/DC: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23a7a-175">/xmp/dc:description</span></span>                 | <span data-ttu-id="23a7a-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-176">unicode</span></span>        |
| <span data-ttu-id="23a7a-177">9</span><span class="sxs-lookup"><span data-stu-id="23a7a-177">9</span></span>     | <span data-ttu-id="23a7a-178">/XMP/ <xmpalt> DC: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23a7a-178">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="23a7a-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-179">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="23a7a-180">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="23a7a-180">Remove Paths</span></span>



| <span data-ttu-id="23a7a-181">Auftrag</span><span class="sxs-lookup"><span data-stu-id="23a7a-181">Order</span></span> | <span data-ttu-id="23a7a-182">Pfad</span><span class="sxs-lookup"><span data-stu-id="23a7a-182">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="23a7a-183">1</span><span class="sxs-lookup"><span data-stu-id="23a7a-183">1</span></span>     | <span data-ttu-id="23a7a-184">/App1/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="23a7a-184">/app1/ifd/{ushort=40091}</span></span>            |
| <span data-ttu-id="23a7a-185">2</span><span class="sxs-lookup"><span data-stu-id="23a7a-185">2</span></span>     | <span data-ttu-id="23a7a-186">/XMP/DC: Title</span><span class="sxs-lookup"><span data-stu-id="23a7a-186">/xmp/dc:title</span></span>                       |
| <span data-ttu-id="23a7a-187">3</span><span class="sxs-lookup"><span data-stu-id="23a7a-187">3</span></span>     | <span data-ttu-id="23a7a-188">/App1/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="23a7a-188">/app1/ifd/exif/{ushort=37510}</span></span>       |
| <span data-ttu-id="23a7a-189">4</span><span class="sxs-lookup"><span data-stu-id="23a7a-189">4</span></span>     | <span data-ttu-id="23a7a-190">/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="23a7a-190">/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="23a7a-191">5</span><span class="sxs-lookup"><span data-stu-id="23a7a-191">5</span></span>     | <span data-ttu-id="23a7a-192">/App1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="23a7a-192">/app1/ifd/{ushort=270}</span></span>              |
| <span data-ttu-id="23a7a-193">6</span><span class="sxs-lookup"><span data-stu-id="23a7a-193">6</span></span>     | <span data-ttu-id="23a7a-194">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="23a7a-194">/app13/irb/8bimiptc/iptc/caption</span></span>    |
| <span data-ttu-id="23a7a-195">7</span><span class="sxs-lookup"><span data-stu-id="23a7a-195">7</span></span>     | <span data-ttu-id="23a7a-196">/XMP/DC: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23a7a-196">/xmp/dc:description</span></span>                 |



 

### <a name="tiff-policy"></a><span data-ttu-id="23a7a-197">TIFF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="23a7a-197">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="23a7a-198">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="23a7a-198">Read Paths</span></span>



| <span data-ttu-id="23a7a-199">Auftrag</span><span class="sxs-lookup"><span data-stu-id="23a7a-199">Order</span></span> | <span data-ttu-id="23a7a-200">Pfad</span><span class="sxs-lookup"><span data-stu-id="23a7a-200">Path</span></span>                                    | <span data-ttu-id="23a7a-201">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="23a7a-201">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="23a7a-202">1</span><span class="sxs-lookup"><span data-stu-id="23a7a-202">1</span></span>     | <span data-ttu-id="23a7a-203">/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="23a7a-203">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="23a7a-204">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="23a7a-204">unicode\_bytes</span></span> |
| <span data-ttu-id="23a7a-205">2</span><span class="sxs-lookup"><span data-stu-id="23a7a-205">2</span></span>     | <span data-ttu-id="23a7a-206">/IFD/XMP/ <xmpalt> DC: Title</span><span class="sxs-lookup"><span data-stu-id="23a7a-206">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="23a7a-207">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-207">unicode</span></span>        |
| <span data-ttu-id="23a7a-208">3</span><span class="sxs-lookup"><span data-stu-id="23a7a-208">3</span></span>     | <span data-ttu-id="23a7a-209">/IFD/XMP/DC: Title</span><span class="sxs-lookup"><span data-stu-id="23a7a-209">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="23a7a-210">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-210">unicode</span></span>        |
| <span data-ttu-id="23a7a-211">4</span><span class="sxs-lookup"><span data-stu-id="23a7a-211">4</span></span>     | <span data-ttu-id="23a7a-212">/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="23a7a-212">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="23a7a-213">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-213">unicode</span></span>        |
| <span data-ttu-id="23a7a-214">5</span><span class="sxs-lookup"><span data-stu-id="23a7a-214">5</span></span>     | <span data-ttu-id="23a7a-215">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="23a7a-215">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="23a7a-216">ascii</span><span class="sxs-lookup"><span data-stu-id="23a7a-216">ascii</span></span>          |
| <span data-ttu-id="23a7a-217">6</span><span class="sxs-lookup"><span data-stu-id="23a7a-217">6</span></span>     | <span data-ttu-id="23a7a-218">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="23a7a-218">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="23a7a-219">7</span><span class="sxs-lookup"><span data-stu-id="23a7a-219">7</span></span>     | <span data-ttu-id="23a7a-220">/IFD/XMP/ <xmpalt> DC: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23a7a-220">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="23a7a-221">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-221">unicode</span></span>        |
| <span data-ttu-id="23a7a-222">8</span><span class="sxs-lookup"><span data-stu-id="23a7a-222">8</span></span>     | <span data-ttu-id="23a7a-223">/IFD/XMP/DC: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23a7a-223">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="23a7a-224">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-224">unicode</span></span>        |
| <span data-ttu-id="23a7a-225">9</span><span class="sxs-lookup"><span data-stu-id="23a7a-225">9</span></span>     | <span data-ttu-id="23a7a-226">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="23a7a-226">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="23a7a-227">10</span><span class="sxs-lookup"><span data-stu-id="23a7a-227">10</span></span>    | <span data-ttu-id="23a7a-228">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="23a7a-228">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="23a7a-229">11</span><span class="sxs-lookup"><span data-stu-id="23a7a-229">11</span></span>    | <span data-ttu-id="23a7a-230">/IFD/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="23a7a-230">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="23a7a-231">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-231">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="23a7a-232">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="23a7a-232">Write Paths</span></span>



| <span data-ttu-id="23a7a-233">Auftrag</span><span class="sxs-lookup"><span data-stu-id="23a7a-233">Order</span></span> | <span data-ttu-id="23a7a-234">Pfad</span><span class="sxs-lookup"><span data-stu-id="23a7a-234">Path</span></span>                                    | <span data-ttu-id="23a7a-235">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="23a7a-235">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="23a7a-236">1</span><span class="sxs-lookup"><span data-stu-id="23a7a-236">1</span></span>     | <span data-ttu-id="23a7a-237">/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="23a7a-237">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="23a7a-238">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="23a7a-238">unicode\_bytes</span></span> |
| <span data-ttu-id="23a7a-239">2</span><span class="sxs-lookup"><span data-stu-id="23a7a-239">2</span></span>     | <span data-ttu-id="23a7a-240">/IFD/XMP/DC: Title</span><span class="sxs-lookup"><span data-stu-id="23a7a-240">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="23a7a-241">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-241">unicode</span></span>        |
| <span data-ttu-id="23a7a-242">3</span><span class="sxs-lookup"><span data-stu-id="23a7a-242">3</span></span>     | <span data-ttu-id="23a7a-243">/IFD/XMP/ <xmpalt> DC: Title</span><span class="sxs-lookup"><span data-stu-id="23a7a-243">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="23a7a-244">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-244">unicode</span></span>        |
| <span data-ttu-id="23a7a-245">4</span><span class="sxs-lookup"><span data-stu-id="23a7a-245">4</span></span>     | <span data-ttu-id="23a7a-246">/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="23a7a-246">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="23a7a-247">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-247">unicode</span></span>        |
| <span data-ttu-id="23a7a-248">5</span><span class="sxs-lookup"><span data-stu-id="23a7a-248">5</span></span>     | <span data-ttu-id="23a7a-249">/IFD/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="23a7a-249">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="23a7a-250">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-250">unicode</span></span>        |
| <span data-ttu-id="23a7a-251">6</span><span class="sxs-lookup"><span data-stu-id="23a7a-251">6</span></span>     | <span data-ttu-id="23a7a-252">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="23a7a-252">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="23a7a-253">ascii</span><span class="sxs-lookup"><span data-stu-id="23a7a-253">ascii</span></span>          |
| <span data-ttu-id="23a7a-254">7</span><span class="sxs-lookup"><span data-stu-id="23a7a-254">7</span></span>     | <span data-ttu-id="23a7a-255">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="23a7a-255">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="23a7a-256">8</span><span class="sxs-lookup"><span data-stu-id="23a7a-256">8</span></span>     | <span data-ttu-id="23a7a-257">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="23a7a-257">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="23a7a-258">9</span><span class="sxs-lookup"><span data-stu-id="23a7a-258">9</span></span>     | <span data-ttu-id="23a7a-259">/IFD/XMP/DC: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23a7a-259">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="23a7a-260">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-260">unicode</span></span>        |
| <span data-ttu-id="23a7a-261">10</span><span class="sxs-lookup"><span data-stu-id="23a7a-261">10</span></span>    | <span data-ttu-id="23a7a-262">/IFD/XMP/ <xmpalt> DC: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23a7a-262">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="23a7a-263">Unicode</span><span class="sxs-lookup"><span data-stu-id="23a7a-263">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="23a7a-264">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="23a7a-264">Remove Paths</span></span>



| <span data-ttu-id="23a7a-265">Auftrag</span><span class="sxs-lookup"><span data-stu-id="23a7a-265">Order</span></span> | <span data-ttu-id="23a7a-266">Pfad</span><span class="sxs-lookup"><span data-stu-id="23a7a-266">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="23a7a-267">1</span><span class="sxs-lookup"><span data-stu-id="23a7a-267">1</span></span>     | <span data-ttu-id="23a7a-268">/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="23a7a-268">/ifd/{ushort=40091}</span></span>                     |
| <span data-ttu-id="23a7a-269">2</span><span class="sxs-lookup"><span data-stu-id="23a7a-269">2</span></span>     | <span data-ttu-id="23a7a-270">/IFD/XMP/DC: Title</span><span class="sxs-lookup"><span data-stu-id="23a7a-270">/ifd/xmp/dc:title</span></span>                       |
| <span data-ttu-id="23a7a-271">3</span><span class="sxs-lookup"><span data-stu-id="23a7a-271">3</span></span>     | <span data-ttu-id="23a7a-272">/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="23a7a-272">/ifd/exif/{ushort=37510}</span></span>                |
| <span data-ttu-id="23a7a-273">4</span><span class="sxs-lookup"><span data-stu-id="23a7a-273">4</span></span>     | <span data-ttu-id="23a7a-274">/IFD/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="23a7a-274">/ifd/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="23a7a-275">5</span><span class="sxs-lookup"><span data-stu-id="23a7a-275">5</span></span>     | <span data-ttu-id="23a7a-276">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="23a7a-276">/ifd/{ushort=270}</span></span>                       |
| <span data-ttu-id="23a7a-277">6</span><span class="sxs-lookup"><span data-stu-id="23a7a-277">6</span></span>     | <span data-ttu-id="23a7a-278">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="23a7a-278">/ifd/iptc/caption</span></span>                       |
| <span data-ttu-id="23a7a-279">7</span><span class="sxs-lookup"><span data-stu-id="23a7a-279">7</span></span>     | <span data-ttu-id="23a7a-280">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="23a7a-280">/ifd/irb/8bimiptc/iptc/caption</span></span>          |
| <span data-ttu-id="23a7a-281">8</span><span class="sxs-lookup"><span data-stu-id="23a7a-281">8</span></span>     | <span data-ttu-id="23a7a-282">/IFD/XMP/DC: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23a7a-282">/ifd/xmp/dc:description</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="23a7a-283">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23a7a-283">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="23a7a-284">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23a7a-284">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23a7a-285">System.Title</span><span class="sxs-lookup"><span data-stu-id="23a7a-285">System.Title</span></span>](../properties/props-system-title.md)
</dt> </dl>

 

 
