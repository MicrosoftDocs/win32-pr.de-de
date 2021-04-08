---
title: Inapenforcementclientconnection-Methode der Setup Methode (natzforcementclient. h)
description: Wird von NAPAgent verwendet, um die Isolations Informationen des Clients festzulegen.
ms.assetid: e92d8762-4ae9-40e5-a18e-7da757aa6f9e
keywords:
- Methode der Methode "stisolationinfo"
- Methode der Setup-Info-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, die Methode "Setup solationinfo"
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1cfd7ad227fec6942e0660769f52b3d4f12201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740928"
---
# <a name="inapenforcementclientconnectionsetisolationinfo-method"></a><span data-ttu-id="e3064-106">Inapenforcementclientconnection:: Setup solationinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="e3064-106">INapEnforcementClientConnection::SetIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="e3064-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e3064-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e3064-108">Die **inapenforcementclientconnection:: setisolationinfo** -Methode wird vom NAPAgent verwendet, um die Isolations Informationen des Clients festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e3064-108">The **INapEnforcementClientConnection::SetIsolationInfo** method is used by the NapAgent to set the isolation information of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3064-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3064-109">Syntax</span></span>


```C++
HRESULT SetIsolationInfo(
  [in] const IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e3064-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3064-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3064-111">*IsolationInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3064-111">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3064-112">Ein Zeiger auf eine [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) -Struktur, die den konnektivitätszustand des Clients enthält.</span><span class="sxs-lookup"><span data-stu-id="e3064-112">A pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3064-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3064-113">Return value</span></span>

<span data-ttu-id="e3064-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e3064-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e3064-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e3064-115">Return code</span></span>                                                                                     | <span data-ttu-id="e3064-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3064-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e3064-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e3064-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="e3064-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e3064-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e3064-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="e3064-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="e3064-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="e3064-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e3064-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="e3064-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="e3064-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e3064-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3064-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3064-123">Remarks</span></span>

<span data-ttu-id="e3064-124">Diese Informationen werden von NAPAgent nach der Verarbeitung von sohresponse festgelegt und dürfen nicht vom-Enforcer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e3064-124">This information is set by NapAgent after processing an SoHResponse and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3064-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3064-125">Requirements</span></span>



| <span data-ttu-id="e3064-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3064-126">Requirement</span></span> | <span data-ttu-id="e3064-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e3064-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3064-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3064-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e3064-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3064-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e3064-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3064-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e3064-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3064-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e3064-132">Header</span><span class="sxs-lookup"><span data-stu-id="e3064-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3064-133"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3064-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3064-134">IDL</span><span class="sxs-lookup"><span data-stu-id="e3064-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e3064-135"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3064-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="e3064-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e3064-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3064-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3064-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e3064-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3064-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3064-139">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="e3064-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





