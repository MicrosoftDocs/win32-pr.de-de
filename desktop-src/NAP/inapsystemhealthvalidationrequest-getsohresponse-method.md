---
title: Inapsystemhealthvalidationrequest getsohresponse-Methode (napsystemhealthvalidator. h)
description: Ruft die sohresponse ab.
ms.assetid: 7db9d134-5cd4-4a6c-8576-843b9a920864
keywords:
- Getsohresponse-Methode NAP
- Getsohresponse-Methode NAP, inapsystemhealthvalidationrequest-Schnittstelle
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, getsohresponse-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10174edc2bcb9df8e61c98305e42633d2b984b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344714"
---
# <a name="inapsystemhealthvalidationrequestgetsohresponse-method"></a><span data-ttu-id="b8a8f-106">Inapsystemhealthvalidationrequest:: getsohresponse-Methode</span><span class="sxs-lookup"><span data-stu-id="b8a8f-106">INapSystemHealthValidationRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="b8a8f-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b8a8f-108">Die **inapsystemhealthvalidationrequest:: getsohresponse** -Methode ruft die [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh)ab.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-108">The **INapSystemHealthValidationRequest::GetSoHResponse** method retrieves the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a8f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8a8f-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="b8a8f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8a8f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8a8f-111">*sohresponse* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b8a8f-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a8f-112">Ein Zeiger auf einen Zeiger auf die empfangene [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="b8a8f-112">A pointer to a pointer to the received [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8a8f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8a8f-113">Return value</span></span>

<span data-ttu-id="b8a8f-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b8a8f-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b8a8f-115">Return code</span></span>                                                                                     | <span data-ttu-id="b8a8f-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8a8f-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8a8f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b8a8f-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="b8a8f-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b8a8f-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="b8a8f-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="b8a8f-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b8a8f-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="b8a8f-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="b8a8f-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b8a8f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8a8f-123">Requirements</span></span>



| <span data-ttu-id="b8a8f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8a8f-124">Requirement</span></span> | <span data-ttu-id="b8a8f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b8a8f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a8f-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8a8f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a8f-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b8a8f-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="b8a8f-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8a8f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a8f-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8a8f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8a8f-130">Header</span><span class="sxs-lookup"><span data-stu-id="b8a8f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8a8f-131"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8a8f-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8a8f-132">IDL</span><span class="sxs-lookup"><span data-stu-id="b8a8f-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b8a8f-133"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b8a8f-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="b8a8f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b8a8f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8a8f-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8a8f-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="b8a8f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8a8f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a8f-137">**Inapsystemhealthvalidationrequest**</span><span class="sxs-lookup"><span data-stu-id="b8a8f-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





