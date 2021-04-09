---
title: Inapsystemhealthvalidator-Schnittstelle (napsystemhealthvalidator. h)
description: Muss von SHV-Entwicklern implementiert werden, damit das NAP-System mit einem SHV kommunizieren kann.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- Inapsystemhealthvalidator-Schnittstelle NAP
- Inapsystemhealthvalidator Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce4d47555926c2a3ad5b06315521fea23503d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740904"
---
# <a name="inapsystemhealthvalidator-interface"></a><span data-ttu-id="f1c01-105">Inapsystemhealthvalidator-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f1c01-105">INapSystemHealthValidator interface</span></span>

> [!Note]  
> <span data-ttu-id="f1c01-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f1c01-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f1c01-107">Das **inapsystemhealthvalidator** -Steuerelement stellt Methoden bereit, die von SHV-Entwicklern implementiert werden müssen, damit das NAP-System mit einem SHV kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="f1c01-107">The **INapSystemHealthValidator** provides methods that must be implemented by SHV developers to enable the NAP system to communicate with an SHV.</span></span>

## <a name="members"></a><span data-ttu-id="f1c01-108">Member</span><span class="sxs-lookup"><span data-stu-id="f1c01-108">Members</span></span>

<span data-ttu-id="f1c01-109">Die **inapsystemhealthvalidator** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f1c01-109">The **INapSystemHealthValidator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f1c01-110">**Inapsystemhealthvalidator** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f1c01-110">**INapSystemHealthValidator** also has these types of members:</span></span>

-   [<span data-ttu-id="f1c01-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f1c01-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f1c01-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="f1c01-112">Methods</span></span>

<span data-ttu-id="f1c01-113">Die **inapsystemhealthvalidator** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f1c01-113">The **INapSystemHealthValidator** interface has these methods.</span></span>



| <span data-ttu-id="f1c01-114">Methode</span><span class="sxs-lookup"><span data-stu-id="f1c01-114">Method</span></span>                                                                                   | <span data-ttu-id="f1c01-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1c01-115">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1c01-116">**Inapsystemhealthvalidator:: Validate**</span><span class="sxs-lookup"><span data-stu-id="f1c01-116">**INapSystemHealthValidator::Validate**</span></span>](inapsystemhealthvalidator-validate-method.md) | <span data-ttu-id="f1c01-117">Das NAP-System ruft diese Anwendungs definierte Methode auf, um die von einem Client empfangene [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) zu validieren.</span><span class="sxs-lookup"><span data-stu-id="f1c01-117">The NAP system calls this application defined method to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="f1c01-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1c01-118">Requirements</span></span>



| <span data-ttu-id="f1c01-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1c01-119">Requirement</span></span> | <span data-ttu-id="f1c01-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f1c01-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c01-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1c01-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f1c01-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f1c01-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="f1c01-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1c01-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f1c01-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1c01-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1c01-125">Header</span><span class="sxs-lookup"><span data-stu-id="f1c01-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1c01-126"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1c01-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1c01-127">IDL</span><span class="sxs-lookup"><span data-stu-id="f1c01-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f1c01-128"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f1c01-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1c01-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1c01-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c01-130">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f1c01-130">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f1c01-131">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="f1c01-131">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

