---
title: Inapenforcementclientbinding getsohrequest-Methode (napforcementclient. h)
description: Wird vom Erzwingungs Client zum Abrufen einer SoH-Anforderung für eine bestimmte Verbindung verwendet.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- Getsohrequest-Methode NAP
- Getsohrequest-Methode NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, getsohrequest-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9fed4872df7ab328ab241b070a9eeb07907de85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949669"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a><span data-ttu-id="10dbe-106">Inapenforcementclientbinding:: getsohrequest-Methode</span><span class="sxs-lookup"><span data-stu-id="10dbe-106">INapEnforcementClientBinding::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="10dbe-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="10dbe-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="10dbe-108">Die **inapenforcementclientbinding:: getsohrequest** -Methode wird vom Erzwingungs Client zum Abrufen einer SoH-Anforderung für eine bestimmte Verbindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="10dbe-108">The **INapEnforcementClientBinding::GetSoHRequest** method is used by the enforcement client to retrieve an SoH-request for a particular connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="10dbe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="10dbe-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a><span data-ttu-id="10dbe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="10dbe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10dbe-111">*Verbindung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10dbe-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10dbe-112">Ein com-Zeiger auf eine [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="10dbe-112">A COM pointer to an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface.</span></span> <span data-ttu-id="10dbe-113">Der NAPAgent enthält keine Verweise auf das-Objekt, das dieser Schnittstelle zugeordnet ist, nachdem die-Methode abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="10dbe-113">The NapAgent does not hold references to the object associated with this interface after the method completes.</span></span>

</dd> <dt>

<span data-ttu-id="10dbe-114">*retriggerhint* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="10dbe-114">*retriggerHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10dbe-115">Ein Zeiger auf einen **booleschen** Wert, der angibt, ob die Verbindung erneut ausgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="10dbe-115">A pointer to a **BOOL** that indicates if the connection should be re-triggered.</span></span> <span data-ttu-id="10dbe-116">Es ist **true** , wenn sich der [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) seit dem letzten Aufruf dieser Funktion geändert hat oder wenn [**probationtime**](nap-datatypes.md) abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="10dbe-116">It is **TRUE** if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) has changed since this function was last called or if [**ProbationTime**](nap-datatypes.md) has expired.</span></span> <span data-ttu-id="10dbe-117">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="10dbe-117">Otherwise, **FALSE** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10dbe-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10dbe-118">Return value</span></span>

<span data-ttu-id="10dbe-119">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="10dbe-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="10dbe-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="10dbe-120">Return code</span></span>                                                                                             | <span data-ttu-id="10dbe-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10dbe-121">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="10dbe-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="10dbe-122"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="10dbe-123">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="10dbe-123">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="10dbe-124"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="10dbe-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="10dbe-125">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="10dbe-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="10dbe-126"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="10dbe-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="10dbe-127">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="10dbe-127">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="10dbe-128"><dt>**NAP \_ E \_ nicht \_ Initialisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="10dbe-128"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="10dbe-129">Der Enforcer wurde nicht bereits initialisiert.</span><span class="sxs-lookup"><span data-stu-id="10dbe-129">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="10dbe-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10dbe-130">Remarks</span></span>

<span data-ttu-id="10dbe-131">Der NAPAgent legt die [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) für das Verbindungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="10dbe-131">The NapAgent sets the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the connection object.</span></span>

<span data-ttu-id="10dbe-132">Wenn für diese Verbindung eine [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) aussteht, wird sie verworfen, und die SHAs werden über verwaiste **sohrequests** benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="10dbe-132">If an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was outstanding on this connection, then it is discarded, and the SHAs are notified of orphaned **SoHRequests**.</span></span>

<span data-ttu-id="10dbe-133">Der Erzwingungs Client muss die [**inapenforcementclientbinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) -Methode aufrufen, bevor diese oder eine andere Methode der [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="10dbe-133">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="10dbe-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10dbe-134">Requirements</span></span>



| <span data-ttu-id="10dbe-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10dbe-135">Requirement</span></span> | <span data-ttu-id="10dbe-136">Wert</span><span class="sxs-lookup"><span data-stu-id="10dbe-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10dbe-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10dbe-137">Minimum supported client</span></span><br/> | <span data-ttu-id="10dbe-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10dbe-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="10dbe-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10dbe-139">Minimum supported server</span></span><br/> | <span data-ttu-id="10dbe-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10dbe-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="10dbe-141">Header</span><span class="sxs-lookup"><span data-stu-id="10dbe-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="10dbe-142"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="10dbe-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="10dbe-143">IDL</span><span class="sxs-lookup"><span data-stu-id="10dbe-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="10dbe-144"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="10dbe-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="10dbe-145">DLL</span><span class="sxs-lookup"><span data-stu-id="10dbe-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10dbe-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10dbe-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="10dbe-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10dbe-147">See also</span></span>

<dl> <span data-ttu-id="10dbe-148"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="10dbe-148"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="10dbe-149">**Inapenforcementclientbinding**</span><span class="sxs-lookup"><span data-stu-id="10dbe-149">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





