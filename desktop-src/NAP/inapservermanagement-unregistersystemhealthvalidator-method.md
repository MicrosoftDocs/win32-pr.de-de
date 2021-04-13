---
title: Inapservermanagement unregistersystemhealthvalidator-Methode (napservermanagement. h)
description: Wird verwendet, um die Registrierung eines SHV beim NAP-Server aufzuheben.
ms.assetid: f4148df1-a230-4845-ac8b-9e04be9e0d6c
keywords:
- Unregistersystemhealthvalidator-Methode NAP
- Unregistersystemhealthvalidator-Methode NAP, inapservermanagement-Schnittstelle
- Inapservermanagement Interface NAP, unregistersystemhealthvalidator-Methode
topic_type:
- apiref
api_name:
- INapServerManagement.UnregisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0715445504b862d9ae9e8478b543f8e80378f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518629"
---
# <a name="inapservermanagementunregistersystemhealthvalidator-method"></a><span data-ttu-id="c3f8f-106">Inapservermanagement:: unregistersystemhealthvalidator-Methode</span><span class="sxs-lookup"><span data-stu-id="c3f8f-106">INapServerManagement::UnregisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="c3f8f-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c3f8f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c3f8f-108">Die **inapservermanagement:: unregistersystemhealthvalidator** -Methode wird verwendet, um die Registrierung eines SHV beim NAP-Server aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="c3f8f-108">The **INapServerManagement::UnregisterSystemHealthValidator** method is used to unregister an SHV with the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f8f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3f8f-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthValidator(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="c3f8f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3f8f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3f8f-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3f8f-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3f8f-112">Eine [**systemhealthentityid**](nap-type-constants.md) , die den eindeutigen Bezeichner des SHV enthält, dessen Registrierung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3f8f-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3f8f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3f8f-113">Return value</span></span>

<span data-ttu-id="c3f8f-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c3f8f-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c3f8f-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c3f8f-115">Return code</span></span>                                                                                     | <span data-ttu-id="c3f8f-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3f8f-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c3f8f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f8f-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="c3f8f-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c3f8f-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c3f8f-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f8f-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="c3f8f-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="c3f8f-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c3f8f-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f8f-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="c3f8f-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c3f8f-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3f8f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3f8f-123">Remarks</span></span>

<span data-ttu-id="c3f8f-124">Wenn asynchrone Aufrufe für den SHV ausstehen, werden Sie zu einem späteren Zeitpunkt abgeschlossen und verworfen.</span><span class="sxs-lookup"><span data-stu-id="c3f8f-124">If there are any asynchronous calls pending on the SHV, they will complete at a later time and will be discarded.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f8f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3f8f-125">Requirements</span></span>



| <span data-ttu-id="c3f8f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3f8f-126">Requirement</span></span> | <span data-ttu-id="c3f8f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c3f8f-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f8f-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3f8f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c3f8f-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c3f8f-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="c3f8f-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3f8f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c3f8f-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3f8f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c3f8f-132">Header</span><span class="sxs-lookup"><span data-stu-id="c3f8f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3f8f-133"><dt>Napservermanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3f8f-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="c3f8f-134">IDL</span><span class="sxs-lookup"><span data-stu-id="c3f8f-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c3f8f-135"><dt>Napservermanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c3f8f-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="c3f8f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c3f8f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3f8f-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3f8f-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="c3f8f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3f8f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f8f-139">**Inapservermanagement**</span><span class="sxs-lookup"><span data-stu-id="c3f8f-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





