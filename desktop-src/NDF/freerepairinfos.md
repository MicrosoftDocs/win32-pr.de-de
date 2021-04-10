---
title: Freerepirren Infos-Funktion (ndattributils. h)
description: Hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von repairren Info-Strukturen auf.
ms.assetid: c40f9d10-8d9e-4c79-ac0b-fa88608888f1
keywords:
- Freerepaarinfos-Funktion NDF
topic_type:
- apiref
api_name:
- FreeRepairInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63bf6ab2154376302e4c9dd076ccaf83a0c565c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103287"
---
# <a name="freerepairinfos-function"></a><span data-ttu-id="ca221-104">Freerepirren Infos-Funktion</span><span class="sxs-lookup"><span data-stu-id="ca221-104">FreeRepairInfos function</span></span>

<span data-ttu-id="ca221-105">Die **freerepirren Infos** -Funktion hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von [**repauninfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) -Strukturen auf.</span><span class="sxs-lookup"><span data-stu-id="ca221-105">The **FreeRepairInfos** function deallocates the memory allocated internally to an array of [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structures.</span></span> <span data-ttu-id="ca221-106">Diese Funktion ruft [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um den Speicherplatz freizugeben.</span><span class="sxs-lookup"><span data-stu-id="ca221-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca221-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca221-107">Syntax</span></span>


```C++
VOID FreeRepairInfos(
  _In_ RepairInfo *pInfo,
       ULONG      RepairCount,
       BOOL       bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="ca221-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca221-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca221-109">*pinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca221-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca221-110">Geben Sie Folgendes ein: \**[**repairren Info**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="ca221-110">Type: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="ca221-111">Das Array von-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="ca221-111">The array of structures.</span></span> <span data-ttu-id="ca221-112">Der zugewiesene Speicher, auf den diese Strukturen zeigen, wird freigegeben.</span><span class="sxs-lookup"><span data-stu-id="ca221-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="ca221-113">_RepairCount \*</span><span class="sxs-lookup"><span data-stu-id="ca221-113">_RepairCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="ca221-114">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="ca221-114">Type: **ULONG**</span></span>

<span data-ttu-id="ca221-115">Die Anzahl der Strukturen im Array, auf die von *pinfo* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ca221-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="ca221-116">*bfrepointer*</span><span class="sxs-lookup"><span data-stu-id="ca221-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="ca221-117">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="ca221-117">Type: **BOOL**</span></span>

<span data-ttu-id="ca221-118">True, wenn das Array von-Strukturen ebenfalls gelöscht werden soll. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="ca221-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca221-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca221-119">Return value</span></span>

<span data-ttu-id="ca221-120">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ca221-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca221-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca221-121">Requirements</span></span>



| <span data-ttu-id="ca221-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca221-122">Requirement</span></span> | <span data-ttu-id="ca221-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ca221-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca221-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca221-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ca221-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca221-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ca221-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca221-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ca221-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca221-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ca221-128">Header</span><span class="sxs-lookup"><span data-stu-id="ca221-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca221-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca221-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca221-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca221-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca221-131">**Repairren Info**</span><span class="sxs-lookup"><span data-stu-id="ca221-131">**RepairInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> <dt>

[<span data-ttu-id="ca221-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="ca221-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

