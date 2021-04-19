---
description: Der Helligkeitswert des Bilds (in Spitze Einheiten) in der Regel im Bereich von-99,99 bis 99,99.
ms.assetid: 533f6934-dec8-455a-937c-d4e144be4335
title: System. Photo. Helligkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131b7e2d51f402aa8da4d5e9b266fe1fc1b39b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360228"
---
# <a name="systemphotobrightness"></a><span data-ttu-id="78a18-103">System. Photo. Helligkeit</span><span class="sxs-lookup"><span data-stu-id="78a18-103">System.Photo.Brightness</span></span>

<span data-ttu-id="78a18-104">Der Helligkeitswert des Bilds (in Spitze Einheiten) in der Regel im Bereich von-99,99 bis 99,99.</span><span class="sxs-lookup"><span data-stu-id="78a18-104">The brightness value of the image, in APEX units, usually in the range of -99.99 to 99.99.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="78a18-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78a18-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Brightness
   shellPKey = PKEY_Photo_Brightness
   formatID = 1A701BF6-478C-4361-83AB-3701BB053C58
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="78a18-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78a18-106">Remarks</span></span>

<span data-ttu-id="78a18-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="78a18-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="78a18-108">Einen Vergleich von [System. Photo. Helligkeit]() -Zahlen und Foot-Lambert Messungen finden Sie in der EXIF 2,2-Spezifikation, Anhang C.</span><span class="sxs-lookup"><span data-stu-id="78a18-108">See the EXIF 2.2 specification, Annex C, for a comparison of [System.Photo.Brightness]() numbers and Foot-Lambert measurements.</span></span> <span data-ttu-id="78a18-109">Diese Eigenschaft wird aus [System. Photo. brightnessnumerator](./props-system-photo-brightnessnumerator.md) und [System. Photo. brightnessnenner](./props-system-photo-brightnessdenominator.md)berechnet.</span><span class="sxs-lookup"><span data-stu-id="78a18-109">This property is calculated from [System.Photo.BrightnessNumerator](./props-system-photo-brightnessnumerator.md) and [System.Photo.BrightnessDenominator](./props-system-photo-brightnessdenominator.md).</span></span> <span data-ttu-id="78a18-110">, Wenn der Zähler des aufgezeichneten Werts FFFFFFFF ist. H, "unknown", sollte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="78a18-110">If the numerator of the recorded value is FFFFFFFF.H, "Unknown" should be indicated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78a18-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78a18-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78a18-112">Exchangeable Image File Format für digitale Kameras: EXIF Version 2,2</span><span class="sxs-lookup"><span data-stu-id="78a18-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="78a18-113">propertydescription</span><span class="sxs-lookup"><span data-stu-id="78a18-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="78a18-114">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="78a18-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="78a18-115">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="78a18-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="78a18-116">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="78a18-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="78a18-117">Display Info</span><span class="sxs-lookup"><span data-stu-id="78a18-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="78a18-118">StringFormat</span><span class="sxs-lookup"><span data-stu-id="78a18-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="78a18-119">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="78a18-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="78a18-120">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="78a18-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="78a18-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="78a18-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="78a18-122">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="78a18-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="78a18-123">DrawControl</span><span class="sxs-lookup"><span data-stu-id="78a18-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="78a18-124">editcontrol</span><span class="sxs-lookup"><span data-stu-id="78a18-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="78a18-125">FilterControl</span><span class="sxs-lookup"><span data-stu-id="78a18-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="78a18-126">querycontrol</span><span class="sxs-lookup"><span data-stu-id="78a18-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
