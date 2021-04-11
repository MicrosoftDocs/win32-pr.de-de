---
title: Inapservermanagement registersystemhealthvalidator-Methode (napservermanagement. h)
description: Registriert einen SHV.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- Registersystemhealthvalidator-Methode NAP
- Registersystemhealthvalidator-Methode NAP, inapservermanagement-Schnittstelle
- Inapservermanagement-Schnittstelle NAP, registersystemhealthvalidator-Methode
topic_type:
- apiref
api_name:
- INapServerManagement.RegisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abd8d42da196caa804a8919c6425fda9fcb950c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213753"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a><span data-ttu-id="83958-106">Inapservermanagement:: registersystemhealthvalidator-Methode</span><span class="sxs-lookup"><span data-stu-id="83958-106">INapServerManagement::RegisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="83958-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83958-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="83958-108">Die **inapservermanagement:: registersystemhealthvalidator** -Methode registriert einen SHV.</span><span class="sxs-lookup"><span data-stu-id="83958-108">The **INapServerManagement::RegisterSystemHealthValidator** method registers an SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="83958-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="83958-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a><span data-ttu-id="83958-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="83958-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83958-111">*Validierungs Steuerelement* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83958-111">*validator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83958-112">Ein Zeiger auf eine [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Struktur, die die SHV-Registrierungsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="83958-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="83958-113">*validatorclsid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83958-113">*validatorClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83958-114">Ein Zeiger auf die CLSID der com-Klasse, die die [**inapsystemhealthvalidator**](inapsystemhealthvalidator.md) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="83958-114">A pointer to the CLSID of the COM class that implements the [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83958-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83958-115">Return value</span></span>

<span data-ttu-id="83958-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="83958-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="83958-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="83958-117">Return code</span></span>                                                                                            | <span data-ttu-id="83958-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83958-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="83958-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="83958-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="83958-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="83958-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="83958-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="83958-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="83958-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="83958-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="83958-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="83958-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="83958-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="83958-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="83958-125"><dt>**in \_ \_ Konflikt stehende \_ ID für NAP**</dt></span><span class="sxs-lookup"><span data-stu-id="83958-125"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="83958-126">Die SHV-ID ist bereits registriert.</span><span class="sxs-lookup"><span data-stu-id="83958-126">SHV id is already registered.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="83958-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83958-127">Requirements</span></span>



| <span data-ttu-id="83958-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83958-128">Requirement</span></span> | <span data-ttu-id="83958-129">Wert</span><span class="sxs-lookup"><span data-stu-id="83958-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83958-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83958-130">Minimum supported client</span></span><br/> | <span data-ttu-id="83958-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="83958-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="83958-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83958-132">Minimum supported server</span></span><br/> | <span data-ttu-id="83958-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="83958-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="83958-134">Header</span><span class="sxs-lookup"><span data-stu-id="83958-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="83958-135"><dt>Napservermanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="83958-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="83958-136">IDL</span><span class="sxs-lookup"><span data-stu-id="83958-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="83958-137"><dt>Napservermanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="83958-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="83958-138">DLL</span><span class="sxs-lookup"><span data-stu-id="83958-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83958-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83958-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="83958-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83958-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83958-141">**Inapservermanagement**</span><span class="sxs-lookup"><span data-stu-id="83958-141">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





