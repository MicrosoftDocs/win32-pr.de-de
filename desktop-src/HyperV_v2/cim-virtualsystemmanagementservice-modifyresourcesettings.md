---
description: 'ModifyResourceSettings-Methode der CIM_VirtualSystemManagementService Klasse: Ändert einstellungen für virtuelle Ressourcen.'
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: ModifyResourceSettings-Methode der CIM_VirtualSystemManagementService Klasse
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
ms.openlocfilehash: 26971c80ce6f7d0ffcdcef069d76aef5fdc15138
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112288"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="b5d28-103">ModifyResourceSettings-Methode der CIM \_ VirtualSystemManagementService-Klasse</span><span class="sxs-lookup"><span data-stu-id="b5d28-103">ModifyResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="b5d28-104">Ändert die Einstellungen für virtuelle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b5d28-104">Modifies virtual resource settings.</span></span>

<span data-ttu-id="b5d28-105">Wenn sie auf Teile einer "aktuellen" Konfiguration des virtuellen Systems angewendet werden, können Als Nebeneffekt Ressourcen des aktiven virtuellen Systems geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b5d28-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d28-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5d28-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b5d28-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5d28-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5d28-108">*ResourceSettings* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b5d28-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d28-109">Array von Zeichenfolgen, die jeweils eine eingebettete Instanz der [**Klasse CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) enthalten, die Änderungen an den virtuellen Aspekten einer vorhandenen virtuellen Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b5d28-109">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes modifications to the virtual aspects of an existing virtual resource.</span></span> <span data-ttu-id="b5d28-110">Alle Instanzen müssen über eine gültige **InstanceID** verfügen, um die zu ändernde Einstellung der virtuellen Ressource zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b5d28-110">All instances must have a valid **InstanceID** in order to identify the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="b5d28-111">*ResultingResourceSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5d28-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d28-112">Array von Verweisen auf Instanzen der Klasse [**CIM \_ ResourceAllocationSettingData,**](cim-resourceallocationsettingdata.md) die virtuelle Aspekte der geänderten virtuellen Ressourcen darstellen.</span><span class="sxs-lookup"><span data-stu-id="b5d28-112">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="b5d28-113">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5d28-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d28-114">Wenn der Vorgang lange ausgeführt wird, wird optional ein Auftrag zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5d28-114">If the operation is long running, then optionally a job be returned.</span></span> <span data-ttu-id="b5d28-115">In diesem Fall sind die Instanzen der [**Klasse CIM \_ ResourceAllocationSettingData,**](cim-resourceallocationsettingdata.md) die die geänderten Ressourceneinstellungen darstellen, über die Zuordnung **CIM \_ ConreteComponent aus** der Instanz der Klasse CIM [**\_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) verfügbar, die die betroffene konfiguration des virtuellen Systems darstellt.</span><span class="sxs-lookup"><span data-stu-id="b5d28-115">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the modified resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5d28-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5d28-116">Return value</span></span>

<span data-ttu-id="b5d28-117">Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b5d28-117">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b5d28-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="b5d28-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b5d28-119">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="b5d28-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b5d28-120">**Fehler** (2)</span><span class="sxs-lookup"><span data-stu-id="b5d28-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b5d28-121">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="b5d28-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b5d28-122">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="b5d28-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b5d28-123">**Ungültiger Zustand** (5)</span><span class="sxs-lookup"><span data-stu-id="b5d28-123">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b5d28-124">**Inkompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="b5d28-124">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b5d28-125">**DMTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="b5d28-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b5d28-126">**Methodenparameter überprüft** – Auftrag gestartet (4096)</span><span class="sxs-lookup"><span data-stu-id="b5d28-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b5d28-127">**Reservierte Methode** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="b5d28-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b5d28-128">**Herstellerspezifisch** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="b5d28-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b5d28-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5d28-129">Requirements</span></span>



| <span data-ttu-id="b5d28-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5d28-130">Requirement</span></span> | <span data-ttu-id="b5d28-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b5d28-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d28-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5d28-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d28-133">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b5d28-133">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b5d28-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5d28-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d28-135">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b5d28-135">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b5d28-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5d28-136">Namespace</span></span><br/>                | <span data-ttu-id="b5d28-137">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b5d28-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b5d28-138">MOF</span><span class="sxs-lookup"><span data-stu-id="b5d28-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5d28-139"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5d28-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5d28-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b5d28-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5d28-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5d28-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5d28-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b5d28-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d28-143">**CIM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="b5d28-143">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




