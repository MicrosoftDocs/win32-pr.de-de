---
title: INapSystemHealthValidationRequest2-Schnittstelle (napsystemhealthvalidator. h)
description: Stellt Methoden bereit, die zur Unterstützung von Systemintegritäts-Validierungs Steuerelementen verwendet werden, die vom Anwendungsentwickler definiert werden.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- INapSystemHealthValidationRequest2-Schnittstelle NAP
- INapSystemHealthValidationRequest2 Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12fdbfc46578a4e64a92accc46f6b910a44dd946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342883"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a><span data-ttu-id="7628b-105">INapSystemHealthValidationRequest2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7628b-105">INapSystemHealthValidationRequest2 interface</span></span>

> [!Note]  
> <span data-ttu-id="7628b-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7628b-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7628b-107">Die **INapSystemHealthValidationRequest2** -Schnittstelle stellt Methoden bereit, die zur Unterstützung von Systemintegritäts-Validierungs Steuerelementen verwendet werden, die vom Anwendungsentwickler definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7628b-107">The **INapSystemHealthValidationRequest2** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="7628b-108">Diese Schnittstelle erbt alle Methoden von [**inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md) und sollte stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7628b-108">This interface inherits all the methods of [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="7628b-109">Member</span><span class="sxs-lookup"><span data-stu-id="7628b-109">Members</span></span>

<span data-ttu-id="7628b-110">Die **INapSystemHealthValidationRequest2** -Schnittstelle erbt von [**inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md).</span><span class="sxs-lookup"><span data-stu-id="7628b-110">The **INapSystemHealthValidationRequest2** interface inherits from [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).</span></span> <span data-ttu-id="7628b-111">**INapSystemHealthValidationRequest2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7628b-111">**INapSystemHealthValidationRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="7628b-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="7628b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7628b-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="7628b-113">Methods</span></span>

<span data-ttu-id="7628b-114">Die **INapSystemHealthValidationRequest2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7628b-114">The **INapSystemHealthValidationRequest2** interface has these methods.</span></span>



| <span data-ttu-id="7628b-115">Methode</span><span class="sxs-lookup"><span data-stu-id="7628b-115">Method</span></span>                                                                                                    | <span data-ttu-id="7628b-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7628b-116">Description</span></span>                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="7628b-117">**INapSystemHealthValidationRequest2:: getconfigid**</span><span class="sxs-lookup"><span data-stu-id="7628b-117">**INapSystemHealthValidationRequest2::GetConfigId**</span></span>](inapsystemhealthvalidationrequest2-getconfigid.md) | <span data-ttu-id="7628b-118">Ruft die Konfigurations-ID in einer Validierungs Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="7628b-118">Retrieves the configuration id in a validation request.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7628b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7628b-119">Remarks</span></span>

<span data-ttu-id="7628b-120">Wenn ein SHV [**INapComponentConfig3**](inapcomponentconfig3.md)nicht unterstützt, wird diese Schnittstelle nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="7628b-120">If an SHV doesn t support [**INapComponentConfig3**](inapcomponentconfig3.md), this interface doesn t apply.</span></span>

## <a name="requirements"></a><span data-ttu-id="7628b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7628b-121">Requirements</span></span>



| <span data-ttu-id="7628b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7628b-122">Requirement</span></span> | <span data-ttu-id="7628b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7628b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7628b-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7628b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7628b-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7628b-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="7628b-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7628b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7628b-127">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7628b-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7628b-128">Header</span><span class="sxs-lookup"><span data-stu-id="7628b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7628b-129"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="7628b-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="7628b-130">IDL</span><span class="sxs-lookup"><span data-stu-id="7628b-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7628b-131"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7628b-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="7628b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7628b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7628b-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7628b-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="7628b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7628b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7628b-135">**Inapsystemhealthvalidationrequest**</span><span class="sxs-lookup"><span data-stu-id="7628b-135">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[<span data-ttu-id="7628b-136">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7628b-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="7628b-137">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="7628b-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





