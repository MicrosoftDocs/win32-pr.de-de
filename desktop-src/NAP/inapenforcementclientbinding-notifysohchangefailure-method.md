---
title: Inapenforcementclientbinding notifysohchangefailure-Methode (napforcementclient. h)
description: Wird vom Erzwingungs Client verwendet, um den NAPAgent darüber zu informieren, dass ein vorheriger inapenforcementclientcallback notifysohchange nicht verarbeitet werden konnte.
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- Notifysohchangefailure-Methode NAP
- Notifysohchangefailure-Methode NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, notifysohchangefailure-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifySoHChangeFailure
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af23fd41e5a8b97064c089062eae13e93cf9ff0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479263"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a><span data-ttu-id="5e876-106">Inapenforcementclientbinding:: notifysohchangefailure-Methode</span><span class="sxs-lookup"><span data-stu-id="5e876-106">INapEnforcementClientBinding::NotifySoHChangeFailure method</span></span>

> [!Note]  
> <span data-ttu-id="5e876-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5e876-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5e876-108">Die **inapenforcementclientbinding:: notifysohchangefailure** -Methode wird vom Erzwingungs Client verwendet, um den NAPAgent darüber zu informieren, dass ein vorheriger [**inapenforcementclientcallback:: notifysohchange**](inapenforcementclientcallback-notifysohchange-method.md)nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="5e876-108">The **INapEnforcementClientBinding::NotifySoHChangeFailure** method is used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e876-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e876-109">Syntax</span></span>


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a><span data-ttu-id="5e876-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e876-110">Parameters</span></span>

<span data-ttu-id="5e876-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5e876-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e876-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e876-112">Return value</span></span>

<span data-ttu-id="5e876-113">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5e876-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5e876-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5e876-114">Return code</span></span>                                                                                             | <span data-ttu-id="5e876-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e876-115">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e876-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5e876-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="5e876-117">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5e876-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="5e876-118"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="5e876-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="5e876-119">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="5e876-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5e876-120"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="5e876-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="5e876-121">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5e876-121">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5e876-122"><dt>**NAP \_ E \_ nicht \_ Initialisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="5e876-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="5e876-123">Der Enforcer wurde nicht bereits initialisiert.</span><span class="sxs-lookup"><span data-stu-id="5e876-123">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="5e876-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e876-124">Remarks</span></span>

<span data-ttu-id="5e876-125">Als Ergebnis dieses Methoden Aufrufs versucht NAPAgent, die SoH-Änderung zu einem späteren Zeitpunkt zu übernehmen, indem [**inapenforcementclientcallback:: notifysohchange**](inapenforcementclientcallback-notifysohchange-method.md) erneut aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5e876-125">As a result of this method call the NapAgent retries applying the SoH change at a later time by calling [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) again.</span></span> <span data-ttu-id="5e876-126">Nachdem der Erzwingungs Client [**inapenforcementclientbinding:: getsohrequest**](inapenforcementclientbinding-getsohrequest-method.md)aufgerufen hat, muss er die Änderung anwenden, d. h., nach diesem Punkt werden keine Fehler von der NAPAgent behandelt.</span><span class="sxs-lookup"><span data-stu-id="5e876-126">Once the enforcement client has called [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), it then must apply the change, i.e. no failures are handled by the NapAgent after this point.</span></span>

<span data-ttu-id="5e876-127">Der Erzwingungs Client muss die [**inapenforcementclientbinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) -Methode aufrufen, bevor diese oder eine andere Methode der [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5e876-127">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e876-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e876-128">Requirements</span></span>



| <span data-ttu-id="5e876-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e876-129">Requirement</span></span> | <span data-ttu-id="5e876-130">Wert</span><span class="sxs-lookup"><span data-stu-id="5e876-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e876-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e876-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5e876-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e876-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5e876-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e876-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5e876-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e876-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5e876-135">Header</span><span class="sxs-lookup"><span data-stu-id="5e876-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e876-136"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e876-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e876-137">IDL</span><span class="sxs-lookup"><span data-stu-id="5e876-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e876-138"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e876-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="5e876-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5e876-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e876-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e876-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5e876-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e876-141">See also</span></span>

<dl> <span data-ttu-id="5e876-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5e876-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="5e876-143">**Inapenforcementclientbinding**</span><span class="sxs-lookup"><span data-stu-id="5e876-143">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="5e876-144">**Inapenforcementclientbinding:: getsohrequest**</span><span class="sxs-lookup"><span data-stu-id="5e876-144">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[<span data-ttu-id="5e876-145">**Inapenforcementclientcallback:: notifysohchange**</span><span class="sxs-lookup"><span data-stu-id="5e876-145">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 





