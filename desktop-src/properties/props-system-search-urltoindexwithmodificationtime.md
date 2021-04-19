---
description: Diese Eigenschaft ist identisch mit System. search. urlumindex, mit der Ausnahme, dass Sie den Zeitpunkt enthält, an dem die URL zuletzt geändert wurde.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System. search. urldeindexwithmodificationtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fcc83b9796ae2375f10235a08ba0db313fb1958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363684"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a><span data-ttu-id="0713f-103">System. search. urldeindexwithmodificationtime</span><span class="sxs-lookup"><span data-stu-id="0713f-103">System.Search.UrlToIndexWithModificationTime</span></span>

<span data-ttu-id="0713f-104">Diese Eigenschaft ist identisch mit [**System. search. urlumindex**](props-system-search-urltoindex.md) , mit der Ausnahme, dass Sie den Zeitpunkt enthält, an dem die URL zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0713f-104">This property is the same as [**System.Search.UrlToIndex**](props-system-search-urltoindex.md) except that it includes the time that the URL was last modified.</span></span> <span data-ttu-id="0713f-105">Dies ist eine Optimierung für den Indexer, sodass er keinen Rückruf an den Protokollhandler durchführt, um zu ermitteln, ob der Inhalt erneut indiziert werden muss.</span><span class="sxs-lookup"><span data-stu-id="0713f-105">This is an optimization for the indexer so that it does not have to call back into the protocol handler to ask for this information to determine whether the content needs to be indexed again.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="0713f-106">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0713f-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a><span data-ttu-id="0713f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0713f-107">Remarks</span></span>

<span data-ttu-id="0713f-108">Diese [System. search. urldeindexwithmodificationtime]() -Eigenschaft ist identisch mit der Eigenschaft [System. search. urldeindex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) , mit dem Unterschied, dass Sie auch den Zeitpunkt der letzten Änderung des Dokuments übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="0713f-108">This [System.Search.UrlToIndexWithModificationTime]() property is the same as the [System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) property, except that you also pass in the last modified time of the document.</span></span> <span data-ttu-id="0713f-109">Wenn die Uhrzeit der letzten Änderung übereinstimmt, geht der Indexer davon aus, dass das Dokument bereits indiziert wurde, und löst die Benachrichtigung aus.</span><span class="sxs-lookup"><span data-stu-id="0713f-109">If the last modified time matches, the indexer assumes that the document is already indexed and throws away the notification.</span></span> <span data-ttu-id="0713f-110">Diese Eigenschaft ist ein Vektor mit zwei Elementen, einem **VT \_ LPWSTR** -Wert, der die URL und einen **VT \_ FILETIME** -Wert enthält, der den Zeitpunkt der letzten Änderung enthält.</span><span class="sxs-lookup"><span data-stu-id="0713f-110">This property is a vector with two elements, a **VT\_LPWSTR** value that contains the URL and a **VT\_FILETIME** value that contains the last modified time.</span></span>

<span data-ttu-id="0713f-111">[System. search. urlshindexwithmodificationtime]() wurde \_ \_ \_ \_ in früheren Versionen des Windows-Betriebssystems in früheren Versionen des Windows-Betriebssystems PID gthr dirlink genannt.</span><span class="sxs-lookup"><span data-stu-id="0713f-111">[System.Search.UrlToIndexWithModificationTime]() was called PID\_GTHR\_DIRLINK\_WITH\_TIME in earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="0713f-112">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="0713f-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0713f-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0713f-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0713f-114">[System. search. urlum Index](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0713f-114">[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0713f-115">propertydescription</span><span class="sxs-lookup"><span data-stu-id="0713f-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="0713f-116">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="0713f-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="0713f-117">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="0713f-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="0713f-118">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="0713f-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="0713f-119">Display Info</span><span class="sxs-lookup"><span data-stu-id="0713f-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="0713f-120">StringFormat</span><span class="sxs-lookup"><span data-stu-id="0713f-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="0713f-121">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="0713f-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="0713f-122">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="0713f-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="0713f-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0713f-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="0713f-124">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="0713f-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="0713f-125">DrawControl</span><span class="sxs-lookup"><span data-stu-id="0713f-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="0713f-126">editcontrol</span><span class="sxs-lookup"><span data-stu-id="0713f-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="0713f-127">FilterControl</span><span class="sxs-lookup"><span data-stu-id="0713f-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="0713f-128">querycontrol</span><span class="sxs-lookup"><span data-stu-id="0713f-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
