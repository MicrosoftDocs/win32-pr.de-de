---
description: Definiert ein virtuelles System.
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: Definesystem-Methode der CIM_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e38111d52044ed385fdd8cd19dd9094834e794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354637"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="80a3a-103">Definesystem-Methode der CIM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="80a3a-103">DefineSystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="80a3a-104">Definiert ein virtuelles System.</span><span class="sxs-lookup"><span data-stu-id="80a3a-104">Defines a virtual system.</span></span>

<span data-ttu-id="80a3a-105">Eingaben, die nicht vollständig angegeben sind, können mit Standardwerten aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="80a3a-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="80a3a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="80a3a-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="80a3a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="80a3a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80a3a-108">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80a3a-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80a3a-109">Eine Zeichenfolge, die eine eingebettete Instanz der Klasse [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) enthält, die zum Definieren von Attributen des zu erstellenden virtuellen Systems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="80a3a-109">String containing an embedded instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to define attributes of the virtual system to be created.</span></span>

</dd> <dt>

<span data-ttu-id="80a3a-110">*Resourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80a3a-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80a3a-111">Ein Array von Zeichen folgen, die eine eingebettete Instanz der Klasse [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) enthalten, in der die virtuellen Aspekte einer virtuellen Ressource beschrieben werden, die im Bereich des neuen virtuellen Systems erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="80a3a-111">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be created in the scope of the new virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="80a3a-112">*Referenceconfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80a3a-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80a3a-113">Verweis auf eine [**CIM \_ virtualsystemsettingdat**](cim-virtualsystemsettingdata.md) -Objektinstanz, bei der es sich um das Objekt der obersten Ebene einer virtuellen Referenz Konfiguration handelt.</span><span class="sxs-lookup"><span data-stu-id="80a3a-113">Reference to a [**CIM\_VirtualSystemSettingDat**](cim-virtualsystemsettingdata.md) object instance that is the top level object of a reference virtual system configuration.</span></span> <span data-ttu-id="80a3a-114">Die Referenz Konfiguration wird verwendet, um die Konfiguration des neuen virtuellen Systems zu ergänzen, wenn die Parameter " *SystemSettings* " und " *resourcesettings* " keine entsprechenden Informationen bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="80a3a-114">The reference configuration is used to complement the configuration of the new virtual system if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="80a3a-115">*Resultingsystem* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80a3a-115">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80a3a-116">Wenn ein virtuelles Computersystem erfolgreich definiert wurde, wird ein Verweis auf eine Instanz der Klasse " [**CIM \_ Computersystem**](cim-computersystem.md) " zurückgegeben, die das neu definierte System des virtuellen Computers darstellt.</span><span class="sxs-lookup"><span data-stu-id="80a3a-116">If a virtual computer system is successfully defined, a reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the newly defined virtual computer system is returned.</span></span>

</dd> <dt>

<span data-ttu-id="80a3a-117">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80a3a-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80a3a-118">Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="80a3a-118">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="80a3a-119">In diesem Fall wird die Instanz der Klasse [**CIM \_ Computersystem**](cim-computersystem.md) , die das neue virtuelle System repräsentiert, über [**Association CIM \_ affectedjobelate**](cim-affectedjobelement.md) mit der Eigenschaft " **affectedelta** " angezeigt, die auf die neue Instanz der Klasse " **CIM \_ Computersystem** " und die Eigenschaft " **elementeffects** " auf 5 (Create) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="80a3a-119">In this case, the instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the new virtual system is presented via association [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) with the property **AffectedElement** referring to the new instance of class **CIM\_ComputerSystem** and property **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80a3a-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80a3a-120">Return value</span></span>

<span data-ttu-id="80a3a-121">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="80a3a-121">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="80a3a-122">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="80a3a-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="80a3a-123">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="80a3a-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="80a3a-124">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="80a3a-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="80a3a-125">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="80a3a-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="80a3a-126">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="80a3a-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="80a3a-127">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="80a3a-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="80a3a-128">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="80a3a-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="80a3a-129">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="80a3a-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="80a3a-130">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="80a3a-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="80a3a-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80a3a-131">Requirements</span></span>



| <span data-ttu-id="80a3a-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80a3a-132">Requirement</span></span> | <span data-ttu-id="80a3a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="80a3a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80a3a-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80a3a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="80a3a-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="80a3a-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="80a3a-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80a3a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="80a3a-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="80a3a-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="80a3a-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="80a3a-138">Namespace</span></span><br/>                | <span data-ttu-id="80a3a-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="80a3a-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="80a3a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="80a3a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80a3a-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="80a3a-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80a3a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="80a3a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80a3a-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80a3a-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="80a3a-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80a3a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a3a-145">**CIM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="80a3a-145">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




