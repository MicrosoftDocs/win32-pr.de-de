---
title: Systemmonitor. chartscroll-Eigenschaft
description: Ruft einen Wert ab, der bestimmt, ob das Liniendiagramm in der Ansicht einen Bildlauf ausführt, oder legt diesen fest
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- Chartscroll-Eigenschaft (Sysmon)
- Chartscroll-Eigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt (Sysmon), chartscroll (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956570"
---
# <a name="systemmonitorchartscroll-property"></a><span data-ttu-id="5af40-106">Systemmonitor. chartscroll-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5af40-106">SystemMonitor.ChartScroll property</span></span>

<span data-ttu-id="5af40-107">Ruft einen Wert ab, der bestimmt, ob das Liniendiagramm in der Ansicht einen Bildlauf ausführt, oder legt diesen fest</span><span class="sxs-lookup"><span data-stu-id="5af40-107">Retrieves or sets a value that determines if the line graph scrolls in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="5af40-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5af40-108">Syntax</span></span>


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a><span data-ttu-id="5af40-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5af40-109">Property value</span></span>

<span data-ttu-id="5af40-110">True, wenn das Liniendiagramm von rechts nach links verschoben wird. andernfalls false, wenn das Liniendiagramm von links nach rechts gezeichnet wird und sich auf sich selbst in der Ansicht umschließt.</span><span class="sxs-lookup"><span data-stu-id="5af40-110">True if the line graph scrolls continuously from right to left; otherwise, False if the line graph is drawn from left to right and wraps around on itself in the view.</span></span> <span data-ttu-id="5af40-111">"False" ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="5af40-111">False is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="5af40-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5af40-112">Remarks</span></span>

<span data-ttu-id="5af40-113">Dieser Wert wird ignoriert, wenn [**System Monitor. Display Type**](systemmonitor-displaytype.md) nicht [**DisplayTypeConstants.sysmonlinegraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)ist.</span><span class="sxs-lookup"><span data-stu-id="5af40-113">This value is ignored if the [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="requirements"></a><span data-ttu-id="5af40-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5af40-114">Requirements</span></span>



| <span data-ttu-id="5af40-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5af40-115">Requirement</span></span> | <span data-ttu-id="5af40-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5af40-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5af40-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5af40-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5af40-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5af40-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5af40-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5af40-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5af40-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5af40-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5af40-121">DLL</span><span class="sxs-lookup"><span data-stu-id="5af40-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5af40-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5af40-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





