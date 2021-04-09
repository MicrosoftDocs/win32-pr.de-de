---
title: Utilloadstringwithzugsc-Funktion (ndattributils. h)
description: Ordnet eine Zeichenfolge zu und lädt Sie aus der Ressourcen Tabelle.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- Utilloadstringwithzugsc-Funktion NDF
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e13930fe9bb11ae9c9456152c823491eabc462
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106502"
---
# <a name="utilloadstringwithalloc-function"></a><span data-ttu-id="30a2c-104">Utilloadstringwithzugsc-Funktion</span><span class="sxs-lookup"><span data-stu-id="30a2c-104">UtilLoadStringWithAlloc function</span></span>

<span data-ttu-id="30a2c-105">Die **utilloadstringwithzucfunktion** ordnet eine Zeichenfolge zu und lädt Sie aus der Ressourcen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="30a2c-105">The **UtilLoadStringWithAlloc** function allocates and loads a string out of the resource table.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a2c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="30a2c-106">Syntax</span></span>


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a><span data-ttu-id="30a2c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="30a2c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a2c-108">*UID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30a2c-108">*uID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a2c-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="30a2c-109">Type: **UINT**</span></span>

<span data-ttu-id="30a2c-110">Der Bezeichner der zu ladenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="30a2c-110">Identifier of of the string to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="30a2c-111">*ppwzpuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="30a2c-111">*ppwzBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30a2c-112">Typ: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="30a2c-112">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="30a2c-113">Der Speicherort, an dem die neu zugewiesene Zeichenfolge platziert wird.</span><span class="sxs-lookup"><span data-stu-id="30a2c-113">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="30a2c-114">Die Zeichenfolge muss mit [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) freigegeben werden, wenn Sie nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="30a2c-114">The string must be freed using [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) when it is no longer needed.</span></span>

</dd> <dt>

<span data-ttu-id="30a2c-115">*cchbuffermax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30a2c-115">*cchBufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a2c-116">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="30a2c-116">Type: **UINT**</span></span>

<span data-ttu-id="30a2c-117">Die maximale Anzahl von Zeichen, die aus der Ressourcen Tabelle geladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30a2c-117">The maximum number of characters to load from the resource table.</span></span> <span data-ttu-id="30a2c-118">Wenn die Ressourcen Zeichenfolge länger als die angegebene Anzahl von Zeichen ist, wird Sie abgeschnitten und mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="30a2c-118">If the resource string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="30a2c-119">Dieser Parameter darf nicht auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="30a2c-119">This parameter may not be set to zero.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30a2c-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30a2c-120">Return value</span></span>

<span data-ttu-id="30a2c-121">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="30a2c-121">Type: **HRESULT**</span></span>

<span data-ttu-id="30a2c-122">Mögliche Rückgabewerte sind u. a. die folgenden.</span><span class="sxs-lookup"><span data-stu-id="30a2c-122">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="30a2c-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="30a2c-123">Return code</span></span>                                                                                  | <span data-ttu-id="30a2c-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30a2c-124">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="30a2c-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30a2c-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="30a2c-126">Der Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30a2c-126">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="30a2c-127"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="30a2c-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="30a2c-128">Mindestens ein Parameter wurde nicht ordnungsgemäß bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="30a2c-128">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="30a2c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30a2c-129">Requirements</span></span>



| <span data-ttu-id="30a2c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30a2c-130">Requirement</span></span> | <span data-ttu-id="30a2c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="30a2c-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a2c-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30a2c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="30a2c-133">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30a2c-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="30a2c-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30a2c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="30a2c-135">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30a2c-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="30a2c-136">Header</span><span class="sxs-lookup"><span data-stu-id="30a2c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="30a2c-137"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="30a2c-137"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a2c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30a2c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a2c-139">**Utilstringcopywithzuzuweisung**</span><span class="sxs-lookup"><span data-stu-id="30a2c-139">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="30a2c-140">**Utilassemlestringswithzuweisung**</span><span class="sxs-lookup"><span data-stu-id="30a2c-140">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="30a2c-141">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="30a2c-141">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

