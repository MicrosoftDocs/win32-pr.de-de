---
description: Die fotometadatenrichtlinie für die System. Rating-Eigenschaft.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: System. Rating Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347178"
---
# <a name="systemrating-photo-metadata-policy"></a><span data-ttu-id="394e3-103">System. Rating Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="394e3-103">System.Rating Photo Metadata Policy</span></span>

<span data-ttu-id="394e3-104">Die fotometadatenrichtlinie für die [System. Rating](../properties/props-system-rating.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="394e3-104">The photo metadata policy for the [System.Rating](../properties/props-system-rating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="394e3-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="394e3-105">PKEY</span></span>

<span data-ttu-id="394e3-106">Pkey- \_ Bewertung</span><span class="sxs-lookup"><span data-stu-id="394e3-106">PKEY\_Rating</span></span>

### <a name="containers"></a><span data-ttu-id="394e3-107">Container</span><span class="sxs-lookup"><span data-stu-id="394e3-107">Containers</span></span>

<span data-ttu-id="394e3-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="394e3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="394e3-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="394e3-109">Read-Only</span></span>

<span data-ttu-id="394e3-110">Nein</span><span class="sxs-lookup"><span data-stu-id="394e3-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="394e3-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="394e3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="394e3-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="394e3-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="394e3-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="394e3-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="394e3-114">Kann "VT \_ UI1", "VT \_ UI2" oder "VT UI4" lauten \_ .</span><span class="sxs-lookup"><span data-stu-id="394e3-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="394e3-115">Der Wert kann zwischen 0 und 99 liegen.</span><span class="sxs-lookup"><span data-stu-id="394e3-115">The value may range from 0 to 99.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="394e3-116">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="394e3-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="394e3-117">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="394e3-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="394e3-118">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="394e3-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="394e3-119">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="394e3-119">Read Paths</span></span>



| <span data-ttu-id="394e3-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="394e3-120">Order</span></span> | <span data-ttu-id="394e3-121">Pfad</span><span class="sxs-lookup"><span data-stu-id="394e3-121">Path</span></span>                       | <span data-ttu-id="394e3-122">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="394e3-122">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="394e3-123">1</span><span class="sxs-lookup"><span data-stu-id="394e3-123">1</span></span>     | <span data-ttu-id="394e3-124">/App1/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="394e3-124">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="394e3-125">ushort</span><span class="sxs-lookup"><span data-stu-id="394e3-125">ushort</span></span>      |
| <span data-ttu-id="394e3-126">2</span><span class="sxs-lookup"><span data-stu-id="394e3-126">2</span></span>     | <span data-ttu-id="394e3-127">/XMP/MicrosoftPhoto: Bewertung</span><span class="sxs-lookup"><span data-stu-id="394e3-127">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="394e3-128">Unicode</span><span class="sxs-lookup"><span data-stu-id="394e3-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="394e3-129">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="394e3-129">Write Paths</span></span>



| <span data-ttu-id="394e3-130">Auftrag</span><span class="sxs-lookup"><span data-stu-id="394e3-130">Order</span></span> | <span data-ttu-id="394e3-131">Pfad</span><span class="sxs-lookup"><span data-stu-id="394e3-131">Path</span></span>                       | <span data-ttu-id="394e3-132">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="394e3-132">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="394e3-133">1</span><span class="sxs-lookup"><span data-stu-id="394e3-133">1</span></span>     | <span data-ttu-id="394e3-134">/App1/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="394e3-134">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="394e3-135">ushort</span><span class="sxs-lookup"><span data-stu-id="394e3-135">ushort</span></span>      |
| <span data-ttu-id="394e3-136">2</span><span class="sxs-lookup"><span data-stu-id="394e3-136">2</span></span>     | <span data-ttu-id="394e3-137">/XMP/MicrosoftPhoto: Bewertung</span><span class="sxs-lookup"><span data-stu-id="394e3-137">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="394e3-138">Unicode</span><span class="sxs-lookup"><span data-stu-id="394e3-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="394e3-139">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="394e3-139">Remove Paths</span></span>



| <span data-ttu-id="394e3-140">Auftrag</span><span class="sxs-lookup"><span data-stu-id="394e3-140">Order</span></span> | <span data-ttu-id="394e3-141">Pfad</span><span class="sxs-lookup"><span data-stu-id="394e3-141">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="394e3-142">1</span><span class="sxs-lookup"><span data-stu-id="394e3-142">1</span></span>     | <span data-ttu-id="394e3-143">/App1/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="394e3-143">/app1/ifd/{ushort=18249}</span></span>   |
| <span data-ttu-id="394e3-144">2</span><span class="sxs-lookup"><span data-stu-id="394e3-144">2</span></span>     | <span data-ttu-id="394e3-145">/XMP/microsoftphoto: Bewertung</span><span class="sxs-lookup"><span data-stu-id="394e3-145">/xmp/microsoftphoto:rating</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="394e3-146">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="394e3-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="394e3-147">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="394e3-147">Read Paths</span></span>



| <span data-ttu-id="394e3-148">Auftrag</span><span class="sxs-lookup"><span data-stu-id="394e3-148">Order</span></span> | <span data-ttu-id="394e3-149">Pfad</span><span class="sxs-lookup"><span data-stu-id="394e3-149">Path</span></span>                           | <span data-ttu-id="394e3-150">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="394e3-150">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="394e3-151">1</span><span class="sxs-lookup"><span data-stu-id="394e3-151">1</span></span>     | <span data-ttu-id="394e3-152">/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="394e3-152">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="394e3-153">ushort</span><span class="sxs-lookup"><span data-stu-id="394e3-153">ushort</span></span>      |
| <span data-ttu-id="394e3-154">2</span><span class="sxs-lookup"><span data-stu-id="394e3-154">2</span></span>     | <span data-ttu-id="394e3-155">/IFD/XMP/MicrosoftPhoto: Bewertung</span><span class="sxs-lookup"><span data-stu-id="394e3-155">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="394e3-156">Unicode</span><span class="sxs-lookup"><span data-stu-id="394e3-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="394e3-157">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="394e3-157">Write Paths</span></span>



| <span data-ttu-id="394e3-158">Auftrag</span><span class="sxs-lookup"><span data-stu-id="394e3-158">Order</span></span> | <span data-ttu-id="394e3-159">Pfad</span><span class="sxs-lookup"><span data-stu-id="394e3-159">Path</span></span>                           | <span data-ttu-id="394e3-160">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="394e3-160">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="394e3-161">1</span><span class="sxs-lookup"><span data-stu-id="394e3-161">1</span></span>     | <span data-ttu-id="394e3-162">/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="394e3-162">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="394e3-163">ushort</span><span class="sxs-lookup"><span data-stu-id="394e3-163">ushort</span></span>      |
| <span data-ttu-id="394e3-164">2</span><span class="sxs-lookup"><span data-stu-id="394e3-164">2</span></span>     | <span data-ttu-id="394e3-165">/IFD/XMP/MicrosoftPhoto: Bewertung</span><span class="sxs-lookup"><span data-stu-id="394e3-165">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="394e3-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="394e3-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="394e3-167">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="394e3-167">Remove Paths</span></span>



| <span data-ttu-id="394e3-168">Auftrag</span><span class="sxs-lookup"><span data-stu-id="394e3-168">Order</span></span> | <span data-ttu-id="394e3-169">Pfad</span><span class="sxs-lookup"><span data-stu-id="394e3-169">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="394e3-170">1</span><span class="sxs-lookup"><span data-stu-id="394e3-170">1</span></span>     | <span data-ttu-id="394e3-171">/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="394e3-171">/ifd/{ushort=18249}</span></span>            |
| <span data-ttu-id="394e3-172">2</span><span class="sxs-lookup"><span data-stu-id="394e3-172">2</span></span>     | <span data-ttu-id="394e3-173">/IFD/XMP/microsoftphoto: Bewertung</span><span class="sxs-lookup"><span data-stu-id="394e3-173">/ifd/xmp/microsoftphoto:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="394e3-174">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="394e3-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="394e3-175">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="394e3-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="394e3-176">System. Rating</span><span class="sxs-lookup"><span data-stu-id="394e3-176">System.Rating</span></span>](../properties/props-system-rating.md)
</dt> </dl>

 

 
