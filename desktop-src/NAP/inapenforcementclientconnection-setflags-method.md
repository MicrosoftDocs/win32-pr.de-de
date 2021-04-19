---
title: Inapenforcementclientconnection setFlags-Methode (napforcementclient. h)
description: Wird verwendet, um erstmalige Antworten von Antworten aufgrund von sohrequests zu unterscheiden, die von den-enforcern zwischengespeichert wurden. | Inapenforcementclientconnection setFlags-Methode (napforcementclient. h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- SetFlags-Methode NAP
- SetFlags-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, setFlags-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489997fb97f0e97c5a72d23646af8ae92272628
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355765"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a><span data-ttu-id="79c11-107">Inapenforcementclientconnection:: setFlags-Methode</span><span class="sxs-lookup"><span data-stu-id="79c11-107">INapEnforcementClientConnection::SetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="79c11-108">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="79c11-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="79c11-109">Die **inapenforcementclientconnection:: setFlags** -Methode wird verwendet, um erstmalige Antworten von Antworten aufgrund von sohrequests zu unterscheiden, die von den-enforcern zwischengespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="79c11-109">The **INapEnforcementClientConnection::SetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="79c11-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="79c11-110">Syntax</span></span>


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a><span data-ttu-id="79c11-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="79c11-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79c11-112">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79c11-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79c11-113">Flags, die bestimmen, ob die [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) auf einen zwischengespeicherten **sohrequest** zurückzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="79c11-113">Flags that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="79c11-114">Wenn *Flags* den Wert [**freshsohrequest**](nap-type-constants.md)hat, handelt es sich um eine neue Anforderung. andernfalls handelt es sich um eine zwischengespeicherte Anforderung.</span><span class="sxs-lookup"><span data-stu-id="79c11-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79c11-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79c11-115">Return value</span></span>

<span data-ttu-id="79c11-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="79c11-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="79c11-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="79c11-117">Return code</span></span>                                                                                     | <span data-ttu-id="79c11-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79c11-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="79c11-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="79c11-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="79c11-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="79c11-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="79c11-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="79c11-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="79c11-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="79c11-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="79c11-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="79c11-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="79c11-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="79c11-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="79c11-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79c11-125">Remarks</span></span>

<span data-ttu-id="79c11-126">Dieser Wert wird von NAPAgent festgelegt.</span><span class="sxs-lookup"><span data-stu-id="79c11-126">This value is set by the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="79c11-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79c11-127">Requirements</span></span>



| <span data-ttu-id="79c11-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79c11-128">Requirement</span></span> | <span data-ttu-id="79c11-129">Wert</span><span class="sxs-lookup"><span data-stu-id="79c11-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79c11-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79c11-130">Minimum supported client</span></span><br/> | <span data-ttu-id="79c11-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79c11-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="79c11-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79c11-132">Minimum supported server</span></span><br/> | <span data-ttu-id="79c11-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79c11-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="79c11-134">Header</span><span class="sxs-lookup"><span data-stu-id="79c11-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="79c11-135"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="79c11-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="79c11-136">IDL</span><span class="sxs-lookup"><span data-stu-id="79c11-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79c11-137"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79c11-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="79c11-138">DLL</span><span class="sxs-lookup"><span data-stu-id="79c11-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79c11-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79c11-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="79c11-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79c11-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c11-141">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="79c11-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





