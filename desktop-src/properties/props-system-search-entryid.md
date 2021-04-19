---
description: Die Eingabe-ID für ein Element in einem angegebenen Katalog im Windows-Suchindex.
ms.assetid: 9162e92b-b738-4462-b346-68410f088e95
title: System. search. EntryID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd647338102d17e215973c85ea0e5d84c9bbdf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368985"
---
# <a name="systemsearchentryid"></a><span data-ttu-id="fd984-103">System. search. EntryID</span><span class="sxs-lookup"><span data-stu-id="fd984-103">System.Search.EntryID</span></span>

<span data-ttu-id="fd984-104">Die Eingabe-ID für ein Element in einem angegebenen Katalog im Windows-Suchindex.</span><span class="sxs-lookup"><span data-stu-id="fd984-104">The entry ID for an item within a given catalog in the Windows Search Index.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="fd984-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd984-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.EntryID
   shellPKey = PKEY_Search_EntryID
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Int32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="fd984-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd984-106">Remarks</span></span>

<span data-ttu-id="fd984-107">[System. search. EntryID]() wird in der SQL-Datei verwendet, die zum Abfragen des Indexes generiert wird.</span><span class="sxs-lookup"><span data-stu-id="fd984-107">[System.Search.EntryID]() is used in the SQL that is generated to query the index.</span></span> <span data-ttu-id="fd984-108">Dieser Wert wird im Laufe der Zeit nicht als eindeutig angesehen, weil er möglicherweise wieder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd984-108">This value is not considered unique over time because it may be recycled.</span></span>

<span data-ttu-id="fd984-109">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="fd984-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd984-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd984-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd984-111">propertydescription</span><span class="sxs-lookup"><span data-stu-id="fd984-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="fd984-112">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="fd984-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="fd984-113">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="fd984-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="fd984-114">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="fd984-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="fd984-115">Display Info</span><span class="sxs-lookup"><span data-stu-id="fd984-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="fd984-116">StringFormat</span><span class="sxs-lookup"><span data-stu-id="fd984-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="fd984-117">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="fd984-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="fd984-118">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="fd984-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="fd984-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="fd984-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="fd984-120">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="fd984-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="fd984-121">DrawControl</span><span class="sxs-lookup"><span data-stu-id="fd984-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="fd984-122">editcontrol</span><span class="sxs-lookup"><span data-stu-id="fd984-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="fd984-123">FilterControl</span><span class="sxs-lookup"><span data-stu-id="fd984-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="fd984-124">querycontrol</span><span class="sxs-lookup"><span data-stu-id="fd984-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
