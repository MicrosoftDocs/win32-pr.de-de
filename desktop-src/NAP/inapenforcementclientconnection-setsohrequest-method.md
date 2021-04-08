---
title: Inapenforcementclientconnection setsohrequest-Methode (napforcementclient. h)
description: Legt die SoH-Anforderung fest.
ms.assetid: 87dbb982-a337-4644-a2fe-970bfdd6c140
keywords:
- Setsohrequest-Methode NAP
- Setsohrequest-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, setsohrequest-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92559d532e99bfa29d7f62fd29b279db20f2c0a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740912"
---
# <a name="inapenforcementclientconnectionsetsohrequest-method"></a><span data-ttu-id="a802b-106">Inapenforcementclientconnection:: setsohrequest-Methode</span><span class="sxs-lookup"><span data-stu-id="a802b-106">INapEnforcementClientConnection::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="a802b-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a802b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a802b-108">Die **inapenforcementclientconnection:: setsohrequest** -Methode legt die SoH-Anforderung fest.</span><span class="sxs-lookup"><span data-stu-id="a802b-108">The **INapEnforcementClientConnection::SetSoHRequest** method sets the SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a802b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a802b-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in, unique] const NetworkSoHRequest *sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="a802b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a802b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a802b-111">*sohrequest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a802b-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a802b-112">Ein Zeiger auf eine eindeutige [**networksohrequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) -Struktur, bei der es sich um ein undurchsichtiges Daten-BLOB für den-Enforcer handelt.</span><span class="sxs-lookup"><span data-stu-id="a802b-112">A pointer to a unique [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a802b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a802b-113">Return value</span></span>

<span data-ttu-id="a802b-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a802b-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a802b-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a802b-115">Return code</span></span>                                                                                     | <span data-ttu-id="a802b-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a802b-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a802b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a802b-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a802b-118">Das SoH-Paket ist gültig.</span><span class="sxs-lookup"><span data-stu-id="a802b-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="a802b-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="a802b-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a802b-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="a802b-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a802b-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a802b-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a802b-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a802b-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a802b-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a802b-123">Remarks</span></span>

<span data-ttu-id="a802b-124">Dies wird von NAPAgent festgelegt und von enforcern abgefragt, um die Übertragung zu senden.</span><span class="sxs-lookup"><span data-stu-id="a802b-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="a802b-125">Ein SoH-Paket mit einer Länge von 0 Bytes ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a802b-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="a802b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a802b-126">Requirements</span></span>



| <span data-ttu-id="a802b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a802b-127">Requirement</span></span> | <span data-ttu-id="a802b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a802b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a802b-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a802b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a802b-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a802b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a802b-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a802b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a802b-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a802b-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a802b-133">Header</span><span class="sxs-lookup"><span data-stu-id="a802b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a802b-134"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a802b-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a802b-135">IDL</span><span class="sxs-lookup"><span data-stu-id="a802b-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a802b-136"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a802b-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="a802b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a802b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a802b-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a802b-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a802b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a802b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a802b-140">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="a802b-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





