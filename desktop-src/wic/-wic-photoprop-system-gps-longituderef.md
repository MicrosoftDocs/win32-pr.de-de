---
description: Die fotometadatenrichtlinie für die System. GPS. die-Eigenschaft.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: System. GPS.-metadatenrichtlinie für Fotos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a93d37b59ca7c77bc05e049860cf4e2608eb60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350900"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a><span data-ttu-id="5d56a-103">System. GPS.-metadatenrichtlinie für Fotos</span><span class="sxs-lookup"><span data-stu-id="5d56a-103">System.GPS.LongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="5d56a-104">Die fotometadatenrichtlinie für die [System. GPS. die-](../properties/props-system-gps-longituderef.md) Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5d56a-104">The photo metadata policy for the [System.GPS.LongitudeRef](../properties/props-system-gps-longituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5d56a-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="5d56a-105">PKEY</span></span>

<span data-ttu-id="5d56a-106">Pkey \_ GPS- \_ längs</span><span class="sxs-lookup"><span data-stu-id="5d56a-106">PKEY\_GPS\_LongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="5d56a-107">Container</span><span class="sxs-lookup"><span data-stu-id="5d56a-107">Containers</span></span>

<span data-ttu-id="5d56a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5d56a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5d56a-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5d56a-109">Read-Only</span></span>

<span data-ttu-id="5d56a-110">Nein</span><span class="sxs-lookup"><span data-stu-id="5d56a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5d56a-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="5d56a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5d56a-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5d56a-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="5d56a-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="5d56a-113">Input Type</span></span>

<span data-ttu-id="5d56a-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5d56a-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5d56a-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="5d56a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="5d56a-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="5d56a-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="5d56a-117">Rangfolge von Pfaden (JPEG)</span><span class="sxs-lookup"><span data-stu-id="5d56a-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="5d56a-118">Wenn die Datei im JPEG-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:</span><span class="sxs-lookup"><span data-stu-id="5d56a-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="5d56a-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="5d56a-119">Order</span></span> | <span data-ttu-id="5d56a-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="5d56a-120">Path</span></span>                         | <span data-ttu-id="5d56a-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="5d56a-121">Disk Format</span></span> | <span data-ttu-id="5d56a-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5d56a-122">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="5d56a-123">1</span><span class="sxs-lookup"><span data-stu-id="5d56a-123">1</span></span>     | <span data-ttu-id="5d56a-124">/XMP/EXIF: gpsordneref</span><span class="sxs-lookup"><span data-stu-id="5d56a-124">/xmp/exif:GPSLongitudeRef</span></span>    | <span data-ttu-id="5d56a-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="5d56a-125">Unicode</span></span>     | <span data-ttu-id="5d56a-126">Ja</span><span class="sxs-lookup"><span data-stu-id="5d56a-126">Yes</span></span>      |
| <span data-ttu-id="5d56a-127">2</span><span class="sxs-lookup"><span data-stu-id="5d56a-127">2</span></span>     | <span data-ttu-id="5d56a-128">/App1/IFD/GPS/ \\ {UShort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="5d56a-128">/app1/ifd/gps/\\{ushort=3\\}</span></span> | <span data-ttu-id="5d56a-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="5d56a-129">ASCII</span></span>       | <span data-ttu-id="5d56a-130">Nein</span><span class="sxs-lookup"><span data-stu-id="5d56a-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="5d56a-131">Rangfolge von Pfaden (TIFF)</span><span class="sxs-lookup"><span data-stu-id="5d56a-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="5d56a-132">Wenn die Datei im TIFF-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:</span><span class="sxs-lookup"><span data-stu-id="5d56a-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="5d56a-133">Auftrag</span><span class="sxs-lookup"><span data-stu-id="5d56a-133">Order</span></span> | <span data-ttu-id="5d56a-134">Pfad</span><span class="sxs-lookup"><span data-stu-id="5d56a-134">Path</span></span>                          | <span data-ttu-id="5d56a-135">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="5d56a-135">Disk Format</span></span> | <span data-ttu-id="5d56a-136">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5d56a-136">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="5d56a-137">1</span><span class="sxs-lookup"><span data-stu-id="5d56a-137">1</span></span>     | <span data-ttu-id="5d56a-138">/IFD/XMP/EXIF: gpsordneref</span><span class="sxs-lookup"><span data-stu-id="5d56a-138">/ifd/xmp/exif:GPSLongitudeRef</span></span> | <span data-ttu-id="5d56a-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="5d56a-139">Unicode</span></span>     | <span data-ttu-id="5d56a-140">Ja</span><span class="sxs-lookup"><span data-stu-id="5d56a-140">Yes</span></span>      |
| <span data-ttu-id="5d56a-141">2</span><span class="sxs-lookup"><span data-stu-id="5d56a-141">2</span></span>     | <span data-ttu-id="5d56a-142">/IFD/GPS/ \\ {UShort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="5d56a-142">/ifd/gps/\\{ushort=3\\}</span></span>       | <span data-ttu-id="5d56a-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="5d56a-143">ASCII</span></span>       | <span data-ttu-id="5d56a-144">Nein</span><span class="sxs-lookup"><span data-stu-id="5d56a-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="5d56a-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d56a-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d56a-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d56a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d56a-147">System. GPS. längs-EF</span><span class="sxs-lookup"><span data-stu-id="5d56a-147">System.GPS.LongitudeRef</span></span>](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
