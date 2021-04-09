---
description: Ändert die Einstellungen der virtuellen Ressource.
ms.assetid: 3fb2a65f-9f40-4eb9-99e8-8fe1451427d9
title: Modifyresourcesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 872e81926f717671b741a89c9bf954e452803b36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867063"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="001a7-103">Modifyresourcesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="001a7-103">ModifyResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="001a7-104">Ändert die Einstellungen der virtuellen Ressource.</span><span class="sxs-lookup"><span data-stu-id="001a7-104">Modifies virtual resource settings.</span></span> <span data-ttu-id="001a7-105">Wenn Sie auf Teile einer aktuellen VM-Konfiguration angewendet werden, können die Ressourcen der aktiven virtuellen Maschine als Nebeneffekt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="001a7-105">When applied to parts of a current virtual machine configuration, as a side effect, the resources of the active virtual machine may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="001a7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="001a7-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="001a7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="001a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="001a7-108">*Resourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="001a7-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="001a7-109">Ein Array von Zeichen folgen, die eine eingebettete Instanz einer von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)abgeleiteten Klasse enthalten, die die geänderten Aspekte vorhandener virtueller Ressourcen enthält.</span><span class="sxs-lookup"><span data-stu-id="001a7-109">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="001a7-110">Die **InstanceId-** Eigenschaft der einzelnen Instanzen identifiziert die zu ändernde virtuelle Ressourcen Einstellung.</span><span class="sxs-lookup"><span data-stu-id="001a7-110">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="001a7-111">*Resultingresourcesettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="001a7-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="001a7-112">Ein Array von Verweisen auf Instanzen von Objekten, die von [**CIM \_ resourcezucationsettingdata abgeleitet werden**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) und die virtuellen Aspekte der geänderten virtuellen Ressourcen darstellen.</span><span class="sxs-lookup"><span data-stu-id="001a7-112">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="001a7-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="001a7-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="001a7-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="001a7-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="001a7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="001a7-115">Return value</span></span>

<span data-ttu-id="001a7-116">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="001a7-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="001a7-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="001a7-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="001a7-118">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="001a7-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="001a7-119">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="001a7-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="001a7-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="001a7-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="001a7-121">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="001a7-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="001a7-122">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="001a7-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="001a7-123">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="001a7-123">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="001a7-124">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="001a7-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="001a7-125">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="001a7-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="001a7-126">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="001a7-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="001a7-127">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="001a7-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="001a7-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="001a7-128">Requirements</span></span>



| <span data-ttu-id="001a7-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="001a7-129">Requirement</span></span> | <span data-ttu-id="001a7-130">Wert</span><span class="sxs-lookup"><span data-stu-id="001a7-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="001a7-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="001a7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="001a7-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="001a7-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="001a7-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="001a7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="001a7-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="001a7-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="001a7-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="001a7-135">Namespace</span></span><br/>                | <span data-ttu-id="001a7-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="001a7-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="001a7-137">MOF</span><span class="sxs-lookup"><span data-stu-id="001a7-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="001a7-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="001a7-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="001a7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="001a7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="001a7-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="001a7-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="001a7-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="001a7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="001a7-142">**Modifyvirtualsystemresources (v1)**</span><span class="sxs-lookup"><span data-stu-id="001a7-142">**ModifyVirtualSystemResources (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="001a7-143">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="001a7-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

