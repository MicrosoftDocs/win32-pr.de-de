---
description: Der Shell-Namespace Pfad zum Ziel des Link Elements.
ms.assetid: 05bd6cae-68b2-49ce-ad4f-e395ec88407a
title: System. Link. targetparamesingpath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1414947b988422c0ff37afda4bd55c80ffc9832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355678"
---
# <a name="systemlinktargetparsingpath"></a><span data-ttu-id="50c24-103">System. Link. targetparamesingpath</span><span class="sxs-lookup"><span data-stu-id="50c24-103">System.Link.TargetParsingPath</span></span>

<span data-ttu-id="50c24-104">Der Shell-Namespace Pfad zum Ziel des Link Elements.</span><span class="sxs-lookup"><span data-stu-id="50c24-104">The Shell namespace path to the target of the link item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="50c24-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50c24-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Link.TargetParsingPath
   shellPKey = PKEY_Link_TargetParsingPath
   formatID = B9B4B3FC-2B51-4A42-B5D8-324146AFCF25
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="50c24-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50c24-106">Remarks</span></span>

<span data-ttu-id="50c24-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="50c24-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="50c24-108">Dieser Pfad kann an [**shparameationdisplayname**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) übermittelt werden, um den Pfad zum richtigen Shellordner zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="50c24-108">This path can be passed to [**SHParseDisplayName**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) to parse the path to the correct Shell folder.</span></span> <span data-ttu-id="50c24-109">Wenn das Ziel Element eine Datei ist, ist der Wert identisch mit [System. itempathdisplay](./props-system-itempathdisplay.md). Wenn kein Zugriff auf das Ziel Element über den Shellnamespace möglich ist, ist dieser Wert "VT \_ empty".</span><span class="sxs-lookup"><span data-stu-id="50c24-109">If the target item is a file, the value is identical to [System.ItemPathDisplay](./props-system-itempathdisplay.md).If the target item cannot be accessed through the Shell namespace, this value is VT\_EMPTY.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50c24-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50c24-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50c24-111">propertydescription</span><span class="sxs-lookup"><span data-stu-id="50c24-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="50c24-112">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="50c24-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="50c24-113">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="50c24-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="50c24-114">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="50c24-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="50c24-115">Display Info</span><span class="sxs-lookup"><span data-stu-id="50c24-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="50c24-116">StringFormat</span><span class="sxs-lookup"><span data-stu-id="50c24-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="50c24-117">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="50c24-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="50c24-118">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="50c24-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="50c24-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="50c24-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="50c24-120">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="50c24-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="50c24-121">DrawControl</span><span class="sxs-lookup"><span data-stu-id="50c24-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="50c24-122">editcontrol</span><span class="sxs-lookup"><span data-stu-id="50c24-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="50c24-123">FilterControl</span><span class="sxs-lookup"><span data-stu-id="50c24-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="50c24-124">querycontrol</span><span class="sxs-lookup"><span data-stu-id="50c24-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
