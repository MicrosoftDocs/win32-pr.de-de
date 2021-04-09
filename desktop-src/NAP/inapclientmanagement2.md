---
title: INapClientManagement2-Schnittstelle (napmanagement. h)
description: Stellt Methoden für die NAP-Client Verwaltung bereit. | INapClientManagement2-Schnittstelle (napmanagement. h)
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- INapClientManagement2-Schnittstelle NAP
- INapClientManagement2 Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapClientManagement2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3441b52ddf776337765f39d23528bc223a17b1e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050808"
---
# <a name="inapclientmanagement2-interface"></a><span data-ttu-id="d8057-106">INapClientManagement2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d8057-106">INapClientManagement2 interface</span></span>

> [!Note]  
> <span data-ttu-id="d8057-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d8057-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d8057-108">Die **INapClientManagement2** -Schnittstelle bietet Methoden für die NAP-Client Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="d8057-108">The **INapClientManagement2** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="d8057-109">Diese Schnittstelle erbt alle Methoden von [**inapclientmanagement**](inapclientmanagement.md) und sollte stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8057-109">This interface inherits all the methods of [**INapClientManagement**](inapclientmanagement.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="d8057-110">Member</span><span class="sxs-lookup"><span data-stu-id="d8057-110">Members</span></span>

<span data-ttu-id="d8057-111">Die **INapClientManagement2** -Schnittstelle erbt von [**inapclientmanagement**](inapclientmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="d8057-111">The **INapClientManagement2** interface inherits from [**INapClientManagement**](inapclientmanagement.md).</span></span> <span data-ttu-id="d8057-112">**INapClientManagement2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d8057-112">**INapClientManagement2** also has these types of members:</span></span>

-   [<span data-ttu-id="d8057-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="d8057-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d8057-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="d8057-114">Methods</span></span>

<span data-ttu-id="d8057-115">Die **INapClientManagement2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d8057-115">The **INapClientManagement2** interface has these methods.</span></span>



| <span data-ttu-id="d8057-116">Methode</span><span class="sxs-lookup"><span data-stu-id="d8057-116">Method</span></span>                                                                                                    | <span data-ttu-id="d8057-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8057-117">Description</span></span>                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8057-118">**INapClientManagement2:: getsystemisolationinfoex**</span><span class="sxs-lookup"><span data-stu-id="d8057-118">**INapClientManagement2::GetSystemIsolationInfoEx**</span></span>](inapclientmanagement2-getsystemisolationinfoex.md) | <span data-ttu-id="d8057-119">Ruft Informationen zum Isolations Status und zum erweiterten Isolations Status des NAP-Clients ab.</span><span class="sxs-lookup"><span data-stu-id="d8057-119">Retrieves information about the isolation state and extended isolation state of the Nap client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d8057-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8057-120">Requirements</span></span>



| <span data-ttu-id="d8057-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8057-121">Requirement</span></span> | <span data-ttu-id="d8057-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d8057-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8057-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8057-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d8057-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8057-124">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d8057-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8057-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d8057-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8057-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d8057-127">Header</span><span class="sxs-lookup"><span data-stu-id="d8057-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8057-128"><dt>Napmanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8057-128"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8057-129">IDL</span><span class="sxs-lookup"><span data-stu-id="d8057-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d8057-130"><dt>Napmanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d8057-130"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="d8057-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d8057-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8057-132"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8057-132"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="d8057-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8057-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8057-134">**Inapclientmanagement**</span><span class="sxs-lookup"><span data-stu-id="d8057-134">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> <dt>

[<span data-ttu-id="d8057-135">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d8057-135">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="d8057-136">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="d8057-136">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





