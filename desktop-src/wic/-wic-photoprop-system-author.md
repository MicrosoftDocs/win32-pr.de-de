---
description: Die fotometadatenrichtlinie für die System. Author-Eigenschaft.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: System. Author-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90345257ef1623f7cda1ce4318af7a9f472df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369026"
---
# <a name="systemauthor-photo-metadata-policy"></a><span data-ttu-id="8403e-103">System. Author-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="8403e-103">System.Author Photo Metadata Policy</span></span>

<span data-ttu-id="8403e-104">Die fotometadatenrichtlinie für die [System. Author](../properties/props-system-author.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8403e-104">The photo metadata policy for the [System.Author](../properties/props-system-author.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8403e-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="8403e-105">PKEY</span></span>

<span data-ttu-id="8403e-106">Pkey- \_ Autor</span><span class="sxs-lookup"><span data-stu-id="8403e-106">PKEY\_Author</span></span>

### <a name="containers"></a><span data-ttu-id="8403e-107">Container</span><span class="sxs-lookup"><span data-stu-id="8403e-107">Containers</span></span>

<span data-ttu-id="8403e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="8403e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8403e-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8403e-109">Read-Only</span></span>

<span data-ttu-id="8403e-110">Nein</span><span class="sxs-lookup"><span data-stu-id="8403e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8403e-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="8403e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8403e-112">VT \_ Vector \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="8403e-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="8403e-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="8403e-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="8403e-114">Der VT- \_ Vektor \| VT \_ LPWSTR wird bevorzugt, aber VT \_ LPWSTR wird ebenfalls akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="8403e-114">VT\_VECTOR \| VT\_LPWSTR is preferred, but VT\_LPWSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8403e-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="8403e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="8403e-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="8403e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="8403e-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="8403e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="8403e-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="8403e-118">Read Paths</span></span>



| <span data-ttu-id="8403e-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="8403e-119">Order</span></span> | <span data-ttu-id="8403e-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="8403e-120">Path</span></span>                             | <span data-ttu-id="8403e-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="8403e-121">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="8403e-122">1</span><span class="sxs-lookup"><span data-stu-id="8403e-122">1</span></span>     | <span data-ttu-id="8403e-123">/App1/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="8403e-123">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="8403e-124">ascii</span><span class="sxs-lookup"><span data-stu-id="8403e-124">ascii</span></span>          |
| <span data-ttu-id="8403e-125">2</span><span class="sxs-lookup"><span data-stu-id="8403e-125">2</span></span>     | <span data-ttu-id="8403e-126">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="8403e-126">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="8403e-127">3</span><span class="sxs-lookup"><span data-stu-id="8403e-127">3</span></span>     | <span data-ttu-id="8403e-128">/XMP/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="8403e-128">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="8403e-129">Unicode</span><span class="sxs-lookup"><span data-stu-id="8403e-129">unicode</span></span>        |
| <span data-ttu-id="8403e-130">4</span><span class="sxs-lookup"><span data-stu-id="8403e-130">4</span></span>     | <span data-ttu-id="8403e-131">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="8403e-131">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="8403e-132">5</span><span class="sxs-lookup"><span data-stu-id="8403e-132">5</span></span>     | <span data-ttu-id="8403e-133">/App1/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="8403e-133">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="8403e-134">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="8403e-134">unicode\_bytes</span></span> |
| <span data-ttu-id="8403e-135">6</span><span class="sxs-lookup"><span data-stu-id="8403e-135">6</span></span>     | <span data-ttu-id="8403e-136">/XMP/TIFF: Künstlerin</span><span class="sxs-lookup"><span data-stu-id="8403e-136">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="8403e-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="8403e-137">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="8403e-138">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="8403e-138">Write Paths</span></span>



| <span data-ttu-id="8403e-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="8403e-139">Order</span></span> | <span data-ttu-id="8403e-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="8403e-140">Path</span></span>                             | <span data-ttu-id="8403e-141">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="8403e-141">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="8403e-142">1</span><span class="sxs-lookup"><span data-stu-id="8403e-142">1</span></span>     | <span data-ttu-id="8403e-143">/XMP/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="8403e-143">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="8403e-144">Unicode</span><span class="sxs-lookup"><span data-stu-id="8403e-144">unicode</span></span>        |
| <span data-ttu-id="8403e-145">2</span><span class="sxs-lookup"><span data-stu-id="8403e-145">2</span></span>     | <span data-ttu-id="8403e-146">/XMP/TIFF: Künstlerin</span><span class="sxs-lookup"><span data-stu-id="8403e-146">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="8403e-147">Unicode</span><span class="sxs-lookup"><span data-stu-id="8403e-147">unicode</span></span>        |
| <span data-ttu-id="8403e-148">3</span><span class="sxs-lookup"><span data-stu-id="8403e-148">3</span></span>     | <span data-ttu-id="8403e-149">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="8403e-149">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="8403e-150">4</span><span class="sxs-lookup"><span data-stu-id="8403e-150">4</span></span>     | <span data-ttu-id="8403e-151">/App1/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="8403e-151">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="8403e-152">ascii</span><span class="sxs-lookup"><span data-stu-id="8403e-152">ascii</span></span>          |
| <span data-ttu-id="8403e-153">5</span><span class="sxs-lookup"><span data-stu-id="8403e-153">5</span></span>     | <span data-ttu-id="8403e-154">/App1/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="8403e-154">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="8403e-155">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="8403e-155">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="8403e-156">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="8403e-156">Remove Paths</span></span>



| <span data-ttu-id="8403e-157">Auftrag</span><span class="sxs-lookup"><span data-stu-id="8403e-157">Order</span></span> | <span data-ttu-id="8403e-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="8403e-158">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="8403e-159">1</span><span class="sxs-lookup"><span data-stu-id="8403e-159">1</span></span>     | <span data-ttu-id="8403e-160">/XMP/DC: Ersteller</span><span class="sxs-lookup"><span data-stu-id="8403e-160">/xmp/dc:creator</span></span>                  |
| <span data-ttu-id="8403e-161">2</span><span class="sxs-lookup"><span data-stu-id="8403e-161">2</span></span>     | <span data-ttu-id="8403e-162">/XMP/TIFF: Künstlerin</span><span class="sxs-lookup"><span data-stu-id="8403e-162">/xmp/tiff:artist</span></span>                 |
| <span data-ttu-id="8403e-163">3</span><span class="sxs-lookup"><span data-stu-id="8403e-163">3</span></span>     | <span data-ttu-id="8403e-164">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="8403e-164">/app13/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="8403e-165">4</span><span class="sxs-lookup"><span data-stu-id="8403e-165">4</span></span>     | <span data-ttu-id="8403e-166">/App1/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="8403e-166">/app1/ifd/{ushort=315}</span></span>           |
| <span data-ttu-id="8403e-167">5</span><span class="sxs-lookup"><span data-stu-id="8403e-167">5</span></span>     | <span data-ttu-id="8403e-168">/App1/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="8403e-168">/app1/ifd/{ushort=40093}</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="8403e-169">TIFF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="8403e-169">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="8403e-170">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="8403e-170">Read Paths</span></span>



| <span data-ttu-id="8403e-171">Auftrag</span><span class="sxs-lookup"><span data-stu-id="8403e-171">Order</span></span> | <span data-ttu-id="8403e-172">Pfad</span><span class="sxs-lookup"><span data-stu-id="8403e-172">Path</span></span>                              | <span data-ttu-id="8403e-173">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="8403e-173">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="8403e-174">1</span><span class="sxs-lookup"><span data-stu-id="8403e-174">1</span></span>     | <span data-ttu-id="8403e-175">/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="8403e-175">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="8403e-176">ascii</span><span class="sxs-lookup"><span data-stu-id="8403e-176">ascii</span></span>          |
| <span data-ttu-id="8403e-177">2</span><span class="sxs-lookup"><span data-stu-id="8403e-177">2</span></span>     | <span data-ttu-id="8403e-178">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="8403e-178">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="8403e-179">3</span><span class="sxs-lookup"><span data-stu-id="8403e-179">3</span></span>     | <span data-ttu-id="8403e-180">/IFD/XMP/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="8403e-180">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="8403e-181">Unicode</span><span class="sxs-lookup"><span data-stu-id="8403e-181">unicode</span></span>        |
| <span data-ttu-id="8403e-182">4</span><span class="sxs-lookup"><span data-stu-id="8403e-182">4</span></span>     | <span data-ttu-id="8403e-183">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="8403e-183">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="8403e-184">5</span><span class="sxs-lookup"><span data-stu-id="8403e-184">5</span></span>     | <span data-ttu-id="8403e-185">/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="8403e-185">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="8403e-186">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="8403e-186">unicode\_bytes</span></span> |
| <span data-ttu-id="8403e-187">6</span><span class="sxs-lookup"><span data-stu-id="8403e-187">6</span></span>     | <span data-ttu-id="8403e-188">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="8403e-188">/ifd/irb/8bimiptc/iptc/by-line</span></span>    |                |
| <span data-ttu-id="8403e-189">7</span><span class="sxs-lookup"><span data-stu-id="8403e-189">7</span></span>     | <span data-ttu-id="8403e-190">/IFD/XMP/TIFF: Künstlerin</span><span class="sxs-lookup"><span data-stu-id="8403e-190">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="8403e-191">Unicode</span><span class="sxs-lookup"><span data-stu-id="8403e-191">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="8403e-192">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="8403e-192">Write Paths</span></span>



| <span data-ttu-id="8403e-193">Auftrag</span><span class="sxs-lookup"><span data-stu-id="8403e-193">Order</span></span> | <span data-ttu-id="8403e-194">Pfad</span><span class="sxs-lookup"><span data-stu-id="8403e-194">Path</span></span>                              | <span data-ttu-id="8403e-195">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="8403e-195">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="8403e-196">1</span><span class="sxs-lookup"><span data-stu-id="8403e-196">1</span></span>     | <span data-ttu-id="8403e-197">/IFD/XMP/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="8403e-197">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="8403e-198">Unicode</span><span class="sxs-lookup"><span data-stu-id="8403e-198">unicode</span></span>        |
| <span data-ttu-id="8403e-199">2</span><span class="sxs-lookup"><span data-stu-id="8403e-199">2</span></span>     | <span data-ttu-id="8403e-200">/IFD/XMP/TIFF: Künstlerin</span><span class="sxs-lookup"><span data-stu-id="8403e-200">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="8403e-201">Unicode</span><span class="sxs-lookup"><span data-stu-id="8403e-201">unicode</span></span>        |
| <span data-ttu-id="8403e-202">3</span><span class="sxs-lookup"><span data-stu-id="8403e-202">3</span></span>     | <span data-ttu-id="8403e-203">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="8403e-203">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="8403e-204">4</span><span class="sxs-lookup"><span data-stu-id="8403e-204">4</span></span>     | <span data-ttu-id="8403e-205">/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="8403e-205">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="8403e-206">ASCII- \_ Vektor</span><span class="sxs-lookup"><span data-stu-id="8403e-206">ascii\_vector</span></span>  |
| <span data-ttu-id="8403e-207">5</span><span class="sxs-lookup"><span data-stu-id="8403e-207">5</span></span>     | <span data-ttu-id="8403e-208">/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="8403e-208">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="8403e-209">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="8403e-209">unicode\_bytes</span></span> |
| <span data-ttu-id="8403e-210">6</span><span class="sxs-lookup"><span data-stu-id="8403e-210">6</span></span>     | <span data-ttu-id="8403e-211">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="8403e-211">/ifd/iptc/by-line</span></span>                 |                |



 

### <a name="remove-paths"></a><span data-ttu-id="8403e-212">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="8403e-212">Remove Paths</span></span>



| <span data-ttu-id="8403e-213">Auftrag</span><span class="sxs-lookup"><span data-stu-id="8403e-213">Order</span></span> | <span data-ttu-id="8403e-214">Pfad</span><span class="sxs-lookup"><span data-stu-id="8403e-214">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="8403e-215">1</span><span class="sxs-lookup"><span data-stu-id="8403e-215">1</span></span>     | <span data-ttu-id="8403e-216">/IFD/XMP/DC: Ersteller</span><span class="sxs-lookup"><span data-stu-id="8403e-216">/ifd/xmp/dc:creator</span></span>            |
| <span data-ttu-id="8403e-217">2</span><span class="sxs-lookup"><span data-stu-id="8403e-217">2</span></span>     | <span data-ttu-id="8403e-218">/IFD/XMP/TIFF: Künstlerin</span><span class="sxs-lookup"><span data-stu-id="8403e-218">/ifd/xmp/tiff:artist</span></span>           |
| <span data-ttu-id="8403e-219">3</span><span class="sxs-lookup"><span data-stu-id="8403e-219">3</span></span>     | <span data-ttu-id="8403e-220">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="8403e-220">/ifd/iptc/by-line</span></span>              |
| <span data-ttu-id="8403e-221">4</span><span class="sxs-lookup"><span data-stu-id="8403e-221">4</span></span>     | <span data-ttu-id="8403e-222">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="8403e-222">/ifd/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="8403e-223">5</span><span class="sxs-lookup"><span data-stu-id="8403e-223">5</span></span>     | <span data-ttu-id="8403e-224">/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="8403e-224">/ifd/{ushort=315}</span></span>              |
| <span data-ttu-id="8403e-225">6</span><span class="sxs-lookup"><span data-stu-id="8403e-225">6</span></span>     | <span data-ttu-id="8403e-226">/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="8403e-226">/ifd/{ushort=40093}</span></span>            |



 

### <a name="remarks"></a><span data-ttu-id="8403e-227">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8403e-227">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8403e-228">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8403e-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8403e-229">System.Author</span><span class="sxs-lookup"><span data-stu-id="8403e-229">System.Author</span></span>](../properties/props-system-author.md)
</dt> </dl>

 

 
