---
title: Copyrepairren Info-Funktion (ndattributils. h)
description: Erstellt eine Kopie einer repairiinfo-Struktur.
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- Copyrepairren Info-Funktion NDF
topic_type:
- apiref
api_name:
- CopyRepairInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a24d15ec5a8a69b3c8c40700273ebcb6f32bcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949659"
---
# <a name="copyrepairinfo-function"></a><span data-ttu-id="2830a-104">Copyrepairren Info-Funktion</span><span class="sxs-lookup"><span data-stu-id="2830a-104">CopyRepairInfo function</span></span>

<span data-ttu-id="2830a-105">Die **copyrepairren Info** -Funktion erstellt eine Kopie einer [**repairiinfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2830a-105">The **CopyRepairInfo** function creates a copy of a [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2830a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2830a-106">Syntax</span></span>


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a><span data-ttu-id="2830a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2830a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2830a-108">*Dest* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2830a-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2830a-109">Geben Sie Folgendes ein: \**[**repairren Info**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="2830a-109">Type: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="2830a-110">Die zu Aktualisier Ende-Struktur.</span><span class="sxs-lookup"><span data-stu-id="2830a-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="2830a-111">_Source \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2830a-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2830a-112">Geben Sie Folgendes ein: \* Konstante *[**repairren Info**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="2830a-112">Type: \**const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="2830a-113">Die vorhandene zu kopierende-Struktur.</span><span class="sxs-lookup"><span data-stu-id="2830a-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2830a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2830a-114">Return value</span></span>

<span data-ttu-id="2830a-115">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2830a-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2830a-116">Mögliche Rückgabewerte sind u. a. die folgenden.</span><span class="sxs-lookup"><span data-stu-id="2830a-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="2830a-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2830a-117">Return code</span></span>                                                                                   | <span data-ttu-id="2830a-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2830a-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2830a-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2830a-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2830a-120">Der Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2830a-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="2830a-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="2830a-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2830a-122">Mindestens ein Parameter wurde nicht ordnungsgemäß bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2830a-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="2830a-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="2830a-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2830a-124">Es ist nicht genügend Arbeitsspeicher verfügbar, um diesen Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2830a-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2830a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2830a-125">Requirements</span></span>



| <span data-ttu-id="2830a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2830a-126">Requirement</span></span> | <span data-ttu-id="2830a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2830a-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2830a-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2830a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2830a-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2830a-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2830a-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2830a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2830a-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2830a-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2830a-132">Header</span><span class="sxs-lookup"><span data-stu-id="2830a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2830a-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="2830a-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2830a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2830a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2830a-135">**Repairren Info**</span><span class="sxs-lookup"><span data-stu-id="2830a-135">**RepairInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





