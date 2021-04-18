---
title: INapComponentConfig2-Schnittstelle (napcommon. h)
description: Stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit, um eine Netzwerk Richtlinien Server-Benutzeroberfläche (NPS) Remote zu konfigurieren.
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- INapComponentConfig2-Schnittstelle NAP
- INapComponentConfig2 Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapComponentConfig2
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bd6fbea7696d0e4d5eacefd028ce7d33e549e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338329"
---
# <a name="inapcomponentconfig2-interface"></a><span data-ttu-id="79eea-105">INapComponentConfig2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="79eea-105">INapComponentConfig2 interface</span></span>

> [!Note]  
> <span data-ttu-id="79eea-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="79eea-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="79eea-107">Die **INapComponentConfig2** -Schnittstelle stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit, um eine Netzwerk Richtlinien Server-Benutzeroberfläche (NPS) Remote zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="79eea-107">The **INapComponentConfig2** interface provides NAP system configuration methods for system health validators (SHVs) to configure a network policy server (NPS) user interface remotely.</span></span>

> [!Note]  
> <span data-ttu-id="79eea-108">Diese Schnittstelle erbt alle Methoden von [**inapcomponentconfig**](inapcomponentconfig.md) und sollte stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79eea-108">This interface inherits all the methods of [**INapComponentConfig**](inapcomponentconfig.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="79eea-109">Member</span><span class="sxs-lookup"><span data-stu-id="79eea-109">Members</span></span>

<span data-ttu-id="79eea-110">Die **INapComponentConfig2** -Schnittstelle erbt von [**inapcomponentconfig**](inapcomponentconfig.md).</span><span class="sxs-lookup"><span data-stu-id="79eea-110">The **INapComponentConfig2** interface inherits from [**INapComponentConfig**](inapcomponentconfig.md).</span></span> <span data-ttu-id="79eea-111">**INapComponentConfig2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="79eea-111">**INapComponentConfig2** also has these types of members:</span></span>

-   [<span data-ttu-id="79eea-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="79eea-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="79eea-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="79eea-113">Methods</span></span>

<span data-ttu-id="79eea-114">Die **INapComponentConfig2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="79eea-114">The **INapComponentConfig2** interface has these methods.</span></span>



| <span data-ttu-id="79eea-115">Methode</span><span class="sxs-lookup"><span data-stu-id="79eea-115">Method</span></span>                                                                                                | <span data-ttu-id="79eea-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79eea-116">Description</span></span>                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79eea-117">**INapComponentConfig2:: invokeuiformachine**</span><span class="sxs-lookup"><span data-stu-id="79eea-117">**INapComponentConfig2::InvokeUIForMachine**</span></span>](inapcomponentconfig2-invokeuiformachine.md)           | <span data-ttu-id="79eea-118">Wird von SHVs nach Bedarf implementiert, um die Remote Konfiguration direkt auf dem angegebenen Computer zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="79eea-118">Implemented by SHVs as needed to manage remote configuration directly on the machine specified.</span></span><br/>                                                                 |
| [<span data-ttu-id="79eea-119">**INapComponentConfig2:: invokeuifromconfigblob**</span><span class="sxs-lookup"><span data-stu-id="79eea-119">**INapComponentConfig2::InvokeUIFromConfigBlob**</span></span>](inapcomponentconfig2-invokeuifromconfigblob.md)   | <span data-ttu-id="79eea-120">Wird von SHVs nach Bedarf implementiert, um die Konfiguration des Remote Computers in den Arbeitsspeicher zu laden und eine Benutzeroberfläche anzuzeigen, die die Bearbeitung der Konfigurationsdaten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="79eea-120">Implemented by SHVs as needed to load the configuration of the remote machine in memory and to display a UI that allows manipulation of the configuration data.</span></span><br/> |
| [<span data-ttu-id="79eea-121">**INapComponentConfig2:: isremoteconfigsupported**</span><span class="sxs-lookup"><span data-stu-id="79eea-121">**INapComponentConfig2::IsRemoteConfigSupported**</span></span>](inapcomponentconfig2-isremoteconfigsupported.md) | <span data-ttu-id="79eea-122">Wird von SHVs implementiert, um anzugeben, ob die Remote Konfiguration unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="79eea-122">Implemented by SHVs to indicate whether remote configuration is supported.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="79eea-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79eea-123">Remarks</span></span>

<span data-ttu-id="79eea-124">Diese Schnittstelle sollte nicht von Systemintegritäts-Agents (SHAs) oder Quarantäne Erzwingungs Clients (qecs) implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="79eea-124">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="79eea-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79eea-125">Requirements</span></span>



| <span data-ttu-id="79eea-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79eea-126">Requirement</span></span> | <span data-ttu-id="79eea-127">Wert</span><span class="sxs-lookup"><span data-stu-id="79eea-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="79eea-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79eea-128">Minimum supported client</span></span><br/> | <span data-ttu-id="79eea-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="79eea-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="79eea-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79eea-130">Minimum supported server</span></span><br/> | <span data-ttu-id="79eea-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79eea-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="79eea-132">Header</span><span class="sxs-lookup"><span data-stu-id="79eea-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="79eea-133"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="79eea-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="79eea-134">IDL</span><span class="sxs-lookup"><span data-stu-id="79eea-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79eea-135"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79eea-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79eea-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79eea-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79eea-137">**Inapcomponentconfig**</span><span class="sxs-lookup"><span data-stu-id="79eea-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="79eea-138">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="79eea-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="79eea-139">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="79eea-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





