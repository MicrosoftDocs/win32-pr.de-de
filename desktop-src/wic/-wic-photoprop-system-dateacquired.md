---
description: Die fotometadatenrichtlinie für die System. dateerworgenschaft.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: System. dateerworbenes Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218034"
---
# <a name="systemdateacquired-photo-metadata-policy"></a><span data-ttu-id="85d5d-103">System. dateerworbenes Foto-metadatenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="85d5d-103">System.DateAcquired Photo Metadata Policy</span></span>

<span data-ttu-id="85d5d-104">Die fotometadatenrichtlinie für die [System. dateerworgenschaft](../properties/props-system-dateacquired.md) .</span><span class="sxs-lookup"><span data-stu-id="85d5d-104">The photo metadata policy for the [System.DateAcquired](../properties/props-system-dateacquired.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="85d5d-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="85d5d-105">PKEY</span></span>

<span data-ttu-id="85d5d-106">Pkey- \_ datebezogen</span><span class="sxs-lookup"><span data-stu-id="85d5d-106">PKEY\_DateAcquired</span></span>

### <a name="containers"></a><span data-ttu-id="85d5d-107">Container</span><span class="sxs-lookup"><span data-stu-id="85d5d-107">Containers</span></span>

<span data-ttu-id="85d5d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="85d5d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="85d5d-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85d5d-109">Read-Only</span></span>

<span data-ttu-id="85d5d-110">Nein</span><span class="sxs-lookup"><span data-stu-id="85d5d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="85d5d-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="85d5d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="85d5d-112">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="85d5d-112">VT\_FILETIME</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="85d5d-113">Eingabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="85d5d-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="85d5d-114">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="85d5d-114">VT\_FILETIME</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="85d5d-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="85d5d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="85d5d-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="85d5d-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="85d5d-117">Rangfolge von Pfaden (JPEG)</span><span class="sxs-lookup"><span data-stu-id="85d5d-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="85d5d-118">Wenn die Datei im JPEG-Format vorliegt, sucht der Handler in der folgenden Reihenfolge nach den Daten:</span><span class="sxs-lookup"><span data-stu-id="85d5d-118">If the file is in JPEG format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="85d5d-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="85d5d-119">Order</span></span> | <span data-ttu-id="85d5d-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="85d5d-120">Path</span></span>                             | <span data-ttu-id="85d5d-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="85d5d-121">Disk Format</span></span>                        | <span data-ttu-id="85d5d-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="85d5d-122">Required</span></span> |
|-------|----------------------------------|------------------------------------|----------|
| <span data-ttu-id="85d5d-123">1</span><span class="sxs-lookup"><span data-stu-id="85d5d-123">1</span></span>     | <span data-ttu-id="85d5d-124">/XMP/MicrosoftPhoto: dateerworbener</span><span class="sxs-lookup"><span data-stu-id="85d5d-124">/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="85d5d-125">Unicode-Zeichenfolge im XMP-Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="85d5d-125">Unicode string in XMP date format.</span></span> | <span data-ttu-id="85d5d-126">Ja</span><span class="sxs-lookup"><span data-stu-id="85d5d-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="85d5d-127">Rangfolge von Pfaden (TIFF)</span><span class="sxs-lookup"><span data-stu-id="85d5d-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="85d5d-128">Wenn die Datei im TIFF-Format vorliegt, sucht der Handler in der folgenden Reihenfolge nach den Daten:</span><span class="sxs-lookup"><span data-stu-id="85d5d-128">If the file is in TIFF format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="85d5d-129">Auftrag</span><span class="sxs-lookup"><span data-stu-id="85d5d-129">Order</span></span> | <span data-ttu-id="85d5d-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="85d5d-130">Path</span></span>                                 | <span data-ttu-id="85d5d-131">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="85d5d-131">Disk Format</span></span>                        | <span data-ttu-id="85d5d-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="85d5d-132">Required</span></span> |
|-------|--------------------------------------|------------------------------------|----------|
| <span data-ttu-id="85d5d-133">1</span><span class="sxs-lookup"><span data-stu-id="85d5d-133">1</span></span>     | <span data-ttu-id="85d5d-134">/IFD/XMP/MicrosoftPhoto: dateerworbener</span><span class="sxs-lookup"><span data-stu-id="85d5d-134">/ifd/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="85d5d-135">Unicode-Zeichenfolge im XMP-Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="85d5d-135">Unicode string in XMP date format.</span></span> | <span data-ttu-id="85d5d-136">Ja</span><span class="sxs-lookup"><span data-stu-id="85d5d-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="85d5d-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85d5d-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="85d5d-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="85d5d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85d5d-139">System. dateerworbener</span><span class="sxs-lookup"><span data-stu-id="85d5d-139">System.DateAcquired</span></span>](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
