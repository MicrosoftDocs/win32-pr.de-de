---
description: Wird von allen untergeordneten Elementen eines Containers als true ausgegeben (z. b. eine e-Mail oder eine komprimierte Datei mit der Erweiterung ". zip"), die System. search. iscloseddirectory als true ausgibt. Dadurch wird sichergestellt, dass die untergeordneten Elemente im Suchindex enthalten sind.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System. search. isfullyenthaltene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1245f29a2940146a4e5d8f0a392210173be75e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530050"
---
# <a name="systemsearchisfullycontained"></a><span data-ttu-id="9e02f-104">System. search. isfullyenthaltene</span><span class="sxs-lookup"><span data-stu-id="9e02f-104">System.Search.IsFullyContained</span></span>

<span data-ttu-id="9e02f-105">Wird von allen untergeordneten Elementen eines Containers als **true** ausgegeben (z. b. eine e-Mail oder eine komprimierte Datei mit der Erweiterung ". zip"), die [System. search. iscloseddirectory](./props-system-search-iscloseddirectory.md) als **true** ausgibt.</span><span class="sxs-lookup"><span data-stu-id="9e02f-105">Emitted as **TRUE** by all child items of a container (such as an e-mail or a compressed file with a .zip name extension) that emits [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) as **TRUE**.</span></span> <span data-ttu-id="9e02f-106">Dadurch wird sichergestellt, dass die untergeordneten Elemente im Suchindex enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="9e02f-106">This ensures that the child items are included in the search index.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="9e02f-107">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e02f-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="9e02f-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e02f-108">Remarks</span></span>

<span data-ttu-id="9e02f-109">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="9e02f-109">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="9e02f-110">Mithilfe der [System. search. iscloseddirectory](./props-system-search-iscloseddirectory.md) -Eigenschaft kann die indexerleistung optimiert werden, da der Indexer die Enumeration der untergeordneten Elemente eines Containers überspringen kann.</span><span class="sxs-lookup"><span data-stu-id="9e02f-110">The [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) property helps to optimize indexer performance by allowing the indexer to skip the enumeration of a container's child items.</span></span> <span data-ttu-id="9e02f-111">Diese untergeordneten Elemente sind jedoch vom Indexer als nicht besucht gekennzeichnet und werden aus dem Index gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9e02f-111">However, those child items are marked by the indexer as not visited, and as such will be deleted from the index.</span></span> <span data-ttu-id="9e02f-112">Wenn Sie [System. search. isfullyenthaltene]() als **true** ausgeben, wird ein Element nicht aus dem Index gelöscht, obwohl es nicht besucht wurde.</span><span class="sxs-lookup"><span data-stu-id="9e02f-112">By emitting [System.Search.IsFullyContained]() as **TRUE**, an item is not deleted from the index despite having not been visited.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e02f-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e02f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e02f-114">propertydescription</span><span class="sxs-lookup"><span data-stu-id="9e02f-114">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="9e02f-115">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="9e02f-115">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="9e02f-116">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="9e02f-116">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="9e02f-117">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="9e02f-117">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="9e02f-118">Display Info</span><span class="sxs-lookup"><span data-stu-id="9e02f-118">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="9e02f-119">StringFormat</span><span class="sxs-lookup"><span data-stu-id="9e02f-119">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="9e02f-120">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="9e02f-120">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="9e02f-121">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="9e02f-121">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="9e02f-122">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="9e02f-122">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="9e02f-123">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="9e02f-123">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="9e02f-124">DrawControl</span><span class="sxs-lookup"><span data-stu-id="9e02f-124">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="9e02f-125">editcontrol</span><span class="sxs-lookup"><span data-stu-id="9e02f-125">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="9e02f-126">FilterControl</span><span class="sxs-lookup"><span data-stu-id="9e02f-126">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="9e02f-127">querycontrol</span><span class="sxs-lookup"><span data-stu-id="9e02f-127">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
