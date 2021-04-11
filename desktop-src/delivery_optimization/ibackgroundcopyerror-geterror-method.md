---
title: Ibackgroundcopyerror GetError-Methode (deliveryoptimization. h)
description: Ruft den Fehlercode ab und identifiziert den Kontext, in dem der Fehler aufgetreten ist.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- GetError-Methode
- GetError-Methode, ibackgroundcopyerror-Schnittstelle
- Ibackgroundcopyerror-Schnittstelle, GetError-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e14803c225ade6085658582e18b9ba2d52fc90c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949787"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a><span data-ttu-id="2787f-106">Ibackgroundcopyerror:: GetError-Methode</span><span class="sxs-lookup"><span data-stu-id="2787f-106">IBackgroundCopyError::GetError method</span></span>

<span data-ttu-id="2787f-107">Ruft den Fehlercode ab und identifiziert den Kontext, in dem der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2787f-107">Retrieves the error code and identify the context in which the error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="2787f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2787f-108">Syntax</span></span>


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="2787f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2787f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2787f-110">*pContext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2787f-110">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2787f-111">Der Kontext, in dem der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2787f-111">Context in which the error occurred.</span></span> <span data-ttu-id="2787f-112">Eine Liste der Kontext Werte finden Sie in der [**BG_ERROR_CONTEXT**](bg-error-context.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="2787f-112">For a list of context values, see the [**BG_ERROR_CONTEXT**](bg-error-context.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="2787f-113">*perrorcode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2787f-113">*pErrorCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2787f-114">Der Fehlercode des Fehlers, der aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2787f-114">Error code of the error that occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2787f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2787f-115">Return value</span></span>

<span data-ttu-id="2787f-116">Diese Methode gibt **S_OK** bei Erfolg oder einen der standardmäßigen com HRESULT-Werte bei einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2787f-116">This method returns **S_OK** on success or one of the standard COM HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2787f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2787f-117">Requirements</span></span>



| <span data-ttu-id="2787f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2787f-118">Requirement</span></span> | <span data-ttu-id="2787f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2787f-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2787f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2787f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2787f-121">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2787f-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2787f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2787f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2787f-123">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2787f-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2787f-124">Header</span><span class="sxs-lookup"><span data-stu-id="2787f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2787f-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2787f-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2787f-126">IDL</span><span class="sxs-lookup"><span data-stu-id="2787f-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2787f-127"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2787f-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2787f-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2787f-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="2787f-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2787f-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2787f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2787f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2787f-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2787f-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2787f-132">IID</span><span class="sxs-lookup"><span data-stu-id="2787f-132">IID</span></span><br/>                      | <span data-ttu-id="2787f-133">IID_IBackgroundCopyError ist als 19c613a0-fcb8-4f 28-81ae-897c3d078-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="2787f-133">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="2787f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2787f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2787f-135">**Ibackgroundcopyerror**</span><span class="sxs-lookup"><span data-stu-id="2787f-135">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="2787f-136">**Ibackgroundcopyerror:: GetFile**</span><span class="sxs-lookup"><span data-stu-id="2787f-136">**IBackgroundCopyError::GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





