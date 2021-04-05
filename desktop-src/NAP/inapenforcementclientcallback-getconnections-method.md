---
title: Inapenforcementclientcallback GetConnections-Methode (napforcementclient. h)
description: Wird von NAPAgent aufgerufen und vom Erzwingungs Client implementiert, um einen Satz von Verbindungen zurückzugeben.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- GetConnections-Methode NAP
- GetConnections-Methode NAP, inapenforcementclientcallback-Schnittstelle
- Inapenforcementclientcallback-Schnittstelle NAP, GetConnections-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.GetConnections
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acdc68dbc69cabe710414f3fa2501585f3e384e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859285"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a><span data-ttu-id="de893-106">Inapenforcementclientcallback:: GetConnections-Methode</span><span class="sxs-lookup"><span data-stu-id="de893-106">INapEnforcementClientCallback::GetConnections method</span></span>

> [!Note]  
> <span data-ttu-id="de893-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="de893-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="de893-108">Die **inapenforcementclientcallback:: GetConnections** -Rückruf Methode wird von NAPAgent aufgerufen und vom Erzwingungs Client implementiert, um einen Satz von Verbindungen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="de893-108">The **INapEnforcementClientCallback::GetConnections** callback method is called by the NapAgent and implemented by the enforcement client to return a set of connections.</span></span>

## <a name="syntax"></a><span data-ttu-id="de893-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="de893-109">Syntax</span></span>


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a><span data-ttu-id="de893-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="de893-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de893-111">*Verbindungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="de893-111">*connections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de893-112">Ein Zeiger auf den aktuellen Satz von verwalteten [**Verbindungen**](connections-struct.md).</span><span class="sxs-lookup"><span data-stu-id="de893-112">A pointer to the current set of maintained [**Connections**](connections-struct.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de893-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de893-113">Return value</span></span>

<span data-ttu-id="de893-114">Diese Rückruf Methode muss einen der folgenden Fehlercodes zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="de893-114">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="de893-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="de893-115">Return code</span></span>                                                                                                | <span data-ttu-id="de893-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de893-116">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="de893-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="de893-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="de893-118">Gibt diesen Wert zurück, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="de893-118">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="de893-119"><dt>**RPC \_ S- \_ Server nicht \_ verfügbar**</dt></span><span class="sxs-lookup"><span data-stu-id="de893-119"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="de893-120">Durch das zurückgeben dieses Werts wird der Enforcer aus der gebundenen SHA-Liste entfernt, und der entsprechende NAPAgent-Cache Eintrag, der geleert werden soll.</span><span class="sxs-lookup"><span data-stu-id="de893-120">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="de893-121">Der fehlerhafte SHA kann dann mit dem NAPAgent erneut initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="de893-121">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="de893-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de893-122">Requirements</span></span>



| <span data-ttu-id="de893-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de893-123">Requirement</span></span> | <span data-ttu-id="de893-124">Wert</span><span class="sxs-lookup"><span data-stu-id="de893-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de893-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de893-125">Minimum supported client</span></span><br/> | <span data-ttu-id="de893-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de893-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="de893-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de893-127">Minimum supported server</span></span><br/> | <span data-ttu-id="de893-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de893-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="de893-129">Header</span><span class="sxs-lookup"><span data-stu-id="de893-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="de893-130"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="de893-130"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="de893-131">IDL</span><span class="sxs-lookup"><span data-stu-id="de893-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="de893-132"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="de893-132"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de893-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de893-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de893-134">**Inapenforcementclientcallback**</span><span class="sxs-lookup"><span data-stu-id="de893-134">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





