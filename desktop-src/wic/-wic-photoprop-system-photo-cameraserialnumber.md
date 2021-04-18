---
description: Die fotometadatenrichtlinie für die System. Photo. cameraserialnumber-Eigenschaft.
ms.assetid: 85f78f45-5e76-4d52-88a2-ac3c9e2b6a1e
title: System. Photo. cameraserialnumber-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c329cd4c56b49e39de5da97ac9d9f8b14bffb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352673"
---
# <a name="systemphotocameraserialnumber-photo-metadata-policy"></a><span data-ttu-id="bf1e6-103">System. Photo. cameraserialnumber-fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="bf1e6-103">System.Photo.CameraSerialNumber Photo Metadata Policy</span></span>

<span data-ttu-id="bf1e6-104">Die fotometadatenrichtlinie für die [System. Photo. cameraserialnumber](../properties/props-system-photo-cameraserialnumber.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bf1e6-104">The photo metadata policy for the [System.Photo.CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="bf1e6-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="bf1e6-105">PKEY</span></span>

<span data-ttu-id="bf1e6-106">Pkey- \_ Foto \_ cameraserialnumber</span><span class="sxs-lookup"><span data-stu-id="bf1e6-106">PKEY\_Photo\_CameraSerialNumber</span></span>

### <a name="containers"></a><span data-ttu-id="bf1e6-107">Container</span><span class="sxs-lookup"><span data-stu-id="bf1e6-107">Containers</span></span>

<span data-ttu-id="bf1e6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="bf1e6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="bf1e6-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf1e6-109">Read-Only</span></span>

<span data-ttu-id="bf1e6-110">Nein</span><span class="sxs-lookup"><span data-stu-id="bf1e6-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="bf1e6-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="bf1e6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="bf1e6-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="bf1e6-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="bf1e6-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="bf1e6-113">Input Type</span></span>

<span data-ttu-id="bf1e6-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="bf1e6-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="bf1e6-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="bf1e6-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="bf1e6-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="bf1e6-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="bf1e6-117">Rangfolge von Pfaden (JPEG)</span><span class="sxs-lookup"><span data-stu-id="bf1e6-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="bf1e6-118">Wenn die Datei das JPEG-Format hat, werden die Daten vom Handler gelesen, geschrieben und aus folgendem Pfad entfernt:</span><span class="sxs-lookup"><span data-stu-id="bf1e6-118">If the file is in JPEG format, the handler will read, write, and remove the data from the following path:</span></span>



| <span data-ttu-id="bf1e6-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bf1e6-119">Order</span></span> | <span data-ttu-id="bf1e6-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="bf1e6-120">Path</span></span>                                   | <span data-ttu-id="bf1e6-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="bf1e6-121">Disk Format</span></span> | <span data-ttu-id="bf1e6-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="bf1e6-122">Required</span></span> |
|-------|----------------------------------------|-------------|----------|
| <span data-ttu-id="bf1e6-123">1</span><span class="sxs-lookup"><span data-stu-id="bf1e6-123">1</span></span>     | <span data-ttu-id="bf1e6-124">/XMP/MicrosoftPhoto: cameraserialnumber</span><span class="sxs-lookup"><span data-stu-id="bf1e6-124">/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="bf1e6-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="bf1e6-125">Unicode</span></span>     | <span data-ttu-id="bf1e6-126">Ja</span><span class="sxs-lookup"><span data-stu-id="bf1e6-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="bf1e6-127">Rangfolge von Pfaden (TIFF)</span><span class="sxs-lookup"><span data-stu-id="bf1e6-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="bf1e6-128">Wenn die Datei im TIFF-Format vorliegt, werden die Daten vom Handler gelesen, geschrieben und aus folgendem Pfad entfernt.</span><span class="sxs-lookup"><span data-stu-id="bf1e6-128">If the file is in TIFF format, the handler will read, write, and remove the data from the following path</span></span>



| <span data-ttu-id="bf1e6-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bf1e6-129">Order</span></span> | <span data-ttu-id="bf1e6-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="bf1e6-130">Path</span></span>                                       | <span data-ttu-id="bf1e6-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="bf1e6-131">Disk Format</span></span> | <span data-ttu-id="bf1e6-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="bf1e6-132">Required</span></span> |
|-------|--------------------------------------------|-------------|----------|
| <span data-ttu-id="bf1e6-133">1</span><span class="sxs-lookup"><span data-stu-id="bf1e6-133">1</span></span>     | <span data-ttu-id="bf1e6-134">/IFD/XMP/MicrosoftPhoto: cameraserialnumber</span><span class="sxs-lookup"><span data-stu-id="bf1e6-134">/ifd/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="bf1e6-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="bf1e6-135">Unicode</span></span>     | <span data-ttu-id="bf1e6-136">Ja</span><span class="sxs-lookup"><span data-stu-id="bf1e6-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="bf1e6-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf1e6-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf1e6-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bf1e6-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf1e6-139">System. Photo. cameraserialnumber</span><span class="sxs-lookup"><span data-stu-id="bf1e6-139">System.Photo.CameraSerialNumber</span></span>](../properties/props-system-photo-cameraserialnumber.md)
</dt> </dl>

 

 
