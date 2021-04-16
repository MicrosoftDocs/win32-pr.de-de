---
title: System Monitor collectsample-Methode
description: Gibt einen Wert für jeden Zähler im Counter-Objekt an.
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- Collectsample-Methode (Sysmon)
- Collectsample-Methode (Sysmon), Systemmonitor-Schnittstelle
- Systemmonitor-Schnittstelle sysmon, collectsample-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.CollectSample
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1c269d044c17a2ec1322fa969e0c86f468a901
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477097"
---
# <a name="systemmonitorcollectsample-method"></a><span data-ttu-id="c746e-106">Systemmonitor:: collectsample-Methode</span><span class="sxs-lookup"><span data-stu-id="c746e-106">SystemMonitor::CollectSample method</span></span>

<span data-ttu-id="c746e-107">Gibt einen Wert für jeden Zähler [**im Counter-Objekt an**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="c746e-107">Samples a value for each counter in the [**Counters**](counters.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c746e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c746e-108">Syntax</span></span>


```VB
Sub CollectSample()
```



## <a name="parameters"></a><span data-ttu-id="c746e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c746e-109">Parameters</span></span>

<span data-ttu-id="c746e-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c746e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c746e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c746e-111">Return value</span></span>

<span data-ttu-id="c746e-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c746e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c746e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c746e-113">Remarks</span></span>

<span data-ttu-id="c746e-114">" **Collectsample** " nur dann aufzurufen, wenn " [**ManualUpdate**](systemmonitor-manualupdate.md) " den Wert "true" hat und Sie Stichprobenwerte aus der aktuellen Aktivität des Computers verwenden, verwenden Sie diese Methode nicht, wenn Sie eine Stichprobenentnahme</span><span class="sxs-lookup"><span data-stu-id="c746e-114">Call **CollectSample** only if [**ManualUpdate**](systemmonitor-manualupdate.md) is True and you are sampling counter values from the current activity of the computer do not use this method when sampling from a log file.</span></span> <span data-ttu-id="c746e-115">Das Diagramm oder der Bericht wird mit dem neuen Wert aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c746e-115">The graph or report is updated with the new value.</span></span> <span data-ttu-id="c746e-116">Beachten Sie, dass für einige Arten von Diagrammen zwei Beispiele erforderlich sind, um die Daten zu Graphen, z. b. das Liniendiagramm.</span><span class="sxs-lookup"><span data-stu-id="c746e-116">Note that some types of graphs need two samples in order to graph the data, for example, the line graph.</span></span>

<span data-ttu-id="c746e-117">Implementieren Sie das [**onsamplegesammel-**](-systemmonitor-onsamplecollected.md) Ereignis, um eine Benachrichtigung zu erhalten, wenn das Beispiel erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="c746e-117">To receive notification when the sample has been collected, implement the [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="c746e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c746e-118">Requirements</span></span>



| <span data-ttu-id="c746e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c746e-119">Requirement</span></span> | <span data-ttu-id="c746e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c746e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c746e-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c746e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c746e-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c746e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c746e-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c746e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c746e-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c746e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c746e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c746e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c746e-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="c746e-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c746e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c746e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c746e-128">**Counters**</span><span class="sxs-lookup"><span data-stu-id="c746e-128">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="c746e-129">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="c746e-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





