---
description: Entfernt die Einstellungen virtueller Ressourcen aus einer Konfiguration des virtuellen Switches.
ms.assetid: 9992ebcd-8891-42ef-be7e-154f336e37f8
title: Removeresourcesettings-Methode der Msvm_VirtualEthernetSwitchManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9e82117b14ab9975b069e5b340ba9ec504ae65ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041807"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="da2c3-103">Removeresourcesettings-Methode der MSVM \_ virtualethernetzwitchmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="da2c3-103">RemoveResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="da2c3-104">Entfernt die Einstellungen virtueller Ressourcen aus einer Konfiguration des virtuellen Switches.</span><span class="sxs-lookup"><span data-stu-id="da2c3-104">Removes virtual resource settings from a virtual switch configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="da2c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da2c3-105">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="da2c3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da2c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da2c3-107">*Resourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da2c3-107">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da2c3-108">Ein Array von Verweisen auf Instanzen der [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Klasse, wobei jede Instanz die Einstellungen einer virtuellen Ressource innerhalb einer zu entfernenden virtuellen Switch-Konfiguration darstellt.</span><span class="sxs-lookup"><span data-stu-id="da2c3-108">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class, where each instance represents the settings of a virtual resource within a virtual switch configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="da2c3-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="da2c3-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da2c3-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="da2c3-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da2c3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da2c3-111">Return value</span></span>

<span data-ttu-id="da2c3-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="da2c3-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="da2c3-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="da2c3-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="da2c3-114">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="da2c3-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="da2c3-115">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="da2c3-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="da2c3-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="da2c3-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="da2c3-117">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="da2c3-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="da2c3-118">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="da2c3-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="da2c3-119">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="da2c3-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="da2c3-120">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="da2c3-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="da2c3-121">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="da2c3-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="da2c3-122">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="da2c3-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="da2c3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da2c3-123">Requirements</span></span>



| <span data-ttu-id="da2c3-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da2c3-124">Requirement</span></span> | <span data-ttu-id="da2c3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="da2c3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da2c3-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da2c3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="da2c3-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da2c3-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="da2c3-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da2c3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="da2c3-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da2c3-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da2c3-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="da2c3-130">Namespace</span></span><br/>                | <span data-ttu-id="da2c3-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="da2c3-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="da2c3-132">MOF</span><span class="sxs-lookup"><span data-stu-id="da2c3-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da2c3-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="da2c3-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="da2c3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="da2c3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da2c3-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="da2c3-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="da2c3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da2c3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da2c3-137">**Adresssourcesettings**</span><span class="sxs-lookup"><span data-stu-id="da2c3-137">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="da2c3-138">**Modifyresourcesettings**</span><span class="sxs-lookup"><span data-stu-id="da2c3-138">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="da2c3-139">**MSVM \_ virtualethernetzwitchmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="da2c3-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

