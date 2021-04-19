---
title: INapComponentConfig3-Schnittstelle (napcommon. h)
description: Stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit, um Konfigurationsdaten für eine bestimmte Konfigurations-ID festzulegen und zu ändern.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- INapComponentConfig3-Schnittstelle NAP
- INapComponentConfig3 Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0cfead891da106a1a950ba83b9108b5950a738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341360"
---
# <a name="inapcomponentconfig3-interface"></a><span data-ttu-id="6873a-105">INapComponentConfig3-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6873a-105">INapComponentConfig3 interface</span></span>

> [!Note]  
> <span data-ttu-id="6873a-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6873a-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6873a-107">Die **INapComponentConfig3** -Schnittstelle stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit, um Konfigurationsdaten für eine bestimmte Konfigurations-ID festzulegen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6873a-107">The **INapComponentConfig3** interface provides NAP system configuration methods for system health validators (SHVs) to set and modify configuration data for a specific configuration ID.</span></span>

> [!Note]  
> <span data-ttu-id="6873a-108">Diese Schnittstelle erbt alle Methoden von [**INapComponentConfig2**](inapcomponentconfig2.md) und sollte stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6873a-108">This interface inherits all the methods of [**INapComponentConfig2**](inapcomponentconfig2.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="6873a-109">Member</span><span class="sxs-lookup"><span data-stu-id="6873a-109">Members</span></span>

<span data-ttu-id="6873a-110">Die **INapComponentConfig3** -Schnittstelle erbt von [**INapComponentConfig2**](inapcomponentconfig2.md).</span><span class="sxs-lookup"><span data-stu-id="6873a-110">The **INapComponentConfig3** interface inherits from [**INapComponentConfig2**](inapcomponentconfig2.md).</span></span> <span data-ttu-id="6873a-111">**INapComponentConfig3** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6873a-111">**INapComponentConfig3** also has these types of members:</span></span>

-   [<span data-ttu-id="6873a-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="6873a-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6873a-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="6873a-113">Methods</span></span>

<span data-ttu-id="6873a-114">Die **INapComponentConfig3** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6873a-114">The **INapComponentConfig3** interface has these methods.</span></span>



| <span data-ttu-id="6873a-115">Methode</span><span class="sxs-lookup"><span data-stu-id="6873a-115">Method</span></span>                                                                                | <span data-ttu-id="6873a-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6873a-116">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6873a-117">**INapComponentConfig3::D eleteallconfig**</span><span class="sxs-lookup"><span data-stu-id="6873a-117">**INapComponentConfig3::DeleteAllConfig**</span></span>](inapcomponentconfig3-deleteallconfig.md) | <span data-ttu-id="6873a-118">Wird von SHVs implementiert und bietet eine Möglichkeit, den SHV-Speicher nach dem Setup in seinen ursprünglichen Zustand zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="6873a-118">Implemented by SHVs to provide a way to reset the SHV store to its original state after setup.</span></span><br/>      |
| [<span data-ttu-id="6873a-119">**INapComponentConfig3::D eleteconfig**</span><span class="sxs-lookup"><span data-stu-id="6873a-119">**INapComponentConfig3::DeleteConfig**</span></span>](inapcomponentconfig3-deleteconfig.md)       | <span data-ttu-id="6873a-120">Wird von SHVs implementiert, um eine Möglichkeit zum Löschen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.</span><span class="sxs-lookup"><span data-stu-id="6873a-120">Implemented by SHVs to provide a way to delete configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="6873a-121">**INapComponentConfig3:: getconfigfromid**</span><span class="sxs-lookup"><span data-stu-id="6873a-121">**INapComponentConfig3::GetConfigFromID**</span></span>](inapcomponentconfig3-getconfigfromid.md) | <span data-ttu-id="6873a-122">Wird von SHVs implementiert, um eine Möglichkeit zum Abrufen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.</span><span class="sxs-lookup"><span data-stu-id="6873a-122">Implemented by SHVs to provide a way to obtain configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="6873a-123">**INapComponentConfig3:: newconfig**</span><span class="sxs-lookup"><span data-stu-id="6873a-123">**INapComponentConfig3::NewConfig**</span></span>](inapcomponentconfig3-newconfig.md)             | <span data-ttu-id="6873a-124">Wird von SHVs implementiert, um eine Möglichkeit zum Erstellen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.</span><span class="sxs-lookup"><span data-stu-id="6873a-124">Implemented by SHVs to provide a way to create configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="6873a-125">**INapComponentConfig3:: setconfigtoid**</span><span class="sxs-lookup"><span data-stu-id="6873a-125">**INapComponentConfig3::SetConfigToID**</span></span>](inapcomponentconfig3-setconfigtoid.md)     | <span data-ttu-id="6873a-126">Wird von SHVs implementiert und bietet eine Möglichkeit, die Konfigurationsdaten für eine bestimmte Konfigurations-ID festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6873a-126">Implemented by SHVs to provide a way to set the configuration data for a specific configuration ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6873a-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6873a-127">Remarks</span></span>

<span data-ttu-id="6873a-128">Diese Schnittstelle sollte nicht von Systemintegritäts-Agents (SHAs) oder Quarantäne Erzwingungs Clients (qecs) implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="6873a-128">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="6873a-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6873a-129">Requirements</span></span>



| <span data-ttu-id="6873a-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6873a-130">Requirement</span></span> | <span data-ttu-id="6873a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6873a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6873a-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6873a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6873a-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6873a-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6873a-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6873a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6873a-135">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6873a-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6873a-136">Header</span><span class="sxs-lookup"><span data-stu-id="6873a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6873a-137"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6873a-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="6873a-138">IDL</span><span class="sxs-lookup"><span data-stu-id="6873a-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6873a-139"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6873a-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6873a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6873a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6873a-141">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="6873a-141">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> <dt>

[<span data-ttu-id="6873a-142">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6873a-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6873a-143">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="6873a-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





