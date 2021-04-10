---
title: Inapenforcementclientconnection-Methode von "stenforcerprivatedata" (napforcementclient. h)
description: Wird vom-Enforcer verwendet, um private Daten festzulegen.
ms.assetid: 56f6fec7-47ec-4b2c-b8c8-a4d519ba0f91
keywords:
- Methode "stenforcerprivatedata" NAP
- Setup für die Methode "stenforcerprivatedata", "inapenforcementclientconnection"
- Inapenforcementclientconnection-Schnittstelle NAP, die Methode "Setup-forcerprivatedata"
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5773294e229a59ff07db8ef546d9d691b369b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040402"
---
# <a name="inapenforcementclientconnectionsetenforcerprivatedata-method"></a><span data-ttu-id="19de3-106">Inapenforcementclientconnection:: Setup Data-Methode</span><span class="sxs-lookup"><span data-stu-id="19de3-106">INapEnforcementClientConnection::SetEnforcerPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="19de3-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19de3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="19de3-108">Die **inapenforcementclientconnection:: setenforcerprivatedata** -Methode wird vom-Enforcer verwendet, um private Daten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="19de3-108">The **INapEnforcementClientConnection::SetEnforcerPrivateData** method is used by the enforcer to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="19de3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="19de3-109">Syntax</span></span>


```C++
HRESULT SetEnforcerPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="19de3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="19de3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19de3-111">*PRIVATEDATA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19de3-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19de3-112">Ein Zeiger auf ein nicht transparentes datenblob vom Typ " [**PRIVATEDATA**](/windows/win32/api/naptypes/ns-naptypes-privatedata) ", das nur vom Enforcer interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="19de3-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the enforcer can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19de3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19de3-113">Return value</span></span>

<span data-ttu-id="19de3-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="19de3-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="19de3-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="19de3-115">Return code</span></span>                                                                                     | <span data-ttu-id="19de3-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19de3-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="19de3-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="19de3-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="19de3-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="19de3-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="19de3-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="19de3-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="19de3-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="19de3-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="19de3-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="19de3-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="19de3-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="19de3-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="19de3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19de3-123">Requirements</span></span>



| <span data-ttu-id="19de3-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19de3-124">Requirement</span></span> | <span data-ttu-id="19de3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="19de3-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19de3-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19de3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="19de3-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19de3-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="19de3-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19de3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="19de3-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19de3-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="19de3-130">Header</span><span class="sxs-lookup"><span data-stu-id="19de3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="19de3-131"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="19de3-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="19de3-132">IDL</span><span class="sxs-lookup"><span data-stu-id="19de3-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19de3-133"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="19de3-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="19de3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="19de3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19de3-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19de3-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="19de3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19de3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19de3-137">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="19de3-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





