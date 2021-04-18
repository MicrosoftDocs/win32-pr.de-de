---
description: Entfernt die Funktionseinstellungen von einem Ethernet-Switchport.
ms.assetid: 3d45259e-34e4-417b-a895-4926b0eaaf59
title: Removefeaturesettings-Methode der Msvm_VirtualEthernetSwitchManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 919e2b69e2a0ef215a522c601088cb7aa2976a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358597"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="0d3a4-103">Removefeaturesettings-Methode der MSVM \_ virtualethernettwitchmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="0d3a4-103">RemoveFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="0d3a4-104">Entfernt die Funktionseinstellungen von einem Ethernet-Switchport.</span><span class="sxs-lookup"><span data-stu-id="0d3a4-104">Removes feature settings from an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d3a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d3a4-105">Syntax</span></span>


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_FeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0d3a4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d3a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d3a4-107">*Featuresettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d3a4-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3a4-108">Ein Array von Verweisen auf Instanzen der [**MSVM \_ featuresettingdata**](msvm-featuresettingdata.md) -Klasse, die die zu entfernenden Funktionseinstellungen darstellen.</span><span class="sxs-lookup"><span data-stu-id="0d3a4-108">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the feature settings to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="0d3a4-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0d3a4-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3a4-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="0d3a4-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d3a4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d3a4-111">Return value</span></span>

<span data-ttu-id="0d3a4-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0d3a4-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0d3a4-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="0d3a4-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0d3a4-114">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="0d3a4-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0d3a4-115">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="0d3a4-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0d3a4-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="0d3a4-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0d3a4-117">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="0d3a4-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0d3a4-118">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="0d3a4-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0d3a4-119">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0d3a4-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0d3a4-120">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="0d3a4-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0d3a4-121">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="0d3a4-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0d3a4-122">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="0d3a4-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0d3a4-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d3a4-123">Requirements</span></span>



| <span data-ttu-id="0d3a4-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d3a4-124">Requirement</span></span> | <span data-ttu-id="0d3a4-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0d3a4-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d3a4-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d3a4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0d3a4-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d3a4-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0d3a4-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d3a4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0d3a4-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d3a4-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d3a4-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d3a4-130">Namespace</span></span><br/>                | <span data-ttu-id="0d3a4-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0d3a4-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0d3a4-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0d3a4-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d3a4-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0d3a4-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d3a4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0d3a4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d3a4-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d3a4-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0d3a4-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d3a4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3a4-137">**Addfeaturesettings**</span><span class="sxs-lookup"><span data-stu-id="0d3a4-137">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="0d3a4-138">**Modifyfeaturesettings**</span><span class="sxs-lookup"><span data-stu-id="0d3a4-138">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="0d3a4-139">**MSVM \_ virtualethernetzwitchmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="0d3a4-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

