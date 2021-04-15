---
description: Gibt die Breite an.
ms.assetid: f36f81b3-4e3d-4e06-a039-c243fd69c937
title: System. GPS. Latitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996c0edf41e03bc7f4a824ae9ed812450eb36e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527371"
---
# <a name="systemgpslatitude"></a><span data-ttu-id="0765a-103">System. GPS. Latitude</span><span class="sxs-lookup"><span data-stu-id="0765a-103">System.GPS.Latitude</span></span>

<span data-ttu-id="0765a-104">Gibt die Breite an.</span><span class="sxs-lookup"><span data-stu-id="0765a-104">Indicates latitude.</span></span> <span data-ttu-id="0765a-105">Dies ist ein Array von drei Werten, wie folgt: Index 0 ist das Grad, Index 1 ist die Minuten, Index 2 ist die Sekunden.</span><span class="sxs-lookup"><span data-stu-id="0765a-105">This is an array of three values, as follows: index 0 is the degrees, index 1 is the minutes, index 2 is the seconds.</span></span> <span data-ttu-id="0765a-106">Jede wird aus den Werten in pkey \_ GPS " \_ breiten-umerator" und "pkey \_ GPS \_ latitudinenner" berechnet.</span><span class="sxs-lookup"><span data-stu-id="0765a-106">Each is calculated from the values in PKEY\_GPS\_LatitudeNumerator and PKEY\_GPS\_LatitudeDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="0765a-107">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="0765a-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.GPS.Latitude
   shellPKey = PKEY_GPS_Latitude
   formatID = 8727CFFF-4868-4EC6-AD5B-81B98521D1AB
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="windows-7-windows-vista"></a><span data-ttu-id="0765a-108">Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0765a-108">Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.GPS.Latitude
   shellPKey = PKEY_GPS_Latitude
   formatID = 8727CFFF-4868-4EC6-AD5B-81B98521D1AB
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="0765a-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0765a-109">Remarks</span></span>

<span data-ttu-id="0765a-110">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="0765a-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="0765a-111">Die Anforderung eines bestimmten indirekten Zeichen folgen Verweises für das `label` Attribut von **Labelinfo** wurde für Windows Vista mit Service Pack 1 (SP1) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0765a-111">The requirement of a specific indirect string reference for the `label` attribute of **labelInfo** was added for Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0765a-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0765a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0765a-113">propertydescription</span><span class="sxs-lookup"><span data-stu-id="0765a-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="0765a-114">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="0765a-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="0765a-115">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="0765a-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="0765a-116">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="0765a-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="0765a-117">Display Info</span><span class="sxs-lookup"><span data-stu-id="0765a-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="0765a-118">StringFormat</span><span class="sxs-lookup"><span data-stu-id="0765a-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="0765a-119">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="0765a-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="0765a-120">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="0765a-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="0765a-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0765a-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="0765a-122">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="0765a-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="0765a-123">DrawControl</span><span class="sxs-lookup"><span data-stu-id="0765a-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="0765a-124">editcontrol</span><span class="sxs-lookup"><span data-stu-id="0765a-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="0765a-125">FilterControl</span><span class="sxs-lookup"><span data-stu-id="0765a-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="0765a-126">querycontrol</span><span class="sxs-lookup"><span data-stu-id="0765a-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
