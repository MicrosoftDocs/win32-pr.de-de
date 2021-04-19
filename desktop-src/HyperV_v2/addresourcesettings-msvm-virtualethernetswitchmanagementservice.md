---
description: Fügt einer Konfiguration des virtuellen Switches Ressourcen hinzu.
ms.assetid: aad5fac1-3884-4a95-abe3-bf192f23ea41
title: Adresssourcesettings-Methode der Msvm_VirtualEthernetSwitchManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: cc29376a03403949c57b831f40b2437ced30a51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349423"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="b8357-103">Adresssourcesettings-Methode der MSVM \_ virtualethernettwitchmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="b8357-103">AddResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="b8357-104">Fügt einer Konfiguration des virtuellen Switches Ressourcen hinzu.</span><span class="sxs-lookup"><span data-stu-id="b8357-104">Adds resources to a virtual switch configuration.</span></span> <span data-ttu-id="b8357-105">Wenn Sie auf eine VM-Konfiguration mit dem Status "State" angewendet werden, werden dem aktiven virtuellen Computer als Nebeneffekt Ressourcen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b8357-105">When applied to a "state" virtual machine configuration, as a side effect resources are added to the active virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8357-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8357-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b8357-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8357-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8357-108">*Affectedconfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8357-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8357-109">Ein Verweis auf ein [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Objekt, das die betroffene Konfiguration des virtuellen Switches darstellt.</span><span class="sxs-lookup"><span data-stu-id="b8357-109">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the affected virtual switch configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b8357-110">*Resourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8357-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8357-111">Ein Array von Zeichen folgen, das eine eingebettete Instanz der [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Klasse enthält, die die virtuellen Aspekte einer virtuellen Ressource beschreibt, die dem virtuellen Switch hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8357-111">An array of strings that contain one embedded instance of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that describes the virtual aspects of a virtual resource to be added to the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="b8357-112">*Resultingresourcesettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b8357-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8357-113">Ein Array von Verweisen auf Instanzen der [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Klasse, die virtuelle Aspekte der hinzugefügten virtuellen Ressourcen darstellt.</span><span class="sxs-lookup"><span data-stu-id="b8357-113">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that represents virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="b8357-114">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b8357-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8357-115">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="b8357-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8357-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8357-116">Return value</span></span>

<span data-ttu-id="b8357-117">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="b8357-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b8357-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="b8357-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b8357-119">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="b8357-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b8357-120">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="b8357-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b8357-121">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="b8357-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b8357-122">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="b8357-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b8357-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="b8357-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b8357-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="b8357-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b8357-125">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="b8357-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b8357-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="b8357-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b8357-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8357-127">Requirements</span></span>



| <span data-ttu-id="b8357-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8357-128">Requirement</span></span> | <span data-ttu-id="b8357-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b8357-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8357-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8357-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b8357-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8357-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b8357-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8357-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b8357-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8357-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8357-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8357-134">Namespace</span></span><br/>                | <span data-ttu-id="b8357-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b8357-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b8357-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b8357-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8357-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b8357-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8357-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b8357-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8357-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8357-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b8357-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8357-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8357-141">**Modifyresourcesettings**</span><span class="sxs-lookup"><span data-stu-id="b8357-141">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="b8357-142">**Removeresourcesettings**</span><span class="sxs-lookup"><span data-stu-id="b8357-142">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="b8357-143">**MSVM \_ virtualethernetzwitchmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="b8357-143">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

