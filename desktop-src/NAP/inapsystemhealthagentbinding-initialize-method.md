---
title: Inapsystemhealthagentbinding Initialize-Methode (napsystemhealthagent. h)
description: Initialisiert den Systemintegritäts-Agent (SHA) und bindet den SHA an den NAPAgent-Dienst.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Methode "NAP initialisieren"
- Initialize-Methode NAP, inapsystemhealthagentbinding-Schnittstelle
- Inapsystemhealthagentbinding-Schnittstelle NAP, Initialize-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee4d4f602303ca1943e47c04ba30ab8f6e75e72
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340388"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a><span data-ttu-id="185c3-106">Inapsystemhealthagentbinding:: Initialize-Methode</span><span class="sxs-lookup"><span data-stu-id="185c3-106">INapSystemHealthAgentBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="185c3-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="185c3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="185c3-108">Die **inapsystemhealthagentbinding:: Initialize** -Methode initialisiert den Systemintegritäts-Agent (SHA) und bindet den SHA an den NAPAgent-Dienst.</span><span class="sxs-lookup"><span data-stu-id="185c3-108">The **INapSystemHealthAgentBinding::Initialize** method initializes the system health agent (SHA) and binds the SHA to the NapAgent service.</span></span> <span data-ttu-id="185c3-109">Diese Methode muss aufgerufen werden, bevor eine andere Methode in der [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="185c3-109">This method must be called before calling any other method on the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="185c3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="185c3-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="185c3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="185c3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="185c3-112">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="185c3-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="185c3-113">Eine eindeutige [systemhealthentityid](nap-datatypes.md) , die die ID des SHA enthält, der an den NAPAgent-Dienst gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="185c3-113">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA being bound to the NapAgent service.</span></span>

</dd> <dt>

<span data-ttu-id="185c3-114">*Rückruf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="185c3-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="185c3-115">Ein com-Zeiger auf eine [**inapsystemhealthagentcallback**](inapsystemhealthagentcallback.md) -Schnittstelle, die vom NAPAgent verwendet wird, um den Integritäts-Agent mit einer Benachrichtigung/einem Prozess zu Rückruf.</span><span class="sxs-lookup"><span data-stu-id="185c3-115">A COM pointer to an [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) interface used by the NapAgent to callback the health agent with a notify/process.</span></span> <span data-ttu-id="185c3-116">Der NAPAgent enthält einen Verweis auf das Objekt, das dieser Schnittstelle zugeordnet ist, bis die [**uninitialisierung**](inapsystemhealthagentbinding-uninitialize-method.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="185c3-116">The NapAgent holds a reference to the object associated with this interface until [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="185c3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="185c3-117">Return value</span></span>

<span data-ttu-id="185c3-118">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="185c3-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="185c3-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="185c3-119">Return code</span></span>                                                                                                | <span data-ttu-id="185c3-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="185c3-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="185c3-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="185c3-121"><dt>**S\_OK** </dt></span></span> </dl>                      | <span data-ttu-id="185c3-122">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="185c3-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="185c3-123"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="185c3-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>            | <span data-ttu-id="185c3-124">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="185c3-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="185c3-125"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="185c3-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>             | <span data-ttu-id="185c3-126">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="185c3-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="185c3-127"><dt>**Fehler \_ bereits \_ Initialisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="185c3-127"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="185c3-128">Wenn das SHA zuvor initialisiert wurde, wird dieser Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="185c3-128">If the SHA has initialized previously, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="185c3-129"><dt>**NAP \_ E \_ nicht \_ registriert**</dt></span><span class="sxs-lookup"><span data-stu-id="185c3-129"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>     | <span data-ttu-id="185c3-130">Wenn der SHA nicht bereits zuvor registriert wurde, wird dieser Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="185c3-130">If the SHA has not registered earlier, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="185c3-131"><dt>**RPC- \_ E \_ getrennt**</dt></span><span class="sxs-lookup"><span data-stu-id="185c3-131"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>        | <span data-ttu-id="185c3-132">Der NAPAgent wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="185c3-132">The NapAgent has been stopped.</span></span> <span data-ttu-id="185c3-133">Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.</span><span class="sxs-lookup"><span data-stu-id="185c3-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="185c3-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="185c3-134">Remarks</span></span>

<span data-ttu-id="185c3-135">Der "NAPAgent" löst keinen SoH-Austausch aufgrund der Initialisierung aus.</span><span class="sxs-lookup"><span data-stu-id="185c3-135">The NapAgent does not trigger a SoH exchange as a result of initialization.</span></span> <span data-ttu-id="185c3-136">Ein Systemintegritäts-Agent muss [**notifysohchange**](inapsystemhealthagentbinding-notifysohchange-method.md) anrufen, um nach der Initialisierung mit dem NAPAgent einen Austausch von SoH-Paketen anzufordern.</span><span class="sxs-lookup"><span data-stu-id="185c3-136">A system health agent must call [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to request an exchange of SoH packets after initializing with the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="185c3-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="185c3-137">Requirements</span></span>



| <span data-ttu-id="185c3-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="185c3-138">Requirement</span></span> | <span data-ttu-id="185c3-139">Wert</span><span class="sxs-lookup"><span data-stu-id="185c3-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="185c3-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="185c3-140">Minimum supported client</span></span><br/> | <span data-ttu-id="185c3-141">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="185c3-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="185c3-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="185c3-142">Minimum supported server</span></span><br/> | <span data-ttu-id="185c3-143">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="185c3-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="185c3-144">Header</span><span class="sxs-lookup"><span data-stu-id="185c3-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="185c3-145"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="185c3-145"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="185c3-146">IDL</span><span class="sxs-lookup"><span data-stu-id="185c3-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="185c3-147"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="185c3-147"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="185c3-148">DLL</span><span class="sxs-lookup"><span data-stu-id="185c3-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="185c3-149"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="185c3-149"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="185c3-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="185c3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="185c3-151">**Inapsystemhealthagentbinding**</span><span class="sxs-lookup"><span data-stu-id="185c3-151">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





