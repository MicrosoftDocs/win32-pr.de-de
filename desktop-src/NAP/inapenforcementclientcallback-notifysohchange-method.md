---
title: Inapenforcementclientcallback notifysohchange-Methode (napforcementclient. h)
description: Wird von NAPAgent verwendet, um den Erzwingungs Client über SoH-Änderungen zu informieren.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- Notifysohchange-Methode NAP
- Notifysohchange-Methode NAP, inapenforcementclientcallback-Schnittstelle
- Inapenforcementclientcallback-Schnittstelle NAP, notifysohchange-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.NotifySoHChange
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b405bca5ae27a68eea780dfcb922d1f986f475c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106431"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a><span data-ttu-id="0cbb2-106">Inapenforcementclientcallback:: notifysohchange-Methode</span><span class="sxs-lookup"><span data-stu-id="0cbb2-106">INapEnforcementClientCallback::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="0cbb2-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0cbb2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0cbb2-108">Die **inapenforcementclientcallback:: notifysohchange** -Rückruf Methode wird vom NAPAgent verwendet, um den Erzwingungs Client über SoH-Änderungen zu informieren.</span><span class="sxs-lookup"><span data-stu-id="0cbb2-108">The **INapEnforcementClientCallback::NotifySoHChange** callback method is used by the NapAgent to inform the enforcement client of SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cbb2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cbb2-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="0cbb2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cbb2-110">Parameters</span></span>

<span data-ttu-id="0cbb2-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0cbb2-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0cbb2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0cbb2-112">Return value</span></span>

<span data-ttu-id="0cbb2-113">Diese Rückruf Methode muss einen der folgenden Fehlercodes zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0cbb2-113">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="0cbb2-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0cbb2-114">Return code</span></span>                                                                                                | <span data-ttu-id="0cbb2-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0cbb2-115">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0cbb2-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0cbb2-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="0cbb2-117">Gibt diesen Wert zurück, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="0cbb2-117">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="0cbb2-118"><dt>**RPC \_ S- \_ Server nicht \_ verfügbar**</dt></span><span class="sxs-lookup"><span data-stu-id="0cbb2-118"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="0cbb2-119">Durch das zurückgeben dieses Werts wird der Enforcer aus der gebundenen SHA-Liste entfernt, und der entsprechende NAPAgent-Cache Eintrag, der geleert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0cbb2-119">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="0cbb2-120">Der fehlerhafte SHA kann dann mit dem NAPAgent erneut initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0cbb2-120">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0cbb2-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cbb2-121">Remarks</span></span>

<span data-ttu-id="0cbb2-122">Der Abschluss der systemfixinstallation ist ein System Integritäts Änderungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0cbb2-122">The completion of system fix-up is a system health change event.</span></span> <span data-ttu-id="0cbb2-123">Dies bedeutet, dass Sie **notifysohchange** aufrufen müssen, wenn eine [**inapsystemhealthagentcallback:: getfixupinfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) -Benachrichtigung anzeigt, dass der Client korrigiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0cbb2-123">That means you must call **NotifySoHChange** when a [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) notification indicates that the client is fixed.</span></span> <span data-ttu-id="0cbb2-124">Wenn ein Client korrigiert wird, hat der **Zustands** Member der [**fixupinfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) -Struktur, die von **getfixupinfo** zurückgegeben wurde, den Wert **fixupstaatuccess**.</span><span class="sxs-lookup"><span data-stu-id="0cbb2-124">When a client is fixed, the **state** member of the [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure returned by **GetFixupInfo** has a value of **fixupStateSuccess**.</span></span>

<span data-ttu-id="0cbb2-125">Nach dem Aufrufen durch den NAPAgent über diesen Rückruf muss der Erzwingungs-Agent dann [**inapenforcementclientbinding:: getsohrequest**](inapenforcementclientbinding-getsohrequest-method.md) aufrufen, um die neue Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0cbb2-125">After being called by the NapAgent via this callback, the enforcement agent must then call [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) to retrieve the new request.</span></span> <span data-ttu-id="0cbb2-126">Dieser Befehl kann im gleichen Thread wie **inapenforcementclientcallback:: notifysohchange** erfolgen.</span><span class="sxs-lookup"><span data-stu-id="0cbb2-126">This call can be made on the same thread as **INapEnforcementClientCallback::NotifySoHChange**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cbb2-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cbb2-127">Requirements</span></span>



| <span data-ttu-id="0cbb2-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0cbb2-128">Requirement</span></span> | <span data-ttu-id="0cbb2-129">Wert</span><span class="sxs-lookup"><span data-stu-id="0cbb2-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cbb2-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0cbb2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0cbb2-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cbb2-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0cbb2-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cbb2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0cbb2-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cbb2-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0cbb2-134">Header</span><span class="sxs-lookup"><span data-stu-id="0cbb2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cbb2-135"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cbb2-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cbb2-136">IDL</span><span class="sxs-lookup"><span data-stu-id="0cbb2-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0cbb2-137"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0cbb2-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cbb2-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cbb2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cbb2-139">**Inapenforcementclientcallback**</span><span class="sxs-lookup"><span data-stu-id="0cbb2-139">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





