---
description: Die fotometadatenrichtlinie für die System. Photo. Flash Manufacturer-Eigenschaft.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: System. Photo. Flash Manufacturer-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1e785dfd00662acf065021a3c80de5c587586c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050437"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a><span data-ttu-id="e9792-103">System. Photo. Flash Manufacturer-Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e9792-103">System.Photo.FlashManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="e9792-104">Die fotometadatenrichtlinie für die [System. Photo. Flash Manufacturer](../properties/props-system-photo-flashmanufacturer.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e9792-104">The photo metadata policy for the [System.Photo.FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e9792-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="e9792-105">PKEY</span></span>

<span data-ttu-id="e9792-106">Pkey \_ Photo- \_ Flash Hersteller</span><span class="sxs-lookup"><span data-stu-id="e9792-106">PKEY\_Photo\_FlashManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="e9792-107">Container</span><span class="sxs-lookup"><span data-stu-id="e9792-107">Containers</span></span>

<span data-ttu-id="e9792-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e9792-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e9792-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9792-109">Read-Only</span></span>

<span data-ttu-id="e9792-110">Nein</span><span class="sxs-lookup"><span data-stu-id="e9792-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e9792-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="e9792-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e9792-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e9792-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="e9792-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="e9792-113">Input Type</span></span>

<span data-ttu-id="e9792-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e9792-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e9792-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="e9792-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e9792-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="e9792-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="e9792-117">Rangfolge von Pfaden (JPEG)</span><span class="sxs-lookup"><span data-stu-id="e9792-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="e9792-118">Wenn die Datei im JPEG-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten den folgenden Pfad.</span><span class="sxs-lookup"><span data-stu-id="e9792-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="e9792-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e9792-119">Order</span></span> | <span data-ttu-id="e9792-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="e9792-120">Path</span></span>                                  | <span data-ttu-id="e9792-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="e9792-121">Disk Format</span></span> | <span data-ttu-id="e9792-122">Datenformat</span><span class="sxs-lookup"><span data-stu-id="e9792-122">Data Format</span></span> | <span data-ttu-id="e9792-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e9792-123">Required</span></span> |
|-------|---------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="e9792-124">1</span><span class="sxs-lookup"><span data-stu-id="e9792-124">1</span></span>     | <span data-ttu-id="e9792-125">/XMP/MicrosoftPhoto: Flash Hersteller</span><span class="sxs-lookup"><span data-stu-id="e9792-125">/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="e9792-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="e9792-126">Unicode</span></span>     |             | <span data-ttu-id="e9792-127">Ja</span><span class="sxs-lookup"><span data-stu-id="e9792-127">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="e9792-128">Rangfolge von Pfaden (TIFF)</span><span class="sxs-lookup"><span data-stu-id="e9792-128">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="e9792-129">Wenn die Datei im TIFF-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten die folgende Rangfolge.</span><span class="sxs-lookup"><span data-stu-id="e9792-129">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="e9792-130">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e9792-130">Order</span></span> | <span data-ttu-id="e9792-131">Pfad</span><span class="sxs-lookup"><span data-stu-id="e9792-131">Path</span></span>                                      | <span data-ttu-id="e9792-132">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="e9792-132">Disk Format</span></span> | <span data-ttu-id="e9792-133">Datenformat</span><span class="sxs-lookup"><span data-stu-id="e9792-133">Data Format</span></span> | <span data-ttu-id="e9792-134">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e9792-134">Required</span></span> |
|-------|-------------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="e9792-135">1</span><span class="sxs-lookup"><span data-stu-id="e9792-135">1</span></span>     | <span data-ttu-id="e9792-136">/IFD/XMP/MicrosoftPhoto: Flash Hersteller</span><span class="sxs-lookup"><span data-stu-id="e9792-136">/ifd/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="e9792-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="e9792-137">Unicode</span></span>     |             | <span data-ttu-id="e9792-138">Ja</span><span class="sxs-lookup"><span data-stu-id="e9792-138">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="e9792-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9792-139">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9792-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9792-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9792-141">System. Photo. Flash Hersteller</span><span class="sxs-lookup"><span data-stu-id="e9792-141">System.Photo.FlashManufacturer</span></span>](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
