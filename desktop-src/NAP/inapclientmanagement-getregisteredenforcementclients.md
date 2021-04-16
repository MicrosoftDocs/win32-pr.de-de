---
title: Inapclientmanagement getregisteredenforcementclients-Methode (napmanagement. h)
description: Ruft Informationen zu den registrierten Erzwingungs Clients ab.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- Getregisteredenforcementclients-Methode NAP
- Getregisteredenforcementclients-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, getregisteredenforcementclients-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredEnforcementClients
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7767f96c9b5410b3de9cfef3695193c0d5572b2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477820"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a><span data-ttu-id="2a88a-106">Inapclientmanagement:: getregisteredenforcementclients-Methode</span><span class="sxs-lookup"><span data-stu-id="2a88a-106">INapClientManagement::GetRegisteredEnforcementClients method</span></span>

> [!Note]  
> <span data-ttu-id="2a88a-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2a88a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2a88a-108">Die **getregisteredenforcementclients** -Methode ruft Informationen zu den registrierten Erzwingungs Clients ab.</span><span class="sxs-lookup"><span data-stu-id="2a88a-108">The **GetRegisteredEnforcementClients** method retrieves information about the registered enforcement clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a88a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a88a-109">Syntax</span></span>


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a><span data-ttu-id="2a88a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a88a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a88a-111">*Anzahl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2a88a-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a88a-112">Ein Zeiger auf eine [**enforcemententitycount**](nap-datatypes.md) , die die Anzahl der registrierten Erzwingungs Clients enthält.</span><span class="sxs-lookup"><span data-stu-id="2a88a-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of registered enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="2a88a-113">*Enforcer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2a88a-113">*enforcers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a88a-114">Ein Zeiger auf ein Array von [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Strukturen, die die registrierten Erzwingungs Clients beschreiben.</span><span class="sxs-lookup"><span data-stu-id="2a88a-114">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures that describe the registered enforcement clients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a88a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a88a-115">Return value</span></span>

<span data-ttu-id="2a88a-116">Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.</span><span class="sxs-lookup"><span data-stu-id="2a88a-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="2a88a-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2a88a-117">Return code</span></span>                                                                                         | <span data-ttu-id="2a88a-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a88a-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a88a-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2a88a-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="2a88a-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2a88a-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2a88a-121"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="2a88a-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="2a88a-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="2a88a-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="2a88a-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="2a88a-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="2a88a-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2a88a-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2a88a-125"><dt>**RPC- \_ E \_ getrennt**</dt></span><span class="sxs-lookup"><span data-stu-id="2a88a-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2a88a-126">Der NAPAgent wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a88a-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="2a88a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a88a-127">Requirements</span></span>



| <span data-ttu-id="2a88a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a88a-128">Requirement</span></span> | <span data-ttu-id="2a88a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2a88a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a88a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a88a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2a88a-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a88a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2a88a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a88a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2a88a-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a88a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2a88a-134">Header</span><span class="sxs-lookup"><span data-stu-id="2a88a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a88a-135"><dt>Napmanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a88a-135"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a88a-136">IDL</span><span class="sxs-lookup"><span data-stu-id="2a88a-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2a88a-137"><dt>Napmanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2a88a-137"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="2a88a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2a88a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a88a-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a88a-139"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="2a88a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a88a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a88a-141">**Inapclientmanagement**</span><span class="sxs-lookup"><span data-stu-id="2a88a-141">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





