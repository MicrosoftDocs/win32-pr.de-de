---
title: Inapcertrelyingparty getabonbedrelyingparties-Methode (napcertrelyingparty. h)
description: Ruft eine Liste der vertrauenden Seiten ab, die abonniert haben.
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- Getabonbedrelyingparties-Methode NAP
- Getabonbedrelyingparties-Methode NAP, inapcertrelyingparty-Schnittstelle
- Inapcertrelyingparty-Schnittstelle NAP, getabonbedrelyingparties-Methode
topic_type:
- apiref
api_name:
- INapCertRelyingParty.GetSubscribedRelyingParties
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84871838324c431278d15bb9e78471f48aa1f34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475489"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a><span data-ttu-id="3a5e2-106">Inapcertrelyingparty:: getabonbedrelyingparties-Methode</span><span class="sxs-lookup"><span data-stu-id="3a5e2-106">INapCertRelyingParty::GetSubscribedRelyingParties method</span></span>

> [!Note]  
> <span data-ttu-id="3a5e2-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a5e2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3a5e2-108">Die **getabonbedrelyingparties** -Methode ruft eine Liste der vertrauenden Seiten ab, die abonniert haben.</span><span class="sxs-lookup"><span data-stu-id="3a5e2-108">The **GetSubscribedRelyingParties** method gets a list of relying parties that have subscribed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a5e2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a5e2-109">Syntax</span></span>


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a><span data-ttu-id="3a5e2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a5e2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a5e2-111">*Anzahl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3a5e2-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5e2-112">Ein Zeiger auf eine [**enforcemententitycount**](nap-datatypes.md) , die die Anzahl der abonnierten vertrauenden Seiten enthält.</span><span class="sxs-lookup"><span data-stu-id="3a5e2-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of subscribed relying parties.</span></span>

</dd> <dt>

<span data-ttu-id="3a5e2-113">*relyingparties* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3a5e2-113">*relyingParties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5e2-114">Ein Zeiger auf einen Zeiger auf eine [**enforcemententityid**](nap-datatypes.md) , die die Liste der abonnierten vertrauenden Seiten enthält.</span><span class="sxs-lookup"><span data-stu-id="3a5e2-114">A pointer to a pointer to an [**EnforcementEntityId**](nap-datatypes.md) that contains the list of subscribed relying parties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a5e2-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a5e2-115">Return value</span></span>

<span data-ttu-id="3a5e2-116">Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="3a5e2-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="3a5e2-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3a5e2-117">Return code</span></span>                                                                                     | <span data-ttu-id="3a5e2-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a5e2-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3a5e2-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a5e2-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="3a5e2-120">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3a5e2-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="3a5e2-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="3a5e2-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="3a5e2-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="3a5e2-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3a5e2-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="3a5e2-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="3a5e2-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3a5e2-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3a5e2-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a5e2-125">Remarks</span></span>

<span data-ttu-id="3a5e2-126">Der Aufrufer muss den Parameter *relyingparties* mithilfe von **CoTaskMemFree** freigeben.</span><span class="sxs-lookup"><span data-stu-id="3a5e2-126">The caller must free the *relyingParties* parameter using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a5e2-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a5e2-127">Requirements</span></span>



| <span data-ttu-id="3a5e2-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a5e2-128">Requirement</span></span> | <span data-ttu-id="3a5e2-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3a5e2-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5e2-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a5e2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5e2-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a5e2-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3a5e2-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a5e2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5e2-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a5e2-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3a5e2-134">Header</span><span class="sxs-lookup"><span data-stu-id="3a5e2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a5e2-135"><dt>Napcertrelyingparty. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a5e2-135"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a5e2-136">IDL</span><span class="sxs-lookup"><span data-stu-id="3a5e2-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3a5e2-137"><dt>Napcertrelyingparty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3a5e2-137"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a5e2-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a5e2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a5e2-139">**Inapcertrelyingparty**</span><span class="sxs-lookup"><span data-stu-id="3a5e2-139">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





