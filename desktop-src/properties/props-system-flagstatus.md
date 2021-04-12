---
description: 'Der Status eines Flags. Werte: (0 = keine 1 = weiß 2 = rot).'
ms.assetid: 0485deab-2408-4147-acaa-cb09e9e0032a
title: System. FlagStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dde42493f2d450854c3f53de5ecab26394f0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215802"
---
# <a name="systemflagstatus"></a><span data-ttu-id="1ad67-104">System. FlagStatus</span><span class="sxs-lookup"><span data-stu-id="1ad67-104">System.FlagStatus</span></span>

<span data-ttu-id="1ad67-105">Der Status eines Flags.</span><span class="sxs-lookup"><span data-stu-id="1ad67-105">The status of a flag.</span></span> <span data-ttu-id="1ad67-106">Werte: (0 = keine 1 = weiß 2 = rot).</span><span class="sxs-lookup"><span data-stu-id="1ad67-106">Values: (0=none 1=white 2=Red).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="1ad67-107">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="1ad67-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.FlagStatus
   shellPKey = PKEY_FlagStatus
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Int32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotFlagged
            value = 0
            text = Not flagged
            defineToken = FLAGSTATUS_NOTFLAGGED
            mnemonics = Unflagged
         enum
            name = Completed
            value = 1
            text = Completed
            defineToken = FLAGSTATUS_COMPLETED
         enum
            name = FollowUp
            value = 2
            text = Follow Up
            defineToken = FLAGSTATUS_FOLLOWUP
            mnemonics = Followup Flag|followup|follow
```

## <a name="windows-vista"></a><span data-ttu-id="1ad67-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ad67-108">Windows Vista</span></span>

```
propertyDescription
   name = System.FlagStatus
   shellPKey = PKEY_FlagStatus
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 12
   SearchInfo
      IsColumn = true
   typeInfo
      type = Int32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Not flagged
            defineName = FLAGSTATUS_NOTFLAGGED
            mnemonics = Unflagged
         enum
            value = 1
            text = Completed
            defineName = FLAGSTATUS_COMPLETED
         enum
            value = 2
            text = Follow Up
            defineName = FLAGSTATUS_FOLLOWUP
            mnemonics = Followup Flag|followup|follow
```

## <a name="remarks"></a><span data-ttu-id="1ad67-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ad67-109">Remarks</span></span>

<span data-ttu-id="1ad67-110">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="1ad67-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ad67-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ad67-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ad67-112">propertydescription</span><span class="sxs-lookup"><span data-stu-id="1ad67-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1ad67-113">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="1ad67-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1ad67-114">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="1ad67-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1ad67-115">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="1ad67-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1ad67-116">Display Info</span><span class="sxs-lookup"><span data-stu-id="1ad67-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1ad67-117">StringFormat</span><span class="sxs-lookup"><span data-stu-id="1ad67-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1ad67-118">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="1ad67-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1ad67-119">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="1ad67-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1ad67-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1ad67-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1ad67-121">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="1ad67-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1ad67-122">DrawControl</span><span class="sxs-lookup"><span data-stu-id="1ad67-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1ad67-123">editcontrol</span><span class="sxs-lookup"><span data-stu-id="1ad67-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1ad67-124">FilterControl</span><span class="sxs-lookup"><span data-stu-id="1ad67-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1ad67-125">querycontrol</span><span class="sxs-lookup"><span data-stu-id="1ad67-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
