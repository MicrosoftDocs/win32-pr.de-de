---
description: Die fotometadatenrichtlinie für die System. Photo. Flash Model-Eigenschaft.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: System. Photo. Flash Model-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ade3769cb0d852239af84b769b85d5b3849589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362332"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a><span data-ttu-id="56d0b-103">System. Photo. Flash Model-fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="56d0b-103">System.Photo.FlashModel Photo Metadata Policy</span></span>

<span data-ttu-id="56d0b-104">Die fotometadatenrichtlinie für die [System. Photo. Flash Model](../properties/props-system-photo-flashmodel.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="56d0b-104">The photo metadata policy for the [System.Photo.FlashModel](../properties/props-system-photo-flashmodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="56d0b-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="56d0b-105">PKEY</span></span>

<span data-ttu-id="56d0b-106">Pkey- \_ Foto- \_ Flash Modell</span><span class="sxs-lookup"><span data-stu-id="56d0b-106">PKEY\_Photo\_FlashModel</span></span>

### <a name="containers"></a><span data-ttu-id="56d0b-107">Container</span><span class="sxs-lookup"><span data-stu-id="56d0b-107">Containers</span></span>

<span data-ttu-id="56d0b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="56d0b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="56d0b-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="56d0b-109">Read-Only</span></span>

<span data-ttu-id="56d0b-110">Nein</span><span class="sxs-lookup"><span data-stu-id="56d0b-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="56d0b-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="56d0b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="56d0b-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="56d0b-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="56d0b-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="56d0b-113">Input Type</span></span>

<span data-ttu-id="56d0b-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="56d0b-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="56d0b-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="56d0b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="56d0b-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="56d0b-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="56d0b-117">Rangfolge von Pfaden (JPEG)</span><span class="sxs-lookup"><span data-stu-id="56d0b-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="56d0b-118">Wenn die Datei im JPEG-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten den folgenden Pfad.</span><span class="sxs-lookup"><span data-stu-id="56d0b-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="56d0b-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="56d0b-119">Order</span></span> | <span data-ttu-id="56d0b-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="56d0b-120">Path</span></span>                           | <span data-ttu-id="56d0b-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="56d0b-121">Disk Format</span></span> | <span data-ttu-id="56d0b-122">Datenformat</span><span class="sxs-lookup"><span data-stu-id="56d0b-122">Data Format</span></span> | <span data-ttu-id="56d0b-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56d0b-123">Required</span></span> |
|-------|--------------------------------|-------------|-------------|----------|
| <span data-ttu-id="56d0b-124">1</span><span class="sxs-lookup"><span data-stu-id="56d0b-124">1</span></span>     | <span data-ttu-id="56d0b-125">/XMP/MicrosoftPhoto: Flash Model</span><span class="sxs-lookup"><span data-stu-id="56d0b-125">/xmp/MicrosoftPhoto:FlashModel</span></span> | <span data-ttu-id="56d0b-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="56d0b-126">Unicode</span></span>     |             | <span data-ttu-id="56d0b-127">Ja</span><span class="sxs-lookup"><span data-stu-id="56d0b-127">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="56d0b-128">Rangfolge von Pfaden (TIFF)</span><span class="sxs-lookup"><span data-stu-id="56d0b-128">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="56d0b-129">Wenn die Datei im TIFF-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten die folgende Rangfolge.</span><span class="sxs-lookup"><span data-stu-id="56d0b-129">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="56d0b-130">Auftrag</span><span class="sxs-lookup"><span data-stu-id="56d0b-130">Order</span></span> | <span data-ttu-id="56d0b-131">Pfad</span><span class="sxs-lookup"><span data-stu-id="56d0b-131">Path</span></span>                               | <span data-ttu-id="56d0b-132">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="56d0b-132">Disk Format</span></span> | <span data-ttu-id="56d0b-133">Datenformat</span><span class="sxs-lookup"><span data-stu-id="56d0b-133">Data Format</span></span> | <span data-ttu-id="56d0b-134">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56d0b-134">Required</span></span> |
|-------|------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="56d0b-135">1</span><span class="sxs-lookup"><span data-stu-id="56d0b-135">1</span></span>     | <span data-ttu-id="56d0b-136">/IFD/XMP/MicrosoftPhoto: Flash Model</span><span class="sxs-lookup"><span data-stu-id="56d0b-136">/ifd/xmp/MicrosoftPhoto:FlashModel</span></span> | <span data-ttu-id="56d0b-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="56d0b-137">Unicode</span></span>     |             | <span data-ttu-id="56d0b-138">Ja</span><span class="sxs-lookup"><span data-stu-id="56d0b-138">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="56d0b-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56d0b-139">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="56d0b-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56d0b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56d0b-141">System. Photo. Flash Model</span><span class="sxs-lookup"><span data-stu-id="56d0b-141">System.Photo.FlashModel</span></span>](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
