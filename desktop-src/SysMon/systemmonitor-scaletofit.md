---
title: System Monitor. scaledefit-Methode
description: Skalierungs Wert Werte, die in das Diagramm passen.
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- Scaledefit-Methode (Sysmon)
- Scaledefit-Methode (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", scaledefit-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.ScaleToFit
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1e481dd44c441ea9e2dd44f2e63a06539da74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741112"
---
# <a name="systemmonitorscaletofit-method"></a><span data-ttu-id="cc977-106">System Monitor. scaledefit-Methode</span><span class="sxs-lookup"><span data-stu-id="cc977-106">SystemMonitor.ScaleToFit method</span></span>

<span data-ttu-id="cc977-107">Skalierungs Wert Werte, die in das Diagramm passen.</span><span class="sxs-lookup"><span data-stu-id="cc977-107">Scale counter values to fit in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc977-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc977-108">Syntax</span></span>


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a><span data-ttu-id="cc977-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc977-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc977-110">*selectedcountersonly* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc977-110">*selectedCountersOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc977-111">True, wenn nur die ausgewählten Indikatoren skaliert werden sollen. andernfalls false, um alle Indikatoren zu skalieren.</span><span class="sxs-lookup"><span data-stu-id="cc977-111">True to scale only the selected counters; otherwise, false to scale all counters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc977-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc977-112">Return value</span></span>

<span data-ttu-id="cc977-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cc977-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc977-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc977-114">Remarks</span></span>

<span data-ttu-id="cc977-115">Mit dieser Methode wird die Diagramm Ansicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cc977-115">This method will clear the graph view.</span></span> <span data-ttu-id="cc977-116">Sysmon verwendet dann den für jeden Zählers angegebenen Skalierungsfaktor, um das Diagramm neu zu zeichnen, wenn es sich bei der Datenquelle um eine Protokolldatei handelt, oder um neue Werte zu erstellen, wenn die Datenquelle eine echt Zeit Aktivität ist.</span><span class="sxs-lookup"><span data-stu-id="cc977-116">SYSMON then uses the scale factor specified for each counter to redraw the graph if the data source is a log file, or begin graphing new counter values if the data source is real time activity.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc977-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc977-117">Requirements</span></span>



| <span data-ttu-id="cc977-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc977-118">Requirement</span></span> | <span data-ttu-id="cc977-119">Wert</span><span class="sxs-lookup"><span data-stu-id="cc977-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc977-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc977-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cc977-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc977-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc977-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc977-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cc977-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc977-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc977-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cc977-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc977-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="cc977-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc977-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc977-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc977-127">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="cc977-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="cc977-128">**"Count. scalefactor"**</span><span class="sxs-lookup"><span data-stu-id="cc977-128">**CounterItem.ScaleFactor**</span></span>](counteritem-scalefactor.md)
</dt> <dt>

[<span data-ttu-id="cc977-129">**"Zählelement. ausgewählt"**</span><span class="sxs-lookup"><span data-stu-id="cc977-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





