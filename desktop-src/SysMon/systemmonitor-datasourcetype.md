---
title: System Monitor DataSourceType (Eigenschaft)
description: Ruft die Quelle der Leistungsdaten des Leistungsindikators ab oder legt Sie fest.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- DataSourceType-Eigenschaft (Sysmon)
- DataSourceType-Eigenschaft (Sysmon), Systemmonitor-Schnittstelle
- Systemmonitor-Schnittstelle sysmon, DataSourceType (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a111d1e617745de1109f8359da158e642e93d17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040823"
---
# <a name="systemmonitordatasourcetype-property"></a><span data-ttu-id="5accf-106">Systemmonitor::D atasourcetype-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5accf-106">SystemMonitor::DataSourceType property</span></span>

<span data-ttu-id="5accf-107">Ruft die Quelle der Leistungsdaten des Leistungsindikators ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="5accf-107">Retrieves or sets the source of the performance counter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5accf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5accf-108">Syntax</span></span>


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="5accf-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5accf-109">Property value</span></span>

<span data-ttu-id="5accf-110">Quelle der Leistungsdaten.</span><span class="sxs-lookup"><span data-stu-id="5accf-110">Source of the performance counter data.</span></span> <span data-ttu-id="5accf-111">Mögliche Werte finden Sie unter [**datasourcetypeer Konstanten**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="5accf-111">For possible values, see [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="5accf-112">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="5accf-112">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5accf-113">Ausnahmetyp</span><span class="sxs-lookup"><span data-stu-id="5accf-113">Exception type</span></span></th>
<th><span data-ttu-id="5accf-114">Bedingung</span><span class="sxs-lookup"><span data-stu-id="5accf-114">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5accf-115"><strong>System.ArgumentException</strong></span><span class="sxs-lookup"><span data-stu-id="5accf-115"><strong>System.ArgumentException</strong></span></span></td>
<td><span data-ttu-id="5accf-116">Sie können diese Ausnahme aus einem der folgenden Gründe erhalten:</span><span class="sxs-lookup"><span data-stu-id="5accf-116">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="5accf-117">Der angegebene Datenquellen Wert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5accf-117">The specified data source value is not valid.</span></span></li>
<li><span data-ttu-id="5accf-118">Wenn es sich bei der Datenquelle um eine Protokolldatei handelt, kann von sysmon eine der angegebenen Dateien nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="5accf-118">If the data source is a log file, SYSMON cannot find one of the specified files.</span></span> <span data-ttu-id="5accf-119">Der Err. Number-Wert ist 0xc0000bd1.</span><span class="sxs-lookup"><span data-stu-id="5accf-119">The Err.Number value is 0xC0000BD1.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="5accf-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5accf-120">Remarks</span></span>

<span data-ttu-id="5accf-121">**Vor Windows Vista:** Sie können keine Protokolldateien aus der [**Protokolldatei Sammlung**](systemmonitor-logfiles.md) hinzufügen oder entfernen, wenn der Wert dieser Eigenschaft auf sysmonlogfiles festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5accf-121">**Prior to Windows Vista:** You cannot add or remove a log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of this property is set to sysmonLogFiles.</span></span> <span data-ttu-id="5accf-122">Legen Sie den Wert dieser Eigenschaft nach dem Erstellen oder Ändern der Protokolldatei Auflistung auf sysmonlogfiles fest.</span><span class="sxs-lookup"><span data-stu-id="5accf-122">Only set the value of this property to sysmonLogFiles after creating or modifying the log file collection.</span></span>

<span data-ttu-id="5accf-123">Außerdem können Sie die Eigenschaften [**sqldsnname**](systemmonitor-sqldsnname.md) und [**sqllogsetname**](systemmonitor-sqllogsetname.md) nicht ändern, wenn der Wert dieser Eigenschaft nicht auf sysmonsqllog festgelegt werden darf.</span><span class="sxs-lookup"><span data-stu-id="5accf-123">Also, you cannot modify the [**SqlDsnName**](systemmonitor-sqldsnname.md) and [**SqlLogSetName**](systemmonitor-sqllogsetname.md) properties if the value of this property must not be set to sysmonSqlLog.</span></span> <span data-ttu-id="5accf-124">Legen Sie den Wert dieser Eigenschaft nach dem Ändern der Server-und Datenbanknamen auf sysmonsqllog fest.</span><span class="sxs-lookup"><span data-stu-id="5accf-124">Only set the value of this property to sysmonSqlLog after modifying the server and database names.</span></span>

## <a name="requirements"></a><span data-ttu-id="5accf-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5accf-125">Requirements</span></span>



| <span data-ttu-id="5accf-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5accf-126">Requirement</span></span> | <span data-ttu-id="5accf-127">Wert</span><span class="sxs-lookup"><span data-stu-id="5accf-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5accf-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5accf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5accf-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5accf-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5accf-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5accf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5accf-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5accf-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5accf-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5accf-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5accf-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5accf-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5accf-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5accf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5accf-135">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="5accf-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





