---
title: Zähler Sammlung (isysmon. h)
description: Verwenden Sie diese Klasse, um die Auflistung der "count"-Objekte zu verwalten. Um dieses Objekt abzurufen, rufen Sie Systemmonitor. Counters auf.
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- Leistungsindikator Sammlung (Sysmon)
- Leistungsindikator Sammlung (Sysmon), beschrieben
topic_type:
- apiref
api_name:
- Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbf8da93f13dce2ce2a290adeab9394ee8addb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345501"
---
# <a name="counters-collection"></a><span data-ttu-id="706fc-106">Zähler Sammlung</span><span class="sxs-lookup"><span data-stu-id="706fc-106">Counters collection</span></span>

<span data-ttu-id="706fc-107">Verwenden Sie diese Klasse, um die Auflistung der " [**count**](counteritem.md) "-Objekte zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="706fc-107">Use this class to manage the collection of [**CounterItem**](counteritem.md) objects.</span></span>

<span data-ttu-id="706fc-108">Um dieses Objekt abzurufen, rufen Sie [**Systemmonitor. Counters**](systemmonitor-counters.md)auf.</span><span class="sxs-lookup"><span data-stu-id="706fc-108">To retrieve this object, call [**SystemMonitor.Counters**](systemmonitor-counters.md).</span></span>

## <a name="members"></a><span data-ttu-id="706fc-109">Member</span><span class="sxs-lookup"><span data-stu-id="706fc-109">Members</span></span>

<span data-ttu-id="706fc-110">Die  indikatorenauflistung enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="706fc-110">The **Counters** collection has these types of members:</span></span>

-   [<span data-ttu-id="706fc-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="706fc-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="706fc-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="706fc-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="706fc-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="706fc-113">Methods</span></span>

<span data-ttu-id="706fc-114">Die  indikatorenauflistung verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="706fc-114">The **Counters** collection has these methods.</span></span>



| <span data-ttu-id="706fc-115">Methode</span><span class="sxs-lookup"><span data-stu-id="706fc-115">Method</span></span>                            | <span data-ttu-id="706fc-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="706fc-116">Description</span></span>                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="706fc-117">**Eren**</span><span class="sxs-lookup"><span data-stu-id="706fc-117">**Add**</span></span>](counters-add.md)       | <span data-ttu-id="706fc-118">Fügt der [**Auflistung eine-**](counteritem.md) Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="706fc-118">Adds a [**CounterItem**](counteritem.md) instance to the collection.</span></span><br/>      |
| [<span data-ttu-id="706fc-119">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="706fc-119">**Remove**</span></span>](counters-remove.md) | <span data-ttu-id="706fc-120">Entfernt eine [**-**](counteritem.md) Instanz aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="706fc-120">Removes a [**CounterItem**](counteritem.md) instance from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="706fc-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="706fc-121">Properties</span></span>

<span data-ttu-id="706fc-122">Die **Zähler** Sammlung verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="706fc-122">The **Counters** collection has these properties.</span></span>



| <span data-ttu-id="706fc-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="706fc-123">Property</span></span>                                   | <span data-ttu-id="706fc-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="706fc-124">Description</span></span>                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="706fc-125">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="706fc-125">**Count**</span></span>](counters-count.md)<br/> | <span data-ttu-id="706fc-126">Ruft die [**Anzahl von Instanzen in der-**](counteritem.md) Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="706fc-126">Retrieves the number of [**CounterItem**](counteritem.md) instances in the collection.</span></span><br/>  |
| [<span data-ttu-id="706fc-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="706fc-127">**Item**</span></span>](counters-item.md)<br/>   | <span data-ttu-id="706fc-128">Ruft [**die angegebene-**](counteritem.md) Instanz aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="706fc-128">Retrieves the specified [**CounterItem**](counteritem.md) instance from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="706fc-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="706fc-129">Remarks</span></span>

<span data-ttu-id="706fc-130">Das **Counters** -Objekt ist die Standard Eigenschaft des [**Systemmonitor**](systemmonitor.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="706fc-130">The **Counters** object is the default property of the [**SystemMonitor**](systemmonitor.md) object.</span></span>

<span data-ttu-id="706fc-131">Fügen Sie dieser Sammlung die Leistungsindikatoren hinzu, die Sie grafisch abbilden möchten.</span><span class="sxs-lookup"><span data-stu-id="706fc-131">Add to this collection those counters that you want to graph.</span></span> <span data-ttu-id="706fc-132">Sysmon Ruft die Werte des Zählers entweder aus dem System oder aus einer Protokolldatei ab, abhängig von der von Ihnen angegebenen [**Datenquelle**](systemmonitor-datasourcetype.md) .</span><span class="sxs-lookup"><span data-stu-id="706fc-132">SYSMON retrieves the counter values either from the system or from a log file depending on the [**data source**](systemmonitor-datasourcetype.md) that you specify.</span></span>

## <a name="requirements"></a><span data-ttu-id="706fc-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="706fc-133">Requirements</span></span>



| <span data-ttu-id="706fc-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="706fc-134">Requirement</span></span> | <span data-ttu-id="706fc-135">Wert</span><span class="sxs-lookup"><span data-stu-id="706fc-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="706fc-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="706fc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="706fc-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="706fc-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="706fc-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="706fc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="706fc-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="706fc-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="706fc-140">Header</span><span class="sxs-lookup"><span data-stu-id="706fc-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="706fc-141"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="706fc-141"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="706fc-142">DLL</span><span class="sxs-lookup"><span data-stu-id="706fc-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="706fc-143"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="706fc-143"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





