---
title: Copyrootkauseinfo-Funktion (ndattributils. h)
description: Erstellt eine Kopie einer rootkauseingabe FO-Struktur.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- Copyrootkausin FO-Funktion NDF
topic_type:
- apiref
api_name:
- CopyRootCauseInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5093d7af6458668a763aa206cacd22a0526aa521
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949660"
---
# <a name="copyrootcauseinfo-function"></a><span data-ttu-id="91b03-104">Copyrootkausin FO-Funktion</span><span class="sxs-lookup"><span data-stu-id="91b03-104">CopyRootCauseInfo function</span></span>

<span data-ttu-id="91b03-105">Die **copyrootcauseingefo** -Funktion erstellt eine Kopie einer [**rootkauseingabe FO**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="91b03-105">The **CopyRootCauseInfo** function creates a copy of a [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="91b03-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="91b03-106">Syntax</span></span>


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a><span data-ttu-id="91b03-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="91b03-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91b03-108">*Dest* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="91b03-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91b03-109">Typ: \**[**rootkauseinfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="91b03-109">Type: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="91b03-110">Die zu Aktualisier Ende-Struktur.</span><span class="sxs-lookup"><span data-stu-id="91b03-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="91b03-111">_Source \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91b03-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b03-112">Geben Sie Folgendes ein: \**Konstanten [**rootkauseinfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="91b03-112">Type: \**const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="91b03-113">Die vorhandene zu kopierende-Struktur.</span><span class="sxs-lookup"><span data-stu-id="91b03-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91b03-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91b03-114">Return value</span></span>

<span data-ttu-id="91b03-115">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="91b03-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="91b03-116">Mögliche Rückgabewerte sind u. a. die folgenden.</span><span class="sxs-lookup"><span data-stu-id="91b03-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="91b03-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="91b03-117">Return code</span></span>                                                                                   | <span data-ttu-id="91b03-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91b03-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="91b03-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="91b03-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="91b03-120">Der Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91b03-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="91b03-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="91b03-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="91b03-122">Mindestens ein Parameter wurde nicht ordnungsgemäß bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="91b03-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="91b03-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="91b03-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="91b03-124">Es ist nicht genügend Arbeitsspeicher verfügbar, um diesen Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="91b03-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="91b03-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91b03-125">Requirements</span></span>



| <span data-ttu-id="91b03-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91b03-126">Requirement</span></span> | <span data-ttu-id="91b03-127">Wert</span><span class="sxs-lookup"><span data-stu-id="91b03-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="91b03-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91b03-128">Minimum supported client</span></span><br/> | <span data-ttu-id="91b03-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91b03-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="91b03-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91b03-130">Minimum supported server</span></span><br/> | <span data-ttu-id="91b03-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91b03-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="91b03-132">Header</span><span class="sxs-lookup"><span data-stu-id="91b03-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="91b03-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="91b03-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91b03-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91b03-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91b03-135">**Rootkauseingefo**</span><span class="sxs-lookup"><span data-stu-id="91b03-135">**RootCauseInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





