---
title: Inapsystemhealthagentrequest getsohresponse-Methode (napsystemhealthagent. h)
description: Wird vom Integritäts-Agent zum Abrufen des sohresponse-BLOBs verwendet, wenn der NAPAgent inapsystemhealthagentcallback processsohresponse aufruft.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- Getsohresponse-Methode NAP
- Getsohresponse-Methode NAP, inapsystemhealthagentrequest-Schnittstelle
- Inapsystemhealthagentrequest-Schnittstelle NAP, getsohresponse-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d593ff897e69b86b554365561e43308adead5250
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103294"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a><span data-ttu-id="65f4a-106">Inapsystemhealthagentrequest:: getsohresponse-Methode</span><span class="sxs-lookup"><span data-stu-id="65f4a-106">INapSystemHealthAgentRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="65f4a-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="65f4a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="65f4a-108">Die **inapsystemhealthagentrequest:: getsohresponse** -Methode wird vom Health-Agent zum Abrufen ihres sohresponse-BLOBs verwendet, wenn der NAPAgent [**inapsystemhealthagentcallback::P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md)aufruft.</span><span class="sxs-lookup"><span data-stu-id="65f4a-108">The **INapSystemHealthAgentRequest::GetSoHResponse** method is used by the health agent to retrieve their SoHResponse blob when the NapAgent calls [**INapSystemHealthAgentCallback::ProcessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="65f4a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="65f4a-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a><span data-ttu-id="65f4a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="65f4a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65f4a-111">*sohresponse* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="65f4a-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65f4a-112">Ein Zeiger auf einen Zeiger auf ein [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket.</span><span class="sxs-lookup"><span data-stu-id="65f4a-112">A pointer to a pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="65f4a-113">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="65f4a-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65f4a-114">Ein Zeiger auf ein Flag, das eine Korrektur durch SHA ermöglicht, wenn das [**shafixupbit**](nap-type-constants.md) festgelegt ist, andernfalls ist die Behebung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="65f4a-114">A pointer to a flag that enables fix-up by the SHA if the [**shaFixup**](nap-type-constants.md) bit is set, otherwise fix-up is disabled.</span></span>



| <span data-ttu-id="65f4a-115">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="65f4a-115">Possible Values</span></span>                                                                                                                                                          | <span data-ttu-id="65f4a-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="65f4a-116">Meaning</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <span data-ttu-id="65f4a-117"><dt>**shafixup**</dt></span><span class="sxs-lookup"><span data-stu-id="65f4a-117"><dt>**shaFixup**</dt></span></span> </dl> | <span data-ttu-id="65f4a-118">Der SHA wird erwartet, dass das Fixup basierend auf der Antwort ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65f4a-118">The SHA is expected to perform the fixup based on the response.</span></span> <span data-ttu-id="65f4a-119">Wenn dieses Flag nicht festgelegt ist, sollte das SHA keine Korrektur durchführen, auch wenn die [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) angibt, dass Sie fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="65f4a-119">If this flag is not set, the SHA should not perform a fix-up even though the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indicates that it is unhealthy.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65f4a-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65f4a-120">Return value</span></span>

<span data-ttu-id="65f4a-121">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="65f4a-121">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="65f4a-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="65f4a-122">Return code</span></span>                                                                                     | <span data-ttu-id="65f4a-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65f4a-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="65f4a-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="65f4a-124"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="65f4a-125">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="65f4a-125">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="65f4a-126"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="65f4a-126"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="65f4a-127">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="65f4a-127">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="65f4a-128"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="65f4a-128"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="65f4a-129">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="65f4a-129">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="65f4a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65f4a-130">Requirements</span></span>



| <span data-ttu-id="65f4a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65f4a-131">Requirement</span></span> | <span data-ttu-id="65f4a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="65f4a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65f4a-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65f4a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="65f4a-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65f4a-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="65f4a-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65f4a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="65f4a-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65f4a-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="65f4a-137">Header</span><span class="sxs-lookup"><span data-stu-id="65f4a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="65f4a-138"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="65f4a-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="65f4a-139">IDL</span><span class="sxs-lookup"><span data-stu-id="65f4a-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65f4a-140"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="65f4a-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="65f4a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="65f4a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65f4a-142"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65f4a-142"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="65f4a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65f4a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65f4a-144">**Inapsystemhealthagentrequest**</span><span class="sxs-lookup"><span data-stu-id="65f4a-144">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





