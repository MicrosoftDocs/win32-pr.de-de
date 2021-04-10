---
title: Freeuiinfo-Funktion (ndattributils. h)
description: Hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einer uiinfo-Struktur auf.
ms.assetid: 41d923fd-2fb3-406e-a5cf-f3ba475685f6
keywords:
- Freeuiinfo-Funktion NDF
topic_type:
- apiref
api_name:
- FreeUiInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a96d859faa80e3e2269981d206c96e780d05c37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103286"
---
# <a name="freeuiinfo-function"></a><span data-ttu-id="53fb1-104">Freeuiinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="53fb1-104">FreeUiInfo function</span></span>

<span data-ttu-id="53fb1-105">Die **freeuiinfo** -Funktion hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einer [**uiinfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) -Struktur auf.</span><span class="sxs-lookup"><span data-stu-id="53fb1-105">The **FreeUiInfo** function deallocates the memory allocated internally to a [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) structure.</span></span> <span data-ttu-id="53fb1-106">Diese Funktion ruft [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um den Speicherplatz freizugeben.</span><span class="sxs-lookup"><span data-stu-id="53fb1-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="53fb1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="53fb1-107">Syntax</span></span>


```C++
VOID FreeUiInfo(
  _In_ UiInfo *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="53fb1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="53fb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53fb1-109">*pinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53fb1-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53fb1-110">Typ: \**[**uiinfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="53fb1-110">Type: \**[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)\** _</span></span>

<span data-ttu-id="53fb1-111">Die-Struktur.</span><span class="sxs-lookup"><span data-stu-id="53fb1-111">The structure.</span></span> <span data-ttu-id="53fb1-112">Der zugewiesene Speicher, auf den von dieser-Struktur verwiesen wird, wird freigegeben.</span><span class="sxs-lookup"><span data-stu-id="53fb1-112">The allocated memory pointed to by this structure will be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53fb1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53fb1-113">Return value</span></span>

<span data-ttu-id="53fb1-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="53fb1-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="53fb1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53fb1-115">Requirements</span></span>



| <span data-ttu-id="53fb1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53fb1-116">Requirement</span></span> | <span data-ttu-id="53fb1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="53fb1-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="53fb1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53fb1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="53fb1-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53fb1-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="53fb1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53fb1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="53fb1-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53fb1-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="53fb1-122">Header</span><span class="sxs-lookup"><span data-stu-id="53fb1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="53fb1-123"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="53fb1-123"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53fb1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53fb1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53fb1-125">_ *Uiinfo*\*</span><span class="sxs-lookup"><span data-stu-id="53fb1-125">_ *UiInfo*\*</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)
</dt> <dt>

[<span data-ttu-id="53fb1-126">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="53fb1-126">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

