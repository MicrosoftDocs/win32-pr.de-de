---
description: Fügt der Konfiguration eines virtuellen Systems generische Einstellungen hinzu.
ms.assetid: ae04be39-0401-43e9-b19b-3539ca1786ec
title: Addsystemcomponentsettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56ca8bed752bab52f6a82e18975dd5df72dbe12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344665"
---
# <a name="addsystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="3e4eb-103">Addsystemcomponentsettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="3e4eb-103">AddSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="3e4eb-104">Fügt der Konfiguration eines virtuellen Systems generische Einstellungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-104">Adds generic settings to a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e4eb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e4eb-105">Syntax</span></span>


```mof
uint32 AddSystemComponentSettings(
  [in]  Msvm_VirtualSystemSettingData   REF AffectedConfiguration,
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3e4eb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e4eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e4eb-107">*Affectedconfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e4eb-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="3e4eb-108">*Componentsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e4eb-108">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4eb-109">Die hinzu zufügenden Komponenten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-109">The component settings to add.</span></span>

</dd> <dt>

<span data-ttu-id="3e4eb-110">*Resultingcomponentsettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3e4eb-110">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4eb-111">Bei Erfolg verweist auf ein [**MSVM \_ systemcomponentsettingdata**](msvm-systemcomponentsettingdata.md) -Element, das die resultierenden Komponenten Einstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-111">On success, references a [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that contains the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="3e4eb-112">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3e4eb-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4eb-113">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e4eb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e4eb-114">Return value</span></span>

<span data-ttu-id="3e4eb-115">Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-115">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="3e4eb-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3e4eb-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3e4eb-117">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="3e4eb-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3e4eb-118">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="3e4eb-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3e4eb-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="3e4eb-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3e4eb-120">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="3e4eb-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3e4eb-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="3e4eb-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3e4eb-122">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="3e4eb-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3e4eb-123">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="3e4eb-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3e4eb-124">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="3e4eb-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3e4eb-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e4eb-125">Requirements</span></span>



| <span data-ttu-id="3e4eb-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e4eb-126">Requirement</span></span> | <span data-ttu-id="3e4eb-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3e4eb-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e4eb-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e4eb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3e4eb-129">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e4eb-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3e4eb-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e4eb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3e4eb-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3e4eb-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3e4eb-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e4eb-132">Namespace</span></span><br/>                | <span data-ttu-id="3e4eb-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3e4eb-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3e4eb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3e4eb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e4eb-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3e4eb-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e4eb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3e4eb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e4eb-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e4eb-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3e4eb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e4eb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e4eb-139">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="3e4eb-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

