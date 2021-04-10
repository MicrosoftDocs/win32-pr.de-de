---
title: Systemmonitor. datapointcount-Eigenschaft
description: Ruft die Anzahl der Datenpunkte ab, die in einem Liniendiagramm angezeigt werden, oder legt Sie fest.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Datapointcount-Eigenschaft (Sysmon)
- Datapointcount-Eigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", datapointcount (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949649"
---
# <a name="systemmonitordatapointcount-property"></a><span data-ttu-id="afe5a-106">Systemmonitor. datapointcount-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="afe5a-106">SystemMonitor.DataPointCount property</span></span>

<span data-ttu-id="afe5a-107">Ruft die Anzahl der Datenpunkte ab, die in einem Liniendiagramm angezeigt werden, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="afe5a-107">Retrieves or sets the number of data points displayed in a line graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="afe5a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="afe5a-108">Syntax</span></span>


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a><span data-ttu-id="afe5a-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="afe5a-109">Property value</span></span>

<span data-ttu-id="afe5a-110">Anzahl von Datenpunkten, die in der Ansicht für ein Liniendiagramm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="afe5a-110">Number of data points displayed in the view for a line graph.</span></span> <span data-ttu-id="afe5a-111">Der Standardwert ist 100 Datenpunkte.</span><span class="sxs-lookup"><span data-stu-id="afe5a-111">The default value is 100 data points.</span></span> <span data-ttu-id="afe5a-112">Der gültige Wertebereich ist 2 bis 1.000.</span><span class="sxs-lookup"><span data-stu-id="afe5a-112">The valid range of values is 2 to 1,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="afe5a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afe5a-113">Remarks</span></span>

<span data-ttu-id="afe5a-114">Diese Eigenschaft wird nur verwendet, wenn [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) **sysmoncurrentactivity** ist.</span><span class="sxs-lookup"><span data-stu-id="afe5a-114">This property is used only if [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is **sysmonCurrentActivity**.</span></span>

## <a name="requirements"></a><span data-ttu-id="afe5a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afe5a-115">Requirements</span></span>



| <span data-ttu-id="afe5a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afe5a-116">Requirement</span></span> | <span data-ttu-id="afe5a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="afe5a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afe5a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afe5a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="afe5a-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afe5a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="afe5a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afe5a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="afe5a-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afe5a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afe5a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="afe5a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afe5a-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="afe5a-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





