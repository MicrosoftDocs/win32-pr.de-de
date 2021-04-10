---
title: Inapenforcementclientconnection getsohresponse-Methode (napforcementclient. h)
description: Ruft den SoH-Response ab, der vom Erzwingungs Client empfangen wurde.
ms.assetid: fc0084a3-a668-435e-8390-f322941c5cd4
keywords:
- Getsohresponse-Methode NAP
- Getsohresponse-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, getsohresponse-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67be4d65135d6e4ce606a83eb08fdeed036cc62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858772"
---
# <a name="inapenforcementclientconnectiongetsohresponse-method"></a><span data-ttu-id="f5d5d-106">Inapenforcementclientconnection:: getsohresponse-Methode</span><span class="sxs-lookup"><span data-stu-id="f5d5d-106">INapEnforcementClientConnection::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="f5d5d-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f5d5d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f5d5d-108">Die **inapenforcementclientconnection:: getsohresponse** -Methode ruft die vom Erzwingungs Client empfangenen SoH-Response ab.</span><span class="sxs-lookup"><span data-stu-id="f5d5d-108">The **INapEnforcementClientConnection::GetSoHResponse** method gets the SoH-Response received by the enforcement client.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d5d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5d5d-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] NetworkSoHResponse **sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="f5d5d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5d5d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5d5d-111">*sohresponse* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f5d5d-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d5d-112">Ein Zeiger auf einen Zeiger auf eine eindeutige [**networksohresponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) -Struktur, bei der es sich um ein undurchsichtiges Daten-BLOB für den-Enforcer handelt.</span><span class="sxs-lookup"><span data-stu-id="f5d5d-112">A pointer to a pointer to a unique [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5d5d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5d5d-113">Return value</span></span>

<span data-ttu-id="f5d5d-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f5d5d-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f5d5d-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f5d5d-115">Return code</span></span>                                                                                     | <span data-ttu-id="f5d5d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5d5d-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5d5d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f5d5d-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f5d5d-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f5d5d-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f5d5d-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="f5d5d-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f5d5d-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="f5d5d-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f5d5d-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f5d5d-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f5d5d-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f5d5d-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f5d5d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5d5d-123">Remarks</span></span>

<span data-ttu-id="f5d5d-124">Ein Paket mit einer Größe von 0 Byte ist gültig.</span><span class="sxs-lookup"><span data-stu-id="f5d5d-124">A zero-byte sized packet is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5d5d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5d5d-125">Requirements</span></span>



| <span data-ttu-id="f5d5d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5d5d-126">Requirement</span></span> | <span data-ttu-id="f5d5d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f5d5d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d5d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5d5d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d5d-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5d5d-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f5d5d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5d5d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d5d-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5d5d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f5d5d-132">Header</span><span class="sxs-lookup"><span data-stu-id="f5d5d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5d5d-133"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5d5d-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5d5d-134">IDL</span><span class="sxs-lookup"><span data-stu-id="f5d5d-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f5d5d-135"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f5d5d-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="f5d5d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f5d5d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5d5d-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5d5d-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f5d5d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5d5d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d5d-139">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="f5d5d-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





