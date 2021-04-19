---
description: Ändert die Funktionseinstellungen eines Ethernet-Switchports.
ms.assetid: 8c21a932-fffb-40fd-9166-d7e351329217
title: Modifyfeaturesettings-Methode der Msvm_VirtualEthernetSwitchManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0bee92019f9457a42a0c87ab619f7de1f7d203ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350296"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="e3e41-103">Modifyfeaturesettings-Methode der MSVM \_ virtualethernetzwitchmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="e3e41-103">ModifyFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="e3e41-104">Ändert die Funktionseinstellungen eines Ethernet-Switchports.</span><span class="sxs-lookup"><span data-stu-id="e3e41-104">Modifies the feature settings of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3e41-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3e41-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e3e41-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3e41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3e41-107">*Featuresettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3e41-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3e41-108">Ein Array von Zeichen folgen, die eine eingebettete Instanz einer von der [**MSVM \_ featuresettingdata**](msvm-featuresettingdata.md) -Klasse abgeleiteten Klasse enthalten, die die zu ändernden Switchport-Funktionseinstellungen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e3e41-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the switch port feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="e3e41-109">*Resultingfeaturesettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e3e41-109">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3e41-110">Ein Array von Verweisen auf Instanzen der [**MSVM \_ featuresettingdata**](msvm-featuresettingdata.md) -Klasse, die die geänderten Funktionseinstellungen darstellen.</span><span class="sxs-lookup"><span data-stu-id="e3e41-110">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="e3e41-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e3e41-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3e41-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="e3e41-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3e41-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3e41-113">Return value</span></span>

<span data-ttu-id="e3e41-114">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="e3e41-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e3e41-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="e3e41-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e3e41-116">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="e3e41-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e3e41-117">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="e3e41-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e3e41-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="e3e41-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e3e41-119">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="e3e41-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e3e41-120">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="e3e41-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e3e41-121">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="e3e41-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e3e41-122">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e3e41-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e3e41-123">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="e3e41-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e3e41-124">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="e3e41-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e3e41-125">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="e3e41-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e3e41-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3e41-126">Requirements</span></span>



| <span data-ttu-id="e3e41-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3e41-127">Requirement</span></span> | <span data-ttu-id="e3e41-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e3e41-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e41-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3e41-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e3e41-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3e41-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e3e41-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3e41-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e3e41-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3e41-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e3e41-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3e41-133">Namespace</span></span><br/>                | <span data-ttu-id="e3e41-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e3e41-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e3e41-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e3e41-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3e41-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e3e41-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3e41-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e3e41-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3e41-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e3e41-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e3e41-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3e41-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3e41-140">**Addfeaturesettings**</span><span class="sxs-lookup"><span data-stu-id="e3e41-140">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="e3e41-141">**Removefeaturesettings**</span><span class="sxs-lookup"><span data-stu-id="e3e41-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="e3e41-142">**MSVM \_ virtualethernetzwitchmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="e3e41-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

