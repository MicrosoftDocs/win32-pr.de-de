---
description: Die fotometadatenrichtlinie für die System. Photo. lensmodel-Eigenschaft.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: System. Photo. lensmodel-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a5249136346407ab9fcd1e4802d6910d3e514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050298"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a><span data-ttu-id="36bc3-103">System. Photo. lensmodel-fotometadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="36bc3-103">System.Photo.LensModel Photo Metadata Policy</span></span>

<span data-ttu-id="36bc3-104">Die fotometadatenrichtlinie für die [System. Photo. lensmodel](../properties/props-system-photo-lensmodel.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="36bc3-104">The photo metadata policy for the [System.Photo.LensModel](../properties/props-system-photo-lensmodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="36bc3-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="36bc3-105">PKEY</span></span>

<span data-ttu-id="36bc3-106">Pkey- \_ Foto \_ lensmodel</span><span class="sxs-lookup"><span data-stu-id="36bc3-106">PKEY\_Photo\_LensModel</span></span>

### <a name="containers"></a><span data-ttu-id="36bc3-107">Container</span><span class="sxs-lookup"><span data-stu-id="36bc3-107">Containers</span></span>

<span data-ttu-id="36bc3-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="36bc3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="36bc3-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36bc3-109">Read-Only</span></span>

<span data-ttu-id="36bc3-110">Nein</span><span class="sxs-lookup"><span data-stu-id="36bc3-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="36bc3-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="36bc3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="36bc3-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="36bc3-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="36bc3-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="36bc3-113">Input Type</span></span>

<span data-ttu-id="36bc3-114">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="36bc3-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="36bc3-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="36bc3-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="36bc3-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="36bc3-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="36bc3-117">Rangfolge von Pfaden (JPEG)</span><span class="sxs-lookup"><span data-stu-id="36bc3-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="36bc3-118">Wenn die Datei im JPEG-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten den folgenden Pfad.</span><span class="sxs-lookup"><span data-stu-id="36bc3-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="36bc3-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="36bc3-119">Order</span></span> | <span data-ttu-id="36bc3-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="36bc3-120">Path</span></span>                          | <span data-ttu-id="36bc3-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="36bc3-121">Disk Format</span></span> | <span data-ttu-id="36bc3-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="36bc3-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="36bc3-123">1</span><span class="sxs-lookup"><span data-stu-id="36bc3-123">1</span></span>     | <span data-ttu-id="36bc3-124">/XMP/MicrosoftPhoto: lensmodel</span><span class="sxs-lookup"><span data-stu-id="36bc3-124">/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="36bc3-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="36bc3-125">Unicode</span></span>     | <span data-ttu-id="36bc3-126">Ja</span><span class="sxs-lookup"><span data-stu-id="36bc3-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="36bc3-127">Rangfolge von Pfaden (TIFF)</span><span class="sxs-lookup"><span data-stu-id="36bc3-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="36bc3-128">Wenn die Datei im TIFF-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten die folgende Rangfolge.</span><span class="sxs-lookup"><span data-stu-id="36bc3-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="36bc3-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="36bc3-129">Order</span></span> | <span data-ttu-id="36bc3-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="36bc3-130">Path</span></span>                              | <span data-ttu-id="36bc3-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="36bc3-131">Disk Format</span></span> | <span data-ttu-id="36bc3-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="36bc3-132">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="36bc3-133">1</span><span class="sxs-lookup"><span data-stu-id="36bc3-133">1</span></span>     | <span data-ttu-id="36bc3-134">/IFD/XMP/MicrosoftPhoto: lensmodel</span><span class="sxs-lookup"><span data-stu-id="36bc3-134">/ifd/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="36bc3-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="36bc3-135">Unicode</span></span>     | <span data-ttu-id="36bc3-136">Ja</span><span class="sxs-lookup"><span data-stu-id="36bc3-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="36bc3-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36bc3-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="36bc3-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36bc3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36bc3-139">System. Photo. lensmodel</span><span class="sxs-lookup"><span data-stu-id="36bc3-139">System.Photo.LensModel</span></span>](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
