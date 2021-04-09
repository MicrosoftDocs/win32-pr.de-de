---
description: Der Shell-Namespace Pfad zum Element.
ms.assetid: e0fb2092-0427-40c9-9e09-aefc5ef017e6
title: System. paramesingpath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae62243ff37464617f87654f8ca1f04c3ea606da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864616"
---
# <a name="systemparsingpath"></a><span data-ttu-id="2cf2c-103">System. paramesingpath</span><span class="sxs-lookup"><span data-stu-id="2cf2c-103">System.ParsingPath</span></span>

<span data-ttu-id="2cf2c-104">Der Shell-Namespace Pfad zum Element.</span><span class="sxs-lookup"><span data-stu-id="2cf2c-104">The Shell namespace path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="2cf2c-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2cf2c-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ParsingPath
   shellPKey = PKEY_ParsingPath
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 30
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="2cf2c-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cf2c-106">Remarks</span></span>

<span data-ttu-id="2cf2c-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="2cf2c-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="2cf2c-108">Dieser Wert kann an [**shparameationdisplayname**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) übermittelt werden, um den Pfad zum richtigen Shellordner zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="2cf2c-108">This value can be passed to [**SHParseDisplayName**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) to parse the path to the correct Shell folder.</span></span> <span data-ttu-id="2cf2c-109">Wenn es sich bei dem Element um eine Datei handelt, ist der Wert identisch mit [System. itempathdisplay](./props-system-itempathdisplay.md).</span><span class="sxs-lookup"><span data-stu-id="2cf2c-109">If the item is a file, the value is identical to [System.ItemPathDisplay](./props-system-itempathdisplay.md).</span></span> <span data-ttu-id="2cf2c-110">Wenn auf das Element nicht über den Shell-Namespace zugegriffen werden kann, ist dieser Wert "VT \_ empty".</span><span class="sxs-lookup"><span data-stu-id="2cf2c-110">If the item cannot be accessed through the Shell namespace, this value is VT\_EMPTY.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cf2c-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2cf2c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cf2c-112">propertydescription</span><span class="sxs-lookup"><span data-stu-id="2cf2c-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2cf2c-113">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="2cf2c-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2cf2c-114">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="2cf2c-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2cf2c-115">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="2cf2c-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2cf2c-116">Display Info</span><span class="sxs-lookup"><span data-stu-id="2cf2c-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2cf2c-117">StringFormat</span><span class="sxs-lookup"><span data-stu-id="2cf2c-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2cf2c-118">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="2cf2c-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2cf2c-119">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="2cf2c-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2cf2c-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2cf2c-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2cf2c-121">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="2cf2c-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2cf2c-122">DrawControl</span><span class="sxs-lookup"><span data-stu-id="2cf2c-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2cf2c-123">editcontrol</span><span class="sxs-lookup"><span data-stu-id="2cf2c-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2cf2c-124">FilterControl</span><span class="sxs-lookup"><span data-stu-id="2cf2c-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2cf2c-125">querycontrol</span><span class="sxs-lookup"><span data-stu-id="2cf2c-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
