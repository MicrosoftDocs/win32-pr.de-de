---
description: Ändert die aktuellen Featureeinstellungen einer Ethernet-Verbindung einer virtuellen Maschine.
ms.assetid: 3caa810f-0444-45cf-88a4-e93d04accb46
title: Modifyfeaturesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c376158008c5ad0e611d3a05c7e73d2e7d1b44cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346068"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="456d8-103">Modifyfeaturesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="456d8-103">ModifyFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="456d8-104">Ändert die aktuellen Featureeinstellungen einer Ethernet-Verbindung einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="456d8-104">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="456d8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="456d8-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="456d8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="456d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="456d8-107">*Featuresettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="456d8-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="456d8-108">Ein Array von Zeichen folgen, die eine eingebettete Instanz einer Klasse enthalten, die von der [**MSVM-Klasse \_ ethernetswitchfeaturesettingdata**](msvm-ethernetswitchfeaturesettingdata.md) abgeleitet wurde, die Änderungen an den aktuellen Featureeinstellungen einer vorhandenen Ethernet-Verbindung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="456d8-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that describes modifications to the current feature settings of an existing Ethernet connection.</span></span> <span data-ttu-id="456d8-109">Die **InstanceId-** Eigenschaft der einzelnen Instanzen identifiziert die Funktionseinstellungen, die geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="456d8-109">The **InstanceID** property of each of these instances identifies the feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="456d8-110">*Resultingfeaturesettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="456d8-110">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="456d8-111">Ein Array von Verweisen auf Instanzen der [**MSVM-Klasse " \_ ethernetzwitchportfeaturesettingdata**](msvm-ethernetswitchportfeaturesettingdata.md) ", die die geänderten Funktionseinstellungen darstellen.</span><span class="sxs-lookup"><span data-stu-id="456d8-111">An array of references to instances of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="456d8-112">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="456d8-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="456d8-113">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="456d8-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="456d8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="456d8-114">Return value</span></span>

<span data-ttu-id="456d8-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="456d8-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="456d8-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="456d8-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="456d8-117">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="456d8-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="456d8-118">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="456d8-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="456d8-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="456d8-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="456d8-120">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="456d8-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="456d8-121">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="456d8-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="456d8-122">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="456d8-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="456d8-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="456d8-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="456d8-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="456d8-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="456d8-125">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="456d8-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="456d8-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="456d8-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="456d8-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="456d8-127">Requirements</span></span>



| <span data-ttu-id="456d8-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="456d8-128">Requirement</span></span> | <span data-ttu-id="456d8-129">Wert</span><span class="sxs-lookup"><span data-stu-id="456d8-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="456d8-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="456d8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="456d8-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="456d8-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="456d8-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="456d8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="456d8-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="456d8-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="456d8-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="456d8-134">Namespace</span></span><br/>                | <span data-ttu-id="456d8-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="456d8-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="456d8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="456d8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="456d8-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="456d8-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="456d8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="456d8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="456d8-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="456d8-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="456d8-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="456d8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="456d8-141">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="456d8-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

