---
description: Entfernt Funktionseinstellungen aus einer Ethernet-Verbindung eines virtuellen Computers.
ms.assetid: 457056d0-7e69-47e4-8744-0136a1816f4a
title: Removefeaturesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c29151f6544d7eb803ec72ee49e455556d8b2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350338"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="bc3be-103">Removefeaturesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="bc3be-103">RemoveFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="bc3be-104">Entfernt Funktionseinstellungen aus einer Ethernet-Verbindung eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="bc3be-104">Removes feature settings from a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc3be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc3be-105">Syntax</span></span>


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_EthernetSwitchPortFeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bc3be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc3be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc3be-107">*Featuresettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc3be-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc3be-108">Ein Array von Zeichen folgen, die eine eingebettete Instanz einer Klasse enthalten, die von der [**MSVM-Klasse \_ ethernetzwitchfeaturesettingdata**](msvm-ethernetswitchfeaturesettingdata.md) abgeleitet ist, die die zu entfernenden Funktionseinstellungen definiert.</span><span class="sxs-lookup"><span data-stu-id="bc3be-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that defines the feature settings to be removed.</span></span> <span data-ttu-id="bc3be-109">Die **InstanceId-** Eigenschaft der einzelnen Instanzen identifiziert die zu entfernenden Funktionseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="bc3be-109">The **InstanceID** property of each of these instances identifies the feature settings to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="bc3be-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc3be-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc3be-111">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="bc3be-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc3be-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc3be-112">Return value</span></span>

<span data-ttu-id="bc3be-113">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="bc3be-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bc3be-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="bc3be-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc3be-115">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="bc3be-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bc3be-116">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="bc3be-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bc3be-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="bc3be-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bc3be-118">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="bc3be-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bc3be-119">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="bc3be-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bc3be-120">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="bc3be-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bc3be-121">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="bc3be-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bc3be-122">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="bc3be-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="bc3be-123">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="bc3be-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bc3be-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc3be-124">Requirements</span></span>



| <span data-ttu-id="bc3be-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc3be-125">Requirement</span></span> | <span data-ttu-id="bc3be-126">Wert</span><span class="sxs-lookup"><span data-stu-id="bc3be-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3be-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc3be-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bc3be-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc3be-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bc3be-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc3be-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bc3be-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc3be-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bc3be-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc3be-131">Namespace</span></span><br/>                | <span data-ttu-id="bc3be-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="bc3be-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bc3be-133">MOF</span><span class="sxs-lookup"><span data-stu-id="bc3be-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc3be-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bc3be-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc3be-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bc3be-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc3be-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc3be-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc3be-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc3be-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc3be-138">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="bc3be-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

