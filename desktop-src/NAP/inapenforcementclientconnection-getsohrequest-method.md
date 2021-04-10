---
title: Inapenforcementclientconnection getsohrequest-Methode (napforcementclient. h)
description: Ruft die aktuelle SoH-Anforderung ab.
ms.assetid: 21397a0d-ef18-494e-9c5a-43d7f6216a67
keywords:
- Getsohrequest-Methode NAP
- Getsohrequest-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, getsohrequest-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6115e607f810aef67911ec7d7800d35207368e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949666"
---
# <a name="inapenforcementclientconnectiongetsohrequest-method"></a><span data-ttu-id="de88a-106">Inapenforcementclientconnection:: getsohrequest-Methode</span><span class="sxs-lookup"><span data-stu-id="de88a-106">INapEnforcementClientConnection::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="de88a-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="de88a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="de88a-108">Die **inapenforcementclientconnection:: getsohrequest** -Methode ruft die aktuelle SoH-Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="de88a-108">The **INapEnforcementClientConnection::GetSoHRequest** method gets the current SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="de88a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="de88a-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] NetworkSoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="de88a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="de88a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de88a-111">*sohrequest* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="de88a-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de88a-112">Ein Zeiger auf einen Zeiger auf eine [**networksohrequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) -Struktur, bei der es sich um ein nicht transparentes Daten-BLOB für den-Enforcer handelt.</span><span class="sxs-lookup"><span data-stu-id="de88a-112">A pointer to a pointer to a [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de88a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de88a-113">Return value</span></span>

<span data-ttu-id="de88a-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="de88a-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="de88a-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="de88a-115">Return code</span></span>                                                                                     | <span data-ttu-id="de88a-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de88a-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="de88a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="de88a-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="de88a-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="de88a-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="de88a-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="de88a-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="de88a-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="de88a-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="de88a-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="de88a-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="de88a-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="de88a-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de88a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de88a-123">Remarks</span></span>

<span data-ttu-id="de88a-124">Dies wird von NAPAgent festgelegt und von enforcern abgefragt, um die Übertragung zu senden.</span><span class="sxs-lookup"><span data-stu-id="de88a-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="de88a-125">Ein SoH-Paket mit einer Länge von 0 Bytes ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="de88a-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="de88a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de88a-126">Requirements</span></span>



| <span data-ttu-id="de88a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de88a-127">Requirement</span></span> | <span data-ttu-id="de88a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="de88a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de88a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de88a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="de88a-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de88a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="de88a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de88a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="de88a-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de88a-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="de88a-133">Header</span><span class="sxs-lookup"><span data-stu-id="de88a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="de88a-134"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="de88a-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="de88a-135">IDL</span><span class="sxs-lookup"><span data-stu-id="de88a-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="de88a-136"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="de88a-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="de88a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="de88a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de88a-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de88a-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="de88a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de88a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de88a-140">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="de88a-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





