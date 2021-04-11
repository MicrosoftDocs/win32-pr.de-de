---
description: Der Wert vom Typ "f Number", wenn das Foto entnommen wurde, das aus den Informationen der austauschbaren Bilddatei (EXIF) gelesen wurde.
ms.assetid: 914dc34d-34e9-4283-be26-203da945d3e9
title: System. Photo. f Number
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22498d498bdf606cb0562f93df9a7b4d40405ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215753"
---
# <a name="systemphotofnumber"></a><span data-ttu-id="8c523-103">System. Photo. f Number</span><span class="sxs-lookup"><span data-stu-id="8c523-103">System.Photo.FNumber</span></span>

<span data-ttu-id="8c523-104">Der Wert vom Typ "f Number", wenn das Foto entnommen wurde, das aus den Informationen der austauschbaren Bilddatei (EXIF) gelesen wurde. Diese Eigenschaft wird anhand von " [System. Photo. vzahlzähler](./props-system-photo-fnumbernumerator.md) " und " [System. Photo. f. Nenner](./props-system-photo-fnumberdenominator.md)" berechnet.</span><span class="sxs-lookup"><span data-stu-id="8c523-104">The FNumber value when the photo was taken, as read from the Exchangeable Image File (EXIF) information.This property is calculated from [System.Photo.FNumberNumerator](./props-system-photo-fnumbernumerator.md) and [System.Photo.FNumberDenominator](./props-system-photo-fnumberdenominator.md).</span></span>

<span data-ttu-id="8c523-105">Die folgenden Werte sind möglich, die aus der EXIF 2,2-Spezifikation entnommen wurden.</span><span class="sxs-lookup"><span data-stu-id="8c523-105">The following are possible values as taken from the EXIF 2.2 specification.</span></span>

-   <span data-ttu-id="8c523-106">1</span><span class="sxs-lookup"><span data-stu-id="8c523-106">1</span></span>
-   <span data-ttu-id="8c523-107">1.4</span><span class="sxs-lookup"><span data-stu-id="8c523-107">1.4</span></span>
-   <span data-ttu-id="8c523-108">2</span><span class="sxs-lookup"><span data-stu-id="8c523-108">2</span></span>
-   <span data-ttu-id="8c523-109">2.8</span><span class="sxs-lookup"><span data-stu-id="8c523-109">2.8</span></span>
-   <span data-ttu-id="8c523-110">4</span><span class="sxs-lookup"><span data-stu-id="8c523-110">4</span></span>
-   <span data-ttu-id="8c523-111">5.6</span><span class="sxs-lookup"><span data-stu-id="8c523-111">5.6</span></span>
-   <span data-ttu-id="8c523-112">8</span><span class="sxs-lookup"><span data-stu-id="8c523-112">8</span></span>
-   <span data-ttu-id="8c523-113">11</span><span class="sxs-lookup"><span data-stu-id="8c523-113">11</span></span>
-   <span data-ttu-id="8c523-114">16</span><span class="sxs-lookup"><span data-stu-id="8c523-114">16</span></span>
-   <span data-ttu-id="8c523-115">22</span><span class="sxs-lookup"><span data-stu-id="8c523-115">22</span></span>
-   <span data-ttu-id="8c523-116">32</span><span class="sxs-lookup"><span data-stu-id="8c523-116">32</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="8c523-117">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c523-117">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.FNumber
   shellPKey = PKEY_Photo_FNumber
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 33437
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="8c523-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c523-118">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.FNumber
   shellPKey = PKEY_Photo_FNumber
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 33437
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="8c523-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c523-119">Remarks</span></span>

<span data-ttu-id="8c523-120">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="8c523-120">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c523-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8c523-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c523-122">Exchangeable Image File Format für digitale Kameras: EXIF Version 2,2</span><span class="sxs-lookup"><span data-stu-id="8c523-122">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="8c523-123">propertydescription</span><span class="sxs-lookup"><span data-stu-id="8c523-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="8c523-124">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="8c523-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="8c523-125">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="8c523-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="8c523-126">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="8c523-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="8c523-127">Display Info</span><span class="sxs-lookup"><span data-stu-id="8c523-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="8c523-128">StringFormat</span><span class="sxs-lookup"><span data-stu-id="8c523-128">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="8c523-129">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="8c523-129">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="8c523-130">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="8c523-130">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="8c523-131">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="8c523-131">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="8c523-132">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="8c523-132">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="8c523-133">DrawControl</span><span class="sxs-lookup"><span data-stu-id="8c523-133">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="8c523-134">editcontrol</span><span class="sxs-lookup"><span data-stu-id="8c523-134">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="8c523-135">FilterControl</span><span class="sxs-lookup"><span data-stu-id="8c523-135">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="8c523-136">querycontrol</span><span class="sxs-lookup"><span data-stu-id="8c523-136">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
