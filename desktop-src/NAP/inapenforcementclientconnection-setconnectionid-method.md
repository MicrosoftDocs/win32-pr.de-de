---
title: Inapenforcementclientconnection setconnectionid-Methode (napforcementclient. h)
description: Wird zum Festlegen der eindeutigen ID der Verbindung verwendet und muss durch den Erzwingungs Client festgelegt werden, sobald die Verbindung erstellt wird.
ms.assetid: 69d1a891-bc86-4c8a-b614-ebcdaa4a9057
keywords:
- Setconnectionid-Methode NAP
- Setconnectionid-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, setconnectionid-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9749be304170ec7706b637429f577e77411ac5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949665"
---
# <a name="inapenforcementclientconnectionsetconnectionid-method"></a><span data-ttu-id="19661-106">Inapenforcementclientconnection:: setconnectionid-Methode</span><span class="sxs-lookup"><span data-stu-id="19661-106">INapEnforcementClientConnection::SetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="19661-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19661-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="19661-108">Die **inapenforcementclientconnection:: setconnectionid** -Methode wird zum Festlegen der eindeutigen ID der Verbindung verwendet und muss durch den Erzwingungs Client festgelegt werden, sobald die Verbindung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="19661-108">The **INapEnforcementClientConnection::SetConnectionId** method is used to set the unique ID of the connection and must be set by the enforcement client as soon as the connection is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="19661-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="19661-109">Syntax</span></span>


```C++
HRESULT SetConnectionId(
  [in] const ConnectionId *connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="19661-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="19661-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19661-111">*ConnectionID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19661-111">*connectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19661-112">Ein Zeiger auf eine [**ConnectionID**](nap-datatypes.md) , die eine Verbindung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="19661-112">A pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19661-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19661-113">Return value</span></span>

<span data-ttu-id="19661-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="19661-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="19661-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="19661-115">Return code</span></span>                                                                                     | <span data-ttu-id="19661-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19661-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="19661-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="19661-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="19661-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="19661-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="19661-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="19661-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="19661-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="19661-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="19661-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="19661-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="19661-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="19661-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="19661-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19661-123">Remarks</span></span>

<span data-ttu-id="19661-124">Diese ConnectionID wird hauptsächlich zu Protokollierungs Zwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="19661-124">This ConnectionID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="19661-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19661-125">Requirements</span></span>



| <span data-ttu-id="19661-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19661-126">Requirement</span></span> | <span data-ttu-id="19661-127">Wert</span><span class="sxs-lookup"><span data-stu-id="19661-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19661-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19661-128">Minimum supported client</span></span><br/> | <span data-ttu-id="19661-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19661-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="19661-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19661-130">Minimum supported server</span></span><br/> | <span data-ttu-id="19661-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19661-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="19661-132">Header</span><span class="sxs-lookup"><span data-stu-id="19661-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="19661-133"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="19661-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="19661-134">IDL</span><span class="sxs-lookup"><span data-stu-id="19661-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19661-135"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="19661-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="19661-136">DLL</span><span class="sxs-lookup"><span data-stu-id="19661-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19661-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19661-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="19661-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19661-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19661-139">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="19661-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





