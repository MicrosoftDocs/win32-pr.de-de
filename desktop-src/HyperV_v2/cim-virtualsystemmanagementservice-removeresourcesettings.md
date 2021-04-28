---
description: 'RemoveResourceSettings-Methode der CIM_VirtualSystemManagementService-Klasse: Entfernt Einstellungen für virtuelle Ressourcen aus einer Konfiguration des virtuellen Systems.'
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: RemoveResourceSettings-Methode der CIM_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: e5c7daabcdcd732c3a5693664e1768ebf66668d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112258"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="17b12-103">RemoveResourceSettings-Methode der CIM \_ VirtualSystemManagementService-Klasse</span><span class="sxs-lookup"><span data-stu-id="17b12-103">RemoveResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="17b12-104">Entfernt Einstellungen für virtuelle Ressourcen aus einer Konfiguration des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="17b12-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="17b12-105">Wenn sie auf Teile einer "aktuellen" Konfiguration des virtuellen Systems angewendet werden, können ressourcen des aktiven virtuellen Systems als Nebeneffekt entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="17b12-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b12-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="17b12-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="17b12-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="17b12-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b12-108">*ResourceSettings* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="17b12-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b12-109">Array von Verweisen auf Instanzen der [**Cim \_ ResourceAllocationSettingData-Klasse,**](cim-resourceallocationsettingdata.md) wobei jede Instanz die Einstellungen einer virtuellen Ressource innerhalb einer konfiguration des virtuellen Systems darstellt, die entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="17b12-109">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) where each instance represents the settings of a virtual resource within a virtual system configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="17b12-110">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="17b12-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17b12-111">Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM \_ ConcreteJob**](cim-concretejob.md) zurückgegeben werden, der den Auftrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="17b12-111">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17b12-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17b12-112">Return value</span></span>

<span data-ttu-id="17b12-113">Gibt bei Erfolg den Wert 0 zurück. andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17b12-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="17b12-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="17b12-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="17b12-115">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="17b12-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="17b12-116">**Fehler** (2)</span><span class="sxs-lookup"><span data-stu-id="17b12-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="17b12-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="17b12-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="17b12-118">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="17b12-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="17b12-119">**Ungültiger Zustand** (5)</span><span class="sxs-lookup"><span data-stu-id="17b12-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="17b12-120">**DMTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="17b12-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="17b12-121">**Methodenparameter überprüft** – Auftrag gestartet (4096)</span><span class="sxs-lookup"><span data-stu-id="17b12-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="17b12-122">**Reservierte Methode** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="17b12-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="17b12-123">**Herstellerspezifisch** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="17b12-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="17b12-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17b12-124">Requirements</span></span>



| <span data-ttu-id="17b12-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17b12-125">Requirement</span></span> | <span data-ttu-id="17b12-126">Wert</span><span class="sxs-lookup"><span data-stu-id="17b12-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17b12-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17b12-127">Minimum supported client</span></span><br/> | <span data-ttu-id="17b12-128">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="17b12-128">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="17b12-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17b12-129">Minimum supported server</span></span><br/> | <span data-ttu-id="17b12-130">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="17b12-130">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="17b12-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="17b12-131">Namespace</span></span><br/>                | <span data-ttu-id="17b12-132">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="17b12-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="17b12-133">MOF</span><span class="sxs-lookup"><span data-stu-id="17b12-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17b12-134"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="17b12-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="17b12-135">DLL</span><span class="sxs-lookup"><span data-stu-id="17b12-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17b12-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="17b12-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="17b12-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="17b12-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b12-138">**CIM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="17b12-138">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




