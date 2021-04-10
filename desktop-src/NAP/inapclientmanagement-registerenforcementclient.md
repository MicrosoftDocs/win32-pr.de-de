---
title: Inapclientmanagement registerenforcementclient-Methode (napmanagement. h)
description: Registriert einen Erzwingungs Client beim NAP-System.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- Registerenforcementclient-Methode NAP
- Registerenforcementclient-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, registerenforcementclient-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8ed4b5fe5a97d60b764341f21f25628c3c3434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104696"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a><span data-ttu-id="90dce-106">Inapclientmanagement:: registerenforcementclient-Methode</span><span class="sxs-lookup"><span data-stu-id="90dce-106">INapClientManagement::RegisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="90dce-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90dce-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="90dce-108">Mit der **registerenforcementclient** -Methode wird ein Erzwingungs Client beim NAP-System registriert.</span><span class="sxs-lookup"><span data-stu-id="90dce-108">The **RegisterEnforcementClient** method registers an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="90dce-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="90dce-109">Syntax</span></span>


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a><span data-ttu-id="90dce-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="90dce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90dce-111">*Enforcer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90dce-111">*enforcer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90dce-112">Ein Zeiger auf eine [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Datenstruktur, die die dem Erzwingungs Client zugeordneten Registrierungsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="90dce-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structure that contains the registration information that is associated with the enforcement client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90dce-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90dce-113">Return value</span></span>

<span data-ttu-id="90dce-114">Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.</span><span class="sxs-lookup"><span data-stu-id="90dce-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="90dce-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="90dce-115">Return code</span></span>                                                                                            | <span data-ttu-id="90dce-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90dce-116">Description</span></span>                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="90dce-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="90dce-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="90dce-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="90dce-118">Operation successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="90dce-119"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="90dce-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="90dce-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="90dce-120">Permissions error, access denied.</span></span><br/>                                      |
| <dl> <span data-ttu-id="90dce-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="90dce-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="90dce-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="90dce-122">System resource limit, could not perform the operation.</span></span><br/>                |
| <dl> <span data-ttu-id="90dce-123"><dt>**in \_ \_ Konflikt stehende \_ ID für NAP**</dt></span><span class="sxs-lookup"><span data-stu-id="90dce-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="90dce-124">Ein Erzwingungs-Agent mit dem angegebenen Bezeichner ist bereits registriert.</span><span class="sxs-lookup"><span data-stu-id="90dce-124">An enforcement agent using the given identifier is already registered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="90dce-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90dce-125">Requirements</span></span>



| <span data-ttu-id="90dce-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90dce-126">Requirement</span></span> | <span data-ttu-id="90dce-127">Wert</span><span class="sxs-lookup"><span data-stu-id="90dce-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="90dce-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90dce-128">Minimum supported client</span></span><br/> | <span data-ttu-id="90dce-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90dce-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="90dce-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90dce-130">Minimum supported server</span></span><br/> | <span data-ttu-id="90dce-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90dce-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="90dce-132">Header</span><span class="sxs-lookup"><span data-stu-id="90dce-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="90dce-133"><dt>Napmanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="90dce-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="90dce-134">IDL</span><span class="sxs-lookup"><span data-stu-id="90dce-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90dce-135"><dt>Napmanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="90dce-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="90dce-136">DLL</span><span class="sxs-lookup"><span data-stu-id="90dce-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90dce-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90dce-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="90dce-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90dce-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90dce-139">**Inapclientmanagement**</span><span class="sxs-lookup"><span data-stu-id="90dce-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





