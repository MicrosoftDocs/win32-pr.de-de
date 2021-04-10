---
title: Inapenforcementclientconnection getenforcerprivatedata-Methode (napforcementclient. h)
description: Wird vom-Enforcer verwendet, um private Daten zu erhalten.
ms.assetid: a1f5b5a7-c862-4e5b-bf9c-b137f99f6165
keywords:
- Getenforcerprivatedata-Methode NAP
- Getenforcerprivatedata-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, getenforcerprivatedata-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592ad0b11abf2b349b0810d67b05f2ee4086060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106419"
---
# <a name="inapenforcementclientconnectiongetenforcerprivatedata-method"></a><span data-ttu-id="a7ff9-106">Inapenforcementclientconnection:: getenforcerprivatedata-Methode</span><span class="sxs-lookup"><span data-stu-id="a7ff9-106">INapEnforcementClientConnection::GetEnforcerPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="a7ff9-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a7ff9-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a7ff9-108">Die **inapenforcementclientconnection:: getenforcerprivatedata** -Methode wird vom-Enforcer verwendet, um private Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a7ff9-108">The **INapEnforcementClientConnection::GetEnforcerPrivateData** method is used by the enforcer to get private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7ff9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7ff9-109">Syntax</span></span>


```C++
HRESULT GetEnforcerPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="a7ff9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7ff9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7ff9-111">*PRIVATEDATA* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a7ff9-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7ff9-112">Ein Zeiger [**auf einen Zeiger auf ein nicht**](/windows/win32/api/naptypes/ns-naptypes-privatedata) transparentes datenblob, das nur vom-Enforcer interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7ff9-112">A pointer to a pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the enforcer can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7ff9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7ff9-113">Return value</span></span>

<span data-ttu-id="a7ff9-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a7ff9-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a7ff9-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a7ff9-115">Return code</span></span>                                                                                     | <span data-ttu-id="a7ff9-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7ff9-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7ff9-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a7ff9-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a7ff9-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a7ff9-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a7ff9-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="a7ff9-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a7ff9-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="a7ff9-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a7ff9-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a7ff9-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a7ff9-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a7ff9-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a7ff9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7ff9-123">Requirements</span></span>



| <span data-ttu-id="a7ff9-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7ff9-124">Requirement</span></span> | <span data-ttu-id="a7ff9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a7ff9-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ff9-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7ff9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a7ff9-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7ff9-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a7ff9-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7ff9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a7ff9-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7ff9-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a7ff9-130">Header</span><span class="sxs-lookup"><span data-stu-id="a7ff9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7ff9-131"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7ff9-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7ff9-132">IDL</span><span class="sxs-lookup"><span data-stu-id="a7ff9-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7ff9-133"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7ff9-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="a7ff9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a7ff9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7ff9-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7ff9-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a7ff9-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7ff9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ff9-137">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="a7ff9-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





