---
title: Inapclientmanagement unregisterenforcementclient-Methode (napmanagement. h)
description: Hebt die Registrierung eines Erzwingungs Clients beim NAP-System auf.
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- Unregisterenforcementclient-Methode NAP
- Unregisterenforcementclient-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, unregisterenforcementclient-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea318cf632ac00d54451b11428907c88159809df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104691"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a><span data-ttu-id="a2691-106">Inapclientmanagement:: unregisterenforcementclient-Methode</span><span class="sxs-lookup"><span data-stu-id="a2691-106">INapClientManagement::UnregisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="a2691-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a2691-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a2691-108">Durch die **unregisterenforcementclient** -Methode wird die Registrierung eines Erzwingungs Clients beim NAP-System aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="a2691-108">The **UnregisterEnforcementClient** method unregisters an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2691-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2691-109">Syntax</span></span>


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="a2691-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2691-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2691-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2691-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2691-112">Ein [**enforcemententityid**](nap-datatypes.md) -Wert, der den Erzwingungs Client für die Aufhebung der Registrierung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a2691-112">An [**EnforcementEntityId**](nap-datatypes.md) value that identifies the enforcement client to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2691-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2691-113">Return value</span></span>

<span data-ttu-id="a2691-114">Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.</span><span class="sxs-lookup"><span data-stu-id="a2691-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="a2691-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a2691-115">Return code</span></span>                                                                                         | <span data-ttu-id="a2691-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2691-116">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a2691-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a2691-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="a2691-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a2691-118">Operation successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="a2691-119"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="a2691-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="a2691-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="a2691-120">Permissions error, access denied.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a2691-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a2691-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="a2691-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a2691-122">System resource limit, could not perform the operation.</span></span><br/>             |
| <dl> <span data-ttu-id="a2691-123"><dt>**NAP \_ E \_ trotzdem \_ gebunden**</dt></span><span class="sxs-lookup"><span data-stu-id="a2691-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="a2691-124">Die Registrierung des Erzwingungs Clients konnte nicht aufgehoben werden, und bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="a2691-124">The enforcement client could not be unregistered and remains bound.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a2691-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2691-125">Requirements</span></span>



| <span data-ttu-id="a2691-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2691-126">Requirement</span></span> | <span data-ttu-id="a2691-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a2691-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2691-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2691-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a2691-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2691-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a2691-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2691-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a2691-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2691-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a2691-132">Header</span><span class="sxs-lookup"><span data-stu-id="a2691-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2691-133"><dt>Napmanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2691-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2691-134">IDL</span><span class="sxs-lookup"><span data-stu-id="a2691-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a2691-135"><dt>Napmanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a2691-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="a2691-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a2691-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2691-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2691-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="a2691-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2691-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2691-139">**Inapclientmanagement**</span><span class="sxs-lookup"><span data-stu-id="a2691-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





