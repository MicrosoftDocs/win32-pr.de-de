---
title: Inapcertrelyingparty-Methode (abonniertbygroup) (napcertrelyingparty. h)
description: Abonniert einen Integritäts Zertifikat Server (HCS).
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- Abonniertbygroup-Methode, NAP
- Abonniertbygroup-Methode NAP, inapcertrelyingparty-Schnittstelle
- Inapcertrelyingparty-Schnittstelle NAP, abonniertbygroup-Methode
topic_type:
- apiref
api_name:
- INapCertRelyingParty.SubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053c3c2dbf00e706003988bd5769cb2aa9201c41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339975"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a><span data-ttu-id="1f9e8-106">Inapcertrelyingparty:: abonbecertbygroup-Methode</span><span class="sxs-lookup"><span data-stu-id="1f9e8-106">INapCertRelyingParty::SubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="1f9e8-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1f9e8-108">Die **abonniertbygroup** -Methode abonniert einen Integritäts Zertifikat Server (HCS).</span><span class="sxs-lookup"><span data-stu-id="1f9e8-108">The **SubscribeCertByGroup** method subscribes to a health certificate server (HCS).</span></span> <span data-ttu-id="1f9e8-109">Die HCS müssen bereits registriert sein, bevor Sie abonniert werden.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-109">The HCS must already be registered before subscribing.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f9e8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f9e8-110">Syntax</span></span>


```C++
HRESULT SubscribeCertByGroup(
  [in]        EnforcementEntityId  id,
  [in]  const BSTR                subscriberName,
  [in]  const  VARIANT            *reserved,
  [out]       BOOL                *certExists
);
```



## <a name="parameters"></a><span data-ttu-id="1f9e8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f9e8-111">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="1f9e8-112">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f9e8-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f9e8-113">Eine [**enforcemententityid**](nap-datatypes.md) , die die ID des abonnierten Erzwingungs Clients enthält.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-113">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is subscribing.</span></span>

</dd> <dt>

<span data-ttu-id="1f9e8-114">*Abonnement Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f9e8-114">*subscriberName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f9e8-115">Der Name des Abonnenten.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-115">The name of the subscriber.</span></span>

> [!Note]  
> <span data-ttu-id="1f9e8-116">Dies wird zurzeit nur für Protokollierungs Zwecke verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-116">This is currently only used for logging purposes.</span></span>

 

</dd> <dt>

<span data-ttu-id="1f9e8-117">*reserviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f9e8-117">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f9e8-118">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-118">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1f9e8-119">*certexists* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1f9e8-119">*certExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f9e8-120">Gibt an, ob ein Integritäts Zertifikat von diesem HCS bereits vom NAPAgent verwaltet wird und im Computerspeicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-120">Indicates whether a health certificate from this HCS is already being maintained by the NapAgent and is present in the machine store.</span></span> <span data-ttu-id="1f9e8-121">**True** gibt an, dass ein Integritäts Zertifikat bereits verwaltet wird und vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-121">If **TRUE**, a health certificate is already being maintained and is present.</span></span> <span data-ttu-id="1f9e8-122">Wenn der Wert **false** ist, wird ein Integritäts Zertifikat zurzeit nicht verwaltet und ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-122">If **FALSE**, a health certificate is not currently being maintained and present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f9e8-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f9e8-123">Return value</span></span>

<span data-ttu-id="1f9e8-124">Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-124">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="1f9e8-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1f9e8-125">Return code</span></span>                                                                                     | <span data-ttu-id="1f9e8-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f9e8-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1f9e8-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f9e8-127"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1f9e8-128">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-128">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="1f9e8-129"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="1f9e8-129"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1f9e8-130">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-130">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1f9e8-131"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="1f9e8-131"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1f9e8-132">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-132">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1f9e8-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f9e8-133">Requirements</span></span>



| <span data-ttu-id="1f9e8-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f9e8-134">Requirement</span></span> | <span data-ttu-id="1f9e8-135">Wert</span><span class="sxs-lookup"><span data-stu-id="1f9e8-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f9e8-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f9e8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1f9e8-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f9e8-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1f9e8-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f9e8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1f9e8-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f9e8-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1f9e8-140">Header</span><span class="sxs-lookup"><span data-stu-id="1f9e8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f9e8-141"><dt>Napcertrelyingparty. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f9e8-141"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f9e8-142">IDL</span><span class="sxs-lookup"><span data-stu-id="1f9e8-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1f9e8-143"><dt>Napcertrelyingparty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1f9e8-143"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f9e8-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f9e8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f9e8-145">**Inapcertrelyingparty**</span><span class="sxs-lookup"><span data-stu-id="1f9e8-145">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





