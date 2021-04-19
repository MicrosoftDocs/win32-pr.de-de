---
title: Systemmonitor. ManualUpdate (Eigenschaft)
description: Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Inhalt des System Monitors manuell oder in angegebenen Intervallen automatisch aktualisiert wird.
ms.assetid: e068a955-ec1d-4f93-9261-25ba87773913
keywords:
- ManualUpdate-Eigenschaft (Sysmon)
- ManualUpdate-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", ManualUpdate (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.ManualUpdate
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1ecb426b47ba9cb7ec50b737f4f32d5ce274eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341605"
---
# <a name="systemmonitormanualupdate-property"></a><span data-ttu-id="7b10a-106">Systemmonitor. ManualUpdate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7b10a-106">SystemMonitor.ManualUpdate property</span></span>

<span data-ttu-id="7b10a-107">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Inhalt des System Monitors manuell oder in angegebenen Intervallen automatisch aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7b10a-107">Retrieves or sets a value indicating whether the contents of the System Monitor will be updated manually, or automatically at specified intervals.</span></span>

<span data-ttu-id="7b10a-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7b10a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b10a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b10a-109">Syntax</span></span>


```VB
Property ManualUpdate As Boolean
```



## <a name="property-value"></a><span data-ttu-id="7b10a-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7b10a-110">Property value</span></span>

<span data-ttu-id="7b10a-111">True gibt an, dass das Diagramm manuell aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7b10a-111">True indicates that graph is updated manually.</span></span> <span data-ttu-id="7b10a-112">False gibt an, dass das Diagramm automatisch basierend auf dem in [**Systemmonitor. updateingeterval**](systemmonitor-updateinterval.md)angegebenen Aktualisierungs Intervall aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7b10a-112">False indicates that the graph is updated automatically based on the update interval specified in [**SystemMonitor.UpdateInterval**](systemmonitor-updateinterval.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b10a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b10a-113">Remarks</span></span>

<span data-ttu-id="7b10a-114">Standardmäßig wird das Diagramm automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7b10a-114">By default, the graph is updated automatically.</span></span>

<span data-ttu-id="7b10a-115">Um das Diagramm manuell zu aktualisieren, wenden Sie die [**Systemmonitor. collectsample**](systemmonitor-collectsample.md) -Methode an.</span><span class="sxs-lookup"><span data-stu-id="7b10a-115">To update the graph manually, call the [**SystemMonitor.CollectSample**](systemmonitor-collectsample.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b10a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b10a-116">Requirements</span></span>



| <span data-ttu-id="7b10a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b10a-117">Requirement</span></span> | <span data-ttu-id="7b10a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7b10a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b10a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b10a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7b10a-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b10a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7b10a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b10a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7b10a-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b10a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7b10a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7b10a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b10a-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="7b10a-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b10a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b10a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b10a-126">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="7b10a-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="7b10a-127">**Systemmonitor. collectsample**</span><span class="sxs-lookup"><span data-stu-id="7b10a-127">**SystemMonitor.CollectSample**</span></span>](systemmonitor-collectsample.md)
</dt> <dt>

[<span data-ttu-id="7b10a-128">**Systemmonitor. updategraph**</span><span class="sxs-lookup"><span data-stu-id="7b10a-128">**SystemMonitor.UpdateGraph**</span></span>](systemmonitor-updategraph.md)
</dt> </dl>

 

 





