---
title: Inapservermanagement-Schnittstelle (napservermanagement. h)
description: Wird verwendet, um den NAP-Server zu verwalten.
ms.assetid: 5c4f9bf1-fe82-48f5-8aa4-5c73ab01a78a
keywords:
- Inapservermanagement-Schnittstelle NAP
- Inapservermanagement-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapServerManagement
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5eed03f535653a3b9244ff1aa74fe499c1bf2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104145"
---
# <a name="inapservermanagement-interface"></a><span data-ttu-id="aeb92-105">Inapservermanagement-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="aeb92-105">INapServerManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="aeb92-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aeb92-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="aeb92-107">Die **inapservermanagement** -Methode stellt Methoden bereit, die zum Verwalten des NAP-Servers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aeb92-107">The **INapServerManagement** provides methods that are used to manage the NAP Server.</span></span>

## <a name="members"></a><span data-ttu-id="aeb92-108">Member</span><span class="sxs-lookup"><span data-stu-id="aeb92-108">Members</span></span>

<span data-ttu-id="aeb92-109">Die **inapservermanagement** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="aeb92-109">The **INapServerManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aeb92-110">**Inapservermanagement** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aeb92-110">**INapServerManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="aeb92-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="aeb92-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aeb92-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="aeb92-112">Methods</span></span>

<span data-ttu-id="aeb92-113">Die **inapservermanagement** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="aeb92-113">The **INapServerManagement** interface has these methods.</span></span>



| <span data-ttu-id="aeb92-114">Methode</span><span class="sxs-lookup"><span data-stu-id="aeb92-114">Method</span></span>                                                                                                                       | <span data-ttu-id="aeb92-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aeb92-115">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="aeb92-116">**Inapservermanagement:: registersystemhealthvalidator**</span><span class="sxs-lookup"><span data-stu-id="aeb92-116">**INapServerManagement::RegisterSystemHealthValidator**</span></span>](inapservermanagement-registersystemhealthvalidator-method.md)     | <span data-ttu-id="aeb92-117">Registriert einen SHV.</span><span class="sxs-lookup"><span data-stu-id="aeb92-117">Registers an SHV.</span></span><br/>                         |
| [<span data-ttu-id="aeb92-118">**Inapservermanagement:: setfailurecategorymappings**</span><span class="sxs-lookup"><span data-stu-id="aeb92-118">**INapServerManagement::SetFailureCategoryMappings**</span></span>](inapservermanagement-setfailurecategorymappings-method.md)           | <span data-ttu-id="aeb92-119">Legt die Zuordnungen der Fehler Kategorie des SHV fest.</span><span class="sxs-lookup"><span data-stu-id="aeb92-119">Sets the SHV's failure category mappings.</span></span><br/> |
| [<span data-ttu-id="aeb92-120">**Inapservermanagement:: unregistersystemhealthvalidator**</span><span class="sxs-lookup"><span data-stu-id="aeb92-120">**INapServerManagement::UnregisterSystemHealthValidator**</span></span>](inapservermanagement-unregistersystemhealthvalidator-method.md) | <span data-ttu-id="aeb92-121">Aufheben der Registrierung eines SHV vom NAP-Server.</span><span class="sxs-lookup"><span data-stu-id="aeb92-121">Deregisters an SHV from the NAP server.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="aeb92-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aeb92-122">Requirements</span></span>



| <span data-ttu-id="aeb92-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aeb92-123">Requirement</span></span> | <span data-ttu-id="aeb92-124">Wert</span><span class="sxs-lookup"><span data-stu-id="aeb92-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb92-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aeb92-125">Minimum supported client</span></span><br/> | <span data-ttu-id="aeb92-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aeb92-126">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="aeb92-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aeb92-127">Minimum supported server</span></span><br/> | <span data-ttu-id="aeb92-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aeb92-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="aeb92-129">Header</span><span class="sxs-lookup"><span data-stu-id="aeb92-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="aeb92-130"><dt>Napservermanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeb92-130"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="aeb92-131">IDL</span><span class="sxs-lookup"><span data-stu-id="aeb92-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aeb92-132"><dt>Napservermanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aeb92-132"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="aeb92-133">DLL</span><span class="sxs-lookup"><span data-stu-id="aeb92-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aeb92-134"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeb92-134"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="aeb92-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aeb92-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb92-136">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="aeb92-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="aeb92-137">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="aeb92-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

