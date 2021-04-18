---
description: Fügt der Konfiguration eines virtuellen Systems Ressourcen hinzu.
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: Adresssourcesettings-Methode der CIM_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9563b1e8421dfa6724971450b117780435f6f39e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347100"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="498e8-103">Adresssourcesettings-Methode der CIM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="498e8-103">AddResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="498e8-104">Fügt der Konfiguration eines virtuellen Systems Ressourcen hinzu.</span><span class="sxs-lookup"><span data-stu-id="498e8-104">Adds resources to a virtual system configuration.</span></span>

<span data-ttu-id="498e8-105">Wenn Sie auf eine virtuelle Systemkonfiguration vom Typ "State" angewendet werden, werden dem aktiven virtuellen System als Nebeneffekte Ressourcen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="498e8-105">When applied to a "state" virtual system configuration, as a side effect resources are added to the active virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="498e8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="498e8-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="498e8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="498e8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="498e8-108">*Affectedconfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="498e8-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="498e8-109">Ein [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Verweis auf die betroffene virtuelle Systemkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="498e8-109">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="498e8-110">*Resourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="498e8-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="498e8-111">Ein Array von Zeichen folgen, die jeweils eine eingebettete Instanz der Klasse [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) enthalten, die die virtuellen Aspekte einer virtuellen Ressource beschreibt, die dem virtuellen System hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="498e8-111">Array of strings each containing one embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be added to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="498e8-112">*Resultingresourcesettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="498e8-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="498e8-113">Array von Verweisen auf Instanzen der Klasse [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) , die virtuelle Aspekte der hinzugefügten virtuellen Ressourcen darstellen.</span><span class="sxs-lookup"><span data-stu-id="498e8-113">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="498e8-114">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="498e8-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="498e8-115">Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="498e8-115">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="498e8-116">In diesem Fall sind die Instanzen der Klasse " [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) ", die die hinzugefügten Ressourcen Einstellungen darstellen, über die "Association CIM"- **\_ Komponente** aus der Instanz der Klasse " [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) " verfügbar, die die betroffene virtuelle Systemkonfiguration darstellt.</span><span class="sxs-lookup"><span data-stu-id="498e8-116">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the added resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="498e8-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="498e8-117">Return value</span></span>

<span data-ttu-id="498e8-118">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="498e8-118">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="498e8-119">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="498e8-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="498e8-120">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="498e8-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="498e8-121">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="498e8-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="498e8-122">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="498e8-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="498e8-123">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="498e8-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="498e8-124">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="498e8-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="498e8-125">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="498e8-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="498e8-126">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="498e8-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="498e8-127">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="498e8-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="498e8-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="498e8-128">Requirements</span></span>



| <span data-ttu-id="498e8-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="498e8-129">Requirement</span></span> | <span data-ttu-id="498e8-130">Wert</span><span class="sxs-lookup"><span data-stu-id="498e8-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="498e8-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="498e8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="498e8-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="498e8-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="498e8-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="498e8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="498e8-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="498e8-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="498e8-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="498e8-135">Namespace</span></span><br/>                | <span data-ttu-id="498e8-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="498e8-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="498e8-137">MOF</span><span class="sxs-lookup"><span data-stu-id="498e8-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="498e8-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="498e8-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="498e8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="498e8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="498e8-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="498e8-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="498e8-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="498e8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="498e8-142">**CIM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="498e8-142">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




