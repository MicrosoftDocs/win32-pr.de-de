---
description: Die QueryTable-Struktur enthält eine Liste der Computer, die derzeit Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: QueryTable-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- QUERYTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2b2976a56b43c55fccb9acb0c593b0dfd37e4404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347954"
---
# <a name="querytable-structure"></a><span data-ttu-id="85ce7-103">QueryTable-Struktur</span><span class="sxs-lookup"><span data-stu-id="85ce7-103">QUERYTABLE structure</span></span>

<span data-ttu-id="85ce7-104">Die **QueryTable** -Struktur enthält eine Liste der Computer, die derzeit Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="85ce7-104">The **QUERYTABLE** structure provides a list of the computers that are currently using Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="85ce7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="85ce7-105">Syntax</span></span>


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a><span data-ttu-id="85ce7-106">Member</span><span class="sxs-lookup"><span data-stu-id="85ce7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="85ce7-107">**nstationqueries**</span><span class="sxs-lookup"><span data-stu-id="85ce7-107">**nStationQueries**</span></span>
</dt> <dd>

<span data-ttu-id="85ce7-108">Bei Eingabe die maximale Anzahl von Computern, die Netzwerkmonitor zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="85ce7-108">On input, the maximum number of computers you want Network Monitor to return.</span></span>

<span data-ttu-id="85ce7-109">Bei Ausgabe die Anzahl der [stationquery](stationquery.md) -Strukturen, die von Netzwerkmonitor zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="85ce7-109">On output, the number of [STATIONQUERY](stationquery.md) structures returned by Network Monitor.</span></span> <span data-ttu-id="85ce7-110">Jede **stationquery** -Struktur stellt einen Computer dar, der zurzeit Daten erfasst.</span><span class="sxs-lookup"><span data-stu-id="85ce7-110">Each **STATIONQUERY** structure represents a computer that is currently capturing data.</span></span>

</dd> <dt>

<span data-ttu-id="85ce7-111">**Stationquery**</span><span class="sxs-lookup"><span data-stu-id="85ce7-111">**StationQuery**</span></span>
</dt> <dd>

<span data-ttu-id="85ce7-112">Bei Eingabe ein Array leerer [stationquery](stationquery.md) -Strukturen, das die Anzahl der in **nstationqueries** angegebenen Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="85ce7-112">On input, an array of empty [STATIONQUERY](stationquery.md) structures that contains the number of elements specified in **nStationQueries**.</span></span>

<span data-ttu-id="85ce7-113">Bei Ausgabe eine gefüllte [Stations Abfrage](stationquery.md) Struktur für jeden Computer, der Daten erfasst.</span><span class="sxs-lookup"><span data-stu-id="85ce7-113">On output, a filled [STATIONQUERY](stationquery.md) structure for each computer that is capturing data.</span></span> <span data-ttu-id="85ce7-114">Die Anzahl der gefüllten Elemente wird von **nstationqueries** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85ce7-114">The number of filled elements is returned by **nStationQueries**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85ce7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85ce7-115">Remarks</span></span>

<span data-ttu-id="85ce7-116">Der Arbeitsspeicher für diese Struktur und das [stationquery](stationquery.md) -Array müssen von der aufrufenden Anwendung zugeordnet und freigegeben werden, nachdem die Informationen nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="85ce7-116">The memory for this structure and the [STATIONQUERY](stationquery.md) array must be allocated by the calling application and freed after the information is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="85ce7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85ce7-117">Requirements</span></span>



| <span data-ttu-id="85ce7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85ce7-118">Requirement</span></span> | <span data-ttu-id="85ce7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="85ce7-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="85ce7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85ce7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="85ce7-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85ce7-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="85ce7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85ce7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="85ce7-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85ce7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="85ce7-124">Header</span><span class="sxs-lookup"><span data-stu-id="85ce7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="85ce7-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85ce7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85ce7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ce7-127">Idelta-DC:: querystations</span><span class="sxs-lookup"><span data-stu-id="85ce7-127">IDelaydC::QueryStations</span></span>](idelaydc-querystations.md)
</dt> <dt>

[<span data-ttu-id="85ce7-128">IESP:: querystations</span><span class="sxs-lookup"><span data-stu-id="85ce7-128">IESP::QueryStations</span></span>](iesp-querystations.md)
</dt> <dt>

[<span data-ttu-id="85ce7-129">"Iran:: querystations"</span><span class="sxs-lookup"><span data-stu-id="85ce7-129">IRTC::QueryStations</span></span>](irtc-querystations.md)
</dt> <dt>

[<span data-ttu-id="85ce7-130">IStats:: querystations</span><span class="sxs-lookup"><span data-stu-id="85ce7-130">IStats::QueryStations</span></span>](istats-querystations.md)
</dt> <dt>

[<span data-ttu-id="85ce7-131">Stationquery</span><span class="sxs-lookup"><span data-stu-id="85ce7-131">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




