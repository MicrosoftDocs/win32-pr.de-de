---
description: Die fotometadatenrichtlinie für die System. Keywords-Eigenschaft.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: System. Keywords Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5d25e7f1919527d474395397d6df62863f7b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217830"
---
# <a name="systemkeywords-photo-metadata-policy"></a><span data-ttu-id="4e384-103">System. Keywords Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="4e384-103">System.Keywords Photo Metadata Policy</span></span>

<span data-ttu-id="4e384-104">Die fotometadatenrichtlinie für die [System. Keywords](../properties/props-system-keywords.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4e384-104">The photo metadata policy for the [System.Keywords](../properties/props-system-keywords.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4e384-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="4e384-105">PKEY</span></span>

<span data-ttu-id="4e384-106">Pkey- \_ Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="4e384-106">PKEY\_Keywords</span></span>

### <a name="containers"></a><span data-ttu-id="4e384-107">Container</span><span class="sxs-lookup"><span data-stu-id="4e384-107">Containers</span></span>

<span data-ttu-id="4e384-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4e384-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4e384-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e384-109">Read-Only</span></span>

<span data-ttu-id="4e384-110">Nein</span><span class="sxs-lookup"><span data-stu-id="4e384-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4e384-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="4e384-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4e384-112">VT \_ Vector \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="4e384-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="4e384-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="4e384-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="4e384-114">Der VT- \_ Vektor \| VT \_ LPWSTR wird bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="4e384-114">VT\_VECTOR \| VT\_LPWSTR is preferred.</span></span> <span data-ttu-id="4e384-115">Ein VT \_ LPWSTR, das eine durch Semikolons getrennte Zeichenfolge enthält, wird ebenfalls akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="4e384-115">A VT\_LPWSTR containing a semicolon-delimited string is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4e384-116">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="4e384-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="4e384-117">Werte aus unterschiedlichen Schemas werden zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="4e384-117">Values from different schemas are merged.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4e384-118">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="4e384-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4e384-119">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="4e384-119">Read Paths</span></span>



| <span data-ttu-id="4e384-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4e384-120">Order</span></span> | <span data-ttu-id="4e384-121">Pfad</span><span class="sxs-lookup"><span data-stu-id="4e384-121">Path</span></span>                              | <span data-ttu-id="4e384-122">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="4e384-122">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="4e384-123">1</span><span class="sxs-lookup"><span data-stu-id="4e384-123">1</span></span>     | <span data-ttu-id="4e384-124">/XMP/ <xmpbag> DC: Subject</span><span class="sxs-lookup"><span data-stu-id="4e384-124">/xmp/<xmpbag>dc:subject</span></span>     | <span data-ttu-id="4e384-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="4e384-125">unicode</span></span>        |
| <span data-ttu-id="4e384-126">2</span><span class="sxs-lookup"><span data-stu-id="4e384-126">2</span></span>     | <span data-ttu-id="4e384-127">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="4e384-127">/app13/irb/8bimiptc/iptc/keywords</span></span> |                |
| <span data-ttu-id="4e384-128">3</span><span class="sxs-lookup"><span data-stu-id="4e384-128">3</span></span>     | <span data-ttu-id="4e384-129">/App1/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="4e384-129">/app1/ifd/{ushort=18247}</span></span>          | <span data-ttu-id="4e384-130">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="4e384-130">unicode\_bytes</span></span> |
| <span data-ttu-id="4e384-131">4</span><span class="sxs-lookup"><span data-stu-id="4e384-131">4</span></span>     | <span data-ttu-id="4e384-132">/App1/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="4e384-132">/app1/ifd/{ushort=40094}</span></span>          | <span data-ttu-id="4e384-133">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="4e384-133">unicode\_bytes</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="4e384-134">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="4e384-134">Write Paths</span></span>



| <span data-ttu-id="4e384-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4e384-135">Order</span></span> | <span data-ttu-id="4e384-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="4e384-136">Path</span></span>                                              | <span data-ttu-id="4e384-137">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="4e384-137">Disk Format</span></span>    |
|-------|---------------------------------------------------|----------------|
| <span data-ttu-id="4e384-138">1</span><span class="sxs-lookup"><span data-stu-id="4e384-138">1</span></span>     | <span data-ttu-id="4e384-139">/XMP/ <xmpbag> DC: Subject</span><span class="sxs-lookup"><span data-stu-id="4e384-139">/xmp/<xmpbag>dc:subject</span></span>                     | <span data-ttu-id="4e384-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="4e384-140">unicode</span></span>        |
| <span data-ttu-id="4e384-141">2</span><span class="sxs-lookup"><span data-stu-id="4e384-141">2</span></span>     | <span data-ttu-id="4e384-142">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="4e384-142">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |                |
| <span data-ttu-id="4e384-143">3</span><span class="sxs-lookup"><span data-stu-id="4e384-143">3</span></span>     | <span data-ttu-id="4e384-144">/App1/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="4e384-144">/app1/ifd/{ushort=18247}</span></span>                          | <span data-ttu-id="4e384-145">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="4e384-145">unicode\_bytes</span></span> |
| <span data-ttu-id="4e384-146">4</span><span class="sxs-lookup"><span data-stu-id="4e384-146">4</span></span>     | <span data-ttu-id="4e384-147">/App1/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="4e384-147">/app1/ifd/{ushort=40094}</span></span>                          | <span data-ttu-id="4e384-148">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="4e384-148">unicode\_bytes</span></span> |
| <span data-ttu-id="4e384-149">5</span><span class="sxs-lookup"><span data-stu-id="4e384-149">5</span></span>     | <span data-ttu-id="4e384-150">/XMP/ <xmpbag> microsoftphoto: lastkeywordxmp</span><span class="sxs-lookup"><span data-stu-id="4e384-150">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  | <span data-ttu-id="4e384-151">Unicode</span><span class="sxs-lookup"><span data-stu-id="4e384-151">unicode</span></span>        |
| <span data-ttu-id="4e384-152">6</span><span class="sxs-lookup"><span data-stu-id="4e384-152">6</span></span>     | <span data-ttu-id="4e384-153">/XMP/ <xmpbag> microsoftphoto: lastkeywordiptc</span><span class="sxs-lookup"><span data-stu-id="4e384-153">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> | <span data-ttu-id="4e384-154">Unicode</span><span class="sxs-lookup"><span data-stu-id="4e384-154">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="4e384-155">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="4e384-155">Remove Paths</span></span>



| <span data-ttu-id="4e384-156">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4e384-156">Order</span></span> | <span data-ttu-id="4e384-157">Pfad</span><span class="sxs-lookup"><span data-stu-id="4e384-157">Path</span></span>                                              |
|-------|---------------------------------------------------|
| <span data-ttu-id="4e384-158">1</span><span class="sxs-lookup"><span data-stu-id="4e384-158">1</span></span>     | <span data-ttu-id="4e384-159">/XMP/DC: Betreff</span><span class="sxs-lookup"><span data-stu-id="4e384-159">/xmp/dc:subject</span></span>                                   |
| <span data-ttu-id="4e384-160">2</span><span class="sxs-lookup"><span data-stu-id="4e384-160">2</span></span>     | <span data-ttu-id="4e384-161">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="4e384-161">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |
| <span data-ttu-id="4e384-162">3</span><span class="sxs-lookup"><span data-stu-id="4e384-162">3</span></span>     | <span data-ttu-id="4e384-163">/App1/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="4e384-163">/app1/ifd/{ushort=18247}</span></span>                          |
| <span data-ttu-id="4e384-164">4</span><span class="sxs-lookup"><span data-stu-id="4e384-164">4</span></span>     | <span data-ttu-id="4e384-165">/App1/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="4e384-165">/app1/ifd/{ushort=40094}</span></span>                          |
| <span data-ttu-id="4e384-166">5</span><span class="sxs-lookup"><span data-stu-id="4e384-166">5</span></span>     | <span data-ttu-id="4e384-167">/XMP/ <xmpbag> microsoftphoto: lastkeywordxmp</span><span class="sxs-lookup"><span data-stu-id="4e384-167">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  |
| <span data-ttu-id="4e384-168">6</span><span class="sxs-lookup"><span data-stu-id="4e384-168">6</span></span>     | <span data-ttu-id="4e384-169">/XMP/ <xmpbag> microsoftphoto: lastkeywordiptc</span><span class="sxs-lookup"><span data-stu-id="4e384-169">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="4e384-170">TIFF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="4e384-170">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4e384-171">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="4e384-171">Read Paths</span></span>



| <span data-ttu-id="4e384-172">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4e384-172">Order</span></span> | <span data-ttu-id="4e384-173">Pfad</span><span class="sxs-lookup"><span data-stu-id="4e384-173">Path</span></span>                              | <span data-ttu-id="4e384-174">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="4e384-174">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="4e384-175">1</span><span class="sxs-lookup"><span data-stu-id="4e384-175">1</span></span>     | <span data-ttu-id="4e384-176">/IFD/XMP/ <xmpbag> DC: Subject</span><span class="sxs-lookup"><span data-stu-id="4e384-176">/ifd/xmp/<xmpbag>dc:subject</span></span> | <span data-ttu-id="4e384-177">Unicode</span><span class="sxs-lookup"><span data-stu-id="4e384-177">unicode</span></span>        |
| <span data-ttu-id="4e384-178">2</span><span class="sxs-lookup"><span data-stu-id="4e384-178">2</span></span>     | <span data-ttu-id="4e384-179">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="4e384-179">/ifd/iptc/keywords</span></span>                |                |
| <span data-ttu-id="4e384-180">3</span><span class="sxs-lookup"><span data-stu-id="4e384-180">3</span></span>     | <span data-ttu-id="4e384-181">/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="4e384-181">/ifd/{ushort=18247}</span></span>               | <span data-ttu-id="4e384-182">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="4e384-182">unicode\_bytes</span></span> |
| <span data-ttu-id="4e384-183">4</span><span class="sxs-lookup"><span data-stu-id="4e384-183">4</span></span>     | <span data-ttu-id="4e384-184">/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="4e384-184">/ifd/{ushort=40094}</span></span>               | <span data-ttu-id="4e384-185">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="4e384-185">unicode\_bytes</span></span> |
| <span data-ttu-id="4e384-186">5</span><span class="sxs-lookup"><span data-stu-id="4e384-186">5</span></span>     | <span data-ttu-id="4e384-187">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="4e384-187">/ifd/irb/8bimiptc/iptc/keywords</span></span>   |                |



 

### <a name="write-paths"></a><span data-ttu-id="4e384-188">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="4e384-188">Write Paths</span></span>



| <span data-ttu-id="4e384-189">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4e384-189">Order</span></span> | <span data-ttu-id="4e384-190">Pfad</span><span class="sxs-lookup"><span data-stu-id="4e384-190">Path</span></span>                                                             | <span data-ttu-id="4e384-191">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="4e384-191">Disk Format</span></span>    |
|-------|------------------------------------------------------------------|----------------|
| <span data-ttu-id="4e384-192">1</span><span class="sxs-lookup"><span data-stu-id="4e384-192">1</span></span>     | <span data-ttu-id="4e384-193">/IFD/XMP/ <xmpbag> DC: Subject</span><span class="sxs-lookup"><span data-stu-id="4e384-193">/ifd/xmp/<xmpbag>dc:subject</span></span>                                | <span data-ttu-id="4e384-194">Unicode</span><span class="sxs-lookup"><span data-stu-id="4e384-194">unicode</span></span>        |
| <span data-ttu-id="4e384-195">2</span><span class="sxs-lookup"><span data-stu-id="4e384-195">2</span></span>     | <span data-ttu-id="4e384-196">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="4e384-196">/ifd/iptc/keywords</span></span>                                               |                |
| <span data-ttu-id="4e384-197">3</span><span class="sxs-lookup"><span data-stu-id="4e384-197">3</span></span>     | <span data-ttu-id="4e384-198">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="4e384-198">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |                |
| <span data-ttu-id="4e384-199">4</span><span class="sxs-lookup"><span data-stu-id="4e384-199">4</span></span>     | <span data-ttu-id="4e384-200">/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="4e384-200">/ifd/{ushort=18247}</span></span>                                              | <span data-ttu-id="4e384-201">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="4e384-201">unicode\_bytes</span></span> |
| <span data-ttu-id="4e384-202">5</span><span class="sxs-lookup"><span data-stu-id="4e384-202">5</span></span>     | <span data-ttu-id="4e384-203">/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="4e384-203">/ifd/{ushort=40094}</span></span>                                              | <span data-ttu-id="4e384-204">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="4e384-204">unicode\_bytes</span></span> |
| <span data-ttu-id="4e384-205">6</span><span class="sxs-lookup"><span data-stu-id="4e384-205">6</span></span>     | <span data-ttu-id="4e384-206">/IFD/XMP/ <xmpbag> microsoftphoto: lastkeywordxmp</span><span class="sxs-lookup"><span data-stu-id="4e384-206">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             | <span data-ttu-id="4e384-207">Unicode</span><span class="sxs-lookup"><span data-stu-id="4e384-207">unicode</span></span>        |
| <span data-ttu-id="4e384-208">7</span><span class="sxs-lookup"><span data-stu-id="4e384-208">7</span></span>     | <span data-ttu-id="4e384-209">/IFD/XMP/ <xmpbag> microsoftphoto: lastkeywordiptc</span><span class="sxs-lookup"><span data-stu-id="4e384-209">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            | <span data-ttu-id="4e384-210">Unicode</span><span class="sxs-lookup"><span data-stu-id="4e384-210">unicode</span></span>        |
| <span data-ttu-id="4e384-211">8</span><span class="sxs-lookup"><span data-stu-id="4e384-211">8</span></span>     | <span data-ttu-id="4e384-212">/IFD/XMP/ <xmpbag> microsoftphoto: lastkeywordiptc \_ TIFF- \_ UNB</span><span class="sxs-lookup"><span data-stu-id="4e384-212">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> | <span data-ttu-id="4e384-213">Unicode</span><span class="sxs-lookup"><span data-stu-id="4e384-213">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="4e384-214">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="4e384-214">Remove Paths</span></span>



| <span data-ttu-id="4e384-215">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4e384-215">Order</span></span> | <span data-ttu-id="4e384-216">Pfad</span><span class="sxs-lookup"><span data-stu-id="4e384-216">Path</span></span>                                                             |
|-------|------------------------------------------------------------------|
| <span data-ttu-id="4e384-217">1</span><span class="sxs-lookup"><span data-stu-id="4e384-217">1</span></span>     | <span data-ttu-id="4e384-218">/IFD/XMP/DC: Betreff</span><span class="sxs-lookup"><span data-stu-id="4e384-218">/ifd/xmp/dc:subject</span></span>                                              |
| <span data-ttu-id="4e384-219">2</span><span class="sxs-lookup"><span data-stu-id="4e384-219">2</span></span>     | <span data-ttu-id="4e384-220">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="4e384-220">/ifd/iptc/keywords</span></span>                                               |
| <span data-ttu-id="4e384-221">3</span><span class="sxs-lookup"><span data-stu-id="4e384-221">3</span></span>     | <span data-ttu-id="4e384-222">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="4e384-222">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |
| <span data-ttu-id="4e384-223">4</span><span class="sxs-lookup"><span data-stu-id="4e384-223">4</span></span>     | <span data-ttu-id="4e384-224">/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="4e384-224">/ifd/{ushort=18247}</span></span>                                              |
| <span data-ttu-id="4e384-225">5</span><span class="sxs-lookup"><span data-stu-id="4e384-225">5</span></span>     | <span data-ttu-id="4e384-226">/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="4e384-226">/ifd/{ushort=40094}</span></span>                                              |
| <span data-ttu-id="4e384-227">6</span><span class="sxs-lookup"><span data-stu-id="4e384-227">6</span></span>     | <span data-ttu-id="4e384-228">/IFD/XMP/ <xmpbag> microsoftphoto: lastkeywordxmp</span><span class="sxs-lookup"><span data-stu-id="4e384-228">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             |
| <span data-ttu-id="4e384-229">7</span><span class="sxs-lookup"><span data-stu-id="4e384-229">7</span></span>     | <span data-ttu-id="4e384-230">/IFD/XMP/ <xmpbag> microsoftphoto: lastkeywordiptc</span><span class="sxs-lookup"><span data-stu-id="4e384-230">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            |
| <span data-ttu-id="4e384-231">8</span><span class="sxs-lookup"><span data-stu-id="4e384-231">8</span></span>     | <span data-ttu-id="4e384-232">/IFD/XMP/ <xmpbag> microsoftphoto: lastkeywordiptc \_ TIFF- \_ UNB</span><span class="sxs-lookup"><span data-stu-id="4e384-232">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="4e384-233">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e384-233">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e384-234">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e384-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e384-235">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="4e384-235">System.Keywords</span></span>](../properties/props-system-keywords.md)
</dt> </dl>

 

 
