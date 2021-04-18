---
title: Counters. Add-Methode
description: Fügt der Auflistung eine-Instanz hinzu.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Methode hinzufügen (Sysmon)
- Add-Methode (Sysmon), counters-Klasse
- Zähler Klasse sysmon, Methode hinzufügen
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c974c5df6f531cd75292290c61534a923e5be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475828"
---
# <a name="countersadd-method"></a><span data-ttu-id="ab8a9-106">Counters. Add-Methode</span><span class="sxs-lookup"><span data-stu-id="ab8a9-106">Counters.Add method</span></span>

<span data-ttu-id="ab8a9-107">Fügt der [**Auflistung eine-**](counteritem.md) Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-107">Adds a [**CounterItem**](counteritem.md) instance to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab8a9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab8a9-108">Syntax</span></span>


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a><span data-ttu-id="ab8a9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab8a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab8a9-110">*Pfadname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab8a9-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab8a9-111">Der Pfad des Zählers.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-111">Path to the counter.</span></span> <span data-ttu-id="ab8a9-112">Der Pfad kann einen Computernamen enthalten und muss einen Leistungs Objektnamen, einen objektinstanznamen, wenn das angegebene Leistungs Objekt mehrere Instanzen unterstützt, und einen Leistungs Namen enthalten.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-112">The path can include a machine name, and must include a performance object name, an object instance name if the specified performance object supports multiple instances, and a counter name.</span></span> <span data-ttu-id="ab8a9-113">Bei dieser Pfadangabe wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-113">This path specification is not case-sensitive.</span></span>

<span data-ttu-id="ab8a9-114">Ausführliche Informationen zum Angeben eines Zählers finden Sie unter [Angeben eines Counter-Pfads](/windows/desktop/PerfCtrs/specifying-a-counter-path).</span><span class="sxs-lookup"><span data-stu-id="ab8a9-114">For details on specifying a counter path, see [Specifying a Counter Path](/windows/desktop/PerfCtrs/specifying-a-counter-path).</span></span>

</dd> </dl>

## <a name="exceptions"></a><span data-ttu-id="ab8a9-115">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="ab8a9-115">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab8a9-116">Ausnahmetyp</span><span class="sxs-lookup"><span data-stu-id="ab8a9-116">Exception type</span></span></th>
<th><span data-ttu-id="ab8a9-117">Bedingung</span><span class="sxs-lookup"><span data-stu-id="ab8a9-117">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab8a9-118"><strong>System. Runtime. InteropServices. COMException</strong></span><span class="sxs-lookup"><span data-stu-id="ab8a9-118"><strong>System.Runtime.InteropServices.COMException</strong></span></span></td>
<td><span data-ttu-id="ab8a9-119">Sie können diese Ausnahme aus einem der folgenden Gründe erhalten:</span><span class="sxs-lookup"><span data-stu-id="ab8a9-119">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="ab8a9-120">Das angegebene Leistungs Objekt wurde auf dem Computer nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-120">The specified performance object was not found on the computer.</span></span> <span data-ttu-id="ab8a9-121">Der Err. Number-Wert ist 0xc0000bb8.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-121">The Err.Number value is 0xC0000BB8.</span></span></li>
<li><span data-ttu-id="ab8a9-122">Der angegebene Counter konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-122">The specified counter could not be found.</span></span> <span data-ttu-id="ab8a9-123">Der Err. Number-Wert ist 0xc0000bb9.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-123">The Err.Number value is 0xC0000BB9.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="ab8a9-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab8a9-124">Remarks</span></span>

<span data-ttu-id="ab8a9-125">Wenn Sie einen Platzhalter Indikator im *Pfadnamen* -Parameter angeben, erstellt die **Add** -Methode ein Objekt vom Typ " [**count**](counteritem.md) " für jeden erweiterten Pfad.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-125">If you specify a wildcard counter in the *pathname* parameter, the **Add** method creates one [**CounterItem**](counteritem.md) object for each expanded path.</span></span> <span data-ttu-id="ab8a9-126">Die **Add** -Methode gibt dann einen Zeiger auf das erste hinzugefügte **ratteritem** zurück.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-126">The **Add** method then returns a pointer to the first added **CounterItem**.</span></span>

<span data-ttu-id="ab8a9-127">Wenn der Platzhalter zu einem doppelten Zählers führt, wird der Fehler nicht gemeldet, und es wird kein Duplikat erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-127">If the wildcard would result in a duplicate counter, the error is not reported and no duplicate is created.</span></span> <span data-ttu-id="ab8a9-128">Wenn vor dem Erstellen aller Indikatoren eine Fehlerbedingung auftritt, wird der Fehler gemeldet, und die verbleibenden Leistungsindikatoren werden nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-128">If an error condition occurs before all counters are created, the error is reported and the remaining counters are not created.</span></span>

<span data-ttu-id="ab8a9-129">Es gibt keine Beschränkung für die Anzahl der Leistungsindikatoren, die Sie hinzufügen können. sysmon zeigt jedoch nur die ersten 1.024-Leistungsindikatoren in der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-129">There is no limit to the number of counters that you can add; however, SYSMON will graph only the first 1,024 counters in the collection.</span></span> <span data-ttu-id="ab8a9-130">Es gibt keine Beschränkung für die Anzahl von Leistungsindikatoren, die in einem Bericht von sysmon angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-130">There is no limit on the number of counters that SYSMON will display in a report.</span></span>

<span data-ttu-id="ab8a9-131">Um eine Benachrichtigung zu erhalten, wenn ein Indikator hinzugefügt wird, implementieren Sie das [oncounteradded](systemmonitor-oncounteradded.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ab8a9-131">To receive notification when a counter is added, implement the [OnCounterAdded](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab8a9-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab8a9-132">Requirements</span></span>



| <span data-ttu-id="ab8a9-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab8a9-133">Requirement</span></span> | <span data-ttu-id="ab8a9-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ab8a9-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab8a9-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab8a9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ab8a9-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab8a9-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ab8a9-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab8a9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ab8a9-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab8a9-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ab8a9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ab8a9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab8a9-140"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ab8a9-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab8a9-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab8a9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab8a9-142">**Ratteritem**</span><span class="sxs-lookup"><span data-stu-id="ab8a9-142">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="ab8a9-143">**Counters**</span><span class="sxs-lookup"><span data-stu-id="ab8a9-143">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="ab8a9-144">**Systemmonitor. browsekunden**</span><span class="sxs-lookup"><span data-stu-id="ab8a9-144">**SystemMonitor.BrowseCounters**</span></span>](systemmonitor-browsecounters.md)
</dt> </dl>

 

