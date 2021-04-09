---
title: Systemmonitor. logviewstoppt (Eigenschaft)
description: Ruft das Enddatum ab oder legt dieses fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- Logviewstoppt-Eigenschaft (Sysmon)
- Logviewstoppt-Eigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", logviewstopps (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStop
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b725ee2efba22453d44f1e15fb9ce231b07cdb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956428"
---
# <a name="systemmonitorlogviewstop-property"></a><span data-ttu-id="2bd4a-106">Systemmonitor. logviewstoppt (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2bd4a-106">SystemMonitor.LogViewStop property</span></span>

<span data-ttu-id="2bd4a-107">Ruft das Enddatum ab oder legt dieses fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-107">Retrieves or sets the ending date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="2bd4a-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bd4a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bd4a-109">Syntax</span></span>


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a><span data-ttu-id="2bd4a-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2bd4a-110">Property value</span></span>

<span data-ttu-id="2bd4a-111">Das Enddatum, das verwendet wird, um die Werte aus den Protokolldateien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-111">Ending date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bd4a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2bd4a-112">Remarks</span></span>

<span data-ttu-id="2bd4a-113">Sysmon Ruft Werte aus den Protokolldateien ab, die in den Dateien " [**Systemmonitor. logviewstart**](systemmonitor-logviewstart.md) " und "End Date" (einschließlich) fallen.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-113">SYSMON retrieves counter values from the log files that falls within the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and stop dates, inclusively.</span></span>

<span data-ttu-id="2bd4a-114">Wenn Sie keinen Endwert angeben oder wenn Sie diese Eigenschaft auf einen Datumswert festlegen, der nach dem letzten in der Protokolldatei enthaltenen Datum liegt, ändert sysmon den Wert in den letzten Datumswert, der in den Protokolldateien gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-114">If you do not specify a stop value or you set this property to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span>

<span data-ttu-id="2bd4a-115">Wenn diese Eigenschaft auf einen Datumswert festgelegt ist, der kleiner als [**logviewstart**](systemmonitor-logviewstart.md)ist, wird der Wert von sysmon in den **logviewstart**-Wert geändert.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-115">If this property is set to a date value that is less than [**LogViewStart**](systemmonitor-logviewstart.md), SYSMON changes the value to the value of **LogViewStart**.</span></span>

<span data-ttu-id="2bd4a-116">Sie müssen das Startdatum festlegen, bevor Sie das Enddatum festlegen. Andernfalls werden beide Werte auf Date. MinValue festgelegt. Wenn Sie die Datumsangaben nach dem Festlegen von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md)festlegen, wird nur der erste Leistungsindikatoren aus der Protokolldatei abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-116">You must set the start date before you set the stop date; otherwise, both values are set to Date.MinValue, and if you set the dates after setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md), then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd4a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bd4a-117">Requirements</span></span>



| <span data-ttu-id="2bd4a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bd4a-118">Requirement</span></span> | <span data-ttu-id="2bd4a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2bd4a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd4a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2bd4a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd4a-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bd4a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2bd4a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2bd4a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd4a-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bd4a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2bd4a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2bd4a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bd4a-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2bd4a-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bd4a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2bd4a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd4a-127">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="2bd4a-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="2bd4a-128">**Systemmonitor. getlogviewrange**</span><span class="sxs-lookup"><span data-stu-id="2bd4a-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="2bd4a-129">**Systemmonitor. logsourcestoptime**</span><span class="sxs-lookup"><span data-stu-id="2bd4a-129">**SystemMonitor.LogSourceStopTime**</span></span>](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[<span data-ttu-id="2bd4a-130">**Systemmonitor. logviewstart**</span><span class="sxs-lookup"><span data-stu-id="2bd4a-130">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="2bd4a-131">**Systemmonitor. setlogviewrange**</span><span class="sxs-lookup"><span data-stu-id="2bd4a-131">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





