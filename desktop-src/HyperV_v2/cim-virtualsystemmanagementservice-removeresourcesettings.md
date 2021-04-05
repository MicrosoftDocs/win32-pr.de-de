---
description: Entfernt die Einstellungen virtueller Ressourcen aus einer Konfiguration des virtuellen Systems.
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: Removeresourcesettings-Methode der CIM_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1f5b3ac1cc53f23d0d899a4c6b5d17408bca3b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755440"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="b90a4-103">Removeresourcesettings-Methode der CIM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="b90a4-103">RemoveResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="b90a4-104">Entfernt die Einstellungen virtueller Ressourcen aus einer Konfiguration des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="b90a4-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="b90a4-105">Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, werden möglicherweise als Nebeneffekt Ressourcen des aktiven virtuellen Systems entfernt.</span><span class="sxs-lookup"><span data-stu-id="b90a4-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b90a4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b90a4-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b90a4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b90a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b90a4-108">*Resourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b90a4-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b90a4-109">Array von Verweisen auf Instanzen der Klasse [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) , wobei jede Instanz die Einstellungen einer virtuellen Ressource innerhalb einer zu entfernenden virtuellen Systemkonfiguration darstellt.</span><span class="sxs-lookup"><span data-stu-id="b90a4-109">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) where each instance represents the settings of a virtual resource within a virtual system configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="b90a4-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b90a4-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b90a4-111">Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM-" \_ concretejob**](cim-concretejob.md) " zurückgegeben werden, der den Auftrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="b90a4-111">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b90a4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b90a4-112">Return value</span></span>

<span data-ttu-id="b90a4-113">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b90a4-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b90a4-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="b90a4-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b90a4-115">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="b90a4-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b90a4-116">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="b90a4-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b90a4-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="b90a4-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b90a4-118">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="b90a4-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b90a4-119">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="b90a4-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b90a4-120">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="b90a4-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b90a4-121">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="b90a4-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b90a4-122">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="b90a4-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b90a4-123">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="b90a4-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b90a4-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b90a4-124">Requirements</span></span>



| <span data-ttu-id="b90a4-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b90a4-125">Requirement</span></span> | <span data-ttu-id="b90a4-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b90a4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b90a4-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b90a4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b90a4-128">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b90a4-128">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b90a4-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b90a4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b90a4-130">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b90a4-130">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b90a4-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="b90a4-131">Namespace</span></span><br/>                | <span data-ttu-id="b90a4-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b90a4-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b90a4-133">MOF</span><span class="sxs-lookup"><span data-stu-id="b90a4-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b90a4-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b90a4-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b90a4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b90a4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b90a4-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b90a4-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b90a4-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b90a4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b90a4-138">**CIM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="b90a4-138">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




