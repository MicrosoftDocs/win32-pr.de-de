---
title: Inapserverinfo getregisteredsystemhealthvalidators-Methode (napservermanagement. h)
description: Ruft eine Liste registrierter SHVs ab.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- Getregisteredsystemhealthvalidators-Methode NAP
- Getregisteredsystemhealthvalidators-Methode NAP, inapserverinfo-Schnittstelle
- Inapserverinfo-Schnittstelle NAP, getregisteredsystemhealthvalidators-Methode
topic_type:
- apiref
api_name:
- INapServerInfo.GetRegisteredSystemHealthValidators
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ffdd4d363c994efbecdb57fe4ad7203393fd1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040875"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a><span data-ttu-id="f248b-106">Inapserverinfo:: getregisteredsystemhealthvalidators-Methode</span><span class="sxs-lookup"><span data-stu-id="f248b-106">INapServerInfo::GetRegisteredSystemHealthValidators method</span></span>

> [!Note]  
> <span data-ttu-id="f248b-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f248b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f248b-108">Die **inapserverinfo:: getregisteredsystemhealthvalidators** -Methode ruft eine Liste registrierter SHVs ab.</span><span class="sxs-lookup"><span data-stu-id="f248b-108">The **INapServerInfo::GetRegisteredSystemHealthValidators** method retrieves a list of registered SHVs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f248b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f248b-109">Syntax</span></span>


```C++
HRESULT GetRegisteredSystemHealthValidators(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **validators,
  [out] CLSID                        **validatorClsids
);
```



## <a name="parameters"></a><span data-ttu-id="f248b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f248b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f248b-111">*Anzahl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f248b-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f248b-112">Ein Zeiger auf eine [**systemhealthentitycount**](nap-type-constants.md) , die die Anzahl der registrierten SHVs enthält.</span><span class="sxs-lookup"><span data-stu-id="f248b-112">A pointer to a [**SystemHealthEntityCount**](nap-type-constants.md) that contains the number of registered SHVs.</span></span>

</dd> <dt>

<span data-ttu-id="f248b-113">*Validierungs Steuerelemente* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f248b-113">*validators* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f248b-114">Ein Zeiger auf einen Zeiger auf eine [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Struktur, die die SHV-Registrierungsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="f248b-114">A pointer to a pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="f248b-115">*validatorclsids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f248b-115">*validatorClsids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f248b-116">Zeiger auf ein Array von IDs für die registrierten SHVs.</span><span class="sxs-lookup"><span data-stu-id="f248b-116">Pointer to an array of IDs for the registered SHVs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f248b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f248b-117">Return value</span></span>

<span data-ttu-id="f248b-118">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f248b-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f248b-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f248b-119">Return code</span></span>                                                                                     | <span data-ttu-id="f248b-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f248b-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f248b-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f248b-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f248b-122">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f248b-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f248b-123"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="f248b-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f248b-124">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="f248b-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f248b-125"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f248b-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f248b-126">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f248b-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f248b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f248b-127">Requirements</span></span>



| <span data-ttu-id="f248b-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f248b-128">Requirement</span></span> | <span data-ttu-id="f248b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f248b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f248b-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f248b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f248b-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f248b-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="f248b-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f248b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f248b-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f248b-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f248b-134">Header</span><span class="sxs-lookup"><span data-stu-id="f248b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f248b-135"><dt>Napservermanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="f248b-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="f248b-136">IDL</span><span class="sxs-lookup"><span data-stu-id="f248b-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f248b-137"><dt>Napservermanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f248b-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="f248b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f248b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f248b-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f248b-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="f248b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f248b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f248b-141">**Napcomponentregistrationinfo**</span><span class="sxs-lookup"><span data-stu-id="f248b-141">**NapComponentRegistrationInfo**</span></span>](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[<span data-ttu-id="f248b-142">**Inapserverinfo**</span><span class="sxs-lookup"><span data-stu-id="f248b-142">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





