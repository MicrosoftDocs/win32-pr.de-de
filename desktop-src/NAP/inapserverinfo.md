---
title: Inapserverinfo-Schnittstelle (napservermanagement. h)
description: Verwaltungs Clients (z. b. WMI-Anbieter oder Befehlszeilen Tools) verwenden, um den Status des NAP-Server Systems abzufragen.
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- Inapserverinfo-Schnittstelle NAP
- Inapserverinfo-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec17e3303fe4af4d359279de6c5fa7aa5f34d409
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339161"
---
# <a name="inapserverinfo-interface"></a><span data-ttu-id="06be2-105">Inapserverinfo-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="06be2-105">INapServerInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="06be2-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="06be2-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="06be2-107">**Inapserverinfo** stellt Methoden bereit, mit denen Verwaltungs Clients (z. b. WMI-Anbieter oder Befehlszeilen Tools) den Status des NAP-Server Systems Abfragen.</span><span class="sxs-lookup"><span data-stu-id="06be2-107">The **INapServerInfo** provides methods that Management clients (for example, WMI providers or command-line tools) use to query the status of the NAP server system.</span></span>

## <a name="members"></a><span data-ttu-id="06be2-108">Member</span><span class="sxs-lookup"><span data-stu-id="06be2-108">Members</span></span>

<span data-ttu-id="06be2-109">Die **inapserverinfo** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="06be2-109">The **INapServerInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="06be2-110">**Inapserverinfo** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="06be2-110">**INapServerInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="06be2-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="06be2-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="06be2-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="06be2-112">Methods</span></span>

<span data-ttu-id="06be2-113">Die **inapserverinfo** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="06be2-113">The **INapServerInfo** interface has these methods.</span></span>



| <span data-ttu-id="06be2-114">Methode</span><span class="sxs-lookup"><span data-stu-id="06be2-114">Method</span></span>                                                                                                                   | <span data-ttu-id="06be2-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06be2-115">Description</span></span>                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="06be2-116">**Inapserverinfo:: getfailurecategorymappings**</span><span class="sxs-lookup"><span data-stu-id="06be2-116">**INapServerInfo::GetFailureCategoryMappings**</span></span>](inapserverinfo-getfailurecategorymappings-method.md)                   | <span data-ttu-id="06be2-117">Ruft die Zuordnungen der Fehlerkategorien für einen angegebenen SHV ab.</span><span class="sxs-lookup"><span data-stu-id="06be2-117">Retrieves the failure category mappings for a specified SHV.</span></span><br/> |
| [<span data-ttu-id="06be2-118">**Inapserverinfo:: getnapserverinfo**</span><span class="sxs-lookup"><span data-stu-id="06be2-118">**INapServerInfo::GetNapServerInfo**</span></span>](inapserverinfo-getnapserverinfo-method.md)                                       | <span data-ttu-id="06be2-119">Ruft Informationen zum NAP-Server ab.</span><span class="sxs-lookup"><span data-stu-id="06be2-119">Retrieves information about the NAP server.</span></span><br/>                  |
| [<span data-ttu-id="06be2-120">**Inapserverinfo:: getregisteredsystemhealthvalidators**</span><span class="sxs-lookup"><span data-stu-id="06be2-120">**INapServerInfo::GetRegisteredSystemHealthValidators**</span></span>](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | <span data-ttu-id="06be2-121">Ruft eine Liste registrierter SHVs ab.</span><span class="sxs-lookup"><span data-stu-id="06be2-121">Retrieves a list of registered SHVs.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="06be2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06be2-122">Remarks</span></span>

<span data-ttu-id="06be2-123">Diese Methoden bieten nur statische Informationen über den NAP-Server und dessen Komponenten im System.</span><span class="sxs-lookup"><span data-stu-id="06be2-123">These methods provide only static information about the NAP Server and its components on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="06be2-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06be2-124">Requirements</span></span>



| <span data-ttu-id="06be2-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06be2-125">Requirement</span></span> | <span data-ttu-id="06be2-126">Wert</span><span class="sxs-lookup"><span data-stu-id="06be2-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06be2-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06be2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="06be2-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="06be2-128">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="06be2-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06be2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="06be2-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06be2-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="06be2-131">Header</span><span class="sxs-lookup"><span data-stu-id="06be2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="06be2-132"><dt>Napservermanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="06be2-132"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="06be2-133">IDL</span><span class="sxs-lookup"><span data-stu-id="06be2-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06be2-134"><dt>Napservermanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="06be2-134"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="06be2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="06be2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06be2-136"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06be2-136"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="06be2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06be2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06be2-138">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="06be2-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="06be2-139">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="06be2-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

