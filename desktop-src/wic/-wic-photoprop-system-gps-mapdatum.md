---
description: Die fotometadatenrichtlinie für die System. GPS. mapdatum-Eigenschaft.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: System. GPS. mapdatum-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7a279c79da3d2b1dd20563af35bd34233a1a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373309"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a><span data-ttu-id="fbd2c-103">System. GPS. mapdatum-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="fbd2c-103">System.GPS.MapDatum Photo Metadata Policy</span></span>

<span data-ttu-id="fbd2c-104">Die fotometadatenrichtlinie für die [System. GPS. mapdatum](../properties/props-system-gps-mapdatum.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="fbd2c-104">The photo metadata policy for the [System.GPS.MapDatum](../properties/props-system-gps-mapdatum.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="fbd2c-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="fbd2c-105">PKEY</span></span>

<span data-ttu-id="fbd2c-106">Pkey \_ GPS \_ mapdatum</span><span class="sxs-lookup"><span data-stu-id="fbd2c-106">PKEY\_GPS\_MapDatum</span></span>

### <a name="containers"></a><span data-ttu-id="fbd2c-107">Container</span><span class="sxs-lookup"><span data-stu-id="fbd2c-107">Containers</span></span>

<span data-ttu-id="fbd2c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="fbd2c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="fbd2c-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fbd2c-109">Read-Only</span></span>

<span data-ttu-id="fbd2c-110">Nein</span><span class="sxs-lookup"><span data-stu-id="fbd2c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="fbd2c-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="fbd2c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="fbd2c-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="fbd2c-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="fbd2c-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="fbd2c-113">Input Type</span></span>

<span data-ttu-id="fbd2c-114">VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird ebenfalls akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="fbd2c-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="fbd2c-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="fbd2c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="fbd2c-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="fbd2c-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="fbd2c-117">Rangfolge von Pfaden (JPEG)</span><span class="sxs-lookup"><span data-stu-id="fbd2c-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="fbd2c-118">Wenn die Datei im JPEG-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:</span><span class="sxs-lookup"><span data-stu-id="fbd2c-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="fbd2c-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fbd2c-119">Order</span></span> | <span data-ttu-id="fbd2c-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="fbd2c-120">Path</span></span>                          | <span data-ttu-id="fbd2c-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fbd2c-121">Disk Format</span></span> | <span data-ttu-id="fbd2c-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fbd2c-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="fbd2c-123">1</span><span class="sxs-lookup"><span data-stu-id="fbd2c-123">1</span></span>     | <span data-ttu-id="fbd2c-124">/XMP/EXIF: gpsmapdatum</span><span class="sxs-lookup"><span data-stu-id="fbd2c-124">/xmp/exif:GPSMapDatum</span></span>         | <span data-ttu-id="fbd2c-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="fbd2c-125">Unicode</span></span>     | <span data-ttu-id="fbd2c-126">Ja</span><span class="sxs-lookup"><span data-stu-id="fbd2c-126">Yes</span></span>      |
| <span data-ttu-id="fbd2c-127">2</span><span class="sxs-lookup"><span data-stu-id="fbd2c-127">2</span></span>     | <span data-ttu-id="fbd2c-128">/App1/IFD/GPS/ \\ {UShort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="fbd2c-128">/app1/ifd/gps/\\{ushort=18\\}</span></span> | <span data-ttu-id="fbd2c-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="fbd2c-129">ASCII</span></span>       | <span data-ttu-id="fbd2c-130">Nein</span><span class="sxs-lookup"><span data-stu-id="fbd2c-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="fbd2c-131">Rangfolge von Pfaden (TIFF)</span><span class="sxs-lookup"><span data-stu-id="fbd2c-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="fbd2c-132">Wenn die Datei im TIFF-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:</span><span class="sxs-lookup"><span data-stu-id="fbd2c-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="fbd2c-133">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fbd2c-133">Order</span></span> | <span data-ttu-id="fbd2c-134">Pfad</span><span class="sxs-lookup"><span data-stu-id="fbd2c-134">Path</span></span>                      | <span data-ttu-id="fbd2c-135">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="fbd2c-135">Disk Format</span></span> | <span data-ttu-id="fbd2c-136">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fbd2c-136">Required</span></span> |
|-------|---------------------------|-------------|----------|
| <span data-ttu-id="fbd2c-137">1</span><span class="sxs-lookup"><span data-stu-id="fbd2c-137">1</span></span>     | <span data-ttu-id="fbd2c-138">/IFD/XMP/EXIF: gpsmapdatum</span><span class="sxs-lookup"><span data-stu-id="fbd2c-138">/ifd/xmp/exif:GPSMapDatum</span></span> | <span data-ttu-id="fbd2c-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="fbd2c-139">Unicode</span></span>     | <span data-ttu-id="fbd2c-140">Ja</span><span class="sxs-lookup"><span data-stu-id="fbd2c-140">Yes</span></span>      |
| <span data-ttu-id="fbd2c-141">2</span><span class="sxs-lookup"><span data-stu-id="fbd2c-141">2</span></span>     | <span data-ttu-id="fbd2c-142">/IFD/GPS/ \\ {UShort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="fbd2c-142">/ifd/gps/\\{ushort=18\\}</span></span>  | <span data-ttu-id="fbd2c-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="fbd2c-143">ASCII</span></span>       | <span data-ttu-id="fbd2c-144">Nein</span><span class="sxs-lookup"><span data-stu-id="fbd2c-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="fbd2c-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbd2c-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbd2c-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fbd2c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbd2c-147">System. GPS. mapdatum</span><span class="sxs-lookup"><span data-stu-id="fbd2c-147">System.GPS.MapDatum</span></span>](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
