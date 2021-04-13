---
title: Systemmonitor. setlogviewrange-Methode
description: Legt das Startdatum fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.
ms.assetid: ced641d0-cf71-4826-8ff0-c05f20a71aaa
keywords:
- Setlogviewrange-Methode (Sysmon)
- Setlogviewrange-Methode (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", setlogviewrange-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.SetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534a7dc3bf711832ec99e4202f4f56cc347f336b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391703"
---
# <a name="systemmonitorsetlogviewrange-method"></a><span data-ttu-id="a3d3e-106">Systemmonitor. setlogviewrange-Methode</span><span class="sxs-lookup"><span data-stu-id="a3d3e-106">SystemMonitor.SetLogViewRange method</span></span>

<span data-ttu-id="a3d3e-107">Legt das Startdatum fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3d3e-107">Sets the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d3e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3d3e-108">Syntax</span></span>


```VB
SystemMonitor.SetLogViewRange( _
  ByVal StartTime As Date, _
  ByVal StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="a3d3e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3d3e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3d3e-110">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d3e-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d3e-111">Das Startdatum, das verwendet wird, um die Werte aus den Protokolldateien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a3d3e-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="a3d3e-112">*Stoppzeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d3e-112">*StopTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d3e-113">Das Enddatum, das verwendet wird, um die Werte aus den Protokolldateien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a3d3e-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3d3e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3d3e-114">Return value</span></span>

<span data-ttu-id="a3d3e-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a3d3e-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3d3e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3d3e-116">Remarks</span></span>

<span data-ttu-id="a3d3e-117">Sysmon Ruft Werte aus den Protokolldateien ab, die in den Anfangs-und Enddatums Angaben (einschließlich) fallen.</span><span class="sxs-lookup"><span data-stu-id="a3d3e-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="a3d3e-118">Wenn Sie kein Startdatum angeben oder wenn Sie das Startdatum auf einen Datumswert festlegen, der außerhalb des Bereichs der in den Protokolldateien gefundenen Datumswerte liegt, wird der Wert von sysmon in den frühesten in den Protokolldateien gefundenen Datumswert geändert.</span><span class="sxs-lookup"><span data-stu-id="a3d3e-118">If you do not specify a start date or if you set the start date to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span> <span data-ttu-id="a3d3e-119">Wenn der Startwert größer als der Endzeit Wert ist, ändert sysmon den Startwert so, dass er mit dem Wert des Endwerts identisch ist.</span><span class="sxs-lookup"><span data-stu-id="a3d3e-119">If the start value is greater than the stop value, SYSMON changes the start value to be the same value as the stop value.</span></span>

<span data-ttu-id="a3d3e-120">Wenn Sie keinen Endwert angeben oder den Wert für die Beendigung auf einen Datumswert festlegen, der nach dem letzten in der Protokolldatei befindlichen Datum liegt, ändert sysmon den Wert in den letzten Datumswert, der in den Protokolldateien gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="a3d3e-120">If you do not specify a stop value or you set the stop value to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span> <span data-ttu-id="a3d3e-121">Wenn der Wert für die Beendigung kleiner ist als der Wert für die Beendigung, ändert sysmon den Endzeit Wert, sodass er dem Wert des Startwerts entspricht.</span><span class="sxs-lookup"><span data-stu-id="a3d3e-121">If the stop value is less than the stop value, SYSMON changes the stop value to be the same value as the start value.</span></span>

<span data-ttu-id="a3d3e-122">Wenn Sie ein Start-und ein Enddatum angeben, sollten Sie die Datumsangaben vor dem Festlegen von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="a3d3e-122">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span> <span data-ttu-id="a3d3e-123">Wenn Sie die Datumsangaben nach dem Festlegen von **Systemmonitor. DataSourceType** festlegen, wird nur der erste Leistungsindikatoren aus der Protokolldatei abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a3d3e-123">If you set the dates after setting **SystemMonitor.DataSourceType**, then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d3e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3d3e-124">Requirements</span></span>



| <span data-ttu-id="a3d3e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3d3e-125">Requirement</span></span> | <span data-ttu-id="a3d3e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a3d3e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3d3e-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3d3e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a3d3e-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3d3e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a3d3e-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3d3e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a3d3e-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3d3e-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3d3e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a3d3e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3d3e-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a3d3e-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3d3e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3d3e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3d3e-134">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="a3d3e-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="a3d3e-135">**Systemmonitor. getlogviewrange**</span><span class="sxs-lookup"><span data-stu-id="a3d3e-135">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> </dl>

 

 





