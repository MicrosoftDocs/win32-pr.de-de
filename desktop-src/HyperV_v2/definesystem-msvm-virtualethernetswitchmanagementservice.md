---
description: Erstellt einen neuen virtuellen Switch.
ms.assetid: de7495e9-48c5-427a-b9bb-0821b53a9b09
title: Definesystem-Methode der Msvm_VirtualEthernetSwitchManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd6e2dfb7d9cf7e64fb76c35f6f3c3b8457d69d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867076"
---
# <a name="definesystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="74e11-103">Definesystem-Methode der MSVM \_ virtualethernettwitchmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="74e11-103">DefineSystem method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="74e11-104">Erstellt einen neuen virtuellen Switch.</span><span class="sxs-lookup"><span data-stu-id="74e11-104">Creates a new virtual switch.</span></span> <span data-ttu-id="74e11-105">Eigenschaften, die nicht angegeben sind, werden mit Standardwerten aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="74e11-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="74e11-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="74e11-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="74e11-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="74e11-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74e11-108">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74e11-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74e11-109">Eine eingebettete Instanz der [**MSVM \_ virtualethernetzwitchsettingdata**](msvm-virtualethernetswitchsettingdata.md) -Klasse, die verwendet wird, um die Attribute des zu erstellenden virtuellen Switches zu definieren.</span><span class="sxs-lookup"><span data-stu-id="74e11-109">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that is used to define the attributes of the virtual switch to be created.</span></span> <span data-ttu-id="74e11-110">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="74e11-110">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="74e11-111">*Resourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74e11-111">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74e11-112">Ein Array von eingebetteten Instanzen der [**MSVM-Klasse \_ ethernetportzudationsettingdata**](msvm-ethernetportallocationsettingdata.md) , die die Einstellungen der Switchports beschreibt, die im Bereich des neuen virtuellen Switches erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="74e11-112">An array of embedded instances of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that describes the settings of the switch ports to be created in the scope of the new virtual switch.</span></span> <span data-ttu-id="74e11-113">Wenn **null** angegeben wird, wird der virtuelle Switch ohne Ressourcen erstellt (d. h. keine Switchports).</span><span class="sxs-lookup"><span data-stu-id="74e11-113">If **Null** is specified, the virtual switch will be created with no resources (i.e. no switch ports).</span></span>

</dd> <dt>

<span data-ttu-id="74e11-114">*Referenceconfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74e11-114">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74e11-115">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="74e11-115">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74e11-116">*Resultingsystem* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="74e11-116">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74e11-117">Wenn ein virtueller Switch erfolgreich erstellt wurde, ist dies ein Verweis auf eine Instanz der [**MSVM \_ virtualethernwitch**](msvm-virtualethernetswitch.md) -Klasse, die den neu definierten virtuellen Switch darstellt.</span><span class="sxs-lookup"><span data-stu-id="74e11-117">If a virtual switch is successfully created, a reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the newly defined virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="74e11-118">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="74e11-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74e11-119">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="74e11-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74e11-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74e11-120">Return value</span></span>

<span data-ttu-id="74e11-121">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="74e11-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="74e11-122">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="74e11-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="74e11-123">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="74e11-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="74e11-124">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="74e11-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="74e11-125">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="74e11-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="74e11-126">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="74e11-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="74e11-127">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="74e11-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="74e11-128">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="74e11-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="74e11-129">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="74e11-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="74e11-130">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="74e11-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="74e11-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74e11-131">Requirements</span></span>



| <span data-ttu-id="74e11-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74e11-132">Requirement</span></span> | <span data-ttu-id="74e11-133">Wert</span><span class="sxs-lookup"><span data-stu-id="74e11-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74e11-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74e11-134">Minimum supported client</span></span><br/> | <span data-ttu-id="74e11-135">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74e11-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="74e11-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74e11-136">Minimum supported server</span></span><br/> | <span data-ttu-id="74e11-137">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74e11-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74e11-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="74e11-138">Namespace</span></span><br/>                | <span data-ttu-id="74e11-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="74e11-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="74e11-140">MOF</span><span class="sxs-lookup"><span data-stu-id="74e11-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74e11-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="74e11-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74e11-142">DLL</span><span class="sxs-lookup"><span data-stu-id="74e11-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74e11-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74e11-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74e11-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74e11-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74e11-145">**MSVM \_ virtualethernetzwitchmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="74e11-145">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

