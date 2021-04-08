---
title: Inapenforcementclientconnection getisolationinfo-Methode (natzforcementclient. h)
description: Wird verwendet, um die Isolations Informationen des Clients zu erhalten.
ms.assetid: 33040554-dcbe-4563-b047-fc7e28bac55c
keywords:
- Getisolationinfo-Methode NAP
- Getisolationinfo-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, getisolationinfo-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890f7268801fda77a9794ed21c4d36e78a52dd5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957210"
---
# <a name="inapenforcementclientconnectiongetisolationinfo-method"></a><span data-ttu-id="0d705-106">Inapenforcementclientconnection:: getisolationinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="0d705-106">INapEnforcementClientConnection::GetIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="0d705-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d705-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0d705-108">Die **inapenforcementclientconnection:: getisolationinfo** -Methode wird verwendet, um die Isolations Informationen des Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0d705-108">The **INapEnforcementClientConnection::GetIsolationInfo** method is used get the isolation information of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d705-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d705-109">Syntax</span></span>


```C++
HRESULT GetIsolationInfo(
  [out] IsolationInfo **isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="0d705-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d705-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d705-111">*IsolationInfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0d705-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d705-112">Ein Zeiger auf einen Zeiger auf eine [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) -Struktur, die den konnektivitätszustand des Clients enthält.</span><span class="sxs-lookup"><span data-stu-id="0d705-112">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d705-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d705-113">Return value</span></span>

<span data-ttu-id="0d705-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0d705-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0d705-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0d705-115">Return code</span></span>                                                                                     | <span data-ttu-id="0d705-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d705-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d705-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0d705-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0d705-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0d705-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0d705-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="0d705-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0d705-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="0d705-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0d705-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="0d705-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0d705-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0d705-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d705-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d705-123">Remarks</span></span>

<span data-ttu-id="0d705-124">Diese Informationen werden von NAPAgent nach der Verarbeitung von [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) festgelegt und dürfen nicht vom-Enforcer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0d705-124">This information is set by the NapAgent after processing a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d705-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d705-125">Requirements</span></span>



| <span data-ttu-id="0d705-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d705-126">Requirement</span></span> | <span data-ttu-id="0d705-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0d705-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d705-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d705-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0d705-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d705-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0d705-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d705-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0d705-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d705-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0d705-132">Header</span><span class="sxs-lookup"><span data-stu-id="0d705-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d705-133"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d705-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d705-134">IDL</span><span class="sxs-lookup"><span data-stu-id="0d705-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d705-135"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d705-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="0d705-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0d705-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d705-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d705-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="0d705-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d705-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d705-139">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="0d705-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





