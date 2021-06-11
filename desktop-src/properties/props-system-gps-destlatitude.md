---
description: Erfahren Sie, wie die System.GPS.DestL persistent -Eigenschaft den Breitengrad des Zielpunkts angibt.
ms.assetid: 63d8a3a3-76ec-4121-b48b-eb5034117d04
title: System.GPS.DestL persistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbed51e89926b8bb505457bd9fd7bf7bd3b69ff2
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988965"
---
# <a name="systemgpsdestlatitude"></a><span data-ttu-id="73e00-103">System.GPS.DestL persistent</span><span class="sxs-lookup"><span data-stu-id="73e00-103">System.GPS.DestLatitude</span></span>

<span data-ttu-id="73e00-104">Gibt den Breitengrad des Zielpunkts an.</span><span class="sxs-lookup"><span data-stu-id="73e00-104">Indicates the latitude of the destination point.</span></span> <span data-ttu-id="73e00-105">Dies ist ein Array von drei Werten: Index 0 ist der Grad, Index 1 ist die Minuten, Index 2 die Sekunden.</span><span class="sxs-lookup"><span data-stu-id="73e00-105">This is an array of three values, as follows: index 0 is the degrees, index 1 is the minutes, index 2 is the seconds.</span></span> <span data-ttu-id="73e00-106">Jede wird anhand der Werte in PKEY \_ GPS \_ DestLatorsNumerator und PKEY \_ GPS \_ DestLoloDenominator berechnet.</span><span class="sxs-lookup"><span data-stu-id="73e00-106">Each is calculated from the values in PKEY\_GPS\_DestLatitudeNumerator and PKEY\_GPS\_DestLatitudeDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="73e00-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73e00-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.GPS.DestLatitude
   shellPKey = PKEY_GPS_DestLatitude
   formatID = 9D1D7CC5-5C39-451C-86B3-928E2D18CC47
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="73e00-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="73e00-108">Remarks</span></span>

<span data-ttu-id="73e00-109">PKEY-Werte werden in Propkey.h definiert.</span><span class="sxs-lookup"><span data-stu-id="73e00-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73e00-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="73e00-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73e00-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="73e00-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="73e00-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="73e00-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="73e00-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="73e00-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="73e00-114">Typeinfo</span><span class="sxs-lookup"><span data-stu-id="73e00-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="73e00-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="73e00-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="73e00-116">Stringformat</span><span class="sxs-lookup"><span data-stu-id="73e00-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="73e00-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="73e00-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="73e00-118">Numberformat</span><span class="sxs-lookup"><span data-stu-id="73e00-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="73e00-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="73e00-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="73e00-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="73e00-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="73e00-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="73e00-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="73e00-122">editControl</span><span class="sxs-lookup"><span data-stu-id="73e00-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="73e00-123">Filtercontrol</span><span class="sxs-lookup"><span data-stu-id="73e00-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="73e00-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="73e00-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
