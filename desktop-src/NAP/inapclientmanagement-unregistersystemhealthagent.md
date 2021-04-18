---
title: Inapclientmanagement unregistersystemhealthagent-Methode (napmanagement. h)
description: Hebt die Registrierung eines SHA beim NAP-System auf.
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- Unregistersystemhealthagent-Methode NAP
- Unregistersystemhealthagent-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, unregistersystemhealthagent-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff7af1c279090d12883d2a4e06ee9bcc364438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340351"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a><span data-ttu-id="b369e-106">Inapclientmanagement:: unregistersystemhealthagent-Methode</span><span class="sxs-lookup"><span data-stu-id="b369e-106">INapClientManagement::UnregisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="b369e-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b369e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b369e-108">Die **unregistersystemhealthagent** -Methode hebt die Registrierung eines SHA beim NAP-System auf.</span><span class="sxs-lookup"><span data-stu-id="b369e-108">The **UnregisterSystemHealthAgent** method unregisters an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b369e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b369e-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="b369e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b369e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b369e-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b369e-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b369e-112">Eine [**systemhealthentityid**](nap-datatypes.md) , die den Systemintegritäts-Agent identifiziert, dessen Registrierung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b369e-112">A [**SystemHealthEntityId**](nap-datatypes.md) that identifies the System Health Agent to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b369e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b369e-113">Return value</span></span>

<span data-ttu-id="b369e-114">Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.</span><span class="sxs-lookup"><span data-stu-id="b369e-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="b369e-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b369e-115">Return code</span></span>                                                                                         | <span data-ttu-id="b369e-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b369e-116">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b369e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b369e-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="b369e-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b369e-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b369e-119"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="b369e-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="b369e-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="b369e-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b369e-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="b369e-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="b369e-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b369e-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b369e-123"><dt>**NAP \_ E \_ trotzdem \_ gebunden**</dt></span><span class="sxs-lookup"><span data-stu-id="b369e-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="b369e-124">Der SHA bleibt gebunden, und die Registrierung konnte nicht aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="b369e-124">The SHA remains bound and could not be unregistered.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="b369e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b369e-125">Requirements</span></span>



| <span data-ttu-id="b369e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b369e-126">Requirement</span></span> | <span data-ttu-id="b369e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b369e-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b369e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b369e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b369e-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b369e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b369e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b369e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b369e-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b369e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b369e-132">Header</span><span class="sxs-lookup"><span data-stu-id="b369e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b369e-133"><dt>Napmanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="b369e-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="b369e-134">IDL</span><span class="sxs-lookup"><span data-stu-id="b369e-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b369e-135"><dt>Napmanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b369e-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="b369e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b369e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b369e-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b369e-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="b369e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b369e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b369e-139">**Inapclientmanagement**</span><span class="sxs-lookup"><span data-stu-id="b369e-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





