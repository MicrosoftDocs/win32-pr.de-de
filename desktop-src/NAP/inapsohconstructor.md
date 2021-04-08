---
title: Inapsohconstructor-Schnittstelle (napprotocol. h)
description: Werden von SHAs zum Erstellen von sohrequests und von SHVs zum Erstellen von sohantworten verwendet.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- Inapsohconstructor-Schnittstelle NAP
- Inapsohconstructor Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546a6d3b4ec262fdd725af24211338e848b2b848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949479"
---
# <a name="inapsohconstructor-interface"></a><span data-ttu-id="74fbe-105">Inapsohconstructor-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="74fbe-105">INapSoHConstructor interface</span></span>

> [!Note]  
> <span data-ttu-id="74fbe-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="74fbe-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="74fbe-107">Der **inapsohconstructor** stellt Methoden bereit, die von SHAs zum Erstellen von [**sohrequests**](/windows/win32/api/naptypes/ns-naptypes-soh) und von SHVs zum Erstellen von **sohantworten** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74fbe-107">The **INapSoHConstructor** provides methods that are used by SHAs to construct [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to construct **SoHResponses**.</span></span>

## <a name="members"></a><span data-ttu-id="74fbe-108">Member</span><span class="sxs-lookup"><span data-stu-id="74fbe-108">Members</span></span>

<span data-ttu-id="74fbe-109">Die **inapsohconstructor** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="74fbe-109">The **INapSoHConstructor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="74fbe-110">**Inapsohconstructor** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="74fbe-110">**INapSoHConstructor** also has these types of members:</span></span>

-   [<span data-ttu-id="74fbe-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="74fbe-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="74fbe-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="74fbe-112">Methods</span></span>

<span data-ttu-id="74fbe-113">Die **inapsohconstructor** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="74fbe-113">The **INapSoHConstructor** interface has these methods.</span></span>



| <span data-ttu-id="74fbe-114">Methode</span><span class="sxs-lookup"><span data-stu-id="74fbe-114">Method</span></span>                                                                                   | <span data-ttu-id="74fbe-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74fbe-115">Description</span></span>                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [<span data-ttu-id="74fbe-116">**Inapsohconstructor:: appendattribute**</span><span class="sxs-lookup"><span data-stu-id="74fbe-116">**INapSoHConstructor::AppendAttribute**</span></span>](inapsohconstructor-appendattribute-method.md) | <span data-ttu-id="74fbe-117">Fügt ein TLV am Ende des SoH-Puffers hinzu.</span><span class="sxs-lookup"><span data-stu-id="74fbe-117">Adds a TLV to the end of the SoH buffer.</span></span><br/> |
| [<span data-ttu-id="74fbe-118">**Inapsohconstructor:: getsoh**</span><span class="sxs-lookup"><span data-stu-id="74fbe-118">**INapSoHConstructor::GetSoH**</span></span>](inapsohconstructor-getsoh-method.md)                   | <span data-ttu-id="74fbe-119">Ruft das erstellte SoH-Paket ab.</span><span class="sxs-lookup"><span data-stu-id="74fbe-119">Retrieves the constructed SoH packet.</span></span><br/>    |
| [<span data-ttu-id="74fbe-120">**Inapsohconstructor:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="74fbe-120">**INapSoHConstructor::Initialize**</span></span>](inapsohconstructor-initialize-method.md)           | <span data-ttu-id="74fbe-121">Initialisiert das SoH-Paket.</span><span class="sxs-lookup"><span data-stu-id="74fbe-121">Initializes the SoH packet.</span></span><br/>              |
| [<span data-ttu-id="74fbe-122">**Inapsohconstructor:: Validate**</span><span class="sxs-lookup"><span data-stu-id="74fbe-122">**INapSoHConstructor::Validate**</span></span>](inapsohconstructor-validate-method.md)               | <span data-ttu-id="74fbe-123">Überprüft die Gültigkeit des SoH-Pakets.</span><span class="sxs-lookup"><span data-stu-id="74fbe-123">Checks the validity of the SoH packet.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="74fbe-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74fbe-124">Requirements</span></span>



| <span data-ttu-id="74fbe-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74fbe-125">Requirement</span></span> | <span data-ttu-id="74fbe-126">Wert</span><span class="sxs-lookup"><span data-stu-id="74fbe-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="74fbe-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74fbe-127">Minimum supported client</span></span><br/> | <span data-ttu-id="74fbe-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74fbe-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="74fbe-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74fbe-129">Minimum supported server</span></span><br/> | <span data-ttu-id="74fbe-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74fbe-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="74fbe-131">Header</span><span class="sxs-lookup"><span data-stu-id="74fbe-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="74fbe-132"><dt>Napprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="74fbe-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="74fbe-133">IDL</span><span class="sxs-lookup"><span data-stu-id="74fbe-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="74fbe-134"><dt>Napprotocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="74fbe-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="74fbe-135">DLL</span><span class="sxs-lookup"><span data-stu-id="74fbe-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74fbe-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74fbe-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="74fbe-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74fbe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74fbe-138">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="74fbe-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="74fbe-139">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="74fbe-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

