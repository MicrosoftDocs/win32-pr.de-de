---
title: Freerootkauseinfos-Funktion (ndattributils. h)
description: Hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von rootkauseingefo-Strukturen auf.
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- Freerootcauseingefos-Funktion NDF
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d302a1c58f1a77aafa7611f437f3d445f29f9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740896"
---
# <a name="freerootcauseinfos-function"></a><span data-ttu-id="36550-104">Freerootkausan Fos-Funktion</span><span class="sxs-lookup"><span data-stu-id="36550-104">FreeRootCauseInfos function</span></span>

<span data-ttu-id="36550-105">Die **freerootkausan Fos** -Funktion hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von [**rootkauseingefo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) -Strukturen auf.</span><span class="sxs-lookup"><span data-stu-id="36550-105">The **FreeRootCauseInfos** function deallocates the memory allocated internally to an array of [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) structures.</span></span> <span data-ttu-id="36550-106">Diese Funktion ruft [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um den Speicherplatz freizugeben.</span><span class="sxs-lookup"><span data-stu-id="36550-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="36550-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="36550-107">Syntax</span></span>


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="36550-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="36550-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36550-109">*pinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36550-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36550-110">Typ: \**[**rootkauseinfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="36550-110">Type: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="36550-111">Das Array von-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="36550-111">The array of structures.</span></span> <span data-ttu-id="36550-112">Der zugewiesene Speicher, auf den diese Strukturen zeigen, wird freigegeben.</span><span class="sxs-lookup"><span data-stu-id="36550-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="36550-113">_RootCauseCount \*</span><span class="sxs-lookup"><span data-stu-id="36550-113">_RootCauseCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="36550-114">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="36550-114">Type: **ULONG**</span></span>

<span data-ttu-id="36550-115">Die Anzahl der Strukturen im Array, auf die von *pinfo* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="36550-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="36550-116">*bfrepointer*</span><span class="sxs-lookup"><span data-stu-id="36550-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="36550-117">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="36550-117">Type: **BOOL**</span></span>

<span data-ttu-id="36550-118">True, wenn das Array von-Strukturen ebenfalls gelöscht werden soll. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="36550-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36550-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36550-119">Return value</span></span>

<span data-ttu-id="36550-120">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="36550-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="36550-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36550-121">Requirements</span></span>



| <span data-ttu-id="36550-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36550-122">Requirement</span></span> | <span data-ttu-id="36550-123">Wert</span><span class="sxs-lookup"><span data-stu-id="36550-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="36550-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36550-124">Minimum supported client</span></span><br/> | <span data-ttu-id="36550-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36550-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="36550-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36550-126">Minimum supported server</span></span><br/> | <span data-ttu-id="36550-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36550-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="36550-128">Header</span><span class="sxs-lookup"><span data-stu-id="36550-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="36550-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="36550-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36550-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36550-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36550-131">**Rootkauseingefo**</span><span class="sxs-lookup"><span data-stu-id="36550-131">**RootCauseInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[<span data-ttu-id="36550-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="36550-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

