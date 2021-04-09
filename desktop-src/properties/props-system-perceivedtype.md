---
description: Der wahrgenommene Dateityp, der auf seinem kanonischen Typ basiert.
ms.assetid: dc5122a1-43b3-4c91-a44f-315fec5b4862
title: System.PerceivedType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc0be5e2ba481d113981efc264c4da66428e675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959580"
---
# <a name="systemperceivedtype"></a><span data-ttu-id="834db-103">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="834db-103">System.PerceivedType</span></span>

<span data-ttu-id="834db-104">Der wahrgenommene Dateityp, der auf seinem kanonischen Typ basiert.</span><span class="sxs-lookup"><span data-stu-id="834db-104">The perceived file type based on its canonical type.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="834db-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="834db-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.PerceivedType
   shellPKey = PKEY_PerceivedType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Custom
            value = -3
            text = Custom
         enum
            name = Unspecified
            value = -2
            text = Unspecified
         enum
            name = Folder
            value = -1
            text = Folder
            mnemonics = folders
         enum
            name = Unknown
            value = 0
            text = Unknown
         enum
            name = Text
            value = 1
            text = Text
         enum
            name = Image
            value = 2
            text = Image
            mnemonics = images|picture|pictures|pic|pics
         enum
            name = Audio
            value = 3
            text = Audio
         enum
            name = Video
            value = 4
            text = Video
            mnemonics = videos
         enum
            name = Compressed
            value = 5
            text = Compressed
         enum
            name = Document
            value = 6
            text = Document
            mnemonics = documents|doc|docs
         enum
            name = System
            value = 7
            text = System
         enum
            name = Application
            value = 8
            text = Application
         enum
            name = GameMedia
            value = 9
            text = Game Media
         enum
            name = Contacts
            value = 10
            text = Contacts
```

## <a name="windows-vista"></a><span data-ttu-id="834db-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="834db-106">Windows Vista</span></span>

```
propertyDescription
   name = System.PerceivedType
   shellPKey = PKEY_PerceivedType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = -3
            text = Custom
         enum
            value = -2
            text = Unspecified
         enum
            value = -1
            text = Folder
            mnemonics = folders
         enum
            value = 0
            text = Unknown
         enum
            value = 1
            text = Text
         enum
            value = 2
            text = Image
            mnemonics = images|picture|pictures|pic|pics
         enum
            value = 3
            text = Audio
         enum
            value = 4
            text = Video
            mnemonics = videos
         enum
            value = 5
            text = Compressed
         enum
            value = 6
            text = Document
            mnemonics = documents|doc|docs
         enum
            value = 7
            text = System
         enum
            value = 8
            text = Application
         enum
            value = 9
            text = Game Media
         enum
            value = 10
            text = Contacts
```

## <a name="remarks"></a><span data-ttu-id="834db-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="834db-107">Remarks</span></span>

<span data-ttu-id="834db-108">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="834db-108">PKEY values are defined in Propkey.h.</span></span> <span data-ttu-id="834db-109">Dieser Wert wird automatisch von der Shell zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="834db-109">This value is automatically assigned by the Shell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="834db-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="834db-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="834db-111">propertydescription</span><span class="sxs-lookup"><span data-stu-id="834db-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="834db-112">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="834db-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="834db-113">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="834db-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="834db-114">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="834db-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="834db-115">Display Info</span><span class="sxs-lookup"><span data-stu-id="834db-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="834db-116">StringFormat</span><span class="sxs-lookup"><span data-stu-id="834db-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="834db-117">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="834db-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="834db-118">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="834db-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="834db-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="834db-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="834db-120">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="834db-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="834db-121">DrawControl</span><span class="sxs-lookup"><span data-stu-id="834db-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="834db-122">editcontrol</span><span class="sxs-lookup"><span data-stu-id="834db-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="834db-123">FilterControl</span><span class="sxs-lookup"><span data-stu-id="834db-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="834db-124">querycontrol</span><span class="sxs-lookup"><span data-stu-id="834db-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
