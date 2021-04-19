---
description: Ändert die Ressourcen Einstellungen für einen virtuellen Switch.
ms.assetid: 1ae2456f-921c-4ea6-b3fb-7065110063fb
title: Modifyresourcesettings-Methode der Msvm_VirtualEthernetSwitchManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f40044b20389914281ad4f651019f3e8dc6b6148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373197"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="d1a38-103">Modifyresourcesettings-Methode der MSVM \_ virtualethernetzwitchmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="d1a38-103">ModifyResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="d1a38-104">Ändert die Ressourcen Einstellungen für einen virtuellen Switch.</span><span class="sxs-lookup"><span data-stu-id="d1a38-104">Modifies resource settings for a virtual switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1a38-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1a38-105">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d1a38-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1a38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1a38-107">*Resourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1a38-107">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1a38-108">Ein Array von Zeichen folgen, die eine eingebettete Instanz einer von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)abgeleiteten Klasse enthalten, die die geänderten Aspekte vorhandener virtueller Ressourcen enthält.</span><span class="sxs-lookup"><span data-stu-id="d1a38-108">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="d1a38-109">Die **InstanceId-** Eigenschaft der einzelnen Instanzen identifiziert die zu ändernde virtuelle Ressourcen Einstellung.</span><span class="sxs-lookup"><span data-stu-id="d1a38-109">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="d1a38-110">*Resultingresourcesettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d1a38-110">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1a38-111">Ein Array von Verweisen auf Instanzen von Objekten, die von [**CIM \_ resourcezucationsettingdata abgeleitet werden**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) und die virtuellen Aspekte der geänderten virtuellen Ressourcen darstellen.</span><span class="sxs-lookup"><span data-stu-id="d1a38-111">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="d1a38-112">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d1a38-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1a38-113">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="d1a38-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1a38-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1a38-114">Return value</span></span>

<span data-ttu-id="d1a38-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="d1a38-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d1a38-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="d1a38-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d1a38-117">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="d1a38-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d1a38-118">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="d1a38-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d1a38-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="d1a38-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d1a38-120">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="d1a38-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d1a38-121">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="d1a38-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d1a38-122">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="d1a38-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d1a38-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="d1a38-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d1a38-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="d1a38-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d1a38-125">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="d1a38-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d1a38-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="d1a38-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d1a38-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1a38-127">Requirements</span></span>



| <span data-ttu-id="d1a38-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1a38-128">Requirement</span></span> | <span data-ttu-id="d1a38-129">Wert</span><span class="sxs-lookup"><span data-stu-id="d1a38-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a38-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1a38-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d1a38-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1a38-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d1a38-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1a38-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d1a38-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1a38-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1a38-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1a38-134">Namespace</span></span><br/>                | <span data-ttu-id="d1a38-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d1a38-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d1a38-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d1a38-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1a38-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d1a38-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1a38-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d1a38-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1a38-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1a38-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d1a38-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1a38-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a38-141">**Adresssourcesettings**</span><span class="sxs-lookup"><span data-stu-id="d1a38-141">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="d1a38-142">**Removeresourcesettings**</span><span class="sxs-lookup"><span data-stu-id="d1a38-142">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="d1a38-143">**MSVM \_ virtualethernetzwitchmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="d1a38-143">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

