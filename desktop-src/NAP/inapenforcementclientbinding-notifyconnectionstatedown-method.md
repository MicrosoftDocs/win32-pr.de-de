---
title: Inapenforcementclientbinding notifyconnectionstatedown-Methode (napforcementclient. h)
description: Wird verwendet, um den NAPAgent darüber zu informieren, dass eine Verbindung zu einem Erzwingungs Client nicht mehr besteht.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- Notifyconnectionstatedown-Methode NAP
- Notifyconnectionstatedown-Methode NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, notifyconnectionstatedown-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifyConnectionStateDown
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3129883342f493fd56a4cc81513910e8789ca4f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519279"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a><span data-ttu-id="5471c-106">Inapenforcementclientbinding:: notifyconnectionstatedown-Methode</span><span class="sxs-lookup"><span data-stu-id="5471c-106">INapEnforcementClientBinding::NotifyConnectionStateDown method</span></span>

> [!Note]  
> <span data-ttu-id="5471c-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5471c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5471c-108">Die **inapenforcementclientbinding:: notifyconnectionstatedown** -Methode wird verwendet, um den NAPAgent darüber zu informieren, dass eine Verbindung zu einem Erzwingungs Client nicht mehr besteht.</span><span class="sxs-lookup"><span data-stu-id="5471c-108">The **INapEnforcementClientBinding::NotifyConnectionStateDown** method is used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span>

## <a name="syntax"></a><span data-ttu-id="5471c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5471c-109">Syntax</span></span>


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a><span data-ttu-id="5471c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5471c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5471c-111">*downcxn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5471c-111">*downCxn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5471c-112">Ein com-Zeiger auf die [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Schnittstelle der nach-unten-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="5471c-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the down connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5471c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5471c-113">Return value</span></span>

<span data-ttu-id="5471c-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5471c-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5471c-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5471c-115">Return code</span></span>                                                                                             | <span data-ttu-id="5471c-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5471c-116">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5471c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5471c-117"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="5471c-118">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5471c-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="5471c-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="5471c-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="5471c-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="5471c-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5471c-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="5471c-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="5471c-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5471c-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5471c-123"><dt>**NAP \_ E \_ nicht \_ Initialisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="5471c-123"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="5471c-124">Der Enforcer wurde nicht bereits initialisiert.</span><span class="sxs-lookup"><span data-stu-id="5471c-124">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="5471c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5471c-125">Remarks</span></span>

<span data-ttu-id="5471c-126">Wenn eine der von einem Erzwingungs Client eingerichteten Verbindungen herunterfährt, sollte der Erzwingungs Client die Verbindung aus der aktiven Liste entfernen und den NAPAgent mithilfe dieser Methode informieren.</span><span class="sxs-lookup"><span data-stu-id="5471c-126">When any of the connections established by an enforcement client go down, the enforcement client should remove the connection from its active list and inform the NapAgent using this method.</span></span> <span data-ttu-id="5471c-127">Sobald dieser Rückruf zurückkehrt, kann das Verbindungs Objekt freigegeben und freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5471c-127">As soon as this call returns, the connection object can be released and freed.</span></span> <span data-ttu-id="5471c-128">Der NAPAgent hält keine Verweise auf das Verbindungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="5471c-128">The NapAgent will not hold references to the connection object.</span></span>

<span data-ttu-id="5471c-129">Als Ergebnis dieser Benachrichtigung aktualisiert der NAPAgent den NAP-Status des Systems entsprechend.</span><span class="sxs-lookup"><span data-stu-id="5471c-129">As a result of this notification, the NapAgent updates its system NAP state as appropriate.</span></span>

<span data-ttu-id="5471c-130">Der Erzwingungs Client muss die [**inapenforcementclientbinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) -Methode aufrufen, bevor diese oder eine andere Methode der [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5471c-130">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="5471c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5471c-131">Requirements</span></span>



| <span data-ttu-id="5471c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5471c-132">Requirement</span></span> | <span data-ttu-id="5471c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5471c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5471c-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5471c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5471c-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5471c-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5471c-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5471c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5471c-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5471c-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5471c-138">Header</span><span class="sxs-lookup"><span data-stu-id="5471c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5471c-139"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5471c-139"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5471c-140">IDL</span><span class="sxs-lookup"><span data-stu-id="5471c-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5471c-141"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5471c-141"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="5471c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5471c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5471c-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5471c-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5471c-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5471c-144">See also</span></span>

<dl> <span data-ttu-id="5471c-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5471c-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="5471c-146">**Inapenforcementclientbinding**</span><span class="sxs-lookup"><span data-stu-id="5471c-146">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





