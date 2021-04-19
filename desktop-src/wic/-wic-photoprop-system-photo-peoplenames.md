---
description: Die fotometadatenrichtlinie für die System. Photo. peoplenames-Eigenschaft.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: System. Photo. People Ames Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3de9f5adda67fcd0e555194500f109df078bdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360724"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a><span data-ttu-id="4180c-103">System. Photo. People Ames Photo Metadata-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="4180c-103">System.Photo.PeopleNames Photo Metadata Policy</span></span>

<span data-ttu-id="4180c-104">Die fotometadatenrichtlinie für die [System. Photo. peoplenames](../properties/props-system-photo-peoplenames.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4180c-104">The photo metadata policy for the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4180c-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="4180c-105">PKEY</span></span>

<span data-ttu-id="4180c-106">Pkey- \_ Foto \_ People Ames</span><span class="sxs-lookup"><span data-stu-id="4180c-106">PKEY\_Photo\_PeopleNames</span></span>

### <a name="containers"></a><span data-ttu-id="4180c-107">Container</span><span class="sxs-lookup"><span data-stu-id="4180c-107">Containers</span></span>

<span data-ttu-id="4180c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4180c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4180c-109">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4180c-109">Read-Only</span></span>

<span data-ttu-id="4180c-110">Nein</span><span class="sxs-lookup"><span data-stu-id="4180c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4180c-111">Ausgabe-PROPVARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="4180c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4180c-112">VT \_ Vector \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="4180c-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="4180c-113">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="4180c-113">Input Type</span></span>

<span data-ttu-id="4180c-114">Stringmulti</span><span class="sxs-lookup"><span data-stu-id="4180c-114">StringMulti</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4180c-115">Richtlinie zur Konfliktlösung</span><span class="sxs-lookup"><span data-stu-id="4180c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="4180c-116">Werte aus unterschiedlichen Schemas sind abgestimmt.</span><span class="sxs-lookup"><span data-stu-id="4180c-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4180c-117">JPEG-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="4180c-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4180c-118">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="4180c-118">Read Paths</span></span>



| <span data-ttu-id="4180c-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4180c-119">Order</span></span> | <span data-ttu-id="4180c-120">Pfad</span><span class="sxs-lookup"><span data-stu-id="4180c-120">Path</span></span>                                                           | <span data-ttu-id="4180c-121">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="4180c-121">Disk Format</span></span> |
|-------|----------------------------------------------------------------|-------------|
| <span data-ttu-id="4180c-122">1</span><span class="sxs-lookup"><span data-stu-id="4180c-122">1</span></span>     | <span data-ttu-id="4180c-123">/XMP/ <xmpstruct> MP: RegionInfo/ <xmpbag> MPRI: Regionen</span><span class="sxs-lookup"><span data-stu-id="4180c-123">/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions</span></span> | <span data-ttu-id="4180c-124">ushort</span><span class="sxs-lookup"><span data-stu-id="4180c-124">ushort</span></span>      |



 

### <a name="write-paths"></a><span data-ttu-id="4180c-125">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="4180c-125">Write Paths</span></span>

<span data-ttu-id="4180c-126">Diese Eigenschaft kann nicht mithilfe der metadatenrichtlinie geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4180c-126">This property cannot be written using the metadata policy.</span></span>

### <a name="remove-paths"></a><span data-ttu-id="4180c-127">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="4180c-127">Remove Paths</span></span>



| <span data-ttu-id="4180c-128">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4180c-128">Order</span></span> | <span data-ttu-id="4180c-129">Pfad</span><span class="sxs-lookup"><span data-stu-id="4180c-129">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="4180c-130">1</span><span class="sxs-lookup"><span data-stu-id="4180c-130">1</span></span>     | <span data-ttu-id="4180c-131">/XMP/ <xmpstruct> MP: RegionInfo</span><span class="sxs-lookup"><span data-stu-id="4180c-131">/xmp/<xmpstruct>MP:RegionInfo</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="4180c-132">TIFF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="4180c-132">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4180c-133">Pfade lesen</span><span class="sxs-lookup"><span data-stu-id="4180c-133">Read Paths</span></span>



| <span data-ttu-id="4180c-134">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4180c-134">Order</span></span> | <span data-ttu-id="4180c-135">Pfad</span><span class="sxs-lookup"><span data-stu-id="4180c-135">Path</span></span>                                                               | <span data-ttu-id="4180c-136">Datenträger Format</span><span class="sxs-lookup"><span data-stu-id="4180c-136">Disk Format</span></span> |
|-------|--------------------------------------------------------------------|-------------|
| <span data-ttu-id="4180c-137">1</span><span class="sxs-lookup"><span data-stu-id="4180c-137">1</span></span>     | <span data-ttu-id="4180c-138">/IFD/XMP/ <xmpstruct> MP: RegionInfo/ <xmpbag> MPRI: Regionen</span><span class="sxs-lookup"><span data-stu-id="4180c-138">/ifd/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions</span></span> | <span data-ttu-id="4180c-139">ushort</span><span class="sxs-lookup"><span data-stu-id="4180c-139">ushort</span></span>      |



 

### <a name="write-paths"></a><span data-ttu-id="4180c-140">Schreib Pfade</span><span class="sxs-lookup"><span data-stu-id="4180c-140">Write Paths</span></span>

<span data-ttu-id="4180c-141">Diese Eigenschaft kann nicht mithilfe der metadatenrichtlinie geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4180c-141">This property cannot be written using the metadata policy.</span></span>

### <a name="remove-paths"></a><span data-ttu-id="4180c-142">Pfade entfernen</span><span class="sxs-lookup"><span data-stu-id="4180c-142">Remove Paths</span></span>



| <span data-ttu-id="4180c-143">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4180c-143">Order</span></span> | <span data-ttu-id="4180c-144">Pfad</span><span class="sxs-lookup"><span data-stu-id="4180c-144">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="4180c-145">1</span><span class="sxs-lookup"><span data-stu-id="4180c-145">1</span></span>     | <span data-ttu-id="4180c-146">/IFD/XMP/ <xmpstruct> MP: RegionInfo</span><span class="sxs-lookup"><span data-stu-id="4180c-146">/ifd/xmp/<xmpstruct>MP:RegionInfo</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4180c-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4180c-147">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4180c-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4180c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4180c-149">System. Photo. Program Mode</span><span class="sxs-lookup"><span data-stu-id="4180c-149">System.Photo.ProgramMode</span></span>](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
