---
title: Inapenforcementclientconnection GetConnectionID-Methode (napforcementclient. h)
description: Wird verwendet, um die eindeutige Verbindungs-ID des Clients zu erhalten.
ms.assetid: bf744aa6-5786-473f-9508-db4ee0c75578
keywords:
- GetConnectionID-Methode NAP
- GetConnectionID-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, GetConnectionID-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3ca16aea3c77ccf78359c3cdf5ab6461bc2219e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106425"
---
# <a name="inapenforcementclientconnectiongetconnectionid-method"></a><span data-ttu-id="7458d-106">Inapenforcementclientconnection:: GetConnectionID-Methode</span><span class="sxs-lookup"><span data-stu-id="7458d-106">INapEnforcementClientConnection::GetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="7458d-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7458d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7458d-108">Die **inapenforcementclientconnection:: GetConnectionID** -Methode wird verwendet, um die eindeutige Verbindungs-ID des Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7458d-108">The **INapEnforcementClientConnection::GetConnectionId** method is used to get the unique connection ID of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="7458d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7458d-109">Syntax</span></span>


```C++
HRESULT GetConnectionId(
  [out] ConnectionId **connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="7458d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7458d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7458d-111">*ConnectionID* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7458d-111">*connectionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7458d-112">Ein Zeiger auf einen Zeiger auf eine [**ConnectionID**](nap-datatypes.md) , die diese Verbindung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7458d-112">A pointer to a pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies this connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7458d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7458d-113">Return value</span></span>

<span data-ttu-id="7458d-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7458d-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7458d-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7458d-115">Return code</span></span>                                                                                     | <span data-ttu-id="7458d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7458d-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7458d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7458d-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="7458d-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7458d-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7458d-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="7458d-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="7458d-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="7458d-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7458d-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="7458d-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="7458d-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7458d-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7458d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7458d-123">Remarks</span></span>

<span data-ttu-id="7458d-124">Die Verbindungs-ID wird in erster Linie zu Protokollierungs Zwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="7458d-124">The connection ID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="7458d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7458d-125">Requirements</span></span>



| <span data-ttu-id="7458d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7458d-126">Requirement</span></span> | <span data-ttu-id="7458d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7458d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7458d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7458d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7458d-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7458d-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7458d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7458d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7458d-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7458d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7458d-132">Header</span><span class="sxs-lookup"><span data-stu-id="7458d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7458d-133"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7458d-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="7458d-134">IDL</span><span class="sxs-lookup"><span data-stu-id="7458d-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7458d-135"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7458d-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="7458d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7458d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7458d-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7458d-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7458d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7458d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7458d-139">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="7458d-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





