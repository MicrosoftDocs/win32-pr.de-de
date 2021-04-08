---
title: Inapsystemhealthagentcallback notifysystemisolationstatechange-Methode (napsystemhealthagent. h)
description: Wird von NAPAgent aufgerufen, um anzugeben, dass sich der System Isolations Status oder die Endzeit der Bewährungszeit geändert hat.
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- Notifysystemisolationstatechange-Methode NAP
- Notifysystemisolationstatechange-Methode NAP, inapsystemhealthagentcallback-Schnittstelle
- Inapsystemhealthagentcallback-Schnittstelle NAP, notifysystemsolationstatechange-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifySystemIsolationStateChange
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c519d1569fe2e43cc6012ffa30c5bfb4402cc56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741953"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a><span data-ttu-id="6ebf6-106">Inapsystemhealthagentcallback:: notifysystemsolationstatechange-Methode</span><span class="sxs-lookup"><span data-stu-id="6ebf6-106">INapSystemHealthAgentCallback::NotifySystemIsolationStateChange method</span></span>

> [!Note]  
> <span data-ttu-id="6ebf6-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6ebf6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6ebf6-108">Die **inapsystemhealthagentcallback:: notifysystemsolationstatechange** -Methode wird von NAPAgent aufgerufen, um anzugeben, dass sich der System Isolations Status oder die Endzeit der Bewährungszeit geändert hat.</span><span class="sxs-lookup"><span data-stu-id="6ebf6-108">The **INapSystemHealthAgentCallback::NotifySystemIsolationStateChange** method is called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ebf6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ebf6-109">Syntax</span></span>


```C++
HRESULT NotifySystemIsolationStateChange();
```



## <a name="parameters"></a><span data-ttu-id="6ebf6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ebf6-110">Parameters</span></span>

<span data-ttu-id="6ebf6-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6ebf6-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ebf6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ebf6-112">Return value</span></span>

<span data-ttu-id="6ebf6-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6ebf6-113">This method can return one of these values.</span></span>



| <span data-ttu-id="6ebf6-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6ebf6-114">Return code</span></span>                                                                          | <span data-ttu-id="6ebf6-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ebf6-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="6ebf6-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6ebf6-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6ebf6-117">Gibt die erfolgreiche Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="6ebf6-117">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6ebf6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ebf6-118">Remarks</span></span>

<span data-ttu-id="6ebf6-119">Diese Rückruf Methode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="6ebf6-119">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="6ebf6-120">Der Integritäts-Agent kann den NAP-Systemstatus mithilfe von [**inapsystemhealthagentbinding:: getsystemsolationinfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md)Abfragen.</span><span class="sxs-lookup"><span data-stu-id="6ebf6-120">The health agent can query the system NAP state using the [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ebf6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ebf6-121">Requirements</span></span>



| <span data-ttu-id="6ebf6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ebf6-122">Requirement</span></span> | <span data-ttu-id="6ebf6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6ebf6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ebf6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ebf6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6ebf6-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ebf6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6ebf6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ebf6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6ebf6-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ebf6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6ebf6-128">Header</span><span class="sxs-lookup"><span data-stu-id="6ebf6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ebf6-129"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ebf6-129"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ebf6-130">IDL</span><span class="sxs-lookup"><span data-stu-id="6ebf6-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ebf6-131"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ebf6-131"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ebf6-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ebf6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ebf6-133">**Inapsystemhealthagentcallback**</span><span class="sxs-lookup"><span data-stu-id="6ebf6-133">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





