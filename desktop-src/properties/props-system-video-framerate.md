---
description: Gibt die Framerate für den Videostream in Frames pro 1000 Sekunden an.
ms.assetid: cd5a2ae0-43ef-44e4-aa70-bca33baf2a56
title: System. Video. Framerate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbdee7991186621a9d636e2072cecafc70176d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216834"
---
# <a name="systemvideoframerate"></a><span data-ttu-id="d497b-103">System. Video. Framerate</span><span class="sxs-lookup"><span data-stu-id="d497b-103">System.Video.FrameRate</span></span>

<span data-ttu-id="d497b-104">Gibt die Framerate für den Videostream in Frames pro 1000 Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="d497b-104">Indicates the frame rate for the video stream, in frames per 1000 seconds.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="d497b-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="d497b-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Video.FrameRate
   shellPKey = PKEY_Video_FrameRate
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 6
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="d497b-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d497b-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Video.FrameRate
   shellPKey = PKEY_Video_FrameRate
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 6
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="d497b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d497b-107">Remarks</span></span>

<span data-ttu-id="d497b-108">Um den abbrechungs Fehler zu verringern, verwendet diese Eigenschaft nicht die Standardframe Raten-Measure von Frames pro Sekunde (fps).</span><span class="sxs-lookup"><span data-stu-id="d497b-108">To help reduce truncation error, this property does not use the standard frame rate measure of frames per second (FPS).</span></span> <span data-ttu-id="d497b-109">Stattdessen misst diese Eigenschaft die Framerate als Frames pro 1000 Sekunden (fps multipliziert mit 1000).</span><span class="sxs-lookup"><span data-stu-id="d497b-109">Instead, this property measures frame rate as frames per 1000 seconds (FPS multiplied by 1000).</span></span> <span data-ttu-id="d497b-110">Beispielsweise würde [System. Video. Framerate]() eine frametrate von 29,97 fps als ganzzahligen Wert 29970 Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="d497b-110">For example, [System.Video.FrameRate]() would express a frame rate of 29.97 FPS as an integer value of 29970.</span></span>

<span data-ttu-id="d497b-111">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="d497b-111">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d497b-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d497b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d497b-113">propertydescription</span><span class="sxs-lookup"><span data-stu-id="d497b-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="d497b-114">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="d497b-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="d497b-115">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="d497b-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="d497b-116">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="d497b-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="d497b-117">Display Info</span><span class="sxs-lookup"><span data-stu-id="d497b-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="d497b-118">StringFormat</span><span class="sxs-lookup"><span data-stu-id="d497b-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="d497b-119">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="d497b-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="d497b-120">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="d497b-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="d497b-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="d497b-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="d497b-122">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="d497b-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="d497b-123">DrawControl</span><span class="sxs-lookup"><span data-stu-id="d497b-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="d497b-124">editcontrol</span><span class="sxs-lookup"><span data-stu-id="d497b-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="d497b-125">FilterControl</span><span class="sxs-lookup"><span data-stu-id="d497b-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="d497b-126">querycontrol</span><span class="sxs-lookup"><span data-stu-id="d497b-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
