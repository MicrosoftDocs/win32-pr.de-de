---
description: Führt ein Upgrade des virtuellen Systems durch.
ms.assetid: 4b24aac9-b7b9-460f-9227-fd3c1e960191
title: Upgradesystemversion-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.UpgradeSystemVersion
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4c34b33da14d8718f2c2414de3aea3079672bbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342826"
---
# <a name="upgradesystemversion-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="c29af-103">Upgradesystemversion-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="c29af-103">UpgradeSystemVersion method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="c29af-104">Führt ein Upgrade des virtuellen Systems durch.</span><span class="sxs-lookup"><span data-stu-id="c29af-104">Upgrades the virtual system.</span></span>

<span data-ttu-id="c29af-105">Bei Anwendung auf die Systemeinstellungen einer "aktuellen" virtuellen Systemkonfiguration</span><span class="sxs-lookup"><span data-stu-id="c29af-105">When applied to the system settings of a "current" virtual system configuration</span></span>

## <a name="syntax"></a><span data-ttu-id="c29af-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c29af-106">Syntax</span></span>


```mof
uint32 UpgradeSystemVersion(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 UpgradeSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c29af-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c29af-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c29af-108">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c29af-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c29af-109">Ein Verweis auf ein [**CIM- \_ Computersystem**](cim-computersystem.md) , das das zu Aktualisier Ende virtuelle Computersystem darstellt.</span><span class="sxs-lookup"><span data-stu-id="c29af-109">A reference to a [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual computer system to be upgraded.</span></span>

</dd> <dt>

<span data-ttu-id="c29af-110">*Upgraabsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c29af-110">*UpgradeSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c29af-111">Die upgradeeinstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="c29af-111">The upgrade setting data.</span></span>

</dd> <dt>

<span data-ttu-id="c29af-112">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c29af-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c29af-113">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="c29af-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c29af-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c29af-114">Return value</span></span>

<span data-ttu-id="c29af-115">Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c29af-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="c29af-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="c29af-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c29af-117">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="c29af-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c29af-118">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="c29af-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c29af-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="c29af-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c29af-120">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="c29af-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c29af-121">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="c29af-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c29af-122">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="c29af-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c29af-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="c29af-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c29af-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="c29af-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c29af-125">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="c29af-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c29af-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="c29af-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c29af-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c29af-127">Requirements</span></span>



| <span data-ttu-id="c29af-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c29af-128">Requirement</span></span> | <span data-ttu-id="c29af-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c29af-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c29af-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c29af-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c29af-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c29af-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c29af-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c29af-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c29af-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c29af-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c29af-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="c29af-134">Namespace</span></span><br/>                | <span data-ttu-id="c29af-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c29af-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c29af-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c29af-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c29af-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c29af-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c29af-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c29af-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c29af-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c29af-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c29af-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c29af-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c29af-141">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="c29af-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

