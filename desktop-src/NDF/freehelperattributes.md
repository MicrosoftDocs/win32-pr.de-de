---
title: Freehelperattributfunktion (ndattributils. h)
description: Hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von \_ hilfsattribut Strukturen auf.
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- Freehelperattributs-Funktion NDF
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400addd7d32914cb4e849e4e0bfae76ccc3ddf22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475987"
---
# <a name="freehelperattributes-function"></a><span data-ttu-id="7d671-104">Freehelperattributs-Funktion</span><span class="sxs-lookup"><span data-stu-id="7d671-104">FreeHelperAttributes function</span></span>

<span data-ttu-id="7d671-105">Die **freehelperattributfunktion** hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von [**\_ hilfsattribut**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) Strukturen auf.</span><span class="sxs-lookup"><span data-stu-id="7d671-105">The **FreeHelperAttributes** function deallocates the memory allocated internally to an array of [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structures.</span></span> <span data-ttu-id="7d671-106">Diese Funktion ruft [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um den Speicherplatz freizugeben.</span><span class="sxs-lookup"><span data-stu-id="7d671-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d671-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d671-107">Syntax</span></span>


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="7d671-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d671-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d671-109">*pinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d671-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d671-110">Type: \**[**helper- \_ Attribut**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _</span><span class="sxs-lookup"><span data-stu-id="7d671-110">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="7d671-111">Das Array von-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="7d671-111">The array of structures.</span></span> <span data-ttu-id="7d671-112">Der zugewiesene Speicher, auf den diese Strukturen zeigen, wird freigegeben.</span><span class="sxs-lookup"><span data-stu-id="7d671-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="7d671-113">_HelperAttributeCount \*</span><span class="sxs-lookup"><span data-stu-id="7d671-113">_HelperAttributeCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="7d671-114">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="7d671-114">Type: **ULONG**</span></span>

<span data-ttu-id="7d671-115">Die Anzahl der Strukturen im Array, auf die von *pinfo* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7d671-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="7d671-116">*bfrepointer*</span><span class="sxs-lookup"><span data-stu-id="7d671-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="7d671-117">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="7d671-117">Type: **BOOL**</span></span>

<span data-ttu-id="7d671-118">True, wenn das Array von-Strukturen ebenfalls gelöscht werden soll. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="7d671-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d671-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d671-119">Return value</span></span>

<span data-ttu-id="7d671-120">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7d671-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d671-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d671-121">Requirements</span></span>



| <span data-ttu-id="7d671-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d671-122">Requirement</span></span> | <span data-ttu-id="7d671-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7d671-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d671-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d671-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7d671-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d671-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7d671-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d671-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7d671-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d671-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7d671-128">Header</span><span class="sxs-lookup"><span data-stu-id="7d671-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d671-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d671-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d671-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d671-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d671-131">**HELPER- \_ Attribut**</span><span class="sxs-lookup"><span data-stu-id="7d671-131">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[<span data-ttu-id="7d671-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="7d671-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

