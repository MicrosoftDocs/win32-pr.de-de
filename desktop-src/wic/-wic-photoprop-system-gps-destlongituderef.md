---
description: Die fotometadatenrichtlinie für die Eigenschaft System. GPS. destlängs Deref.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: System. GPS. destlängs Deref-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8139fcf5218d9863393888d7ab7b188a53e7f55f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362900"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a><span data-ttu-id="df585-103">System. GPS. destlängs Deref-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="df585-103">System.GPS.DestLongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="df585-104">Die fotometadatenrichtlinie für die Eigenschaft [System. GPS. destlängs Deref](../properties/props-system-gps-destlongituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="df585-104">The photo metadata policy for the [System.GPS.DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="df585-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="df585-105">PKEY</span></span>

<span data-ttu-id="df585-106">pkey \_ GPS. Destlängs Deref</span><span class="sxs-lookup"><span data-stu-id="df585-106">PKEY\_GPS.DestLongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="df585-107">Container</span><span class="sxs-lookup"><span data-stu-id="df585-107">Containers</span></span>

<span data-ttu-id="df585-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="df585-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="df585-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df585-109">Read-Only</span></span>

<span data-ttu-id="df585-110">Nein</span><span class="sxs-lookup"><span data-stu-id="df585-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="df585-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="df585-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="df585-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="df585-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="df585-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="df585-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="df585-114">VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird ebenfalls akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="df585-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="df585-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="df585-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="df585-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="df585-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="df585-117">Rangfolge von Pfaden (JPEG)</span><span class="sxs-lookup"><span data-stu-id="df585-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="df585-118">Wenn die Datei im JPEG-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:</span><span class="sxs-lookup"><span data-stu-id="df585-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="df585-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="df585-119">Order</span></span> | <span data-ttu-id="df585-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="df585-120">Path</span></span>                          | <span data-ttu-id="df585-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="df585-121">Disk Format</span></span> | <span data-ttu-id="df585-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="df585-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="df585-123">1</span><span class="sxs-lookup"><span data-stu-id="df585-123">1</span></span>     | <span data-ttu-id="df585-124">/XMP/EXIF: gpsdestlängs Deref</span><span class="sxs-lookup"><span data-stu-id="df585-124">/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="df585-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="df585-125">Unicode</span></span>     | <span data-ttu-id="df585-126">Ja</span><span class="sxs-lookup"><span data-stu-id="df585-126">Yes</span></span>      |
| <span data-ttu-id="df585-127">2</span><span class="sxs-lookup"><span data-stu-id="df585-127">2</span></span>     | <span data-ttu-id="df585-128">/App1/IFD/GPS/ \\ {UShort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="df585-128">/app1/ifd/gps/\\{ushort=21\\}</span></span> | <span data-ttu-id="df585-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="df585-129">ASCII</span></span>       | <span data-ttu-id="df585-130">Nein</span><span class="sxs-lookup"><span data-stu-id="df585-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="df585-131">Rangfolge von Pfaden (TIFF)</span><span class="sxs-lookup"><span data-stu-id="df585-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="df585-132">Wenn die Datei im TIFF-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:</span><span class="sxs-lookup"><span data-stu-id="df585-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="df585-133">Auftrag</span><span class="sxs-lookup"><span data-stu-id="df585-133">Order</span></span> | <span data-ttu-id="df585-134">Pfad</span><span class="sxs-lookup"><span data-stu-id="df585-134">Path</span></span>                              | <span data-ttu-id="df585-135">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="df585-135">Disk Format</span></span> | <span data-ttu-id="df585-136">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="df585-136">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="df585-137">1</span><span class="sxs-lookup"><span data-stu-id="df585-137">1</span></span>     | <span data-ttu-id="df585-138">/IFD/XMP/EXIF: gpsdestlängs Deref</span><span class="sxs-lookup"><span data-stu-id="df585-138">/ifd/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="df585-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="df585-139">Unicode</span></span>     | <span data-ttu-id="df585-140">Ja</span><span class="sxs-lookup"><span data-stu-id="df585-140">Yes</span></span>      |
| <span data-ttu-id="df585-141">2</span><span class="sxs-lookup"><span data-stu-id="df585-141">2</span></span>     | <span data-ttu-id="df585-142">/IFD/GPS/ \\ {UShort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="df585-142">/ifd/gps/\\{ushort=21\\}</span></span>          | <span data-ttu-id="df585-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="df585-143">ASCII</span></span>       | <span data-ttu-id="df585-144">Nein</span><span class="sxs-lookup"><span data-stu-id="df585-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="df585-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df585-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="df585-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df585-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df585-147">System. GPS. destlängs Deref</span><span class="sxs-lookup"><span data-stu-id="df585-147">System.GPS.DestLongitudeRef</span></span>](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
