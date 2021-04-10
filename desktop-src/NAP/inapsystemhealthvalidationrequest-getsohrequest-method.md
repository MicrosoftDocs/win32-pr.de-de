---
title: Inapsystemhealthvalidationrequest getsohrequest-Methode (napsystemhealthvalidator. h)
description: Ermöglicht System Integritätsprüfungen (SHVs) das Abrufen und Überprüfen der sohrequest-Informationen, die von Ihrem System Integritäts-Agent (System Health Agent, SHA) auf dem Client gesendet werden.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- Getsohrequest-Methode NAP
- Getsohrequest-Methode NAP, inapsystemhealthvalidationrequest-Schnittstelle
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, getsohrequest-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306c9307f99f91e0b0a48a1c5ffeaf19b4ea1f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106418"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a><span data-ttu-id="52399-106">Inapsystemhealthvalidationrequest:: getsohrequest-Methode</span><span class="sxs-lookup"><span data-stu-id="52399-106">INapSystemHealthValidationRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="52399-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="52399-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="52399-108">Mit der **inapsystemhealthvalidationrequest:: getsohrequest** -Methode können System Integritätsprüfungen (SHVs) die [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Informationen abrufen und überprüfen, die von ihren Systemintegritäts-Agent-Entsprechungen (System Health Agent, SHA) auf dem Client gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="52399-108">The **INapSystemHealthValidationRequest::GetSoHRequest** method allows System Health Validators (SHVs) to retrieve and validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) information sent by their System Health Agent (SHA) counterparts on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="52399-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="52399-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a><span data-ttu-id="52399-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="52399-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52399-111">*sohrequest* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="52399-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52399-112">Ein Zeiger auf einen Zeiger auf eine [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="52399-112">A pointer to a pointer to an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> <dt>

<span data-ttu-id="52399-113">*napsystemgenerated* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="52399-113">*napSystemGenerated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52399-114">Ein **boolescher** Wert, der **true** ist, wenn das SoH vom NAPAgent im Auftrag des SHA erstellt wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="52399-114">A **BOOL** that is **TRUE** if the SoH was created by the NapAgent on behalf of the SHA and **FALSE** otherwise.</span></span> <span data-ttu-id="52399-115">Es wird hauptsächlich verwendet, um einen SHA-Fehler für den SHV anzugeben.</span><span class="sxs-lookup"><span data-stu-id="52399-115">It is primarily used to indicate an SHA failure to the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52399-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52399-116">Return value</span></span>

<span data-ttu-id="52399-117">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="52399-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="52399-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="52399-118">Return code</span></span>                                                                                     | <span data-ttu-id="52399-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52399-119">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="52399-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="52399-120"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="52399-121">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="52399-121">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="52399-122"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="52399-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="52399-123">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="52399-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="52399-124"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="52399-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="52399-125">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="52399-125">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="52399-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52399-126">Remarks</span></span>

<span data-ttu-id="52399-127">Der *sohrequest* -Parameter gibt möglicherweise **null** zurück, wenn der Client kein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) an den SHV gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="52399-127">The *sohRequest* parameter may return **NULL** if the client did not send an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the SHV.</span></span> <span data-ttu-id="52399-128">In diesem Szenario kann der SHV eine **sohresponse** mit dem Fehlercode " [**NAP \_ E \_ Missing \_ SoH**](nap-error-constants.md)" auffüllen.</span><span class="sxs-lookup"><span data-stu-id="52399-128">In that scenario the SHV can populate an **SoHResponse** with the error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>

<span data-ttu-id="52399-129">Wenn der Parameter " *napsystemgenerated* " den Wert " **true**" hat, lautet das *sohrequest* -Format wie folgt:</span><span class="sxs-lookup"><span data-stu-id="52399-129">If the *napSystemGenerated* parameter is **TRUE**, the format of *SoHRequest* is as follows:</span></span>

-   <span data-ttu-id="52399-130">[**sohattributetypesystemhealthid**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="52399-130">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="52399-131">[**sohattributetypefailurecategory**](sohattributetype-enum.md) =  [ **failurecategoryclientcomponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="52399-131">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="52399-132">[**sohattributetypeerrorcodes**](sohattributetype-enum.md)  =  [ **<SHA-Failure-Error-Code>**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="52399-132">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**<sha-failure-error-code>**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="52399-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52399-133">Requirements</span></span>



| <span data-ttu-id="52399-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52399-134">Requirement</span></span> | <span data-ttu-id="52399-135">Wert</span><span class="sxs-lookup"><span data-stu-id="52399-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52399-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52399-136">Minimum supported client</span></span><br/> | <span data-ttu-id="52399-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52399-137">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="52399-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52399-138">Minimum supported server</span></span><br/> | <span data-ttu-id="52399-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52399-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52399-140">Header</span><span class="sxs-lookup"><span data-stu-id="52399-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="52399-141"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="52399-141"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="52399-142">IDL</span><span class="sxs-lookup"><span data-stu-id="52399-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="52399-143"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="52399-143"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="52399-144">DLL</span><span class="sxs-lookup"><span data-stu-id="52399-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52399-145"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52399-145"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="52399-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52399-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52399-147">**Inapsystemhealthvalidationrequest**</span><span class="sxs-lookup"><span data-stu-id="52399-147">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





