---
title: Inapenforcementclientconnection setprivatedata-Methode (napforcementclient. h)
description: Wird von NAPAgent verwendet, um private Daten festzulegen.
ms.assetid: 2559a612-8857-4e60-b5bc-dd8235ff69f9
keywords:
- Setprivatedata-Methode NAP
- Setprivatedata-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, setprivatedata-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e73248e546b1f0e48438553877f0523bd30b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040400"
---
# <a name="inapenforcementclientconnectionsetprivatedata-method"></a><span data-ttu-id="ca069-106">Inapenforcementclientconnection:: setprivatedata-Methode</span><span class="sxs-lookup"><span data-stu-id="ca069-106">INapEnforcementClientConnection::SetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="ca069-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ca069-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ca069-108">Die **inapenforcementclientconnection:: setprivatedata** -Methode wird vom NAPAgent verwendet, um private Daten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ca069-108">The **INapEnforcementClientConnection::SetPrivateData** method is used by the NapAgent to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca069-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca069-109">Syntax</span></span>


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="ca069-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca069-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca069-111">*PRIVATEDATA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca069-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca069-112">Ein Zeiger auf ein [**PRIVATEDATA**](/windows/win32/api/naptypes/ns-naptypes-privatedata) -datenblob, das nur von NAPAgent interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ca069-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data blob that only the NapAgent can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca069-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca069-113">Return value</span></span>

<span data-ttu-id="ca069-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ca069-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ca069-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ca069-115">Return code</span></span>                                                                                     | <span data-ttu-id="ca069-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca069-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca069-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca069-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="ca069-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ca069-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ca069-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="ca069-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="ca069-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="ca069-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ca069-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ca069-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="ca069-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ca069-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ca069-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca069-123">Requirements</span></span>



| <span data-ttu-id="ca069-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca069-124">Requirement</span></span> | <span data-ttu-id="ca069-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ca069-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca069-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca069-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ca069-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca069-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ca069-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca069-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ca069-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca069-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ca069-130">Header</span><span class="sxs-lookup"><span data-stu-id="ca069-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca069-131"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca069-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca069-132">IDL</span><span class="sxs-lookup"><span data-stu-id="ca069-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ca069-133"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca069-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="ca069-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ca069-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca069-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca069-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="ca069-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca069-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca069-137">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="ca069-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





