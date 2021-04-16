---
title: Inapenforcementclientconnection setsohresponse-Methode (napforcementclient. h)
description: Legt den SoH-Response fest und wird vom Erzwingungs Client beim Empfang eines Pakets verwendet.
ms.assetid: 718669c7-73cf-44f4-8463-c59fdbe215cc
keywords:
- Setsohresponse-Methode NAP
- Setsohresponse-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, setsohresponse-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdc403a1ff68e28f7d262e64ebe558226741b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478033"
---
# <a name="inapenforcementclientconnectionsetsohresponse-method"></a><span data-ttu-id="4f9b9-106">Inapenforcementclientconnection:: setsohresponse-Methode</span><span class="sxs-lookup"><span data-stu-id="4f9b9-106">INapEnforcementClientConnection::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="4f9b9-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4f9b9-108">Die **inapenforcementclientconnection:: setsohresponse** -Methode legt die SoH-Response fest und wird vom Erzwingungs Client beim Empfang eines Pakets verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-108">The **INapEnforcementClientConnection::SetSoHResponse** method sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f9b9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f9b9-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const NetworkSoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="4f9b9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f9b9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f9b9-111">*sohresponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f9b9-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f9b9-112">Ein Zeiger auf eine eindeutige [**networksohresponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) -Struktur, bei der es sich um ein undurchsichtiges Daten-BLOB für den-Enforcer handelt.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-112">A pointer to a unique [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f9b9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f9b9-113">Return value</span></span>

<span data-ttu-id="4f9b9-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4f9b9-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4f9b9-115">Return code</span></span>                                                                                     | <span data-ttu-id="4f9b9-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f9b9-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f9b9-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4f9b9-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="4f9b9-118">Das SoH-Paket ist gültig.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="4f9b9-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="4f9b9-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="4f9b9-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4f9b9-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="4f9b9-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="4f9b9-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4f9b9-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f9b9-123">Remarks</span></span>

<span data-ttu-id="4f9b9-124">Ein Paket mit 0 (null) ist gültig.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-124">A zero-sized packet is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f9b9-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f9b9-125">Requirements</span></span>



| <span data-ttu-id="4f9b9-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f9b9-126">Requirement</span></span> | <span data-ttu-id="4f9b9-127">Wert</span><span class="sxs-lookup"><span data-stu-id="4f9b9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f9b9-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f9b9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4f9b9-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f9b9-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4f9b9-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f9b9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4f9b9-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f9b9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4f9b9-132">Header</span><span class="sxs-lookup"><span data-stu-id="4f9b9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f9b9-133"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f9b9-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f9b9-134">IDL</span><span class="sxs-lookup"><span data-stu-id="4f9b9-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4f9b9-135"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4f9b9-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="4f9b9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4f9b9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f9b9-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f9b9-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4f9b9-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f9b9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f9b9-139">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="4f9b9-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





