---
title: Count. Value-Eigenschaft
description: Ruft den letzten samplingwert des Zählers ab.
ms.assetid: c5aeaa00-e185-484d-8a7a-d45a21690e20
keywords:
- Eigenschafts-sysmon
- Value-Eigenschaft (Sysmon), ratteritem-Klasse
- Namteritem Class sysmon, Value-Eigenschaft
topic_type:
- apiref
api_name:
- CounterItem.Value
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c0d6bd9e1751e34c980bc95f790314017eeb49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342215"
---
# <a name="counteritemvalue-property"></a><span data-ttu-id="385d1-106">Count. Value-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="385d1-106">CounterItem.Value property</span></span>

<span data-ttu-id="385d1-107">Ruft den letzten samplingwert des Zählers ab.</span><span class="sxs-lookup"><span data-stu-id="385d1-107">Retrieves the last sampled value of the counter.</span></span>

<span data-ttu-id="385d1-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="385d1-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="385d1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="385d1-109">Syntax</span></span>


```VB
Property Value As Double
```



## <a name="property-value"></a><span data-ttu-id="385d1-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="385d1-110">Property value</span></span>

<span data-ttu-id="385d1-111">Der zuletzt erfasste Wert des Zählers.</span><span class="sxs-lookup"><span data-stu-id="385d1-111">Last sampled value of the counter.</span></span> <span data-ttu-id="385d1-112">Der Wert ist-1, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="385d1-112">The value is -1 if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="385d1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="385d1-113">Remarks</span></span>

<span data-ttu-id="385d1-114">Dies ist die Standard Eigenschaft des [**ratteritem**](counteritem.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="385d1-114">This is the default property of the [**CounterItem**](counteritem.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="385d1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="385d1-115">Requirements</span></span>



| <span data-ttu-id="385d1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="385d1-116">Requirement</span></span> | <span data-ttu-id="385d1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="385d1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="385d1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="385d1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="385d1-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="385d1-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="385d1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="385d1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="385d1-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="385d1-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="385d1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="385d1-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="385d1-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="385d1-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="385d1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="385d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="385d1-125">**Ratteritem**</span><span class="sxs-lookup"><span data-stu-id="385d1-125">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="385d1-126">**"Count. GetValue"**</span><span class="sxs-lookup"><span data-stu-id="385d1-126">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





