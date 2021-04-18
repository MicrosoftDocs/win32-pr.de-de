---
title: Systemmonitor. Logfiles (Eigenschaft)
description: Sammlung von einer oder mehreren Protokolldateien, die als Quelle der im System Monitor angezeigten Indikatoren verwendet werden sollen.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Logfiles-Eigenschaft (Sysmon)
- Logfiles-Eigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", Logfiles (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8127433319290b44498b272834923784b714052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340329"
---
# <a name="systemmonitorlogfiles-property"></a><span data-ttu-id="7df24-106">Systemmonitor. Logfiles (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7df24-106">SystemMonitor.LogFiles property</span></span>

<span data-ttu-id="7df24-107">Sammlung von einer oder mehreren Protokolldateien, die als Quelle der im System Monitor angezeigten Indikatoren verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7df24-107">Collection of one or more log files to use as the source of counter values displayed in the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df24-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7df24-108">Syntax</span></span>


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a><span data-ttu-id="7df24-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7df24-109">Property value</span></span>

<span data-ttu-id="7df24-110">Sammlung von [**logfileitem**](logfileitem.md) -Objekten, die die Protokolldateien angeben, die als Datenquelle für das Diagramm verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7df24-110">Collection of [**LogFileItem**](logfileitem.md) objects that specify the log files used as the data source for the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="7df24-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7df24-111">Remarks</span></span>

<span data-ttu-id="7df24-112">Der Wert von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) darf nicht auf sysmonlogfiles festgelegt werden, um eine Protokolldatei in der Protokolldatei Sammlung hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="7df24-112">To add or remove a log file from the log file collection, the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) must not be set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="7df24-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7df24-113">Requirements</span></span>



| <span data-ttu-id="7df24-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7df24-114">Requirement</span></span> | <span data-ttu-id="7df24-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7df24-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7df24-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7df24-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7df24-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7df24-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7df24-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7df24-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7df24-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7df24-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7df24-120">DLL</span><span class="sxs-lookup"><span data-stu-id="7df24-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7df24-121"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="7df24-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df24-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7df24-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df24-123">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="7df24-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="7df24-124">**Systemmonitor. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="7df24-124">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> <dt>

[<span data-ttu-id="7df24-125">**Systemmonitor. logviewstart**</span><span class="sxs-lookup"><span data-stu-id="7df24-125">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="7df24-126">**Systemmonitor. logviewstoppt**</span><span class="sxs-lookup"><span data-stu-id="7df24-126">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="7df24-127">**Systemmonitor. sqllogsetname**</span><span class="sxs-lookup"><span data-stu-id="7df24-127">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





