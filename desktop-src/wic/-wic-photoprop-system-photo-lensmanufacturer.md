---
description: Die fotometadatenrichtlinie für die System. Photo. lensmanufacturer-Eigenschaft.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: System. Photo. lensmanufacturer-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6696e7113a14a9b5b26a26f38258f30a5ba82cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217382"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a><span data-ttu-id="8f023-103">System. Photo. lensmanufacturer-fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="8f023-103">System.Photo.LensManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="8f023-104">Die fotometadatenrichtlinie für die [System. Photo. lensmanufacturer](../properties/props-system-photo-lensmanufacturer.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8f023-104">The photo metadata policy for the [System.Photo.LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8f023-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="8f023-105">PKEY</span></span>

<span data-ttu-id="8f023-106">Pkey- \_ Foto \_ lensmanufacturer</span><span class="sxs-lookup"><span data-stu-id="8f023-106">PKEY\_Photo\_LensManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="8f023-107">Container</span><span class="sxs-lookup"><span data-stu-id="8f023-107">Containers</span></span>

<span data-ttu-id="8f023-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="8f023-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8f023-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f023-109">Read-Only</span></span>

<span data-ttu-id="8f023-110">Nein</span><span class="sxs-lookup"><span data-stu-id="8f023-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8f023-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="8f023-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8f023-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="8f023-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="8f023-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="8f023-113">Input Type</span></span>

<span data-ttu-id="8f023-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8f023-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8f023-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="8f023-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="8f023-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="8f023-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="8f023-117">Rangfolge von Pfaden (JPEG)</span><span class="sxs-lookup"><span data-stu-id="8f023-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="8f023-118">Wenn die Datei im JPEG-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten den folgenden Pfad.</span><span class="sxs-lookup"><span data-stu-id="8f023-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="8f023-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="8f023-119">Order</span></span> | <span data-ttu-id="8f023-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="8f023-120">Path</span></span>                                 | <span data-ttu-id="8f023-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="8f023-121">Disk Format</span></span> | <span data-ttu-id="8f023-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8f023-122">Required</span></span> |
|-------|--------------------------------------|-------------|----------|
| <span data-ttu-id="8f023-123">1</span><span class="sxs-lookup"><span data-stu-id="8f023-123">1</span></span>     | <span data-ttu-id="8f023-124">/XMP/MicrosoftPhoto: lensmanufacturer</span><span class="sxs-lookup"><span data-stu-id="8f023-124">/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="8f023-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="8f023-125">Unicode</span></span>     | <span data-ttu-id="8f023-126">Ja</span><span class="sxs-lookup"><span data-stu-id="8f023-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="8f023-127">Rangfolge von Pfaden (TIFF)</span><span class="sxs-lookup"><span data-stu-id="8f023-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="8f023-128">Wenn die Datei im TIFF-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten die folgende Rangfolge.</span><span class="sxs-lookup"><span data-stu-id="8f023-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="8f023-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="8f023-129">Order</span></span> | <span data-ttu-id="8f023-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="8f023-130">Path</span></span>                                     | <span data-ttu-id="8f023-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="8f023-131">Disk Format</span></span> | <span data-ttu-id="8f023-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8f023-132">Required</span></span> |
|-------|------------------------------------------|-------------|----------|
| <span data-ttu-id="8f023-133">1</span><span class="sxs-lookup"><span data-stu-id="8f023-133">1</span></span>     | <span data-ttu-id="8f023-134">/IFD/XMP/MicrosoftPhoto: lensmanufacturer</span><span class="sxs-lookup"><span data-stu-id="8f023-134">/ifd/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="8f023-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="8f023-135">Unicode</span></span>     | <span data-ttu-id="8f023-136">Ja</span><span class="sxs-lookup"><span data-stu-id="8f023-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="8f023-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f023-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f023-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f023-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f023-139">System. Photo. lensmanufacturer</span><span class="sxs-lookup"><span data-stu-id="8f023-139">System.Photo.LensManufacturer</span></span>](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
