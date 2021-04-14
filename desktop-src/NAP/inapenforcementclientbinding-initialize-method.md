---
title: Inapenforcementclientbinding Initialize-Methode (napforcementclient. h)
description: Startet den NAPAgent-Dienst automatisch.
ms.assetid: 6b51043d-a8e7-41e4-9da9-e7f18f9bd068
keywords:
- Methode "NAP initialisieren"
- Initialize-Methode NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, Initialize-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4d385e47bbbfe2e315d0a93d1f92542e8328e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475999"
---
# <a name="inapenforcementclientbindinginitialize-method"></a><span data-ttu-id="e2338-106">Inapenforcementclientbinding:: Initialize-Methode</span><span class="sxs-lookup"><span data-stu-id="e2338-106">INapEnforcementClientBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="e2338-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e2338-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e2338-108">Mit der **inapenforcementclientbinding:: Initialize** -Methode wird der NAPAgent-Dienst automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="e2338-108">The **INapEnforcementClientBinding::Initialize** method starts up the NapAgent service automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2338-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2338-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId           id,
  [in] INapEnforcementClientCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="e2338-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2338-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2338-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2338-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2338-112">Eine [**enforcemententityid**](nap-datatypes.md) , die den Erzwingungs Client und seine Version identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e2338-112">An [**EnforcementEntityId**](nap-datatypes.md) that identifies the enforcement client and its version.</span></span>

</dd> <dt>

<span data-ttu-id="e2338-113">*Rückruf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2338-113">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2338-114">Ein com-Zeiger auf eine [**inapenforcementclientcallback**](inapenforcementclientcallback.md) -Schnittstelle, die vom NAPAgent verwendet wird, um die Erzwingungs Clients mit Benachrichtigen/verarbeiten zu Rückruf.</span><span class="sxs-lookup"><span data-stu-id="e2338-114">A COM pointer to an [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interface used by the NapAgent to callback the enforcement clients with notify/process.</span></span> <span data-ttu-id="e2338-115">Der NAPAgent enthält einen Verweis auf das Objekt, das dieser Schnittstelle zugeordnet ist, bis [**inapenforcementclientbinding:: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e2338-115">The NapAgent holds a reference to the object associated with this interface until [**INapEnforcementClientBinding::Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2338-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2338-116">Return value</span></span>

<span data-ttu-id="e2338-117">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e2338-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e2338-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e2338-118">Return code</span></span>                                                                                                         | <span data-ttu-id="e2338-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2338-119">Description</span></span>                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e2338-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e2338-120"><dt>**S\_OK** </dt></span></span> </dl>                               | <span data-ttu-id="e2338-121">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e2338-121">The operation is successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="e2338-122"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="e2338-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>                     | <span data-ttu-id="e2338-123">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="e2338-123">Permissions error, access denied.</span></span><br/>                                             |
| <dl> <span data-ttu-id="e2338-124"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="e2338-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>                      | <span data-ttu-id="e2338-125">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e2338-125">System resource limit, could not perform the operation.</span></span><br/>                       |
| <dl> <span data-ttu-id="e2338-126"><dt>**HRESULT (Fehler \_ bereits \_ initialisiert)**</dt></span><span class="sxs-lookup"><span data-stu-id="e2338-126"><dt>**HRESULT(ERROR\_ALREADY\_INITIALIZED)**</dt></span></span> </dl> | <span data-ttu-id="e2338-127">Wenn der Enforcer zuvor initialisiert wurde, wird dieser Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2338-127">If the enforcer has initialized previously, then this error code is returned.</span></span><br/> |
| <dl> <span data-ttu-id="e2338-128"><dt>**NAP \_ E \_ nicht \_ registriert**</dt></span><span class="sxs-lookup"><span data-stu-id="e2338-128"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>              | <span data-ttu-id="e2338-129">Wenn der Enforcer nicht zuvor registriert wurde, wird dieser Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2338-129">If the enforcer has not registered earlier, this error code is returned.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="e2338-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2338-130">Remarks</span></span>

<span data-ttu-id="e2338-131">Der Erzwingungs Client muss die **inapenforcementclientbinding:: Initialize** -Methode aufrufen, bevor eine andere Methode der [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e2338-131">The enforcement client must call the **INapEnforcementClientBinding::Initialize** method before calling any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2338-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2338-132">Requirements</span></span>



| <span data-ttu-id="e2338-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2338-133">Requirement</span></span> | <span data-ttu-id="e2338-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e2338-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2338-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2338-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e2338-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2338-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e2338-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2338-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e2338-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2338-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e2338-139">Header</span><span class="sxs-lookup"><span data-stu-id="e2338-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2338-140"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2338-140"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2338-141">IDL</span><span class="sxs-lookup"><span data-stu-id="e2338-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e2338-142"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e2338-142"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="e2338-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e2338-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2338-144"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2338-144"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e2338-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2338-145">See also</span></span>

<dl> <span data-ttu-id="e2338-146"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e2338-146"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="e2338-147">**Inapenforcementclientbinding**</span><span class="sxs-lookup"><span data-stu-id="e2338-147">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="e2338-148">**Inapenforcementclientbinding:: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="e2338-148">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)
</dt> </dl>

 

 





