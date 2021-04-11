---
title: Systemmonitor. Display Type (Eigenschaft)
description: Ruft den Diagrammtyp ab, der zum Diagramm der Leistungs Indikatorendaten verwendet wird, oder legt ihn fest.
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- DisplayType-Eigenschaft (Sysmon)
- DisplayType-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, Display Type (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103833"
---
# <a name="systemmonitordisplaytype-property"></a><span data-ttu-id="b5d17-106">Systemmonitor. Display Type (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b5d17-106">SystemMonitor.DisplayType property</span></span>

<span data-ttu-id="b5d17-107">Ruft den Diagrammtyp ab, der zum Diagramm der Leistungs Indikatorendaten verwendet wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="b5d17-107">Retrieves or sets the type of graph used to graph the performance counter data.</span></span>

<span data-ttu-id="b5d17-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b5d17-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d17-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5d17-109">Syntax</span></span>


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="b5d17-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b5d17-110">Property value</span></span>

<span data-ttu-id="b5d17-111">Der Diagrammtyp, der verwendet wird, um die Leistungsdaten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b5d17-111">Type of graph used to graph the performance counter data.</span></span> <span data-ttu-id="b5d17-112">Mögliche Werte finden Sie unter [**displaytypekonstanten**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span><span class="sxs-lookup"><span data-stu-id="b5d17-112">For possible values, see [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="b5d17-113">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="b5d17-113">Exceptions</span></span>



| <span data-ttu-id="b5d17-114">Ausnahmetyp</span><span class="sxs-lookup"><span data-stu-id="b5d17-114">Exception type</span></span>               | <span data-ttu-id="b5d17-115">Bedingung</span><span class="sxs-lookup"><span data-stu-id="b5d17-115">Condition</span></span>                                         |
|------------------------------|---------------------------------------------------|
| <span data-ttu-id="b5d17-116">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="b5d17-116">**System.ArgumentException**</span></span> | <span data-ttu-id="b5d17-117">Der angegebene Diagramm-oder Berichts Wert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b5d17-117">The specified graph or report value is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b5d17-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5d17-118">Requirements</span></span>



| <span data-ttu-id="b5d17-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5d17-119">Requirement</span></span> | <span data-ttu-id="b5d17-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b5d17-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d17-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5d17-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d17-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5d17-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b5d17-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5d17-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d17-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5d17-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5d17-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b5d17-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5d17-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b5d17-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5d17-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5d17-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d17-128">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="b5d17-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





