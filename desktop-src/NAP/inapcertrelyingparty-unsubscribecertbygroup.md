---
title: Inapcertrelyingparty unabonniert bygroup-Methode (napcertrelyingparty. h)
description: Abonniert einen Integritäts Zertifikat Server (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- Unabonniertbygroup-Methode NAP
- Unabonnebecertbygroup-Methode NAP, inapcertrelyingparty-Schnittstelle
- Inapcertrelyingparty Interface NAP, unabonnebecertbygroup-Methode
topic_type:
- apiref
api_name:
- INapCertRelyingParty.UnSubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01bbad5ef48b5f709f93f018c56b5798907d08c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956610"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a><span data-ttu-id="0a822-106">Inapcertrelyingparty:: unabonnebecertbygroup-Methode</span><span class="sxs-lookup"><span data-stu-id="0a822-106">INapCertRelyingParty::UnSubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="0a822-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0a822-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0a822-108">Die **unabonniertbygroup** -Methode entabonniert einen Integritäts Zertifikat Server (HCS).</span><span class="sxs-lookup"><span data-stu-id="0a822-108">The **UnSubscribeCertByGroup** method unsubscribes from a health certificate server (HCS).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a822-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a822-109">Syntax</span></span>


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a><span data-ttu-id="0a822-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a822-110">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="0a822-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a822-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a822-112">Eine [**enforcemententityid**](nap-datatypes.md) , die die ID des Erzwingungs Clients enthält, der abonniert wird.</span><span class="sxs-lookup"><span data-stu-id="0a822-112">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is unsubscribing.</span></span>

</dd> <dt>

 <span data-ttu-id="0a822-113">*reserviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a822-113">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a822-114">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="0a822-114">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a822-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a822-115">Return value</span></span>

<span data-ttu-id="0a822-116">Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="0a822-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="0a822-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0a822-117">Return code</span></span>                                                                                     | <span data-ttu-id="0a822-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a822-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a822-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a822-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0a822-120">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0a822-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="0a822-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="0a822-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0a822-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="0a822-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0a822-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="0a822-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0a822-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0a822-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0a822-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a822-125">Remarks</span></span>

<span data-ttu-id="0a822-126">Wenn keine anderen Abonnenten für die HCS vorhanden sind, löscht der NAPAgent die entsprechenden Integritäts Zertifikate aus dem Speicher des lokalen Computers.</span><span class="sxs-lookup"><span data-stu-id="0a822-126">If there are no other subscribers to the HCS, the NapAgent will delete the corresponding health certificates from the local machine store.</span></span>

<span data-ttu-id="0a822-127">Rufen Sie vor dem Aufrufen dieser Methode " [**abonbecertbygroup**](inapcertrelyingparty-subscribecertbygroup.md)" auf.</span><span class="sxs-lookup"><span data-stu-id="0a822-127">Before calling this method, call [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a822-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a822-128">Requirements</span></span>



| <span data-ttu-id="0a822-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a822-129">Requirement</span></span> | <span data-ttu-id="0a822-130">Wert</span><span class="sxs-lookup"><span data-stu-id="0a822-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a822-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a822-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0a822-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a822-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0a822-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a822-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0a822-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a822-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0a822-135">Header</span><span class="sxs-lookup"><span data-stu-id="0a822-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a822-136"><dt>Napcertrelyingparty. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a822-136"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a822-137">IDL</span><span class="sxs-lookup"><span data-stu-id="0a822-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0a822-138"><dt>Napcertrelyingparty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0a822-138"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a822-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a822-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a822-140">**Inapcertrelyingparty**</span><span class="sxs-lookup"><span data-stu-id="0a822-140">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





