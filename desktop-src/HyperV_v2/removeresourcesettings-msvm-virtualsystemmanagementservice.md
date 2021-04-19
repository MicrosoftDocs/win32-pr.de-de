---
description: Entfernt die Einstellungen der virtuellen Ressource aus der Konfiguration einer virtuellen Maschine.
ms.assetid: 74d9a70a-5258-4e4b-8131-b25513d11a4b
title: Removeresourcesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 20a7c9fb10e4f7a6356e47f8c743266095de2042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356801"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="70eec-103">Removeresourcesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="70eec-103">RemoveResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="70eec-104">Entfernt die Einstellungen der virtuellen Ressource aus der Konfiguration einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="70eec-104">Removes virtual resource settings from a virtual machine configuration.</span></span> <span data-ttu-id="70eec-105">Wenn Sie auf Teile einer aktuellen VM-Konfiguration angewendet wird, wird die aktive virtuelle Maschine möglicherweise entfernt.</span><span class="sxs-lookup"><span data-stu-id="70eec-105">When applied to parts of a current virtual machine configuration, the active virtual machine may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="70eec-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="70eec-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="70eec-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="70eec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70eec-108">*Resourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70eec-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70eec-109">Ein Array von Verweisen auf Instanzen der [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Klasse, wobei jede Instanz die Einstellungen einer virtuellen Ressource innerhalb einer zu entfernenden virtuellen Computerkonfiguration darstellt.</span><span class="sxs-lookup"><span data-stu-id="70eec-109">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class, where each instance represents the settings of a virtual resource within a virtual machine configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="70eec-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="70eec-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70eec-111">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="70eec-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70eec-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70eec-112">Return value</span></span>

<span data-ttu-id="70eec-113">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="70eec-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="70eec-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="70eec-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="70eec-115">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="70eec-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="70eec-116">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="70eec-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="70eec-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="70eec-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="70eec-118">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="70eec-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="70eec-119">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="70eec-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="70eec-120">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="70eec-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="70eec-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="70eec-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="70eec-122">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="70eec-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="70eec-123">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="70eec-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="70eec-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70eec-124">Requirements</span></span>



| <span data-ttu-id="70eec-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70eec-125">Requirement</span></span> | <span data-ttu-id="70eec-126">Wert</span><span class="sxs-lookup"><span data-stu-id="70eec-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70eec-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="70eec-127">Minimum supported client</span></span><br/> | <span data-ttu-id="70eec-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70eec-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="70eec-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="70eec-129">Minimum supported server</span></span><br/> | <span data-ttu-id="70eec-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70eec-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70eec-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="70eec-131">Namespace</span></span><br/>                | <span data-ttu-id="70eec-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="70eec-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="70eec-133">MOF</span><span class="sxs-lookup"><span data-stu-id="70eec-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70eec-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="70eec-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="70eec-135">DLL</span><span class="sxs-lookup"><span data-stu-id="70eec-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70eec-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="70eec-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="70eec-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70eec-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70eec-138">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="70eec-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

