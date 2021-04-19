---
description: Die fotometadatenrichtlinie für die System. GPS. destlatituderef-Eigenschaft.
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: System. GPS. destlatituderef-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838e4688f0c3342091e5995885689a44fab38739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357882"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a><span data-ttu-id="b178c-103">System. GPS. destlatituderef-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b178c-103">System.GPS.DestLatitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="b178c-104">Die fotometadatenrichtlinie für die [System. GPS. destlatituderef](../properties/props-system-gps-destlatituderef.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b178c-104">The photo metadata policy for the [System.GPS.DestLatitudeRef](../properties/props-system-gps-destlatituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b178c-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="b178c-105">PKEY</span></span>

<span data-ttu-id="b178c-106">Pkey \_ GPS \_ destlatituderef</span><span class="sxs-lookup"><span data-stu-id="b178c-106">PKEY\_GPS\_DestLatitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="b178c-107">Container</span><span class="sxs-lookup"><span data-stu-id="b178c-107">Containers</span></span>

<span data-ttu-id="b178c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b178c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b178c-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b178c-109">Read-Only</span></span>

<span data-ttu-id="b178c-110">Nein</span><span class="sxs-lookup"><span data-stu-id="b178c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b178c-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="b178c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b178c-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="b178c-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="b178c-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="b178c-113">Input Type</span></span>

<span data-ttu-id="b178c-114">VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="b178c-114">VT\_LPWSTR is preferred, but VT\_LPSTR is accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b178c-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="b178c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b178c-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="b178c-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="b178c-117">Rangfolge von Pfaden (JPEG)</span><span class="sxs-lookup"><span data-stu-id="b178c-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="b178c-118">Wenn die Datei im JPEG-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:</span><span class="sxs-lookup"><span data-stu-id="b178c-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="b178c-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b178c-119">Order</span></span> | <span data-ttu-id="b178c-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="b178c-120">Path</span></span>                          | <span data-ttu-id="b178c-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b178c-121">Disk Format</span></span> | <span data-ttu-id="b178c-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b178c-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="b178c-123">1</span><span class="sxs-lookup"><span data-stu-id="b178c-123">1</span></span>     | <span data-ttu-id="b178c-124">/XMP/EXIF: gpsdestlatituderef</span><span class="sxs-lookup"><span data-stu-id="b178c-124">/xmp/exif:GPSDestLatitudeRef</span></span>  | <span data-ttu-id="b178c-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="b178c-125">Unicode</span></span>     | <span data-ttu-id="b178c-126">Ja</span><span class="sxs-lookup"><span data-stu-id="b178c-126">Yes</span></span>      |
| <span data-ttu-id="b178c-127">2</span><span class="sxs-lookup"><span data-stu-id="b178c-127">2</span></span>     | <span data-ttu-id="b178c-128">/App1/IFD/GPS/ \\ {UShort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="b178c-128">/app1/ifd/gps/\\{ushort=19\\}</span></span> | <span data-ttu-id="b178c-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="b178c-129">ASCII</span></span>       | <span data-ttu-id="b178c-130">Nein</span><span class="sxs-lookup"><span data-stu-id="b178c-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="b178c-131">Rangfolge von Pfaden (TIFF)</span><span class="sxs-lookup"><span data-stu-id="b178c-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="b178c-132">Wenn die Datei im TIFF-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:</span><span class="sxs-lookup"><span data-stu-id="b178c-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="b178c-133">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b178c-133">Order</span></span> | <span data-ttu-id="b178c-134">Pfad</span><span class="sxs-lookup"><span data-stu-id="b178c-134">Path</span></span>                             | <span data-ttu-id="b178c-135">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="b178c-135">Disk Format</span></span> | <span data-ttu-id="b178c-136">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b178c-136">Required</span></span> |
|-------|----------------------------------|-------------|----------|
| <span data-ttu-id="b178c-137">1</span><span class="sxs-lookup"><span data-stu-id="b178c-137">1</span></span>     | <span data-ttu-id="b178c-138">/IFD/XMP/EXIF: gpsdestlatituderef</span><span class="sxs-lookup"><span data-stu-id="b178c-138">/ifd/xmp/exif:GPSDestLatitudeRef</span></span> | <span data-ttu-id="b178c-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="b178c-139">Unicode</span></span>     | <span data-ttu-id="b178c-140">Ja</span><span class="sxs-lookup"><span data-stu-id="b178c-140">Yes</span></span>      |
| <span data-ttu-id="b178c-141">2</span><span class="sxs-lookup"><span data-stu-id="b178c-141">2</span></span>     | <span data-ttu-id="b178c-142">/IFD/GPS/ \\ {UShort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="b178c-142">/ifd/gps/\\{ushort=19\\}</span></span>         | <span data-ttu-id="b178c-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="b178c-143">ASCII</span></span>       | <span data-ttu-id="b178c-144">Nein</span><span class="sxs-lookup"><span data-stu-id="b178c-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="b178c-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b178c-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b178c-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b178c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b178c-147">System. GPS. destlatituderef</span><span class="sxs-lookup"><span data-stu-id="b178c-147">System.GPS.DestLatitudeRef</span></span>](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
