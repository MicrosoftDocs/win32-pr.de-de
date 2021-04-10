---
title: Inapclientmanagement getregisteredsystemhealthagents-Methode (napmanagement. h)
description: Ruft Informationen über die registrierten SHAs ab.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- Getregisteredsystemhealthagents-Methode NAP
- Getregisteredsystemhealthagents-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, getregisteredsystemhealthagents-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredSystemHealthAgents
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4852e2d4c1ffa08b1a7ea7b3d8395c1b116cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956770"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a><span data-ttu-id="22af4-106">Inapclientmanagement:: getregisteredsystemhealthagents-Methode</span><span class="sxs-lookup"><span data-stu-id="22af4-106">INapClientManagement::GetRegisteredSystemHealthAgents method</span></span>

> [!Note]  
> <span data-ttu-id="22af4-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="22af4-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="22af4-108">Die **getregisteredsystemhealthagents** -Methode ruft Informationen über die registrierten SHAs ab.</span><span class="sxs-lookup"><span data-stu-id="22af4-108">The **GetRegisteredSystemHealthAgents** method retrieves information about the registered SHAs.</span></span>

## <a name="syntax"></a><span data-ttu-id="22af4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="22af4-109">Syntax</span></span>


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a><span data-ttu-id="22af4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22af4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22af4-111">*Anzahl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="22af4-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22af4-112">Ein Zeiger auf einen [**systemhealthentitycount**](nap-datatypes.md) , der die Anzahl der registrierten SHAs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="22af4-112">A pointer to a [**SystemHealthEntityCount**](nap-datatypes.md) that describes the number of registered SHAs.</span></span>

</dd> <dt>

<span data-ttu-id="22af4-113">*Agents* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="22af4-113">*agents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22af4-114">Ein Zeiger auf ein Array von [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Strukturen, das die registrierten SHAs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="22af4-114">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures that describe the registered SHAs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22af4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22af4-115">Return value</span></span>

<span data-ttu-id="22af4-116">Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.</span><span class="sxs-lookup"><span data-stu-id="22af4-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="22af4-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="22af4-117">Return code</span></span>                                                                                         | <span data-ttu-id="22af4-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22af4-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="22af4-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22af4-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="22af4-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="22af4-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="22af4-121"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="22af4-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="22af4-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="22af4-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="22af4-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="22af4-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="22af4-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="22af4-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="22af4-125"><dt>**RPC- \_ E \_ getrennt**</dt></span><span class="sxs-lookup"><span data-stu-id="22af4-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="22af4-126">Der NAPAgent wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22af4-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="22af4-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22af4-127">Requirements</span></span>



| <span data-ttu-id="22af4-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22af4-128">Requirement</span></span> | <span data-ttu-id="22af4-129">Wert</span><span class="sxs-lookup"><span data-stu-id="22af4-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="22af4-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22af4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="22af4-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22af4-131">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="22af4-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22af4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="22af4-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22af4-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="22af4-134">Header</span><span class="sxs-lookup"><span data-stu-id="22af4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="22af4-135"><dt>Napmanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="22af4-135"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="22af4-136">IDL</span><span class="sxs-lookup"><span data-stu-id="22af4-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="22af4-137"><dt>Napmanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="22af4-137"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="22af4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="22af4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22af4-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22af4-139"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="22af4-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22af4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22af4-141">**Inapclientmanagement**</span><span class="sxs-lookup"><span data-stu-id="22af4-141">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





