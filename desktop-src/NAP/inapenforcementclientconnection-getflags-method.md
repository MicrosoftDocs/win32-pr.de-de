---
title: Inapenforcementclientconnection GetFlags-Methode (napforcementclient. h)
description: Wird verwendet, um erstmalige Antworten von Antworten aufgrund von sohrequests zu unterscheiden, die von den-enforcern zwischengespeichert wurden. | Inapenforcementclientconnection GetFlags-Methode (napforcementclient. h)
ms.assetid: e8399615-5190-46f7-a3bf-3070de548953
keywords:
- GetFlags-Methode NAP
- GetFlags-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, GetFlags-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a35e183b5d4f606d21f4afce8cca68135732a35c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354944"
---
# <a name="inapenforcementclientconnectiongetflags-method"></a><span data-ttu-id="cba8d-107">Inapenforcementclientconnection:: GetFlags-Methode</span><span class="sxs-lookup"><span data-stu-id="cba8d-107">INapEnforcementClientConnection::GetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="cba8d-108">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cba8d-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cba8d-109">Die **inapenforcementclientconnection:: GetFlags** -Methode wird verwendet, um erstmalige Antworten von Antworten aufgrund von sohrequests zu unterscheiden, die von den-enforcern zwischengespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="cba8d-109">The **INapEnforcementClientConnection::GetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="cba8d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="cba8d-110">Syntax</span></span>


```C++
HRESULT GetFlags(
  [out] UINT8 *flags
);
```



## <a name="parameters"></a><span data-ttu-id="cba8d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cba8d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cba8d-112">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cba8d-112">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cba8d-113">Ein Zeiger auf ein Flag, das bestimmt, ob die [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) auf einen zwischengespeicherten **sohrequest** zurückzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="cba8d-113">A pointer to a flag that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="cba8d-114">Wenn *Flags* den Wert [**freshsohrequest**](nap-type-constants.md)hat, handelt es sich um eine neue Anforderung. andernfalls handelt es sich um eine zwischengespeicherte Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cba8d-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cba8d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cba8d-115">Return value</span></span>

<span data-ttu-id="cba8d-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cba8d-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="cba8d-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cba8d-117">Return code</span></span>                                                                                     | <span data-ttu-id="cba8d-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cba8d-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="cba8d-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cba8d-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="cba8d-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="cba8d-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cba8d-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="cba8d-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="cba8d-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="cba8d-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="cba8d-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="cba8d-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="cba8d-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cba8d-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cba8d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cba8d-125">Requirements</span></span>



| <span data-ttu-id="cba8d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cba8d-126">Requirement</span></span> | <span data-ttu-id="cba8d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="cba8d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cba8d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cba8d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cba8d-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cba8d-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cba8d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cba8d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cba8d-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cba8d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cba8d-132">Header</span><span class="sxs-lookup"><span data-stu-id="cba8d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cba8d-133"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="cba8d-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="cba8d-134">IDL</span><span class="sxs-lookup"><span data-stu-id="cba8d-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cba8d-135"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cba8d-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="cba8d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cba8d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cba8d-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cba8d-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="cba8d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cba8d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba8d-139">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="cba8d-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





