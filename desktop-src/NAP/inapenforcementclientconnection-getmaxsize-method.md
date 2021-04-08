---
title: Inapenforcementclientconnection getmaxsize-Methode (napforcementclient. h)
description: Ruft die maximale Größe des SoH-Pakets für diesen Client ab.
ms.assetid: 054bc783-db5d-4801-8984-6b8a131744a2
keywords:
- Getmaxsize-Methode NAP
- Getmaxsize-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, getmaxsize-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3d86cc71cd5da906146ab1577d58311d167d484
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740936"
---
# <a name="inapenforcementclientconnectiongetmaxsize-method"></a><span data-ttu-id="f9341-106">Inapenforcementclientconnection:: getmaxsize-Methode</span><span class="sxs-lookup"><span data-stu-id="f9341-106">INapEnforcementClientConnection::GetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="f9341-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f9341-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f9341-108">Die **inapenforcementclientconnection:: getmaxsize** -Methode ruft die maximale Größe des SoH-Pakets für diesen Client ab.</span><span class="sxs-lookup"><span data-stu-id="f9341-108">The **INapEnforcementClientConnection::GetMaxSize** method gets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9341-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9341-109">Syntax</span></span>


```C++
HRESULT GetMaxSize(
  [out] ProtocolMaxSize *maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="f9341-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9341-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9341-111">*MaxSize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f9341-111">*maxSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9341-112">Ein Zeiger auf einen [**protocolmaxsize**](nap-datatypes.md) -Wert, der die maximale Größe (in Bytes) des SoH-Pakets angibt.</span><span class="sxs-lookup"><span data-stu-id="f9341-112">A pointer to a [**ProtocolMaxSize**](nap-datatypes.md) that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9341-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9341-113">Return value</span></span>

<span data-ttu-id="f9341-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f9341-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f9341-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f9341-115">Return code</span></span>                                                                                     | <span data-ttu-id="f9341-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9341-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9341-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9341-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f9341-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f9341-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f9341-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="f9341-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f9341-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="f9341-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f9341-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f9341-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f9341-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f9341-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f9341-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9341-123">Requirements</span></span>



| <span data-ttu-id="f9341-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9341-124">Requirement</span></span> | <span data-ttu-id="f9341-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f9341-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9341-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9341-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f9341-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9341-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f9341-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9341-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f9341-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9341-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f9341-130">Header</span><span class="sxs-lookup"><span data-stu-id="f9341-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9341-131"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9341-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9341-132">IDL</span><span class="sxs-lookup"><span data-stu-id="f9341-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9341-133"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9341-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="f9341-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f9341-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9341-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9341-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f9341-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9341-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9341-137">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="f9341-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





