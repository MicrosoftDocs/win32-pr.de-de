---
description: Ändert die Einstellungen der virtuellen Ressource.
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: Modifyresourcesettings-Methode der CIM_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e27729429d02c2412e05344779cc40461dbd9dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485363"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="8a2e5-103">Modifyresourcesettings-Methode der CIM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="8a2e5-103">ModifyResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="8a2e5-104">Ändert die Einstellungen der virtuellen Ressource.</span><span class="sxs-lookup"><span data-stu-id="8a2e5-104">Modifies virtual resource settings.</span></span>

<span data-ttu-id="8a2e5-105">Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, können die Ressourcen des aktiven virtuellen Systems ggf. geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8a2e5-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a2e5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a2e5-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8a2e5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a2e5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a2e5-108">*Resourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a2e5-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a2e5-109">Ein Array von Zeichen folgen, die jeweils eine eingebettete Instanz der Klasse [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) enthalten, die Änderungen an den virtuellen Aspekten einer vorhandenen virtuellen Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8a2e5-109">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes modifications to the virtual aspects of an existing virtual resource.</span></span> <span data-ttu-id="8a2e5-110">Alle Instanzen müssen über eine gültige **InstanceId** verfügen, um die zu ändernde virtuelle Ressourcen Einstellung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8a2e5-110">All instances must have a valid **InstanceID** in order to identify the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="8a2e5-111">*Resultingresourcesettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8a2e5-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a2e5-112">Array von Verweisen auf Instanzen der Klasse [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) , die virtuelle Aspekte der geänderten virtuellen Ressourcen darstellen.</span><span class="sxs-lookup"><span data-stu-id="8a2e5-112">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="8a2e5-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8a2e5-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a2e5-114">Wenn der Vorgang lange ausgeführt wird, wird optional ein Auftrag zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8a2e5-114">If the operation is long running, then optionally a job be returned.</span></span> <span data-ttu-id="8a2e5-115">In diesem Fall sind die Instanzen der Klasse " [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) ", die die geänderten Ressourcen Einstellungen darstellen, über Association CIM "Configuration Manager" aus der Instanz der Klasse " [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) " verfügbar, die die betroffene virtuelle Systemkonfiguration darstellt. **\_**</span><span class="sxs-lookup"><span data-stu-id="8a2e5-115">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the modified resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a2e5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a2e5-116">Return value</span></span>

<span data-ttu-id="8a2e5-117">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8a2e5-117">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8a2e5-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="8a2e5-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8a2e5-119">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="8a2e5-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8a2e5-120">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="8a2e5-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8a2e5-121">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="8a2e5-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8a2e5-122">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="8a2e5-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8a2e5-123">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="8a2e5-123">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8a2e5-124">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="8a2e5-124">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8a2e5-125">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="8a2e5-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8a2e5-126">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="8a2e5-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8a2e5-127">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="8a2e5-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8a2e5-128">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="8a2e5-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8a2e5-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a2e5-129">Requirements</span></span>



| <span data-ttu-id="8a2e5-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a2e5-130">Requirement</span></span> | <span data-ttu-id="8a2e5-131">Wert</span><span class="sxs-lookup"><span data-stu-id="8a2e5-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a2e5-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a2e5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8a2e5-133">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8a2e5-133">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8a2e5-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a2e5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8a2e5-135">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8a2e5-135">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8a2e5-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a2e5-136">Namespace</span></span><br/>                | <span data-ttu-id="8a2e5-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8a2e5-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8a2e5-138">MOF</span><span class="sxs-lookup"><span data-stu-id="8a2e5-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a2e5-139"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8a2e5-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a2e5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="8a2e5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a2e5-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a2e5-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8a2e5-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a2e5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a2e5-143">**CIM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="8a2e5-143">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




