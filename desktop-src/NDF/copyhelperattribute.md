---
title: Copyhelperattribute-Funktion (ndattributils. h)
description: Erstellt eine Kopie einer \_ hilfsattribut Struktur.
ms.assetid: ff49be29-4cd8-4730-929f-c66a7325704f
keywords:
- Copyhelperattribute-Funktion NDF
topic_type:
- apiref
api_name:
- CopyHelperAttribute
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59fac3449ee48659980681c836d24406c4db7e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338328"
---
# <a name="copyhelperattribute-function"></a><span data-ttu-id="dbab8-104">Copyhelperattribute-Funktion</span><span class="sxs-lookup"><span data-stu-id="dbab8-104">CopyHelperAttribute function</span></span>

<span data-ttu-id="dbab8-105">Die **copyhelperattribute** -Funktion erstellt eine Kopie einer [**\_ hilfsattribut**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) Struktur.</span><span class="sxs-lookup"><span data-stu-id="dbab8-105">The **CopyHelperAttribute** function creates a copy of a [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbab8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbab8-106">Syntax</span></span>


```C++
HRESULT CopyHelperAttribute(
  _Out_       HELPER_ATTRIBUTE *Dest,
  _In_  const HELPER_ATTRIBUTE *Source
);
```



## <a name="parameters"></a><span data-ttu-id="dbab8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbab8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbab8-108">*Dest* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dbab8-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbab8-109">Type: \**[**helper- \_ Attribut**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _</span><span class="sxs-lookup"><span data-stu-id="dbab8-109">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="dbab8-110">Die zu Aktualisier Ende-Struktur.</span><span class="sxs-lookup"><span data-stu-id="dbab8-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="dbab8-111">_Source \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbab8-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbab8-112">Geben Sie Folgendes ein: \* Konstante *[**\_ hilfsattribut**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _</span><span class="sxs-lookup"><span data-stu-id="dbab8-112">Type: \**const [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="dbab8-113">Die vorhandene zu kopierende-Struktur.</span><span class="sxs-lookup"><span data-stu-id="dbab8-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbab8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbab8-114">Return value</span></span>

<span data-ttu-id="dbab8-115">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="dbab8-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="dbab8-116">Mögliche Rückgabewerte sind u. a. die folgenden.</span><span class="sxs-lookup"><span data-stu-id="dbab8-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="dbab8-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dbab8-117">Return code</span></span>                                                                                   | <span data-ttu-id="dbab8-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbab8-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dbab8-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dbab8-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dbab8-120">Der Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbab8-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="dbab8-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="dbab8-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dbab8-122">Mindestens ein Parameter wurde nicht ordnungsgemäß bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dbab8-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="dbab8-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="dbab8-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dbab8-124">Es ist nicht genügend Arbeitsspeicher verfügbar, um diesen Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="dbab8-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dbab8-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbab8-125">Requirements</span></span>



| <span data-ttu-id="dbab8-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbab8-126">Requirement</span></span> | <span data-ttu-id="dbab8-127">Wert</span><span class="sxs-lookup"><span data-stu-id="dbab8-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbab8-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbab8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dbab8-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbab8-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dbab8-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbab8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dbab8-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbab8-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dbab8-132">Header</span><span class="sxs-lookup"><span data-stu-id="dbab8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbab8-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbab8-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbab8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbab8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbab8-135">**HELPER- \_ Attribut**</span><span class="sxs-lookup"><span data-stu-id="dbab8-135">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> </dl>

 

 





