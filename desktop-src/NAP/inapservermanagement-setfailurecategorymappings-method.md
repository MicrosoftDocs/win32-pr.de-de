---
title: Inapservermanagement setfailurecategorymappings-Methode (napservermanagement. h)
description: Wird verwendet, um die Fehler Kategoriezuordnungen von SHV festzulegen.
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- Setfailurecategorymappings-Methode NAP
- Setfailurecategorymappings-Methode NAP, inapservermanagement-Schnittstelle
- Inapservermanagement-Schnittstelle NAP, setfailurecategorymappings-Methode
topic_type:
- apiref
api_name:
- INapServerManagement.SetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a220d6603ef5bbb49377ac0e212d5d98afa4bdd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956768"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a><span data-ttu-id="a45b1-106">Inapservermanagement:: setfailurecategorymappings-Methode</span><span class="sxs-lookup"><span data-stu-id="a45b1-106">INapServerManagement::SetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="a45b1-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a45b1-108">Die **inapservermanagement:: setfailurecategorymappings** -Methode wird verwendet, um die SHV-Zuordnungen für die Fehler Kategorie festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a45b1-108">The **INapServerManagement::SetFailureCategoryMappings** method is used to set the SHV's failure category mappings.</span></span>

## <a name="syntax"></a><span data-ttu-id="a45b1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a45b1-109">Syntax</span></span>


```C++
HRESULT SetFailureCategoryMappings(
  [in]       SystemHealthEntityId   id,
  [in] const FailureCategoryMapping mapping
);
```



## <a name="parameters"></a><span data-ttu-id="a45b1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a45b1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a45b1-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a45b1-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a45b1-112">Eine [**systemhealthentityid**](nap-type-constants.md) , die den eindeutigen Bezeichner des SHV enthält.</span><span class="sxs-lookup"><span data-stu-id="a45b1-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="a45b1-113">*Zuordnung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a45b1-113">*mapping* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a45b1-114">Eine [**failurecategorymapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) -Struktur, die die Fehler Kategorie-Mapping-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="a45b1-114">A [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure that contains the failure category mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a45b1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a45b1-115">Return value</span></span>

<span data-ttu-id="a45b1-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a45b1-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a45b1-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a45b1-117">Return code</span></span>                                                                                     | <span data-ttu-id="a45b1-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a45b1-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a45b1-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a45b1-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a45b1-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a45b1-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a45b1-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="a45b1-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a45b1-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="a45b1-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a45b1-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a45b1-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a45b1-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a45b1-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a45b1-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a45b1-125">Requirements</span></span>



| <span data-ttu-id="a45b1-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a45b1-126">Requirement</span></span> | <span data-ttu-id="a45b1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a45b1-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a45b1-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a45b1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a45b1-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a45b1-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="a45b1-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a45b1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a45b1-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a45b1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a45b1-132">Header</span><span class="sxs-lookup"><span data-stu-id="a45b1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a45b1-133"><dt>Napservermanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="a45b1-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="a45b1-134">IDL</span><span class="sxs-lookup"><span data-stu-id="a45b1-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a45b1-135"><dt>Napservermanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a45b1-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="a45b1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a45b1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a45b1-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a45b1-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="a45b1-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a45b1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a45b1-139">**Inapservermanagement**</span><span class="sxs-lookup"><span data-stu-id="a45b1-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





