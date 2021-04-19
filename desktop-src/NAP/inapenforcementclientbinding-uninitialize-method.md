---
title: Inapenforcementclientbinding-Methode zur uninitialisierung (napforcementclient. h)
description: Schließt den NAPAgent-Dienst ab.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Methode "NAP initialisieren"
- Uninitialize-Methode, NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, Uninitialize-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4132ff1a498a598483758623a588fa26e8b75021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342487"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a><span data-ttu-id="0f27a-106">Inapenforcementclientbinding:: Uninitialize-Methode</span><span class="sxs-lookup"><span data-stu-id="0f27a-106">INapEnforcementClientBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="0f27a-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0f27a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0f27a-108">Die **inapenforcementclientbinding:: Uninitialize** -Methode beendet den NAPAgent-Dienst.</span><span class="sxs-lookup"><span data-stu-id="0f27a-108">The **INapEnforcementClientBinding::Uninitialize** method concludes the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f27a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f27a-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="0f27a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f27a-110">Parameters</span></span>

<span data-ttu-id="0f27a-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0f27a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f27a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f27a-112">Return value</span></span>

<span data-ttu-id="0f27a-113">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0f27a-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0f27a-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0f27a-114">Return code</span></span>                                                                                     | <span data-ttu-id="0f27a-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f27a-115">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f27a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f27a-116"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0f27a-117">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0f27a-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="0f27a-118"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="0f27a-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0f27a-119">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="0f27a-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0f27a-120"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="0f27a-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0f27a-121">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0f27a-121">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f27a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f27a-122">Remarks</span></span>

<span data-ttu-id="0f27a-123">Der NAPAgent blockiert die weitere Verarbeitung, bis alle vorhandenen Aufrufe an die [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle und die [**inapenforcementclientcallback**](inapenforcementclientcallback.md) -Schnittstelle vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="0f27a-123">The NapAgent blocks further processing until all existing calls on the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) and [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interfaces complete.</span></span> <span data-ttu-id="0f27a-124">Am Ende dieses Aufrufes gibt der NAPAgent alle Verweise auf com-Zeiger für Erzwingungs Clients frei.</span><span class="sxs-lookup"><span data-stu-id="0f27a-124">At the end of this call, the NapAgent releases all its references on enforcement client COM pointers.</span></span>

<span data-ttu-id="0f27a-125">Bevor diese Funktion aufgerufen wird, muss der Enforcer für alle aktiven Verbindungen [**inapenforcementclientbinding:: notifyconnectionstatedown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) aufrufen, sodass die SHAs benachrichtigt werden können, wenn eine ihrer SoH-Requests verwaist ist.</span><span class="sxs-lookup"><span data-stu-id="0f27a-125">Before this function is called, the enforcer must call [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) on all its active connections, so the SHAs can be notified if any of their SoH-Requests were orphaned.</span></span>

<span data-ttu-id="0f27a-126">Der Erzwingungs Client muss die [**inapenforcementclientbinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) -Methode aufrufen, bevor diese oder eine andere Methode der [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0f27a-126">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f27a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f27a-127">Requirements</span></span>



| <span data-ttu-id="0f27a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f27a-128">Requirement</span></span> | <span data-ttu-id="0f27a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="0f27a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f27a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f27a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0f27a-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f27a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0f27a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f27a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0f27a-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f27a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0f27a-134">Header</span><span class="sxs-lookup"><span data-stu-id="0f27a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f27a-135"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f27a-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f27a-136">IDL</span><span class="sxs-lookup"><span data-stu-id="0f27a-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f27a-137"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f27a-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="0f27a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0f27a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f27a-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f27a-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="0f27a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f27a-140">See also</span></span>

<dl> <span data-ttu-id="0f27a-141"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="0f27a-141"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="0f27a-142">**Inapenforcementclientbinding**</span><span class="sxs-lookup"><span data-stu-id="0f27a-142">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="0f27a-143">**Inapenforcementclientbinding:: notifyconnectionstatedown**</span><span class="sxs-lookup"><span data-stu-id="0f27a-143">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[<span data-ttu-id="0f27a-144">**Inapenforcementclientcallback**</span><span class="sxs-lookup"><span data-stu-id="0f27a-144">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





