---
title: Inapsystemhealthagentrequest getsohrequest-Methode (napsystemhealthagent. h)
description: Kann von SHAs, die zuvor vom NAPAgent zwischengespeichert wurden, verwendet werden.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- Getsohrequest-Methode NAP
- Getsohrequest-Methode NAP, inapsystemhealthagentrequest-Schnittstelle
- Inapsystemhealthagentrequest-Schnittstelle NAP, getsohrequest-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab52e52c952c2dc1f891098e10c3ecb688052295
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040934"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a><span data-ttu-id="24eb6-106">Inapsystemhealthagentrequest:: getsohrequest-Methode</span><span class="sxs-lookup"><span data-stu-id="24eb6-106">INapSystemHealthAgentRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="24eb6-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="24eb6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="24eb6-108">Die **inapsystemhealthagentrequest:: getsohrequest** -Methode kann von SHAs, die zuvor von NAPAgent zwischengespeichert wurden, verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24eb6-108">The **INapSystemHealthAgentRequest::GetSoHRequest** method can be used by SHAs get SoHs previously cached by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="24eb6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="24eb6-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="24eb6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="24eb6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24eb6-111">*sohrequest* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="24eb6-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24eb6-112">Ein Zeiger auf einen Zeiger auf einen [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="24eb6-112">A pointer to a pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24eb6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24eb6-113">Return value</span></span>

<span data-ttu-id="24eb6-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="24eb6-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="24eb6-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="24eb6-115">Return code</span></span>                                                                                            | <span data-ttu-id="24eb6-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24eb6-116">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="24eb6-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="24eb6-117"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="24eb6-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="24eb6-118">Operation succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="24eb6-119"><dt>**NAP \_ E \_ kein \_ zwischengespeichertes \_ SoH**</dt></span><span class="sxs-lookup"><span data-stu-id="24eb6-119"><dt>**NAP\_E\_NO\_CACHED\_SOH**</dt></span></span> </dl> | <span data-ttu-id="24eb6-120">Der SoH wurde nicht gefunden. NAPAgent verfügt über keine zwischengespeicherte Kopie.</span><span class="sxs-lookup"><span data-stu-id="24eb6-120">The SoH is not found; NapAgent does not have a cached copy.</span></span><br/> |
| <dl> <span data-ttu-id="24eb6-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="24eb6-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="24eb6-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="24eb6-122">Permissions error, access denied.</span></span><br/>                           |
| <dl> <span data-ttu-id="24eb6-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="24eb6-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="24eb6-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="24eb6-124">System resource limit, could not perform the operation.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="24eb6-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24eb6-125">Requirements</span></span>



| <span data-ttu-id="24eb6-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24eb6-126">Requirement</span></span> | <span data-ttu-id="24eb6-127">Wert</span><span class="sxs-lookup"><span data-stu-id="24eb6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24eb6-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24eb6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="24eb6-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24eb6-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="24eb6-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24eb6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="24eb6-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24eb6-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="24eb6-132">Header</span><span class="sxs-lookup"><span data-stu-id="24eb6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="24eb6-133"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="24eb6-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="24eb6-134">IDL</span><span class="sxs-lookup"><span data-stu-id="24eb6-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="24eb6-135"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="24eb6-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="24eb6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="24eb6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24eb6-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24eb6-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="24eb6-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24eb6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24eb6-139">**Inapsystemhealthagentrequest**</span><span class="sxs-lookup"><span data-stu-id="24eb6-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





