---
title: Systemmonitor. logviewstart (Eigenschaft)
description: Ruft das Startdatum ab oder legt dieses fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- Logviewstart-Eigenschaft (Sysmon)
- Logviewstart-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, logviewstart (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStart
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967c44940b195c4d8ddd3028e1d4f307827bbbfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949746"
---
# <a name="systemmonitorlogviewstart-property"></a><span data-ttu-id="141ad-106">Systemmonitor. logviewstart (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="141ad-106">SystemMonitor.LogViewStart property</span></span>

<span data-ttu-id="141ad-107">Ruft das Startdatum ab oder legt dieses fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="141ad-107">Retrieves or sets the starting date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="141ad-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="141ad-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="141ad-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="141ad-109">Syntax</span></span>


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a><span data-ttu-id="141ad-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="141ad-110">Property value</span></span>

<span data-ttu-id="141ad-111">Das Startdatum, das verwendet wird, um die Werte aus den Protokolldateien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="141ad-111">Starting date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="141ad-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="141ad-112">Remarks</span></span>

<span data-ttu-id="141ad-113">Sysmon Ruft Werte aus den Protokolldateien ab, die in den Datumsangaben "Start" und " [**Systemmonitor. logviewend**](systemmonitor-logviewstop.md) " fallen.</span><span class="sxs-lookup"><span data-stu-id="141ad-113">SYSMON retrieves counter values from the log files that falls within the start and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) dates, inclusively.</span></span>

<span data-ttu-id="141ad-114">Wenn Sie kein Startdatum angeben oder wenn Sie diese Eigenschaft auf einen Datumswert festlegen, der außerhalb des Bereichs der in den Protokolldateien gefundenen Datumswerte liegt, wird der Wert von sysmon in den frühesten in den Protokolldateien gefundenen Datumswert geändert.</span><span class="sxs-lookup"><span data-stu-id="141ad-114">If you do not specify a start date or if you set this property to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span>

<span data-ttu-id="141ad-115">Wenn diese Eigenschaft auf einen Datumswert festgelegt ist, der größer als [**logviewstoppt**](systemmonitor-logviewstop.md)ist, wird der Wert von sysmon in den Wert von **logviewstoppt** geändert.</span><span class="sxs-lookup"><span data-stu-id="141ad-115">If this property is set to a date value that is greater than [**LogViewStop**](systemmonitor-logviewstop.md), SYSMON changes the value to the value of **LogViewStop**.</span></span>

<span data-ttu-id="141ad-116">Wenn Sie ein Start-und ein Enddatum angeben, sollten Sie die Datumsangaben vor dem Festlegen von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="141ad-116">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="141ad-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="141ad-117">Requirements</span></span>



| <span data-ttu-id="141ad-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="141ad-118">Requirement</span></span> | <span data-ttu-id="141ad-119">Wert</span><span class="sxs-lookup"><span data-stu-id="141ad-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="141ad-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="141ad-120">Minimum supported client</span></span><br/> | <span data-ttu-id="141ad-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="141ad-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="141ad-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="141ad-122">Minimum supported server</span></span><br/> | <span data-ttu-id="141ad-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="141ad-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="141ad-124">DLL</span><span class="sxs-lookup"><span data-stu-id="141ad-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="141ad-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="141ad-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="141ad-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="141ad-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="141ad-127">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="141ad-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="141ad-128">**Systemmonitor. getlogviewrange**</span><span class="sxs-lookup"><span data-stu-id="141ad-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="141ad-129">**Systemmonitor. Logfiles**</span><span class="sxs-lookup"><span data-stu-id="141ad-129">**SystemMonitor.LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> <dt>

[<span data-ttu-id="141ad-130">**Systemmonitor. logviewstoppt**</span><span class="sxs-lookup"><span data-stu-id="141ad-130">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="141ad-131">**Systemmonitor. logsourcestarttime**</span><span class="sxs-lookup"><span data-stu-id="141ad-131">**SystemMonitor.LogSourceStartTime**</span></span>](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[<span data-ttu-id="141ad-132">**Systemmonitor. setlogviewrange**</span><span class="sxs-lookup"><span data-stu-id="141ad-132">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





