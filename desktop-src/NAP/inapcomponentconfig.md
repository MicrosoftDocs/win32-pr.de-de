---
title: Inapcomponentconfig-Schnittstelle (napcommon. h)
description: Stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit.
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- Inapcomponentconfig-Schnittstelle NAP
- Inapcomponentconfig-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapComponentConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a13ae74ba1de79803ff4a2d3716eec7fe934a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391778"
---
# <a name="inapcomponentconfig-interface"></a><span data-ttu-id="60ecd-105">Inapcomponentconfig-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="60ecd-105">INapComponentConfig interface</span></span>

> [!Note]  
> <span data-ttu-id="60ecd-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60ecd-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="60ecd-107">Die **inapcomponentconfig** -Schnittstelle stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit.</span><span class="sxs-lookup"><span data-stu-id="60ecd-107">The **INapComponentConfig** interface provides NAP system configuration methods for system health validators (SHVs).</span></span>

> [!Note]  
> <span data-ttu-id="60ecd-108">[**INapComponentConfig2**](inapcomponentconfig2.md) und [**INapComponentConfig3**](inapcomponentconfig3.md) erben alle Methoden dieser Schnittstelle und sollten stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60ecd-108">[**INapComponentConfig2**](inapcomponentconfig2.md) and [**INapComponentConfig3**](inapcomponentconfig3.md) inherit all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="60ecd-109">Member</span><span class="sxs-lookup"><span data-stu-id="60ecd-109">Members</span></span>

<span data-ttu-id="60ecd-110">Die **inapcomponentconfig** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="60ecd-110">The **INapComponentConfig** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="60ecd-111">**Inapcomponentconfig** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="60ecd-111">**INapComponentConfig** also has these types of members:</span></span>

-   [<span data-ttu-id="60ecd-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="60ecd-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="60ecd-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="60ecd-113">Methods</span></span>

<span data-ttu-id="60ecd-114">Die **inapcomponentconfig** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="60ecd-114">The **INapComponentConfig** interface has these methods.</span></span>



| <span data-ttu-id="60ecd-115">Methode</span><span class="sxs-lookup"><span data-stu-id="60ecd-115">Method</span></span>                                                                          | <span data-ttu-id="60ecd-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60ecd-116">Description</span></span>                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="60ecd-117">**Inapcomponentconfig:: GetConfig**</span><span class="sxs-lookup"><span data-stu-id="60ecd-117">**INapComponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)         | <span data-ttu-id="60ecd-118">Ruft die Konfiguration der SHV-Komponente ab.</span><span class="sxs-lookup"><span data-stu-id="60ecd-118">Retrieves the SHV component configuration.</span></span><br/>                                |
| [<span data-ttu-id="60ecd-119">**Inapcomponentconfig:: invokeui**</span><span class="sxs-lookup"><span data-stu-id="60ecd-119">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)           | <span data-ttu-id="60ecd-120">Hiermit wird die angepasste Benutzeroberfläche für eine SHV-Komponente gestartet.</span><span class="sxs-lookup"><span data-stu-id="60ecd-120">Launches the customized user interface for an SHV component.</span></span><br/>              |
| [<span data-ttu-id="60ecd-121">**Inapcomponentconfig:: isuisupported**</span><span class="sxs-lookup"><span data-stu-id="60ecd-121">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md) | <span data-ttu-id="60ecd-122">Gibt an, ob die SHV-Komponente eine angepasste Benutzeroberfläche unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60ecd-122">Specifies whether the SHV component supports a customized user interface.</span></span><br/> |
| [<span data-ttu-id="60ecd-123">**Inapcomponentconfig:: setconfig**</span><span class="sxs-lookup"><span data-stu-id="60ecd-123">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)         | <span data-ttu-id="60ecd-124">Legt die Konfiguration der SHV-Komponente fest.</span><span class="sxs-lookup"><span data-stu-id="60ecd-124">Sets the SHV component configuration.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="60ecd-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60ecd-125">Remarks</span></span>

<span data-ttu-id="60ecd-126">Diese Schnittstelle sollte nicht von Systemintegritäts-Agents (SHAs) oder Quarantäne Erzwingungs Clients (qecs) implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="60ecd-126">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="60ecd-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60ecd-127">Requirements</span></span>



| <span data-ttu-id="60ecd-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60ecd-128">Requirement</span></span> | <span data-ttu-id="60ecd-129">Wert</span><span class="sxs-lookup"><span data-stu-id="60ecd-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60ecd-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60ecd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="60ecd-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="60ecd-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="60ecd-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60ecd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="60ecd-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60ecd-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="60ecd-134">Header</span><span class="sxs-lookup"><span data-stu-id="60ecd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="60ecd-135"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="60ecd-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="60ecd-136">IDL</span><span class="sxs-lookup"><span data-stu-id="60ecd-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60ecd-137"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60ecd-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60ecd-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60ecd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ecd-139">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="60ecd-139">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="60ecd-140">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="60ecd-140">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

