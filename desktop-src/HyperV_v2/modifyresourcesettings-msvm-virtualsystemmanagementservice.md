---
description: 'ModifyResourceSettings-Methode der Msvm_VirtualSystemManagementService Klasse: Ändert einstellungen für virtuelle Ressourcen.'
ms.assetid: 3fb2a65f-9f40-4eb9-99e8-8fe1451427d9
title: ModifyResourceSettings-Methode der Msvm_VirtualSystemManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 09ca0bb9fea02b6acc5599d9f907b1e60fdbd9ec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119338"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="cfa17-103">ModifyResourceSettings-Methode der Msvm \_ VirtualSystemManagementService-Klasse</span><span class="sxs-lookup"><span data-stu-id="cfa17-103">ModifyResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="cfa17-104">Ändert die Einstellungen für virtuelle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="cfa17-104">Modifies virtual resource settings.</span></span> <span data-ttu-id="cfa17-105">Wenn sie auf Teile einer aktuellen Konfiguration eines virtuellen Computers angewendet werden, können die Ressourcen des aktiven virtuellen Computers als Nebeneffekt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cfa17-105">When applied to parts of a current virtual machine configuration, as a side effect, the resources of the active virtual machine may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfa17-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfa17-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="cfa17-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfa17-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfa17-108">*ResourceSettings* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cfa17-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfa17-109">Ein Array von Zeichenfolgen, die eine eingebettete Instanz einer von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)abgeleiteten Klasse enthalten, die die geänderten Aspekte vorhandener virtueller Ressourcen enthalten.</span><span class="sxs-lookup"><span data-stu-id="cfa17-109">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="cfa17-110">Die **InstanceID-Eigenschaft** jeder Instanz identifiziert die zu ändernde Einstellung der virtuellen Ressource.</span><span class="sxs-lookup"><span data-stu-id="cfa17-110">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="cfa17-111">*ResultingResourceSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cfa17-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfa17-112">Ein Array von Verweisen auf Instanzen von Objekten, die von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) abgeleitet wurden und virtuelle Aspekte der geänderten virtuellen Ressourcen darstellen.</span><span class="sxs-lookup"><span data-stu-id="cfa17-112">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="cfa17-113">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cfa17-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfa17-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cfa17-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfa17-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfa17-115">Return value</span></span>

<span data-ttu-id="cfa17-116">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="cfa17-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cfa17-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="cfa17-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cfa17-118">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="cfa17-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cfa17-119">**Fehler** (2)</span><span class="sxs-lookup"><span data-stu-id="cfa17-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cfa17-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="cfa17-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cfa17-121">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="cfa17-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cfa17-122">**Ungültiger Zustand** (5)</span><span class="sxs-lookup"><span data-stu-id="cfa17-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="cfa17-123">**Inkompatible** Parameter (6)</span><span class="sxs-lookup"><span data-stu-id="cfa17-123">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="cfa17-124">**DMTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="cfa17-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cfa17-125">**Methodenparameter überprüft** – Auftrag gestartet (4096)</span><span class="sxs-lookup"><span data-stu-id="cfa17-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cfa17-126">**Reservierte Methode** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="cfa17-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="cfa17-127">**Herstellerspezifisch** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="cfa17-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cfa17-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfa17-128">Requirements</span></span>



| <span data-ttu-id="cfa17-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfa17-129">Requirement</span></span> | <span data-ttu-id="cfa17-130">Wert</span><span class="sxs-lookup"><span data-stu-id="cfa17-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa17-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfa17-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cfa17-132">nur Windows 8 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfa17-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cfa17-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfa17-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cfa17-134">Nur Windows Server \[ 2012-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfa17-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cfa17-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="cfa17-135">Namespace</span></span><br/>                | <span data-ttu-id="cfa17-136">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="cfa17-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cfa17-137">MOF</span><span class="sxs-lookup"><span data-stu-id="cfa17-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfa17-138"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfa17-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfa17-139">DLL</span><span class="sxs-lookup"><span data-stu-id="cfa17-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfa17-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cfa17-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cfa17-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cfa17-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa17-142">**ModifyVirtualSystemResources (V1)**</span><span class="sxs-lookup"><span data-stu-id="cfa17-142">**ModifyVirtualSystemResources (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="cfa17-143">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="cfa17-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

