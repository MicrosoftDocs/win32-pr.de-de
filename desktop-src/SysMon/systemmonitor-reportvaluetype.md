---
title: Systemmonitor. reportvaluetype (Eigenschaft)
description: Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob im Histogramm und in den Berichts Ansichten der letzte Wert, der während des Samplingintervalls Stichprobe oder ein berechneter Wert aus der Stichprobe erfasst wurde
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- Reportvaluetype-Eigenschaft (Sysmon)
- Reportvaluetype-Eigenschaft sysmon, Systemmonitor-Klasse
- Systemmonitor-Klasse (Sysmon), reportvaluetype-Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc340516f1d99bb77dcc5a31c03eb189d2d70a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956426"
---
# <a name="systemmonitorreportvaluetype-property"></a><span data-ttu-id="886db-106">Systemmonitor. reportvaluetype (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="886db-106">SystemMonitor.ReportValueType property</span></span>

<span data-ttu-id="886db-107">Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob im Histogramm und in den Berichts Ansichten der letzte Wert, der während des Samplingintervalls Stichprobe oder ein berechneter Wert aus der Stichprobe erfasst wurde</span><span class="sxs-lookup"><span data-stu-id="886db-107">Retrieves or sets a value that determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling, such as the average or minimum counter value.</span></span>

<span data-ttu-id="886db-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="886db-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="886db-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="886db-109">Syntax</span></span>


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="886db-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="886db-110">Property value</span></span>

<span data-ttu-id="886db-111">Bestimmt, ob das Histogramm und die Berichts Sichten den letzten Wert, der während des Samplingintervalls als Stichprobe oder einen berechneten Wert aus dem Samplingintervall</span><span class="sxs-lookup"><span data-stu-id="886db-111">Determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling interval.</span></span> <span data-ttu-id="886db-112">Mögliche Werte finden Sie unter [**reportvaluetypeer Konstanten**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="886db-112">For possible values, see [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).</span></span>

## <a name="remarks"></a><span data-ttu-id="886db-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="886db-113">Remarks</span></span>

<span data-ttu-id="886db-114">Sysmon ignoriert diesen Wert und verwendet [**ReportValueTypeConstants.sysmondefaultvalue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) , wenn [**Systemmonitor. DisplayType**](systemmonitor-displaytype.md) nicht [**DisplayTypeConstants.sysmonhistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) oder **DisplayTypeConstants.sysmonreport** ist.</span><span class="sxs-lookup"><span data-stu-id="886db-114">SYSMON ignores this value and uses [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) if [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) or **DisplayTypeConstants.sysmonReport**.</span></span>

## <a name="requirements"></a><span data-ttu-id="886db-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="886db-115">Requirements</span></span>



| <span data-ttu-id="886db-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="886db-116">Requirement</span></span> | <span data-ttu-id="886db-117">Wert</span><span class="sxs-lookup"><span data-stu-id="886db-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="886db-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="886db-118">Minimum supported client</span></span><br/> | <span data-ttu-id="886db-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="886db-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="886db-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="886db-120">Minimum supported server</span></span><br/> | <span data-ttu-id="886db-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="886db-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="886db-122">DLL</span><span class="sxs-lookup"><span data-stu-id="886db-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="886db-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="886db-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="886db-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="886db-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="886db-125">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="886db-125">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





