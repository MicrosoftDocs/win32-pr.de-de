---
description: Die fotometadatenrichtlinie für die System. Image. CompressedBitsPerPixel-Eigenschaft.
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: System. Image. CompressedBitsPerPixel-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45b3b1e8b29cdf992cd3b451a2e8a43947139a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356196"
---
# <a name="systemimagecompressedbitsperpixel-photo-metadata-policy"></a><span data-ttu-id="112cf-103">System. Image. CompressedBitsPerPixel-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="112cf-103">System.Image.CompressedBitsPerPixel Photo Metadata Policy</span></span>

<span data-ttu-id="112cf-104">Die fotometadatenrichtlinie für die [System. Image. CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="112cf-104">The photo metadata policy for the [System.Image.CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="112cf-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="112cf-105">PKEY</span></span>

<span data-ttu-id="112cf-106">Pkey- \_ Image \_ CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="112cf-106">PKEY\_Image\_CompressedBitsPerPixel</span></span>

### <a name="containers"></a><span data-ttu-id="112cf-107">Container</span><span class="sxs-lookup"><span data-stu-id="112cf-107">Containers</span></span>

<span data-ttu-id="112cf-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="112cf-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="112cf-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="112cf-109">Read-Only</span></span>

<span data-ttu-id="112cf-110">Ja</span><span class="sxs-lookup"><span data-stu-id="112cf-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="112cf-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="112cf-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="112cf-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="112cf-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="112cf-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="112cf-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="112cf-114">Dieser Wert wird aus System. Image. compressedbitsperpixelnumerator und System. Image. compressedbitsperpixelnenner generiert.</span><span class="sxs-lookup"><span data-stu-id="112cf-114">This value is generated from System.Image.CompressedBitsPerPixelNumerator and System.Image.CompressedBitsPerPixelDenominator.</span></span> <span data-ttu-id="112cf-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="112cf-115">It cannot be written directly.</span></span> <span data-ttu-id="112cf-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="112cf-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="112cf-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="112cf-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="112cf-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="112cf-118">Read Paths</span></span>



| <span data-ttu-id="112cf-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="112cf-119">Order</span></span> | <span data-ttu-id="112cf-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="112cf-120">Path</span></span>                             | <span data-ttu-id="112cf-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="112cf-121">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="112cf-122">1</span><span class="sxs-lookup"><span data-stu-id="112cf-122">1</span></span>     | <span data-ttu-id="112cf-123">/App1/IFD/EXIF/{ushort = 37122}</span><span class="sxs-lookup"><span data-stu-id="112cf-123">/app1/ifd/exif/{ushort=37122}</span></span>    |             |
| <span data-ttu-id="112cf-124">2</span><span class="sxs-lookup"><span data-stu-id="112cf-124">2</span></span>     | <span data-ttu-id="112cf-125">/XMP/EXIF: CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="112cf-125">/xmp/exif:CompressedBitsPerPixel</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="112cf-126">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="112cf-126">Remove Paths</span></span>



| <span data-ttu-id="112cf-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="112cf-127">Order</span></span> | <span data-ttu-id="112cf-128">Pfad</span><span class="sxs-lookup"><span data-stu-id="112cf-128">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="112cf-129">1</span><span class="sxs-lookup"><span data-stu-id="112cf-129">1</span></span>     | <span data-ttu-id="112cf-130">/App1/IFD/EXIF/{ushort = 37122}</span><span class="sxs-lookup"><span data-stu-id="112cf-130">/app1/ifd/exif/{ushort=37122}</span></span>    |
| <span data-ttu-id="112cf-131">2</span><span class="sxs-lookup"><span data-stu-id="112cf-131">2</span></span>     | <span data-ttu-id="112cf-132">/XMP/EXIF: CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="112cf-132">/xmp/exif:compressedbitsperpixel</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="112cf-133">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="112cf-133">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="112cf-134">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="112cf-134">Read Paths</span></span>



| <span data-ttu-id="112cf-135">Auftrag</span><span class="sxs-lookup"><span data-stu-id="112cf-135">Order</span></span> | <span data-ttu-id="112cf-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="112cf-136">Path</span></span>                                 | <span data-ttu-id="112cf-137">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="112cf-137">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="112cf-138">1</span><span class="sxs-lookup"><span data-stu-id="112cf-138">1</span></span>     | <span data-ttu-id="112cf-139">/IFD/EXIF/{ushort = 37122}</span><span class="sxs-lookup"><span data-stu-id="112cf-139">/ifd/exif/{ushort=37122}</span></span>             |             |
| <span data-ttu-id="112cf-140">2</span><span class="sxs-lookup"><span data-stu-id="112cf-140">2</span></span>     | <span data-ttu-id="112cf-141">/IFD/XMP/EXIF: CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="112cf-141">/ifd/xmp/exif:CompressedBitsPerPixel</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="112cf-142">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="112cf-142">Remove Paths</span></span>



| <span data-ttu-id="112cf-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="112cf-143">Order</span></span> | <span data-ttu-id="112cf-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="112cf-144">Path</span></span>                                 |
|-------|--------------------------------------|
| <span data-ttu-id="112cf-145">1</span><span class="sxs-lookup"><span data-stu-id="112cf-145">1</span></span>     | <span data-ttu-id="112cf-146">/IFD/EXIF/{ushort = 37122}</span><span class="sxs-lookup"><span data-stu-id="112cf-146">/ifd/exif/{ushort=37122}</span></span>             |
| <span data-ttu-id="112cf-147">2</span><span class="sxs-lookup"><span data-stu-id="112cf-147">2</span></span>     | <span data-ttu-id="112cf-148">/IFD/XMP/EXIF: CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="112cf-148">/ifd/xmp/exif:compressedbitsperpixel</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="112cf-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="112cf-149">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="112cf-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="112cf-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="112cf-151">System. Image. CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="112cf-151">System.Image.CompressedBitsPerPixel</span></span>](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
