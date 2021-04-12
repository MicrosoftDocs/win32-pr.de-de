---
title: Freerepirren infoexs-Funktion (ndattributils. h)
description: Hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von repairiinfoex-Strukturen auf.
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- Freerepirren infoexs-Funktion NDF
topic_type:
- apiref
api_name:
- FreeRepairInfoExs
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094c745486526caa870a500019de3aa819b6fe5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517927"
---
# <a name="freerepairinfoexs-function"></a><span data-ttu-id="12261-104">Freerepirren infoexs-Funktion</span><span class="sxs-lookup"><span data-stu-id="12261-104">FreeRepairInfoExs function</span></span>

<span data-ttu-id="12261-105">Die **freerepirren infoexs** -Funktion hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array der [**repauninfoex**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) -Strukturen auf.</span><span class="sxs-lookup"><span data-stu-id="12261-105">The **FreeRepairInfoExs** function deallocates the memory allocated internally to an array of [**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) structures.</span></span> <span data-ttu-id="12261-106">Diese Funktion ruft [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um den Speicherplatz freizugeben.</span><span class="sxs-lookup"><span data-stu-id="12261-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="12261-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="12261-107">Syntax</span></span>


```C++
VOID FreeRepairInfoExs(
  _In_ RepairInfoEx *pInfo,
       ULONG        RepairCount,
       BOOL         bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="12261-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="12261-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12261-109">*pinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12261-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12261-110">Geben Sie Folgendes ein: \**[**repairren INFOEX**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) \** _</span><span class="sxs-lookup"><span data-stu-id="12261-110">Type: \**[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)\** _</span></span>

<span data-ttu-id="12261-111">Das Array von-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="12261-111">The array of structures.</span></span> <span data-ttu-id="12261-112">Der zugewiesene Speicher, auf den diese Strukturen zeigen, wird freigegeben.</span><span class="sxs-lookup"><span data-stu-id="12261-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="12261-113">_RepairCount \*</span><span class="sxs-lookup"><span data-stu-id="12261-113">_RepairCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="12261-114">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="12261-114">Type: **ULONG**</span></span>

<span data-ttu-id="12261-115">Die Anzahl der Strukturen im Array, auf die von *pinfo* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="12261-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="12261-116">*bfrepointer*</span><span class="sxs-lookup"><span data-stu-id="12261-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="12261-117">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="12261-117">Type: **BOOL**</span></span>

<span data-ttu-id="12261-118">True, wenn das Array von-Strukturen ebenfalls gelöscht werden soll. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="12261-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12261-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12261-119">Return value</span></span>

<span data-ttu-id="12261-120">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="12261-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="12261-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12261-121">Requirements</span></span>



| <span data-ttu-id="12261-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12261-122">Requirement</span></span> | <span data-ttu-id="12261-123">Wert</span><span class="sxs-lookup"><span data-stu-id="12261-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="12261-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12261-124">Minimum supported client</span></span><br/> | <span data-ttu-id="12261-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12261-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="12261-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12261-126">Minimum supported server</span></span><br/> | <span data-ttu-id="12261-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12261-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="12261-128">Header</span><span class="sxs-lookup"><span data-stu-id="12261-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="12261-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="12261-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12261-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12261-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12261-131">**Repairren INFOEX**</span><span class="sxs-lookup"><span data-stu-id="12261-131">**RepairInfoEx**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[<span data-ttu-id="12261-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="12261-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

