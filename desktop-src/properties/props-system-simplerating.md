---
description: Ein Bewertungssystem, das einen Bereich von ganzzahligen Werten zwischen 0 und 5 verwendet.
ms.assetid: 50353ba9-86dd-4172-91b4-1898c8fc5522
title: System. simplerating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4741edd076b6027bc5f8dfbe3b2ff2a31374a7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350114"
---
# <a name="systemsimplerating"></a><span data-ttu-id="452f5-103">System. simplerating</span><span class="sxs-lookup"><span data-stu-id="452f5-103">System.SimpleRating</span></span>

<span data-ttu-id="452f5-104">Ein Bewertungssystem, das einen Bereich von ganzzahligen Werten zwischen 0 und 5 verwendet.</span><span class="sxs-lookup"><span data-stu-id="452f5-104">A rating system that uses a range of integer values between 0 and 5.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="452f5-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="452f5-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.SimpleRating
   shellPKey = PKEY_SimpleRating
   formatID = A09F084E-AD41-489F-8076-AA5BE3082BCA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="452f5-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="452f5-106">Remarks</span></span>

<span data-ttu-id="452f5-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="452f5-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="452f5-108">Aus Kompatibilitätsgründen mit dem Windows Vista-Shell-Bewertungssystem sollte der Eigenschafts Handler auch die [System. Rating](./props-system-rating.md) -Eigenschaft mit der Zuordnung auffüllen, wie für diese Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="452f5-108">For compatibility with the Windows Vista Shell rating system, your property handler should also populate the [System.Rating](./props-system-rating.md) property with the mapping as described for that property.</span></span>

<span data-ttu-id="452f5-109">Verwenden Sie die folgende Tabelle, um von [System. Rating](./props-system-rating.md) in [System. simplerating]()zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="452f5-109">Use the following table to convert from [System.Rating](./props-system-rating.md) to [System.SimpleRating]().</span></span>



| <span data-ttu-id="452f5-110">System. Rating</span><span class="sxs-lookup"><span data-stu-id="452f5-110">System.Rating</span></span> | <span data-ttu-id="452f5-111">System. simplerating</span><span class="sxs-lookup"><span data-stu-id="452f5-111">System.SimpleRating</span></span> |
|---------------|---------------------|
| <span data-ttu-id="452f5-112">0</span><span class="sxs-lookup"><span data-stu-id="452f5-112">0</span></span>             | <span data-ttu-id="452f5-113">0</span><span class="sxs-lookup"><span data-stu-id="452f5-113">0</span></span>                   |
| <span data-ttu-id="452f5-114">1-12</span><span class="sxs-lookup"><span data-stu-id="452f5-114">1-12</span></span>          | <span data-ttu-id="452f5-115">1</span><span class="sxs-lookup"><span data-stu-id="452f5-115">1</span></span>                   |
| <span data-ttu-id="452f5-116">13-37</span><span class="sxs-lookup"><span data-stu-id="452f5-116">13-37</span></span>         | <span data-ttu-id="452f5-117">2</span><span class="sxs-lookup"><span data-stu-id="452f5-117">2</span></span>                   |
| <span data-ttu-id="452f5-118">38-62</span><span class="sxs-lookup"><span data-stu-id="452f5-118">38-62</span></span>         | <span data-ttu-id="452f5-119">3</span><span class="sxs-lookup"><span data-stu-id="452f5-119">3</span></span>                   |
| <span data-ttu-id="452f5-120">63-87</span><span class="sxs-lookup"><span data-stu-id="452f5-120">63-87</span></span>         | <span data-ttu-id="452f5-121">4</span><span class="sxs-lookup"><span data-stu-id="452f5-121">4</span></span>                   |
| <span data-ttu-id="452f5-122">88-99</span><span class="sxs-lookup"><span data-stu-id="452f5-122">88-99</span></span>         | <span data-ttu-id="452f5-123">5</span><span class="sxs-lookup"><span data-stu-id="452f5-123">5</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="452f5-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="452f5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="452f5-125">propertydescription</span><span class="sxs-lookup"><span data-stu-id="452f5-125">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="452f5-126">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="452f5-126">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="452f5-127">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="452f5-127">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="452f5-128">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="452f5-128">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="452f5-129">Display Info</span><span class="sxs-lookup"><span data-stu-id="452f5-129">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="452f5-130">StringFormat</span><span class="sxs-lookup"><span data-stu-id="452f5-130">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="452f5-131">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="452f5-131">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="452f5-132">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="452f5-132">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="452f5-133">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="452f5-133">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="452f5-134">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="452f5-134">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="452f5-135">DrawControl</span><span class="sxs-lookup"><span data-stu-id="452f5-135">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="452f5-136">editcontrol</span><span class="sxs-lookup"><span data-stu-id="452f5-136">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="452f5-137">FilterControl</span><span class="sxs-lookup"><span data-stu-id="452f5-137">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="452f5-138">querycontrol</span><span class="sxs-lookup"><span data-stu-id="452f5-138">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
