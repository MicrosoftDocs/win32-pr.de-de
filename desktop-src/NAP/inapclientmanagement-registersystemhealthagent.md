---
title: Inapclientmanagement registersystemhealthagent-Methode (napmanagement. h)
description: Registriert einen SHA beim NAP-System.
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- Registersystemhealthagent-Methode NAP
- Registersystemhealthagent-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, registersystemhealthagent-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581c49a117a2b8aaa2c4dda2c6573e4a6327b688
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477817"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a><span data-ttu-id="76b01-106">Inapclientmanagement:: registersystemhealthagent-Methode</span><span class="sxs-lookup"><span data-stu-id="76b01-106">INapClientManagement::RegisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="76b01-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76b01-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="76b01-108">Mit der **registersystemhealthagent** -Methode wird ein SHA beim NAP-System registriert.</span><span class="sxs-lookup"><span data-stu-id="76b01-108">The **RegisterSystemHealthAgent** method registers an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="76b01-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="76b01-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a><span data-ttu-id="76b01-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="76b01-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76b01-111">*Agent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76b01-111">*agent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76b01-112">Ein Zeiger auf eine [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Struktur, die die Registrierungsinformationen für den SHA enthält.</span><span class="sxs-lookup"><span data-stu-id="76b01-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the registration information for the SHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76b01-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76b01-113">Return value</span></span>

<span data-ttu-id="76b01-114">Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.</span><span class="sxs-lookup"><span data-stu-id="76b01-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="76b01-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="76b01-115">Return code</span></span>                                                                                            | <span data-ttu-id="76b01-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76b01-116">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="76b01-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="76b01-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="76b01-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="76b01-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="76b01-119"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="76b01-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="76b01-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="76b01-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="76b01-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="76b01-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="76b01-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="76b01-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="76b01-123"><dt>**in \_ \_ Konflikt stehende \_ ID für NAP**</dt></span><span class="sxs-lookup"><span data-stu-id="76b01-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="76b01-124">Ein SHA, der diese ID verwendet, ist bereits registriert.</span><span class="sxs-lookup"><span data-stu-id="76b01-124">An SHA that uses this ID is already registered.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="76b01-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76b01-125">Requirements</span></span>



| <span data-ttu-id="76b01-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76b01-126">Requirement</span></span> | <span data-ttu-id="76b01-127">Wert</span><span class="sxs-lookup"><span data-stu-id="76b01-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="76b01-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76b01-128">Minimum supported client</span></span><br/> | <span data-ttu-id="76b01-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76b01-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="76b01-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76b01-130">Minimum supported server</span></span><br/> | <span data-ttu-id="76b01-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76b01-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="76b01-132">Header</span><span class="sxs-lookup"><span data-stu-id="76b01-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="76b01-133"><dt>Napmanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="76b01-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="76b01-134">IDL</span><span class="sxs-lookup"><span data-stu-id="76b01-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="76b01-135"><dt>Napmanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="76b01-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="76b01-136">DLL</span><span class="sxs-lookup"><span data-stu-id="76b01-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76b01-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76b01-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="76b01-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76b01-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76b01-139">**Inapclientmanagement**</span><span class="sxs-lookup"><span data-stu-id="76b01-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





