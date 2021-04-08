---
description: Die fotometadatenrichtlinie für die System. GPS. DOP-Eigenschaft.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: System. GPS. DOP-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960660"
---
# <a name="systemgpsdop-photo-metadata-policy"></a><span data-ttu-id="d2c54-103">System. GPS. DOP-fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d2c54-103">System.GPS.DOP Photo Metadata Policy</span></span>

<span data-ttu-id="d2c54-104">Die fotometadatenrichtlinie für die [System. GPS. DOP-](../properties/props-system-gps-dop.md) Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d2c54-104">The photo metadata policy for the [System.GPS.DOP](../properties/props-system-gps-dop.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d2c54-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="d2c54-105">PKEY</span></span>

<span data-ttu-id="d2c54-106">pkey \_ GPS- \_ DOP</span><span class="sxs-lookup"><span data-stu-id="d2c54-106">PKEY\_GPS\_DOP</span></span>

### <a name="containers"></a><span data-ttu-id="d2c54-107">Container</span><span class="sxs-lookup"><span data-stu-id="d2c54-107">Containers</span></span>

<span data-ttu-id="d2c54-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d2c54-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d2c54-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2c54-109">Read-Only</span></span>

<span data-ttu-id="d2c54-110">Ja</span><span class="sxs-lookup"><span data-stu-id="d2c54-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d2c54-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="d2c54-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d2c54-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="d2c54-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d2c54-113">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="d2c54-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="d2c54-114">Dieser Wert kann durch Schreiben in System. GPS. dopnumerator und System. GPS. dopnenner geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d2c54-114">This value can be written by writing to System.GPS.DOPNumerator and System.GPS.DOPDenominator.</span></span> <span data-ttu-id="d2c54-115">Sie kann nicht direkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d2c54-115">It cannot be written directly.</span></span> <span data-ttu-id="d2c54-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="d2c54-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="d2c54-117">Rangfolge von Pfaden (JPEG)</span><span class="sxs-lookup"><span data-stu-id="d2c54-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="d2c54-118">Wenn die Datei im JPEG-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:</span><span class="sxs-lookup"><span data-stu-id="d2c54-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="d2c54-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="d2c54-119">Order</span></span> | <span data-ttu-id="d2c54-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="d2c54-120">Path</span></span>                          | <span data-ttu-id="d2c54-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="d2c54-121">Disk Format</span></span>   | <span data-ttu-id="d2c54-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d2c54-122">Required</span></span> |
|-------|-------------------------------|---------------|----------|
| <span data-ttu-id="d2c54-123">1</span><span class="sxs-lookup"><span data-stu-id="d2c54-123">1</span></span>     | <span data-ttu-id="d2c54-124">/XMP/EXIF: gpsdop</span><span class="sxs-lookup"><span data-stu-id="d2c54-124">/xmp/exif:GPSDOP</span></span>              | <span data-ttu-id="d2c54-125">XMP-rational</span><span class="sxs-lookup"><span data-stu-id="d2c54-125">XMP rational</span></span>  | <span data-ttu-id="d2c54-126">Ja</span><span class="sxs-lookup"><span data-stu-id="d2c54-126">Yes</span></span>      |
| <span data-ttu-id="d2c54-127">2</span><span class="sxs-lookup"><span data-stu-id="d2c54-127">2</span></span>     | <span data-ttu-id="d2c54-128">/App1/IFD/GPS/ \\ {UShort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="d2c54-128">/app1/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="d2c54-129">EXIF rational</span><span class="sxs-lookup"><span data-stu-id="d2c54-129">EXIF rational</span></span> | <span data-ttu-id="d2c54-130">Nein</span><span class="sxs-lookup"><span data-stu-id="d2c54-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="d2c54-131">Rangfolge von Pfaden (TIFF)</span><span class="sxs-lookup"><span data-stu-id="d2c54-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="d2c54-132">Wenn die Datei im TIFF-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:</span><span class="sxs-lookup"><span data-stu-id="d2c54-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="d2c54-133">Auftrag</span><span class="sxs-lookup"><span data-stu-id="d2c54-133">Order</span></span> | <span data-ttu-id="d2c54-134">Pfad</span><span class="sxs-lookup"><span data-stu-id="d2c54-134">Path</span></span>                     | <span data-ttu-id="d2c54-135">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="d2c54-135">Disk Format</span></span>   | <span data-ttu-id="d2c54-136">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d2c54-136">Required</span></span> |
|-------|--------------------------|---------------|----------|
| <span data-ttu-id="d2c54-137">1</span><span class="sxs-lookup"><span data-stu-id="d2c54-137">1</span></span>     | <span data-ttu-id="d2c54-138">/IFD/XMP/EXIF: gpsdop</span><span class="sxs-lookup"><span data-stu-id="d2c54-138">/ifd/xmp/exif:GPSDop</span></span>     | <span data-ttu-id="d2c54-139">XMP-rational</span><span class="sxs-lookup"><span data-stu-id="d2c54-139">XMP rational</span></span>  | <span data-ttu-id="d2c54-140">Ja</span><span class="sxs-lookup"><span data-stu-id="d2c54-140">Yes</span></span>      |
| <span data-ttu-id="d2c54-141">2</span><span class="sxs-lookup"><span data-stu-id="d2c54-141">2</span></span>     | <span data-ttu-id="d2c54-142">/IFD/GPS/ \\ {UShort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="d2c54-142">/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="d2c54-143">EXIF rational</span><span class="sxs-lookup"><span data-stu-id="d2c54-143">EXIF rational</span></span> | <span data-ttu-id="d2c54-144">Nein</span><span class="sxs-lookup"><span data-stu-id="d2c54-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="d2c54-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2c54-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2c54-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2c54-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2c54-147">System. GPS. DOP</span><span class="sxs-lookup"><span data-stu-id="d2c54-147">System.GPS.DOP</span></span>](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
