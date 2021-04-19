---
description: Die fotometadatenrichtlinie für die System. Photo. Makernote-Eigenschaft.
ms.assetid: e1018bc6-3fd2-4212-afee-6811bfe99f14
title: System. Photo. Makernote Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df1a16205d6a9d1229d3627e6b9cc8c746d8a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349261"
---
# <a name="systemphotomakernote-photo-metadata-policy"></a><span data-ttu-id="b4857-103">System. Photo. Makernote Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b4857-103">System.Photo.MakerNote Photo Metadata Policy</span></span>

<span data-ttu-id="b4857-104">Die fotometadatenrichtlinie für die [System. Photo. Makernote](../properties/props-system-photo-makernote.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b4857-104">The photo metadata policy for the [System.Photo.MakerNote](../properties/props-system-photo-makernote.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b4857-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="b4857-105">PKEY</span></span>

<span data-ttu-id="b4857-106">Pkey- \_ Foto ( \_ Makernote)</span><span class="sxs-lookup"><span data-stu-id="b4857-106">PKEY\_Photo\_MakerNote</span></span>

### <a name="containers"></a><span data-ttu-id="b4857-107">Container</span><span class="sxs-lookup"><span data-stu-id="b4857-107">Containers</span></span>

<span data-ttu-id="b4857-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b4857-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b4857-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4857-109">Read-Only</span></span>

<span data-ttu-id="b4857-110">Nein</span><span class="sxs-lookup"><span data-stu-id="b4857-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b4857-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="b4857-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b4857-112">VT- \_ Vektor \| VTUI1</span><span class="sxs-lookup"><span data-stu-id="b4857-112">VT\_VECTOR \| VTUI1</span></span>

### <a name="input-type"></a><span data-ttu-id="b4857-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="b4857-113">Input Type</span></span>

<span data-ttu-id="b4857-114">Buffer</span><span class="sxs-lookup"><span data-stu-id="b4857-114">Buffer</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b4857-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="b4857-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b4857-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="b4857-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b4857-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b4857-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b4857-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="b4857-118">Read Paths</span></span>



| <span data-ttu-id="b4857-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b4857-119">Order</span></span> | <span data-ttu-id="b4857-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="b4857-120">Path</span></span>                          | <span data-ttu-id="b4857-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b4857-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b4857-122">1</span><span class="sxs-lookup"><span data-stu-id="b4857-122">1</span></span>     | <span data-ttu-id="b4857-123">/App1/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="b4857-123">/app1/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b4857-124">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="b4857-124">Write Paths</span></span>



| <span data-ttu-id="b4857-125">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b4857-125">Order</span></span> | <span data-ttu-id="b4857-126">Pfad</span><span class="sxs-lookup"><span data-stu-id="b4857-126">Path</span></span>                          | <span data-ttu-id="b4857-127">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b4857-127">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b4857-128">1</span><span class="sxs-lookup"><span data-stu-id="b4857-128">1</span></span>     | <span data-ttu-id="b4857-129">/App1/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="b4857-129">/app1/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b4857-130">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="b4857-130">Remove Paths</span></span>



| <span data-ttu-id="b4857-131">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b4857-131">Order</span></span> | <span data-ttu-id="b4857-132">Pfad</span><span class="sxs-lookup"><span data-stu-id="b4857-132">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="b4857-133">1</span><span class="sxs-lookup"><span data-stu-id="b4857-133">1</span></span>     | <span data-ttu-id="b4857-134">/App1/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="b4857-134">/app1/ifd/exif/{ushort=37500}</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="b4857-135">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="b4857-135">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b4857-136">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="b4857-136">Read Paths</span></span>



| <span data-ttu-id="b4857-137">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b4857-137">Order</span></span> | <span data-ttu-id="b4857-138">Pfad</span><span class="sxs-lookup"><span data-stu-id="b4857-138">Path</span></span>                     | <span data-ttu-id="b4857-139">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b4857-139">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="b4857-140">1</span><span class="sxs-lookup"><span data-stu-id="b4857-140">1</span></span>     | <span data-ttu-id="b4857-141">/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="b4857-141">/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b4857-142">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="b4857-142">Write Paths</span></span>



| <span data-ttu-id="b4857-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b4857-143">Order</span></span> | <span data-ttu-id="b4857-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="b4857-144">Path</span></span>                     | <span data-ttu-id="b4857-145">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b4857-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="b4857-146">1</span><span class="sxs-lookup"><span data-stu-id="b4857-146">1</span></span>     | <span data-ttu-id="b4857-147">/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="b4857-147">/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b4857-148">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="b4857-148">Remove Paths</span></span>



| <span data-ttu-id="b4857-149">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b4857-149">Order</span></span> | <span data-ttu-id="b4857-150">Pfad</span><span class="sxs-lookup"><span data-stu-id="b4857-150">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="b4857-151">1</span><span class="sxs-lookup"><span data-stu-id="b4857-151">1</span></span>     | <span data-ttu-id="b4857-152">/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="b4857-152">/ifd/exif/{ushort=37500}</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b4857-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4857-153">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4857-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4857-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4857-155">System. Photo. Makernote</span><span class="sxs-lookup"><span data-stu-id="b4857-155">System.Photo.MakerNote</span></span>](../properties/props-system-photo-makernote.md)
</dt> </dl>

 

 
