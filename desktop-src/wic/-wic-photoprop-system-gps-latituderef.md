---
description: Die fotometadatenrichtlinie für die System. GPS. latituderef-Eigenschaft.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: System. GPS. latituderef-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782fbcecbed90c9c75c1ae5fe9d5409496f842a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217518"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a><span data-ttu-id="1bac5-103">System. GPS. latituderef-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="1bac5-103">System.GPS.LatitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="1bac5-104">Die fotometadatenrichtlinie für die [System. GPS. latituderef](../properties/props-system-gps-latitude.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1bac5-104">The photo metadata policy for the [System.GPS.LatitudeRef](../properties/props-system-gps-latitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1bac5-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="1bac5-105">PKEY</span></span>

<span data-ttu-id="1bac5-106">Pkey \_ GPS- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="1bac5-106">PKEY\_GPS\_LatitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="1bac5-107">Container</span><span class="sxs-lookup"><span data-stu-id="1bac5-107">Containers</span></span>

<span data-ttu-id="1bac5-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1bac5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1bac5-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1bac5-109">Read-Only</span></span>

<span data-ttu-id="1bac5-110">Nein</span><span class="sxs-lookup"><span data-stu-id="1bac5-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1bac5-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="1bac5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1bac5-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="1bac5-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="1bac5-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="1bac5-113">Input Type</span></span>

<span data-ttu-id="1bac5-114">VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird ebenfalls akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="1bac5-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1bac5-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="1bac5-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="1bac5-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="1bac5-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="1bac5-117">Rangfolge von Pfaden (JPEG)</span><span class="sxs-lookup"><span data-stu-id="1bac5-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="1bac5-118">Wenn die Datei im JPEG-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:</span><span class="sxs-lookup"><span data-stu-id="1bac5-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="1bac5-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1bac5-119">Order</span></span> | <span data-ttu-id="1bac5-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="1bac5-120">Path</span></span>                         | <span data-ttu-id="1bac5-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="1bac5-121">Disk Format</span></span> | <span data-ttu-id="1bac5-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1bac5-122">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="1bac5-123">1</span><span class="sxs-lookup"><span data-stu-id="1bac5-123">1</span></span>     | <span data-ttu-id="1bac5-124">/XMP/EXIF: gpslatituderef</span><span class="sxs-lookup"><span data-stu-id="1bac5-124">/xmp/exif:GPSLatitudeRef</span></span>     | <span data-ttu-id="1bac5-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="1bac5-125">Unicode</span></span>     | <span data-ttu-id="1bac5-126">Ja</span><span class="sxs-lookup"><span data-stu-id="1bac5-126">Yes</span></span>      |
| <span data-ttu-id="1bac5-127">2</span><span class="sxs-lookup"><span data-stu-id="1bac5-127">2</span></span>     | <span data-ttu-id="1bac5-128">/App1/IFD/GPS/ \\ {UShort = 1 \\ }</span><span class="sxs-lookup"><span data-stu-id="1bac5-128">/app1/ifd/gps/\\{ushort=1\\}</span></span> | <span data-ttu-id="1bac5-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="1bac5-129">ASCII</span></span>       | <span data-ttu-id="1bac5-130">Nein</span><span class="sxs-lookup"><span data-stu-id="1bac5-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="1bac5-131">Rangfolge von Pfaden (TIFF)</span><span class="sxs-lookup"><span data-stu-id="1bac5-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="1bac5-132">Wenn die Datei im TIFF-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:</span><span class="sxs-lookup"><span data-stu-id="1bac5-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="1bac5-133">Auftrag</span><span class="sxs-lookup"><span data-stu-id="1bac5-133">Order</span></span> | <span data-ttu-id="1bac5-134">Pfad</span><span class="sxs-lookup"><span data-stu-id="1bac5-134">Path</span></span>                         | <span data-ttu-id="1bac5-135">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="1bac5-135">Disk Format</span></span> | <span data-ttu-id="1bac5-136">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1bac5-136">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="1bac5-137">1</span><span class="sxs-lookup"><span data-stu-id="1bac5-137">1</span></span>     | <span data-ttu-id="1bac5-138">/IFD/XMP/EXIF: gpslatituderef</span><span class="sxs-lookup"><span data-stu-id="1bac5-138">/ifd/xmp/exif:GPSLatitudeRef</span></span> | <span data-ttu-id="1bac5-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="1bac5-139">Unicode</span></span>     | <span data-ttu-id="1bac5-140">Ja</span><span class="sxs-lookup"><span data-stu-id="1bac5-140">Yes</span></span>      |
| <span data-ttu-id="1bac5-141">2</span><span class="sxs-lookup"><span data-stu-id="1bac5-141">2</span></span>     | <span data-ttu-id="1bac5-142">/IFD/GPS/ \\ {UShort = 1 \\ }</span><span class="sxs-lookup"><span data-stu-id="1bac5-142">/ifd/gps/\\{ushort=1\\}</span></span>      | <span data-ttu-id="1bac5-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="1bac5-143">ASCII</span></span>       | <span data-ttu-id="1bac5-144">Nein</span><span class="sxs-lookup"><span data-stu-id="1bac5-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="1bac5-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1bac5-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bac5-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1bac5-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bac5-147">System. GPS. latituderef</span><span class="sxs-lookup"><span data-stu-id="1bac5-147">System.GPS.LatitudeRef</span></span>](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
