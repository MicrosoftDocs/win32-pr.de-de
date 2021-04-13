---
title: Systemmonitor. getlogviewrange-Methode
description: Ruft das Startdatum ab, das zum Abrufen von Counter-Werten aus den Protokolldateien verwendet wird.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Getlogviewrange-Methode (Sysmon)
- Getlogviewrange-Methode (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", getlogviewrange-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d494a5861ff9c0d2c076abe2bdad749d21653500
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517798"
---
# <a name="systemmonitorgetlogviewrange-method"></a><span data-ttu-id="ad296-106">Systemmonitor. getlogviewrange-Methode</span><span class="sxs-lookup"><span data-stu-id="ad296-106">SystemMonitor.GetLogViewRange method</span></span>

<span data-ttu-id="ad296-107">Ruft das Startdatum ab, das zum Abrufen von Counter-Werten aus den Protokolldateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad296-107">Retrieves the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad296-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad296-108">Syntax</span></span>


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="ad296-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad296-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad296-110">*StartTime* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ad296-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad296-111">Das Startdatum, das verwendet wird, um die Werte aus den Protokolldateien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ad296-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="ad296-112">*Stoppzeit* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ad296-112">*StopTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad296-113">Das Enddatum, das verwendet wird, um die Werte aus den Protokolldateien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ad296-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad296-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad296-114">Return value</span></span>

<span data-ttu-id="ad296-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ad296-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad296-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad296-116">Remarks</span></span>

<span data-ttu-id="ad296-117">Sysmon Ruft Werte aus den Protokolldateien ab, die in den Anfangs-und Enddatums Angaben (einschließlich) fallen.</span><span class="sxs-lookup"><span data-stu-id="ad296-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="ad296-118">Die Verwendung dieser Methode ist mit dem Zugriff auf die Eigenschaften [**Systemmonitor. logviewstart**](systemmonitor-logviewstart.md) und [**Systemmonitor. logviewstoppt**](systemmonitor-logviewstop.md) identisch.</span><span class="sxs-lookup"><span data-stu-id="ad296-118">Using this method is the same as accessing the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad296-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad296-119">Requirements</span></span>



| <span data-ttu-id="ad296-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad296-120">Requirement</span></span> | <span data-ttu-id="ad296-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ad296-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad296-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad296-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ad296-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad296-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ad296-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad296-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ad296-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad296-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad296-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ad296-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad296-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ad296-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad296-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad296-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad296-129">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="ad296-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="ad296-130">**Systemmonitor. setlogviewrange**</span><span class="sxs-lookup"><span data-stu-id="ad296-130">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





