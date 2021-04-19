---
description: Wird von einem Container-IFilter für jede untergeordnete URL innerhalb des Containers ausgegeben. Die untergeordneten Elemente werden schließlich vom Indexer durchlaufen, wenn Sie sich innerhalb des Bereichs befinden.
ms.assetid: e864b3fa-6d43-40fe-9556-474953098947
title: System. search. urlum Index
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4832279237cb7a3659b37d6502bd853caff113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348666"
---
# <a name="systemsearchurltoindex"></a><span data-ttu-id="5150d-104">System. search. urlum Index</span><span class="sxs-lookup"><span data-stu-id="5150d-104">System.Search.UrlToIndex</span></span>

<span data-ttu-id="5150d-105">Wird von einem Container- [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) für jede untergeordnete URL innerhalb des Containers ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="5150d-105">Emitted by a container [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) for each child URL within the container.</span></span> <span data-ttu-id="5150d-106">Die untergeordneten Elemente werden schließlich vom Indexer durchlaufen, wenn Sie sich innerhalb des Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="5150d-106">The children are eventually crawled by the indexer if they are within scope.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="5150d-107">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5150d-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.UrlToIndex
   shellPKey = PKEY_Search_UrlToIndex
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
```

## <a name="remarks"></a><span data-ttu-id="5150d-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5150d-108">Remarks</span></span>

<span data-ttu-id="5150d-109">Diese Eigenschaft enthält eine URL und wird von einem Protokollhandler für jede untergeordnete URL oder dieses directtoy unter der aktuellen URL ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="5150d-109">This property contains a URL and is emitted by a protocol handler for each child URL or directoy under the current URL.</span></span> <span data-ttu-id="5150d-110">Der Indexer ruft den Protokollhandler zurück und fordert das Indizieren dieses Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="5150d-110">The indexer calls back into the protocol handler, and asks for that document to be indexed.</span></span> <span data-ttu-id="5150d-111">[System. search. urldeindex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) wurde \_ \_ in früheren Versionen des Windows-Betriebssystems in früheren Versionen des Windows-Betriebssystems PID gthr dirlink genannt.</span><span class="sxs-lookup"><span data-stu-id="5150d-111">[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) was called PID\_GTHR\_DIRLINK in earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="5150d-112">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="5150d-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5150d-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5150d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5150d-114">System. search. urldeindexwithmodificationtime</span><span class="sxs-lookup"><span data-stu-id="5150d-114">System.Search.UrlToIndexWithModificationTime</span></span>](./props-system-search-urltoindexwithmodificationtime.md)
</dt> <dt>

[<span data-ttu-id="5150d-115">propertydescription</span><span class="sxs-lookup"><span data-stu-id="5150d-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="5150d-116">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="5150d-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="5150d-117">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="5150d-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="5150d-118">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="5150d-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="5150d-119">Display Info</span><span class="sxs-lookup"><span data-stu-id="5150d-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="5150d-120">StringFormat</span><span class="sxs-lookup"><span data-stu-id="5150d-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="5150d-121">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="5150d-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="5150d-122">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="5150d-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="5150d-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5150d-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="5150d-124">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="5150d-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="5150d-125">DrawControl</span><span class="sxs-lookup"><span data-stu-id="5150d-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="5150d-126">editcontrol</span><span class="sxs-lookup"><span data-stu-id="5150d-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="5150d-127">FilterControl</span><span class="sxs-lookup"><span data-stu-id="5150d-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="5150d-128">querycontrol</span><span class="sxs-lookup"><span data-stu-id="5150d-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
