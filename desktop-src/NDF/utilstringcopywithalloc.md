---
title: Utilstringcopywithzuzuordnungsfunktion (ndattributils. h)
description: Ordnet eine Quell Zeichenfolge zu und kopiert sie.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- Utilstringcopywithzuzuordnungsfunktion NDF
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68bd1815ff09473f0431dde19a12a87603a9dec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340577"
---
# <a name="utilstringcopywithalloc-function"></a><span data-ttu-id="16afb-104">Utilstringcopywithzuzuordnungsfunktion</span><span class="sxs-lookup"><span data-stu-id="16afb-104">UtilStringCopyWithAlloc function</span></span>

<span data-ttu-id="16afb-105">Die Funktion " **utilstringcopywithzuzuordnungs** " weist eine Quell Zeichenfolge zu und kopiert sie.</span><span class="sxs-lookup"><span data-stu-id="16afb-105">The **UtilStringCopyWithAlloc** function allocates and copies a source string.</span></span>

## <a name="syntax"></a><span data-ttu-id="16afb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="16afb-106">Syntax</span></span>


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a><span data-ttu-id="16afb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="16afb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16afb-108">*Puffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="16afb-108">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16afb-109">Typ: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="16afb-109">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="16afb-110">Der Speicherort, an dem der Zeiger auf den zugeordneten Arbeitsspeicher gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="16afb-110">The location where the pointer to the allocated memory is stored.</span></span> <span data-ttu-id="16afb-111">Wenn Sie nicht mehr benötigt wird, muss Sie mit [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="16afb-111">When no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="16afb-112">Dieser Puffer wird immer mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="16afb-112">This buffer is always null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="16afb-113">*Buffermax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16afb-113">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16afb-114">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="16afb-114">Type: **UINT**</span></span>

<span data-ttu-id="16afb-115">Die maximale Anzahl von Zeichen, die aus der *Quelle* gelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="16afb-115">The maximum number of characters to read from *Source*.</span></span>

</dd> <dt>

<span data-ttu-id="16afb-116">*Quelle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16afb-116">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16afb-117">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="16afb-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="16afb-118">Die zu kopierende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="16afb-118">The string to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16afb-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16afb-119">Return value</span></span>

<span data-ttu-id="16afb-120">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="16afb-120">Type: **HRESULT**</span></span>

<span data-ttu-id="16afb-121">Mögliche Rückgabewerte sind u. a. die folgenden.</span><span class="sxs-lookup"><span data-stu-id="16afb-121">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="16afb-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="16afb-122">Return code</span></span>                                                                                  | <span data-ttu-id="16afb-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16afb-123">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="16afb-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="16afb-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="16afb-125">Der Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16afb-125">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="16afb-126"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="16afb-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="16afb-127">Mindestens ein Parameter wurde nicht ordnungsgemäß bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="16afb-127">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="16afb-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16afb-128">Requirements</span></span>



| <span data-ttu-id="16afb-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16afb-129">Requirement</span></span> | <span data-ttu-id="16afb-130">Wert</span><span class="sxs-lookup"><span data-stu-id="16afb-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="16afb-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16afb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="16afb-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16afb-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="16afb-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16afb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="16afb-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16afb-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="16afb-135">Header</span><span class="sxs-lookup"><span data-stu-id="16afb-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="16afb-136"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="16afb-136"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16afb-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16afb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16afb-138">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="16afb-138">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[<span data-ttu-id="16afb-139">**Utilassemlestringswithzuweisung**</span><span class="sxs-lookup"><span data-stu-id="16afb-139">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="16afb-140">**Utilloadstringwithzuordc**</span><span class="sxs-lookup"><span data-stu-id="16afb-140">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> </dl>

 

