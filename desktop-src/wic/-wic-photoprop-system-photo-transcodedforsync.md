---
description: Die fotometadatenrichtlinie für die System. Photo. transcodedforsync-Eigenschaft.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: System. Photo. transcodedforsync Photo-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5884ad469fcf7b5dffc8c4ad14f0ee5ff90cd07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867327"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a><span data-ttu-id="bbab7-103">System. Photo. transcodedforsync Photo-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="bbab7-103">System.Photo.TranscodedForSync Photo Metadata Policy</span></span>

<span data-ttu-id="bbab7-104">Die fotometadatenrichtlinie für die [System. Photo. transcodedforsync](../properties/props-system-photo-transcodedforsync.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bbab7-104">The photo metadata policy for the [System.Photo.TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="bbab7-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="bbab7-105">PKEY</span></span>

<span data-ttu-id="bbab7-106">Pkey- \_ Foto \_ transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="bbab7-106">PKEY\_Photo\_TranscodedForSync</span></span>

### <a name="containers"></a><span data-ttu-id="bbab7-107">Container</span><span class="sxs-lookup"><span data-stu-id="bbab7-107">Containers</span></span>

<span data-ttu-id="bbab7-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="bbab7-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="bbab7-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbab7-109">Read-Only</span></span>

<span data-ttu-id="bbab7-110">Nein</span><span class="sxs-lookup"><span data-stu-id="bbab7-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="bbab7-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="bbab7-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="bbab7-112">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="bbab7-112">VT\_BOOL</span></span>

### <a name="input-type"></a><span data-ttu-id="bbab7-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="bbab7-113">Input Type</span></span>

<span data-ttu-id="bbab7-114">Boolesch.</span><span class="sxs-lookup"><span data-stu-id="bbab7-114">Boolean.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="bbab7-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="bbab7-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="bbab7-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="bbab7-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="bbab7-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="bbab7-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="bbab7-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="bbab7-118">Read Paths</span></span>



| <span data-ttu-id="bbab7-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bbab7-119">Order</span></span> | <span data-ttu-id="bbab7-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="bbab7-120">Path</span></span>                                  | <span data-ttu-id="bbab7-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="bbab7-121">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="bbab7-122">1</span><span class="sxs-lookup"><span data-stu-id="bbab7-122">1</span></span>     | <span data-ttu-id="bbab7-123">/App1/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="bbab7-123">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="bbab7-124">bool \_ UShort</span><span class="sxs-lookup"><span data-stu-id="bbab7-124">bool\_ushort</span></span> |
| <span data-ttu-id="bbab7-125">2</span><span class="sxs-lookup"><span data-stu-id="bbab7-125">2</span></span>     | <span data-ttu-id="bbab7-126">/XMP/MicrosoftPhoto: transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="bbab7-126">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="bbab7-127">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="bbab7-127">Write Paths</span></span>



| <span data-ttu-id="bbab7-128">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bbab7-128">Order</span></span> | <span data-ttu-id="bbab7-129">Pfad</span><span class="sxs-lookup"><span data-stu-id="bbab7-129">Path</span></span>                                  | <span data-ttu-id="bbab7-130">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="bbab7-130">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="bbab7-131">1</span><span class="sxs-lookup"><span data-stu-id="bbab7-131">1</span></span>     | <span data-ttu-id="bbab7-132">/App1/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="bbab7-132">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="bbab7-133">bool \_ UShort</span><span class="sxs-lookup"><span data-stu-id="bbab7-133">bool\_ushort</span></span> |
| <span data-ttu-id="bbab7-134">2</span><span class="sxs-lookup"><span data-stu-id="bbab7-134">2</span></span>     | <span data-ttu-id="bbab7-135">/XMP/MicrosoftPhoto: transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="bbab7-135">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="bbab7-136">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="bbab7-136">Remove Paths</span></span>



| <span data-ttu-id="bbab7-137">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bbab7-137">Order</span></span> | <span data-ttu-id="bbab7-138">Pfad</span><span class="sxs-lookup"><span data-stu-id="bbab7-138">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="bbab7-139">1</span><span class="sxs-lookup"><span data-stu-id="bbab7-139">1</span></span>     | <span data-ttu-id="bbab7-140">/App1/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="bbab7-140">/app1/ifd/{ushort=18248}</span></span>              |
| <span data-ttu-id="bbab7-141">2</span><span class="sxs-lookup"><span data-stu-id="bbab7-141">2</span></span>     | <span data-ttu-id="bbab7-142">/XMP/microsoftphoto: transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="bbab7-142">/xmp/microsoftphoto:transcodedforsync</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="bbab7-143">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="bbab7-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="bbab7-144">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="bbab7-144">Read Paths</span></span>



| <span data-ttu-id="bbab7-145">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bbab7-145">Order</span></span> | <span data-ttu-id="bbab7-146">Pfad</span><span class="sxs-lookup"><span data-stu-id="bbab7-146">Path</span></span>                                      | <span data-ttu-id="bbab7-147">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="bbab7-147">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="bbab7-148">1</span><span class="sxs-lookup"><span data-stu-id="bbab7-148">1</span></span>     | <span data-ttu-id="bbab7-149">/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="bbab7-149">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="bbab7-150">bool \_ UShort</span><span class="sxs-lookup"><span data-stu-id="bbab7-150">bool\_ushort</span></span> |
| <span data-ttu-id="bbab7-151">2</span><span class="sxs-lookup"><span data-stu-id="bbab7-151">2</span></span>     | <span data-ttu-id="bbab7-152">/IFD/XMP/MicrosoftPhoto: transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="bbab7-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="bbab7-153">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="bbab7-153">Write Paths</span></span>



| <span data-ttu-id="bbab7-154">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bbab7-154">Order</span></span> | <span data-ttu-id="bbab7-155">Pfad</span><span class="sxs-lookup"><span data-stu-id="bbab7-155">Path</span></span>                                      | <span data-ttu-id="bbab7-156">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="bbab7-156">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="bbab7-157">1</span><span class="sxs-lookup"><span data-stu-id="bbab7-157">1</span></span>     | <span data-ttu-id="bbab7-158">/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="bbab7-158">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="bbab7-159">bool \_ UShort</span><span class="sxs-lookup"><span data-stu-id="bbab7-159">bool\_ushort</span></span> |
| <span data-ttu-id="bbab7-160">2</span><span class="sxs-lookup"><span data-stu-id="bbab7-160">2</span></span>     | <span data-ttu-id="bbab7-161">/IFD/XMP/MicrosoftPhoto: transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="bbab7-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="bbab7-162">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="bbab7-162">Remove Paths</span></span>



| <span data-ttu-id="bbab7-163">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bbab7-163">Order</span></span> | <span data-ttu-id="bbab7-164">Pfad</span><span class="sxs-lookup"><span data-stu-id="bbab7-164">Path</span></span>                                      |
|-------|-------------------------------------------|
| <span data-ttu-id="bbab7-165">1</span><span class="sxs-lookup"><span data-stu-id="bbab7-165">1</span></span>     | <span data-ttu-id="bbab7-166">/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="bbab7-166">/ifd/{ushort=18248}</span></span>                       |
| <span data-ttu-id="bbab7-167">2</span><span class="sxs-lookup"><span data-stu-id="bbab7-167">2</span></span>     | <span data-ttu-id="bbab7-168">/IFD/XMP/microsoftphoto: transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="bbab7-168">/ifd/xmp/microsoftphoto:transcodedforsync</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bbab7-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbab7-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbab7-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bbab7-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbab7-171">System. Photo. transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="bbab7-171">System.Photo.TranscodedForSync</span></span>](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
