---
title: System Monitor-browscounters-Methode
description: Zeigt das Dialogfeld Leistungsindikatoren hinzufügen an.
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- Browscounters-Methode (Sysmon)
- Browscounters-Methode (Sysmon), Systemmonitor-Schnittstelle
- Systemmonitor-Schnittstelle sysmon, browscounters-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96df5d50ab9fc89963f9d09f4c0cb92479b4ecac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040064"
---
# <a name="systemmonitorbrowsecounters-method"></a><span data-ttu-id="da22c-106">System Monitor:: browscounters-Methode</span><span class="sxs-lookup"><span data-stu-id="da22c-106">SystemMonitor::BrowseCounters method</span></span>

<span data-ttu-id="da22c-107">Zeigt das Dialogfeld Leistungsindikatoren **Hinzufügen** an.</span><span class="sxs-lookup"><span data-stu-id="da22c-107">Displays the **Add Counters** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="da22c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="da22c-108">Syntax</span></span>


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a><span data-ttu-id="da22c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="da22c-109">Parameters</span></span>

<span data-ttu-id="da22c-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="da22c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da22c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da22c-111">Return value</span></span>

<span data-ttu-id="da22c-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="da22c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da22c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da22c-113">Remarks</span></span>

<span data-ttu-id="da22c-114">In diesem Dialogfeld können Benutzer lokale oder Remote-Leistungsindikatoren aus einer Liste von Leistungs Objekten auswählen.</span><span class="sxs-lookup"><span data-stu-id="da22c-114">This dialog box lets the user select local or remote performance counters from a list of performance objects.</span></span> <span data-ttu-id="da22c-115">Die ausgewählten Leistungsindikatoren werden der [**Zähler**](counters.md) Sammlung hinzugefügt und im Diagramm oder Bericht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="da22c-115">The selected counters are added to the [**Counters**](counters.md) collection and displayed in the graph or report.</span></span>

<span data-ttu-id="da22c-116">Um eine Benachrichtigung zu erhalten, wenn ein Indikator hinzugefügt wird, implementieren Sie das [**oncounteradded**](systemmonitor-oncounteradded.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="da22c-116">To receive notification when a counter is added, implement the [**OnCounterAdded**](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="da22c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da22c-117">Requirements</span></span>



| <span data-ttu-id="da22c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da22c-118">Requirement</span></span> | <span data-ttu-id="da22c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="da22c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da22c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da22c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="da22c-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da22c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="da22c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da22c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="da22c-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da22c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da22c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="da22c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da22c-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="da22c-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da22c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da22c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da22c-127">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="da22c-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="da22c-128">**Zähler. Add**</span><span class="sxs-lookup"><span data-stu-id="da22c-128">**Counters.Add**</span></span>](counters-add.md)
</dt> </dl>

 

 





