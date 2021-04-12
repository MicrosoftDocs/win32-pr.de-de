---
description: Gibt den FourCC-Code für den Videostream an.
ms.assetid: c5054fc6-1273-4491-8fb9-30c4b8fc663f
title: System. Video. FourCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475b1cebc0d19a89c70e0ebae2be4b7673697c23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216835"
---
# <a name="systemvideofourcc"></a><span data-ttu-id="dd711-103">System. Video. FourCC</span><span class="sxs-lookup"><span data-stu-id="dd711-103">System.Video.FourCC</span></span>

<span data-ttu-id="dd711-104">Gibt den FourCC-Code für den Videostream an.</span><span class="sxs-lookup"><span data-stu-id="dd711-104">Specifies the FOURCC code for the video stream.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="dd711-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd711-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Video.FourCC
   shellPKey = PKEY_Video_FourCC
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 44
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
```

## <a name="remarks"></a><span data-ttu-id="dd711-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd711-106">Remarks</span></span>

<span data-ttu-id="dd711-107">Bei einem FourCC-Code handelt es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="dd711-107">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="dd711-108">Das Video FourCC für H. 264 lautet z. b. ' H264 ' oder 0x34363248.</span><span class="sxs-lookup"><span data-stu-id="dd711-108">For example, the FOURCC for H.264 video is 'H264' or 0x34363248.</span></span>

<span data-ttu-id="dd711-109">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="dd711-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd711-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd711-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd711-111">propertydescription</span><span class="sxs-lookup"><span data-stu-id="dd711-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="dd711-112">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="dd711-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="dd711-113">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="dd711-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="dd711-114">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="dd711-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="dd711-115">Display Info</span><span class="sxs-lookup"><span data-stu-id="dd711-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="dd711-116">StringFormat</span><span class="sxs-lookup"><span data-stu-id="dd711-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="dd711-117">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="dd711-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="dd711-118">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="dd711-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="dd711-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="dd711-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="dd711-120">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="dd711-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="dd711-121">DrawControl</span><span class="sxs-lookup"><span data-stu-id="dd711-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="dd711-122">editcontrol</span><span class="sxs-lookup"><span data-stu-id="dd711-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="dd711-123">FilterControl</span><span class="sxs-lookup"><span data-stu-id="dd711-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="dd711-124">querycontrol</span><span class="sxs-lookup"><span data-stu-id="dd711-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
