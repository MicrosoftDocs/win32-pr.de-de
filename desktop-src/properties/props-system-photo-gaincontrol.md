---
description: Gibt den Grad der Gesamt Anpassung des Bild Abbilds an. Berechnet aus pkey \_ Photo \_ gaincontrolnumerator und pkey \_ Photo \_ gaincontrolnenner.
ms.assetid: 5076e03b-2c8a-4ef4-93d6-271a4bd697a6
title: System. Photo. gaincontrol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8278120e5e65137eda491f52af7bc36f1c163c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959570"
---
# <a name="systemphotogaincontrol"></a><span data-ttu-id="31c8e-104">System. Photo. gaincontrol</span><span class="sxs-lookup"><span data-stu-id="31c8e-104">System.Photo.GainControl</span></span>

<span data-ttu-id="31c8e-105">Gibt den Grad der Gesamt Anpassung des Bild Abbilds an.</span><span class="sxs-lookup"><span data-stu-id="31c8e-105">Indicates the degree of overall image gain adjustment.</span></span> <span data-ttu-id="31c8e-106">Berechnet aus pkey \_ Photo \_ gaincontrolnumerator und pkey \_ Photo \_ gaincontrolnenner.</span><span class="sxs-lookup"><span data-stu-id="31c8e-106">Calculated from PKEY\_Photo\_GainControlNumerator and PKEY\_Photo\_GainControlDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="31c8e-107">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="31c8e-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.GainControl
   shellPKey = PKEY_Photo_GainControl
   formatID = FA304789-00C7-4D80-904A-1E4DCC7265AA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = None
            value = 0.0
            text = None
            defineToken = PHOTO_GAINCONTROL_NONE
         enum
            name = LowGainUp
            value = 1.0
            text = Low gain up
            defineToken = PHOTO_GAINCONTROL_LOWGAINUP
         enum
            name = HighGainUp
            value = 2.0
            text = High gain up
            defineToken = PHOTO_GAINCONTROL_HIGHGAINUP
         enum
            name = LowGainDown
            value = 3.0
            text = Low gain down
            defineToken = PHOTO_GAINCONTROL_LOWGAINDOWN
         enum
            name = HighGainDown
            value = 4.0
            text = High gain down
            defineToken = PHOTO_GAINCONTROL_HIGHGAINDOWN
```

## <a name="windows-vista"></a><span data-ttu-id="31c8e-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31c8e-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.GainControl
   shellPKey = PKEY_Photo_GainControl
   formatID = FA304789-00C7-4D80-904A-1E4DCC7265AA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0.0
            text = None
            defineName = PHOTO_GAINCONTROL_NONE
         enum
            value = 1.0
            text = Low gain up
            defineName = PHOTO_GAINCONTROL_LOWGAINUP
         enum
            value = 2.0
            text = High gain up
            defineName = PHOTO_GAINCONTROL_HIGHGAINUP
         enum
            value = 3.0
            text = Low gain down
            defineName = PHOTO_GAINCONTROL_LOWGAINDOWN
         enum
            value = 4.0
            text = High gain down
            defineName = PHOTO_GAINCONTROL_HIGHGAINDOWN
```

## <a name="remarks"></a><span data-ttu-id="31c8e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31c8e-109">Remarks</span></span>

<span data-ttu-id="31c8e-110">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="31c8e-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31c8e-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="31c8e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31c8e-112">propertydescription</span><span class="sxs-lookup"><span data-stu-id="31c8e-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="31c8e-113">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="31c8e-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="31c8e-114">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="31c8e-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="31c8e-115">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="31c8e-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="31c8e-116">Display Info</span><span class="sxs-lookup"><span data-stu-id="31c8e-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="31c8e-117">StringFormat</span><span class="sxs-lookup"><span data-stu-id="31c8e-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="31c8e-118">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="31c8e-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="31c8e-119">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="31c8e-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="31c8e-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="31c8e-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="31c8e-121">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="31c8e-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="31c8e-122">DrawControl</span><span class="sxs-lookup"><span data-stu-id="31c8e-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="31c8e-123">editcontrol</span><span class="sxs-lookup"><span data-stu-id="31c8e-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="31c8e-124">FilterControl</span><span class="sxs-lookup"><span data-stu-id="31c8e-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="31c8e-125">querycontrol</span><span class="sxs-lookup"><span data-stu-id="31c8e-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
