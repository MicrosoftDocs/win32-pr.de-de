---
description: Stellt eine wohlgeformte URL dar, die auf das Element verweist.
ms.assetid: d592f12b-f8c2-406f-a031-eeb8212e64f7
title: System. itemurl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02beb9629661a052d2ec1fae7c7a34e999e777e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360822"
---
# <a name="systemitemurl"></a><span data-ttu-id="401f5-103">System. itemurl</span><span class="sxs-lookup"><span data-stu-id="401f5-103">System.ItemUrl</span></span>

<span data-ttu-id="401f5-104">Stellt eine wohlgeformte URL dar, die auf das Element verweist.</span><span class="sxs-lookup"><span data-stu-id="401f5-104">Represents a well-formed URL that points to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="401f5-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="401f5-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemUrl
   shellPKey = PKEY_ItemUrl
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 9
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="401f5-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="401f5-106">Remarks</span></span>

<span data-ttu-id="401f5-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="401f5-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="401f5-108">Verwenden Sie zum Verweisen auf Shell-Namespace Elemente über Shell-APIs [System. Parser Path](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="401f5-108">To reference Shell namespace items through Shell APIs, use [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="401f5-109">Beispielwerte:</span><span class="sxs-lookup"><span data-stu-id="401f5-109">Example values:</span></span>



| <span data-ttu-id="401f5-110">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="401f5-110">Item type</span></span> | <span data-ttu-id="401f5-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="401f5-111">Example</span></span>                        |
|-----------|--------------------------------|
| <span data-ttu-id="401f5-112">File</span><span class="sxs-lookup"><span data-stu-id="401f5-112">File</span></span>      | <span data-ttu-id="401f5-113">file:///c:/mydir/Bar/hello.txt</span><span class="sxs-lookup"><span data-stu-id="401f5-113">file:///c:/mydir/bar/hello.txt</span></span> |
| <span data-ttu-id="401f5-114">File</span><span class="sxs-lookup"><span data-stu-id="401f5-114">File</span></span>      | <span data-ttu-id="401f5-115">CSC://{GUID}/...</span><span class="sxs-lookup"><span data-stu-id="401f5-115">csc://{GUID}/...</span></span>               |
| <span data-ttu-id="401f5-116">`Message`</span><span class="sxs-lookup"><span data-stu-id="401f5-116">Message</span></span>   | <span data-ttu-id="401f5-117">MAPI://...</span><span class="sxs-lookup"><span data-stu-id="401f5-117">mapi://...</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="401f5-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="401f5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="401f5-119">propertydescription</span><span class="sxs-lookup"><span data-stu-id="401f5-119">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="401f5-120">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="401f5-120">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="401f5-121">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="401f5-121">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="401f5-122">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="401f5-122">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="401f5-123">Display Info</span><span class="sxs-lookup"><span data-stu-id="401f5-123">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="401f5-124">StringFormat</span><span class="sxs-lookup"><span data-stu-id="401f5-124">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="401f5-125">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="401f5-125">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="401f5-126">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="401f5-126">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="401f5-127">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="401f5-127">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="401f5-128">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="401f5-128">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="401f5-129">DrawControl</span><span class="sxs-lookup"><span data-stu-id="401f5-129">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="401f5-130">editcontrol</span><span class="sxs-lookup"><span data-stu-id="401f5-130">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="401f5-131">FilterControl</span><span class="sxs-lookup"><span data-stu-id="401f5-131">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="401f5-132">querycontrol</span><span class="sxs-lookup"><span data-stu-id="401f5-132">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
