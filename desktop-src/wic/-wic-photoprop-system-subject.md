---
description: Die fotometadatenrichtlinie für die System. Subject-Eigenschaft.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: System. Subject Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceabbab95a52a1155db949dbc60b4525dd5f9d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364118"
---
# <a name="systemsubject-photo-metadata-policy"></a><span data-ttu-id="e1db2-103">System. Subject Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e1db2-103">System.Subject Photo Metadata Policy</span></span>

<span data-ttu-id="e1db2-104">Die fotometadatenrichtlinie für die [System. Subject](../properties/props-system-subject.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e1db2-104">The photo metadata policy for the [System.Subject](../properties/props-system-subject.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e1db2-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="e1db2-105">PKEY</span></span>

<span data-ttu-id="e1db2-106">Pkey- \_ Betreff</span><span class="sxs-lookup"><span data-stu-id="e1db2-106">PKEY\_Subject</span></span>

### <a name="containers"></a><span data-ttu-id="e1db2-107">Container</span><span class="sxs-lookup"><span data-stu-id="e1db2-107">Containers</span></span>

<span data-ttu-id="e1db2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e1db2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e1db2-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1db2-109">Read-Only</span></span>

<span data-ttu-id="e1db2-110">Nein</span><span class="sxs-lookup"><span data-stu-id="e1db2-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e1db2-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="e1db2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e1db2-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e1db2-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="e1db2-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="e1db2-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="e1db2-114">Entweder VT \_ LPWSTR oder VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e1db2-114">Either VT\_LPWSTR or VT\_LPWSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e1db2-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="e1db2-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e1db2-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="e1db2-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e1db2-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e1db2-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e1db2-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="e1db2-118">Read Paths</span></span>



| <span data-ttu-id="e1db2-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e1db2-119">Order</span></span> | <span data-ttu-id="e1db2-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="e1db2-120">Path</span></span>                     | <span data-ttu-id="e1db2-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="e1db2-121">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="e1db2-122">1</span><span class="sxs-lookup"><span data-stu-id="e1db2-122">1</span></span>     | <span data-ttu-id="e1db2-123">/App1/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="e1db2-123">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="e1db2-124">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="e1db2-124">unicode\_bytes</span></span> |
| <span data-ttu-id="e1db2-125">2</span><span class="sxs-lookup"><span data-stu-id="e1db2-125">2</span></span>     | <span data-ttu-id="e1db2-126">/App1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="e1db2-126">/app1/ifd/{ushort=270}</span></span>   | <span data-ttu-id="e1db2-127">ascii</span><span class="sxs-lookup"><span data-stu-id="e1db2-127">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="e1db2-128">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="e1db2-128">Write Paths</span></span>



| <span data-ttu-id="e1db2-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e1db2-129">Order</span></span> | <span data-ttu-id="e1db2-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="e1db2-130">Path</span></span>                     | <span data-ttu-id="e1db2-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="e1db2-131">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="e1db2-132">1</span><span class="sxs-lookup"><span data-stu-id="e1db2-132">1</span></span>     | <span data-ttu-id="e1db2-133">/App1/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="e1db2-133">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="e1db2-134">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="e1db2-134">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="e1db2-135">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="e1db2-135">Remove Paths</span></span>



| <span data-ttu-id="e1db2-136">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e1db2-136">Order</span></span> | <span data-ttu-id="e1db2-137">Pfad</span><span class="sxs-lookup"><span data-stu-id="e1db2-137">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="e1db2-138">1</span><span class="sxs-lookup"><span data-stu-id="e1db2-138">1</span></span>     | <span data-ttu-id="e1db2-139">/App1/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="e1db2-139">/app1/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="e1db2-140">2</span><span class="sxs-lookup"><span data-stu-id="e1db2-140">2</span></span>     | <span data-ttu-id="e1db2-141">/App1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="e1db2-141">/app1/ifd/{ushort=270}</span></span>   |



 

### <a name="tiff-policy"></a><span data-ttu-id="e1db2-142">TIFF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e1db2-142">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e1db2-143">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="e1db2-143">Read Paths</span></span>



| <span data-ttu-id="e1db2-144">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e1db2-144">Order</span></span> | <span data-ttu-id="e1db2-145">Pfad</span><span class="sxs-lookup"><span data-stu-id="e1db2-145">Path</span></span>                | <span data-ttu-id="e1db2-146">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="e1db2-146">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="e1db2-147">1</span><span class="sxs-lookup"><span data-stu-id="e1db2-147">1</span></span>     | <span data-ttu-id="e1db2-148">/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="e1db2-148">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="e1db2-149">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="e1db2-149">unicode\_bytes</span></span> |
| <span data-ttu-id="e1db2-150">2</span><span class="sxs-lookup"><span data-stu-id="e1db2-150">2</span></span>     | <span data-ttu-id="e1db2-151">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="e1db2-151">/ifd/{ushort=270}</span></span>   | <span data-ttu-id="e1db2-152">ascii</span><span class="sxs-lookup"><span data-stu-id="e1db2-152">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="e1db2-153">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="e1db2-153">Write Paths</span></span>



| <span data-ttu-id="e1db2-154">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e1db2-154">Order</span></span> | <span data-ttu-id="e1db2-155">Pfad</span><span class="sxs-lookup"><span data-stu-id="e1db2-155">Path</span></span>                | <span data-ttu-id="e1db2-156">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="e1db2-156">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="e1db2-157">1</span><span class="sxs-lookup"><span data-stu-id="e1db2-157">1</span></span>     | <span data-ttu-id="e1db2-158">/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="e1db2-158">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="e1db2-159">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="e1db2-159">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="e1db2-160">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="e1db2-160">Remove Paths</span></span>



| <span data-ttu-id="e1db2-161">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e1db2-161">Order</span></span> | <span data-ttu-id="e1db2-162">Pfad</span><span class="sxs-lookup"><span data-stu-id="e1db2-162">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="e1db2-163">1</span><span class="sxs-lookup"><span data-stu-id="e1db2-163">1</span></span>     | <span data-ttu-id="e1db2-164">/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="e1db2-164">/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="e1db2-165">2</span><span class="sxs-lookup"><span data-stu-id="e1db2-165">2</span></span>     | <span data-ttu-id="e1db2-166">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="e1db2-166">/ifd/{ushort=270}</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="e1db2-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1db2-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1db2-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1db2-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1db2-169">System. Subject</span><span class="sxs-lookup"><span data-stu-id="e1db2-169">System.Subject</span></span>](../properties/props-system-subject.md)
</dt> </dl>

 

 
