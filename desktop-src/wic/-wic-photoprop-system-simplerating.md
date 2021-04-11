---
description: Die fotometadatenrichtlinie für die System. simplerating-Eigenschaft.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: System. simplerating Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b91e41a0684c8e395992683e0a1d4fe43306a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050292"
---
# <a name="systemsimplerating-photo-metadata-policy"></a><span data-ttu-id="21293-103">System. simplerating Photo Metadata Policy</span><span class="sxs-lookup"><span data-stu-id="21293-103">System.SimpleRating Photo Metadata Policy</span></span>

<span data-ttu-id="21293-104">Die fotometadatenrichtlinie für die [System. simplerating](../properties/props-system-simplerating.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="21293-104">The photo metadata policy for the [System.SimpleRating](../properties/props-system-simplerating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="21293-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="21293-105">PKEY</span></span>

<span data-ttu-id="21293-106">Pkey- \_ simplerating</span><span class="sxs-lookup"><span data-stu-id="21293-106">PKEY\_SimpleRating</span></span>

### <a name="containers"></a><span data-ttu-id="21293-107">Container</span><span class="sxs-lookup"><span data-stu-id="21293-107">Containers</span></span>

<span data-ttu-id="21293-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="21293-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="21293-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21293-109">Read-Only</span></span>

<span data-ttu-id="21293-110">Nein</span><span class="sxs-lookup"><span data-stu-id="21293-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="21293-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="21293-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="21293-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="21293-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="21293-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="21293-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="21293-114">Kann "VT \_ UI1", "VT \_ UI2" oder "VT UI4" lauten \_ .</span><span class="sxs-lookup"><span data-stu-id="21293-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="21293-115">Der ganzzahlige Wert kann zwischen 0 und 5 liegen.</span><span class="sxs-lookup"><span data-stu-id="21293-115">The integer value may range from 0 to 5.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="21293-116">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="21293-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="21293-117">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="21293-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="21293-118">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="21293-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="21293-119">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="21293-119">Read Paths</span></span>



| <span data-ttu-id="21293-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="21293-120">Order</span></span> | <span data-ttu-id="21293-121">Pfad</span><span class="sxs-lookup"><span data-stu-id="21293-121">Path</span></span>                     | <span data-ttu-id="21293-122">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="21293-122">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="21293-123">1</span><span class="sxs-lookup"><span data-stu-id="21293-123">1</span></span>     | <span data-ttu-id="21293-124">/App1/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="21293-124">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="21293-125">ushort</span><span class="sxs-lookup"><span data-stu-id="21293-125">ushort</span></span>      |
| <span data-ttu-id="21293-126">2</span><span class="sxs-lookup"><span data-stu-id="21293-126">2</span></span>     | <span data-ttu-id="21293-127">/XMP/XMP: Bewertung</span><span class="sxs-lookup"><span data-stu-id="21293-127">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="21293-128">Unicode</span><span class="sxs-lookup"><span data-stu-id="21293-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="21293-129">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="21293-129">Write Paths</span></span>



| <span data-ttu-id="21293-130">Auftrag</span><span class="sxs-lookup"><span data-stu-id="21293-130">Order</span></span> | <span data-ttu-id="21293-131">Pfad</span><span class="sxs-lookup"><span data-stu-id="21293-131">Path</span></span>                     | <span data-ttu-id="21293-132">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="21293-132">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="21293-133">1</span><span class="sxs-lookup"><span data-stu-id="21293-133">1</span></span>     | <span data-ttu-id="21293-134">/App1/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="21293-134">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="21293-135">ushort</span><span class="sxs-lookup"><span data-stu-id="21293-135">ushort</span></span>      |
| <span data-ttu-id="21293-136">2</span><span class="sxs-lookup"><span data-stu-id="21293-136">2</span></span>     | <span data-ttu-id="21293-137">/XMP/XMP: Bewertung</span><span class="sxs-lookup"><span data-stu-id="21293-137">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="21293-138">Unicode</span><span class="sxs-lookup"><span data-stu-id="21293-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="21293-139">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="21293-139">Remove Paths</span></span>



| <span data-ttu-id="21293-140">Auftrag</span><span class="sxs-lookup"><span data-stu-id="21293-140">Order</span></span> | <span data-ttu-id="21293-141">Pfad</span><span class="sxs-lookup"><span data-stu-id="21293-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="21293-142">1</span><span class="sxs-lookup"><span data-stu-id="21293-142">1</span></span>     | <span data-ttu-id="21293-143">/App1/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="21293-143">/app1/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="21293-144">2</span><span class="sxs-lookup"><span data-stu-id="21293-144">2</span></span>     | <span data-ttu-id="21293-145">/XMP/XMP: Bewertung</span><span class="sxs-lookup"><span data-stu-id="21293-145">/xmp/xmp:rating</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="21293-146">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="21293-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="21293-147">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="21293-147">Read Paths</span></span>



| <span data-ttu-id="21293-148">Auftrag</span><span class="sxs-lookup"><span data-stu-id="21293-148">Order</span></span> | <span data-ttu-id="21293-149">Pfad</span><span class="sxs-lookup"><span data-stu-id="21293-149">Path</span></span>                | <span data-ttu-id="21293-150">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="21293-150">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="21293-151">1</span><span class="sxs-lookup"><span data-stu-id="21293-151">1</span></span>     | <span data-ttu-id="21293-152">/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="21293-152">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="21293-153">ushort</span><span class="sxs-lookup"><span data-stu-id="21293-153">ushort</span></span>      |
| <span data-ttu-id="21293-154">2</span><span class="sxs-lookup"><span data-stu-id="21293-154">2</span></span>     | <span data-ttu-id="21293-155">/IFD/XMP/XMP: Bewertung</span><span class="sxs-lookup"><span data-stu-id="21293-155">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="21293-156">Unicode</span><span class="sxs-lookup"><span data-stu-id="21293-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="21293-157">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="21293-157">Write Paths</span></span>



| <span data-ttu-id="21293-158">Auftrag</span><span class="sxs-lookup"><span data-stu-id="21293-158">Order</span></span> | <span data-ttu-id="21293-159">Pfad</span><span class="sxs-lookup"><span data-stu-id="21293-159">Path</span></span>                | <span data-ttu-id="21293-160">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="21293-160">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="21293-161">1</span><span class="sxs-lookup"><span data-stu-id="21293-161">1</span></span>     | <span data-ttu-id="21293-162">/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="21293-162">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="21293-163">ushort</span><span class="sxs-lookup"><span data-stu-id="21293-163">ushort</span></span>      |
| <span data-ttu-id="21293-164">2</span><span class="sxs-lookup"><span data-stu-id="21293-164">2</span></span>     | <span data-ttu-id="21293-165">/IFD/XMP/XMP: Bewertung</span><span class="sxs-lookup"><span data-stu-id="21293-165">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="21293-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="21293-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="21293-167">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="21293-167">Remove Paths</span></span>



| <span data-ttu-id="21293-168">Auftrag</span><span class="sxs-lookup"><span data-stu-id="21293-168">Order</span></span> | <span data-ttu-id="21293-169">Pfad</span><span class="sxs-lookup"><span data-stu-id="21293-169">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="21293-170">1</span><span class="sxs-lookup"><span data-stu-id="21293-170">1</span></span>     | <span data-ttu-id="21293-171">/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="21293-171">/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="21293-172">2</span><span class="sxs-lookup"><span data-stu-id="21293-172">2</span></span>     | <span data-ttu-id="21293-173">/IFD/XMP/XMP: Bewertung</span><span class="sxs-lookup"><span data-stu-id="21293-173">/ifd/xmp/xmp:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="21293-174">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21293-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="21293-175">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="21293-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21293-176">System. simplerating</span><span class="sxs-lookup"><span data-stu-id="21293-176">System.SimpleRating</span></span>](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
