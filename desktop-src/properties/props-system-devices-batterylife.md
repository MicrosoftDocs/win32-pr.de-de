---
description: Verbleibende Akku Lebensdauer in Prozent.
ms.assetid: b6f4f5d6-7f12-4104-95ad-b163445d198b
title: System.Devices.Batterylife
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe8f24f5ecaa78231fdc463b718046adc42fc681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368928"
---
# <a name="systemdevicesbatterylife"></a><span data-ttu-id="a08a8-103">System.Devices.Batterylife</span><span class="sxs-lookup"><span data-stu-id="a08a8-103">System.Devices.BatteryLife</span></span>

<span data-ttu-id="a08a8-104">Verbleibende Akku Lebensdauer in Prozent.</span><span class="sxs-lookup"><span data-stu-id="a08a8-104">Remaining battery life, as a percentage.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="a08a8-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="a08a8-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Devices.BatteryLife
   shellPKey = PKEY_Devices_BatteryLife
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 10
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = CriticallyLow
            minValue = 0
            setValue = 5
            text = Critically low battery
            defineToken = BATTERYLIFE_CRITICALLY_LOW
         enumRange
            name = Low
            minValue = 11
            setValue = 18
            text = Low battery
            defineToken = BATTERYLIFE_LOW
         enumRange
            name = Average
            minValue = 26
            setValue = 60
            text = Average battery
            defineToken = BATTERYLIFE_AVERAGE
         enumRange
            name = Full
            minValue = 90
            setValue = 95
            text = Full battery
            defineToken = BATTERYLIFE_FULL
         enumRange
            name = UnknownStatus
            minValue = 101
            setValue = 101
            text = Unknown battery status
            defineToken = BATTERYLIFE_UNKNOWN_STATUS
```

## <a name="remarks"></a><span data-ttu-id="a08a8-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a08a8-106">Remarks</span></span>

<span data-ttu-id="a08a8-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="a08a8-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a08a8-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a08a8-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a08a8-109">propertydescription</span><span class="sxs-lookup"><span data-stu-id="a08a8-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a08a8-110">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="a08a8-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a08a8-111">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="a08a8-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a08a8-112">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="a08a8-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a08a8-113">Display Info</span><span class="sxs-lookup"><span data-stu-id="a08a8-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a08a8-114">StringFormat</span><span class="sxs-lookup"><span data-stu-id="a08a8-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a08a8-115">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="a08a8-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a08a8-116">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="a08a8-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a08a8-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a08a8-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a08a8-118">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="a08a8-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a08a8-119">DrawControl</span><span class="sxs-lookup"><span data-stu-id="a08a8-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a08a8-120">editcontrol</span><span class="sxs-lookup"><span data-stu-id="a08a8-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a08a8-121">FilterControl</span><span class="sxs-lookup"><span data-stu-id="a08a8-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a08a8-122">querycontrol</span><span class="sxs-lookup"><span data-stu-id="a08a8-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
