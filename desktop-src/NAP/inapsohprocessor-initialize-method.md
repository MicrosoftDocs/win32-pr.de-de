---
title: Inapsohprocessor Initialize-Methode (napprotocol. h)
description: Initialisiert das Protokoll Paket und das SoH-Prozessor System. Diese Methode muss genau einmal aufgerufen werden.
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Methode "NAP initialisieren"
- Initialize-Methode, NAP, inapsohprocessor-Schnittstelle
- Inapsohprocessor-Schnittstelle NAP, Initialize-Methode
topic_type:
- apiref
api_name:
- INapSoHProcessor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956468"
---
# <a name="inapsohprocessorinitialize-method"></a><span data-ttu-id="71da8-107">Inapsohprocessor:: Initialize-Methode</span><span class="sxs-lookup"><span data-stu-id="71da8-107">INapSoHProcessor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="71da8-108">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="71da8-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="71da8-109">Mit der **inapsohprocessor:: Initialize** -Methode werden das Protokoll Paket und das SoH-Prozessor System initialisiert.</span><span class="sxs-lookup"><span data-stu-id="71da8-109">The **INapSoHProcessor::Initialize** method initializes the protocol packet and SoH processor system.</span></span> <span data-ttu-id="71da8-110">Diese Methode muss genau einmal aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="71da8-110">This method must be called exactly once.</span></span>

## <a name="syntax"></a><span data-ttu-id="71da8-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="71da8-111">Syntax</span></span>


```C++
HRESULT Initialize(
  [in]  const SoH                  *soh,
  [in]        BOOL                 isRequest,
  [out]       SystemHealthEntityId *id
);
```



## <a name="parameters"></a><span data-ttu-id="71da8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="71da8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71da8-113">*SoH* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71da8-113">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71da8-114">Ein Zeiger auf das zu verarbeitende [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket.</span><span class="sxs-lookup"><span data-stu-id="71da8-114">A pointer to the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="71da8-115">*isrequest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71da8-115">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71da8-116">Ein **boolescher** Wert, der **true** ist, wenn das Paket ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) und **false** ist, wenn es sich um eine **sohresponse** handelt.</span><span class="sxs-lookup"><span data-stu-id="71da8-116">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> <dt>

<span data-ttu-id="71da8-117">*ID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="71da8-117">*id* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71da8-118">Eine eindeutige [systemhealthentityid](nap-datatypes.md) , die die ID des SHA oder SHV enthält, der das Paket erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="71da8-118">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that constructed the packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71da8-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71da8-119">Return value</span></span>

<span data-ttu-id="71da8-120">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="71da8-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="71da8-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="71da8-121">Return code</span></span>                                                                                            | <span data-ttu-id="71da8-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71da8-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="71da8-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71da8-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="71da8-124">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="71da8-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="71da8-125"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="71da8-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="71da8-126">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="71da8-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="71da8-127"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="71da8-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="71da8-128">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="71da8-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="71da8-129"><dt>**\_ \_ Ungültiges NAP- \_ Paket**</dt></span><span class="sxs-lookup"><span data-stu-id="71da8-129"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="71da8-130">Das SoH-Paket ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="71da8-130">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="71da8-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71da8-131">Requirements</span></span>



| <span data-ttu-id="71da8-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71da8-132">Requirement</span></span> | <span data-ttu-id="71da8-133">Wert</span><span class="sxs-lookup"><span data-stu-id="71da8-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="71da8-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71da8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="71da8-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71da8-135">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="71da8-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71da8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="71da8-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71da8-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="71da8-138">Header</span><span class="sxs-lookup"><span data-stu-id="71da8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="71da8-139"><dt>Napprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="71da8-139"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="71da8-140">IDL</span><span class="sxs-lookup"><span data-stu-id="71da8-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71da8-141"><dt>Napprotocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71da8-141"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="71da8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="71da8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71da8-143"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71da8-143"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="71da8-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71da8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71da8-145">**Inapsohprocessor**</span><span class="sxs-lookup"><span data-stu-id="71da8-145">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





