---
title: Inapsystemhealthvalidationrequest-setsohresponse-Methode (napsystemhealthvalidator. h)
description: Ermöglicht System Integritätsprüfungen (SHVs), die sohresponse festzulegen, die auf der Clientseite an Ihren System Integritäts-Agent (SHA)-Gegenstück gesendet wird.
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- Setsohresponse-Methode NAP
- Setsohresponse-Methode NAP, inapsystemhealthvalidationrequest-Schnittstelle
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, setsohresponse-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b818218ef4f8601ecf4927f5e8b90f93e5386b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392110"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a><span data-ttu-id="71b59-106">Inapsystemhealthvalidationrequest:: setsohresponse-Methode</span><span class="sxs-lookup"><span data-stu-id="71b59-106">INapSystemHealthValidationRequest::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="71b59-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="71b59-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="71b59-108">Mit der **inapsystemhealthvalidationrequest:: setsohresponse** -Methode können System Integritätsprüfungen (SHVs) die [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) festlegen, die auf der Clientseite an Ihr System Health Agent (SHA)-Gegenstück gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="71b59-108">The **INapSystemHealthValidationRequest::SetSoHResponse** method allows System Health Validators (SHVs) to set the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) to be sent to its System Health Agent (SHA) counterpart on the client-side.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b59-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="71b59-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="71b59-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="71b59-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71b59-111">*sohresponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71b59-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71b59-112">Ein Zeiger auf eine [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="71b59-112">A pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71b59-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71b59-113">Return value</span></span>

<span data-ttu-id="71b59-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="71b59-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="71b59-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="71b59-115">Return code</span></span>                                                                                     | <span data-ttu-id="71b59-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71b59-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="71b59-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71b59-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="71b59-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="71b59-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="71b59-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="71b59-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="71b59-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="71b59-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="71b59-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="71b59-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="71b59-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="71b59-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="71b59-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71b59-123">Requirements</span></span>



| <span data-ttu-id="71b59-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71b59-124">Requirement</span></span> | <span data-ttu-id="71b59-125">Wert</span><span class="sxs-lookup"><span data-stu-id="71b59-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71b59-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71b59-126">Minimum supported client</span></span><br/> | <span data-ttu-id="71b59-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="71b59-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="71b59-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71b59-128">Minimum supported server</span></span><br/> | <span data-ttu-id="71b59-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71b59-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71b59-130">Header</span><span class="sxs-lookup"><span data-stu-id="71b59-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="71b59-131"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="71b59-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="71b59-132">IDL</span><span class="sxs-lookup"><span data-stu-id="71b59-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71b59-133"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71b59-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="71b59-134">DLL</span><span class="sxs-lookup"><span data-stu-id="71b59-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71b59-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71b59-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="71b59-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71b59-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b59-137">**Inapsystemhealthvalidationrequest**</span><span class="sxs-lookup"><span data-stu-id="71b59-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





