---
description: Fügt der Konfiguration einer virtuellen Maschine Ressourcen hinzu.
ms.assetid: e2878b60-dc8c-48fb-b163-29457a96d130
title: Adresssourcesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b35379e0fe3925bbf0f7c4d753f77d1d207199b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865224"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="7875b-103">Adresssourcesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="7875b-103">AddResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="7875b-104">Fügt der Konfiguration einer virtuellen Maschine Ressourcen hinzu.</span><span class="sxs-lookup"><span data-stu-id="7875b-104">Adds resources to a virtual machine configuration.</span></span> <span data-ttu-id="7875b-105">Wenn Sie auf eine VM-Konfiguration mit dem Status "State" angewendet werden, werden dem aktiven virtuellen Computerressourcen als Nebeneffekte hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7875b-105">When applied to a "state" virtual machine configuration, as a side effect, resources are added to the active virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="7875b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7875b-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7875b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7875b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7875b-108">*Affectedconfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7875b-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7875b-109">Ein Verweis auf ein [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Objekt, das die betroffene Konfiguration der virtuellen Maschine darstellt.</span><span class="sxs-lookup"><span data-stu-id="7875b-109">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the affected virtual machine configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7875b-110">*Resourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7875b-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7875b-111">Ein Array von Zeichen folgen, das eine eingebettete Instanz der [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Klasse enthält, die die virtuellen Aspekte einer virtuellen Ressource beschreibt, die der virtuellen Maschine hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7875b-111">An array of strings that contain one embedded instance of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that describes the virtual aspects of a virtual resource to be added to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="7875b-112">*Resultingresourcesettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7875b-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7875b-113">Ein Array von Verweisen auf Instanzen der [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Klasse, die virtuelle Aspekte der hinzugefügten virtuellen Ressourcen darstellt.</span><span class="sxs-lookup"><span data-stu-id="7875b-113">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that represents virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="7875b-114">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7875b-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7875b-115">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="7875b-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7875b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7875b-116">Return value</span></span>

<span data-ttu-id="7875b-117">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="7875b-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7875b-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="7875b-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7875b-119">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="7875b-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7875b-120">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="7875b-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7875b-121">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="7875b-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7875b-122">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="7875b-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7875b-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="7875b-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7875b-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="7875b-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7875b-125">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="7875b-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7875b-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="7875b-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7875b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7875b-127">Requirements</span></span>



| <span data-ttu-id="7875b-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7875b-128">Requirement</span></span> | <span data-ttu-id="7875b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7875b-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7875b-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7875b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7875b-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7875b-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7875b-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7875b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7875b-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7875b-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7875b-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="7875b-134">Namespace</span></span><br/>                | <span data-ttu-id="7875b-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7875b-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7875b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="7875b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7875b-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7875b-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7875b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7875b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7875b-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7875b-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7875b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7875b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7875b-141">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="7875b-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

