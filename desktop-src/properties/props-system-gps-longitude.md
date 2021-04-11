---
description: Gibt den Längengrad an.
ms.assetid: ef28141f-1b63-4694-b6df-fcc11ce7e50b
title: System. GPS. Längengrad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e65431412b0d46ad7b68100febd4d6e8efd31a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132049"
---
# <a name="systemgpslongitude"></a><span data-ttu-id="5d5a7-103">System. GPS. Längengrad</span><span class="sxs-lookup"><span data-stu-id="5d5a7-103">System.GPS.Longitude</span></span>

<span data-ttu-id="5d5a7-104">Gibt den Längengrad an.</span><span class="sxs-lookup"><span data-stu-id="5d5a7-104">Indicates the longitude.</span></span> <span data-ttu-id="5d5a7-105">Dies ist ein Array von drei Werten, wie folgt: Index 0 ist das Grad, Index 1 ist die Minuten, Index 2 ist die Sekunden.</span><span class="sxs-lookup"><span data-stu-id="5d5a7-105">This is an array of three values, as follows: Index 0 is the degrees, index 1 is the minutes, index 2 is the seconds.</span></span> <span data-ttu-id="5d5a7-106">Jede wird aus den Werten in pkey \_ GPS-Steuerelementen \_ und pkey \_ GPS \_ .</span><span class="sxs-lookup"><span data-stu-id="5d5a7-106">Each is calculated from the values in PKEY\_GPS\_LongitudeNumerator and PKEY\_GPS\_LongitudeDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="5d5a7-107">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="5d5a7-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.GPS.Longitude
   shellPKey = PKEY_GPS_Longitude
   formatID = C4C4DBB2-B593-466B-BBDA-D03D27D5E43A
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="windows-7-windows-vista"></a><span data-ttu-id="5d5a7-108">Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d5a7-108">Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.GPS.Longitude
   shellPKey = PKEY_GPS_Longitude
   formatID = C4C4DBB2-B593-466B-BBDA-D03D27D5E43A
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="5d5a7-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d5a7-109">Remarks</span></span>

<span data-ttu-id="5d5a7-110">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="5d5a7-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="5d5a7-111">Die Anforderung eines bestimmten indirekten Zeichen folgen Verweises für das `label` Attribut von **Labelinfo** wurde für Windows Vista mit Service Pack 1 (SP1) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5d5a7-111">The requirement of a specific indirect string reference for the `label` attribute of **labelInfo** was added for Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d5a7-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d5a7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d5a7-113">propertydescription</span><span class="sxs-lookup"><span data-stu-id="5d5a7-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="5d5a7-114">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="5d5a7-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="5d5a7-115">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="5d5a7-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="5d5a7-116">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="5d5a7-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="5d5a7-117">Display Info</span><span class="sxs-lookup"><span data-stu-id="5d5a7-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="5d5a7-118">StringFormat</span><span class="sxs-lookup"><span data-stu-id="5d5a7-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="5d5a7-119">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="5d5a7-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="5d5a7-120">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="5d5a7-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="5d5a7-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5d5a7-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="5d5a7-122">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="5d5a7-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="5d5a7-123">DrawControl</span><span class="sxs-lookup"><span data-stu-id="5d5a7-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="5d5a7-124">editcontrol</span><span class="sxs-lookup"><span data-stu-id="5d5a7-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="5d5a7-125">FilterControl</span><span class="sxs-lookup"><span data-stu-id="5d5a7-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="5d5a7-126">querycontrol</span><span class="sxs-lookup"><span data-stu-id="5d5a7-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
