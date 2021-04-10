---
title: Systemmonitor. Counters (Eigenschaft)
description: Ruft die Zähler ab, die eine Auflistung von "count"-Objekten enthalten.
ms.assetid: eab21e1f-c8fb-474c-83e3-5ef56483d525
keywords:
- Leistungsindikator Eigenschaft (Sysmon)
- Leistungsindikator Eigenschaft "sysmon", Systemmonitor-Klasse
- Systemmonitor-Klasse (Sysmon), Counters-Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e09cc797c09033e90ba4d584ee63336a52cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103989"
---
# <a name="systemmonitorcounters-property"></a><span data-ttu-id="0b1e3-106">Systemmonitor. Counters (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0b1e3-106">SystemMonitor.Counters property</span></span>

<span data-ttu-id="0b1e3-107">Ruft die **Zähler** ab, die eine Auflistung von " [**count**](counteritem.md) "-Objekten enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b1e3-107">Retrieves the **Counters** which contains a collection of [**CounterItem**](counteritem.md) objects.</span></span>

<span data-ttu-id="0b1e3-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0b1e3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b1e3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b1e3-109">Syntax</span></span>


```VB
Property Counters As ICounters
```



## <a name="property-value"></a><span data-ttu-id="0b1e3-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0b1e3-110">Property value</span></span>

<span data-ttu-id="0b1e3-111">Ein **indikatorenobjekt, das eine Auflistung** von " [**count**](counteritem.md) "-Objekten enthält.</span><span class="sxs-lookup"><span data-stu-id="0b1e3-111">A **Counters** object that contains a collection of [**CounterItem**](counteritem.md) objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b1e3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b1e3-112">Remarks</span></span>

<span data-ttu-id="0b1e3-113">Dies ist die Standard Eigenschaft des [**Systemmonitor**](systemmonitor.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0b1e3-113">This is the default property of the [**SystemMonitor**](systemmonitor.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b1e3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b1e3-114">Requirements</span></span>



| <span data-ttu-id="0b1e3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b1e3-115">Requirement</span></span> | <span data-ttu-id="0b1e3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0b1e3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b1e3-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b1e3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0b1e3-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b1e3-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0b1e3-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b1e3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0b1e3-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b1e3-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b1e3-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0b1e3-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b1e3-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="0b1e3-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b1e3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b1e3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b1e3-124">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="0b1e3-124">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





