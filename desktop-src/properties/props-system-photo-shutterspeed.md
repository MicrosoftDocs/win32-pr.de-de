---
description: Die Auslösegeschwindigkeit der Kamera, wenn das Foto entnommen wurde. Dies wird in Apex Units angegeben.
ms.assetid: 7f51b3b9-d701-4e7a-80bd-87c1a60e56f7
title: System. Photo. shutterspeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172ce97bf87e79dd86f83e68c91940748bbc283f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042175"
---
# <a name="systemphotoshutterspeed"></a><span data-ttu-id="c49f5-104">System. Photo. shutterspeed</span><span class="sxs-lookup"><span data-stu-id="c49f5-104">System.Photo.ShutterSpeed</span></span>

<span data-ttu-id="c49f5-105">Die Auslösegeschwindigkeit der Kamera, wenn das Foto entnommen wurde.</span><span class="sxs-lookup"><span data-stu-id="c49f5-105">The shutter speed of the camera when the photo was taken.</span></span> <span data-ttu-id="c49f5-106">Dies wird in Apex Units angegeben.</span><span class="sxs-lookup"><span data-stu-id="c49f5-106">This is given in APEX units.</span></span> <span data-ttu-id="c49f5-107">Diese Eigenschaft wird aus [System. Photo. shutterspeednumerator](./props-system-photo-shutterspeednumerator.md) und [System. Photo. shutterspeednenner](./props-system-photo-shutterspeeddenominator.md)berechnet.</span><span class="sxs-lookup"><span data-stu-id="c49f5-107">This property is calculated from [System.Photo.ShutterSpeedNumerator](./props-system-photo-shutterspeednumerator.md) and [System.Photo.ShutterSpeedDenominator](./props-system-photo-shutterspeeddenominator.md).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="c49f5-108">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="c49f5-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="c49f5-109">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c49f5-109">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="c49f5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c49f5-110">Remarks</span></span>

<span data-ttu-id="c49f5-111">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="c49f5-111">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="c49f5-112">Die Konvertierung dieses Werts in die Auswertungszeit finden Sie in der Version der austauschbaren Abbild Datei (EXIF) 2,2 (Anhang C).</span><span class="sxs-lookup"><span data-stu-id="c49f5-112">See the Exchangeable Image File (EXIF) 2.2 specification, Annex C, for the conversion of this value to exposure time.</span></span> <span data-ttu-id="c49f5-113">Verwenden Sie [System. Photo. ExposureTime](./props-system-photo-exposuretime.md) in allen shellansichten anstelle von [System. Photo. shutterspeed]().</span><span class="sxs-lookup"><span data-stu-id="c49f5-113">Use [System.Photo.ExposureTime](./props-system-photo-exposuretime.md) in any Shell views instead of [System.Photo.ShutterSpeed]().</span></span>

## <a name="related-topics"></a><span data-ttu-id="c49f5-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c49f5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c49f5-115">Exchangeable Image File Format für digitale Kameras: EXIF Version 2,2</span><span class="sxs-lookup"><span data-stu-id="c49f5-115">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="c49f5-116">propertydescription</span><span class="sxs-lookup"><span data-stu-id="c49f5-116">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c49f5-117">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="c49f5-117">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c49f5-118">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="c49f5-118">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c49f5-119">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="c49f5-119">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c49f5-120">Display Info</span><span class="sxs-lookup"><span data-stu-id="c49f5-120">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c49f5-121">StringFormat</span><span class="sxs-lookup"><span data-stu-id="c49f5-121">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c49f5-122">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="c49f5-122">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c49f5-123">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="c49f5-123">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c49f5-124">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c49f5-124">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c49f5-125">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="c49f5-125">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c49f5-126">DrawControl</span><span class="sxs-lookup"><span data-stu-id="c49f5-126">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c49f5-127">editcontrol</span><span class="sxs-lookup"><span data-stu-id="c49f5-127">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c49f5-128">FilterControl</span><span class="sxs-lookup"><span data-stu-id="c49f5-128">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c49f5-129">querycontrol</span><span class="sxs-lookup"><span data-stu-id="c49f5-129">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
