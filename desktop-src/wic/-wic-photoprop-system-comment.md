---
description: Die fotometadatenrichtlinie für die System. Comment-Eigenschaft.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: System. Comment-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9d7526e05a72b073ac32bd8286a621b33ee62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348598"
---
# <a name="systemcomment-photo-metadata-policy"></a><span data-ttu-id="9d198-103">System. Comment-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="9d198-103">System.Comment Photo Metadata Policy</span></span>

<span data-ttu-id="9d198-104">Die fotometadatenrichtlinie für die [System. Comment](../properties/props-system-comment.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9d198-104">The photo metadata policy for the [System.Comment](../properties/props-system-comment.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9d198-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="9d198-105">PKEY</span></span>

<span data-ttu-id="9d198-106">Pkey- \_ Kommentar</span><span class="sxs-lookup"><span data-stu-id="9d198-106">PKEY\_Comment</span></span>

### <a name="containers"></a><span data-ttu-id="9d198-107">Container</span><span class="sxs-lookup"><span data-stu-id="9d198-107">Containers</span></span>

<span data-ttu-id="9d198-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9d198-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9d198-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d198-109">Read-Only</span></span>

<span data-ttu-id="9d198-110">Nein</span><span class="sxs-lookup"><span data-stu-id="9d198-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9d198-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="9d198-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9d198-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="9d198-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="9d198-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="9d198-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="9d198-114">VT \_ LPWSTR oder VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="9d198-114">VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9d198-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="9d198-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="9d198-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="9d198-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9d198-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="9d198-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9d198-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="9d198-118">Read Paths</span></span>



| <span data-ttu-id="9d198-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9d198-119">Order</span></span> | <span data-ttu-id="9d198-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="9d198-120">Path</span></span>                                | <span data-ttu-id="9d198-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9d198-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="9d198-122">1</span><span class="sxs-lookup"><span data-stu-id="9d198-122">1</span></span>     | <span data-ttu-id="9d198-123">/App1/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="9d198-123">/app1/ifd/{ushort=40092}</span></span>            | <span data-ttu-id="9d198-124">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="9d198-124">unicode\_bytes</span></span> |
| <span data-ttu-id="9d198-125">2</span><span class="sxs-lookup"><span data-stu-id="9d198-125">2</span></span>     | <span data-ttu-id="9d198-126">/App1/IFD/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="9d198-126">/app1/ifd/{ushort=37510}</span></span>            | <span data-ttu-id="9d198-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="9d198-127">unicode</span></span>        |
| <span data-ttu-id="9d198-128">3</span><span class="sxs-lookup"><span data-stu-id="9d198-128">3</span></span>     | <span data-ttu-id="9d198-129">/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="9d198-129">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="9d198-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="9d198-130">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="9d198-131">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="9d198-131">Write Paths</span></span>



| <span data-ttu-id="9d198-132">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9d198-132">Order</span></span> | <span data-ttu-id="9d198-133">Pfad</span><span class="sxs-lookup"><span data-stu-id="9d198-133">Path</span></span>                     | <span data-ttu-id="9d198-134">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9d198-134">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="9d198-135">1</span><span class="sxs-lookup"><span data-stu-id="9d198-135">1</span></span>     | <span data-ttu-id="9d198-136">/App1/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="9d198-136">/app1/ifd/{ushort=40092}</span></span> | <span data-ttu-id="9d198-137">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="9d198-137">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="9d198-138">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="9d198-138">Remove Paths</span></span>



| <span data-ttu-id="9d198-139">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9d198-139">Order</span></span> | <span data-ttu-id="9d198-140">Pfad</span><span class="sxs-lookup"><span data-stu-id="9d198-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="9d198-141">1</span><span class="sxs-lookup"><span data-stu-id="9d198-141">1</span></span>     | <span data-ttu-id="9d198-142">/App1/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="9d198-142">/app1/ifd/{ushort=40092}</span></span>      |
| <span data-ttu-id="9d198-143">2</span><span class="sxs-lookup"><span data-stu-id="9d198-143">2</span></span>     | <span data-ttu-id="9d198-144">/App1/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="9d198-144">/app1/ifd/exif/{ushort=37510}</span></span> |
| <span data-ttu-id="9d198-145">3</span><span class="sxs-lookup"><span data-stu-id="9d198-145">3</span></span>     | <span data-ttu-id="9d198-146">/XMP/EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="9d198-146">/xmp/exif:UserComment</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="9d198-147">TIFF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="9d198-147">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9d198-148">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="9d198-148">Read Paths</span></span>



| <span data-ttu-id="9d198-149">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9d198-149">Order</span></span> | <span data-ttu-id="9d198-150">Pfad</span><span class="sxs-lookup"><span data-stu-id="9d198-150">Path</span></span>                                    | <span data-ttu-id="9d198-151">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9d198-151">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="9d198-152">1</span><span class="sxs-lookup"><span data-stu-id="9d198-152">1</span></span>     | <span data-ttu-id="9d198-153">/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="9d198-153">/ifd/{ushort=40092}</span></span>                     | <span data-ttu-id="9d198-154">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="9d198-154">unicode\_bytes</span></span> |
| <span data-ttu-id="9d198-155">2</span><span class="sxs-lookup"><span data-stu-id="9d198-155">2</span></span>     | <span data-ttu-id="9d198-156">/IFD/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="9d198-156">/ifd/{ushort=37510}</span></span>                     | <span data-ttu-id="9d198-157">Unicode</span><span class="sxs-lookup"><span data-stu-id="9d198-157">unicode</span></span>        |
| <span data-ttu-id="9d198-158">3</span><span class="sxs-lookup"><span data-stu-id="9d198-158">3</span></span>     | <span data-ttu-id="9d198-159">/IFD/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="9d198-159">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="9d198-160">Unicode</span><span class="sxs-lookup"><span data-stu-id="9d198-160">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="9d198-161">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="9d198-161">Write Paths</span></span>



| <span data-ttu-id="9d198-162">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9d198-162">Order</span></span> | <span data-ttu-id="9d198-163">Pfad</span><span class="sxs-lookup"><span data-stu-id="9d198-163">Path</span></span>                | <span data-ttu-id="9d198-164">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="9d198-164">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="9d198-165">1</span><span class="sxs-lookup"><span data-stu-id="9d198-165">1</span></span>     | <span data-ttu-id="9d198-166">/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="9d198-166">/ifd/{ushort=40092}</span></span> | <span data-ttu-id="9d198-167">Unicode- \_ Bytes</span><span class="sxs-lookup"><span data-stu-id="9d198-167">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="9d198-168">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="9d198-168">Remove Paths</span></span>



| <span data-ttu-id="9d198-169">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9d198-169">Order</span></span> | <span data-ttu-id="9d198-170">Pfad</span><span class="sxs-lookup"><span data-stu-id="9d198-170">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="9d198-171">1</span><span class="sxs-lookup"><span data-stu-id="9d198-171">1</span></span>     | <span data-ttu-id="9d198-172">/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="9d198-172">/ifd/{ushort=40092}</span></span>       |
| <span data-ttu-id="9d198-173">2</span><span class="sxs-lookup"><span data-stu-id="9d198-173">2</span></span>     | <span data-ttu-id="9d198-174">/IFD/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="9d198-174">/ifd/{ushort=37510}</span></span>       |
| <span data-ttu-id="9d198-175">3</span><span class="sxs-lookup"><span data-stu-id="9d198-175">3</span></span>     | <span data-ttu-id="9d198-176">/IFD/XMP/EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="9d198-176">/ifd/xmp/exif:UserComment</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9d198-177">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d198-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d198-178">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9d198-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d198-179">System. Comment</span><span class="sxs-lookup"><span data-stu-id="9d198-179">System.Comment</span></span>](../properties/props-system-comment.md)
</dt> </dl>

 

 
