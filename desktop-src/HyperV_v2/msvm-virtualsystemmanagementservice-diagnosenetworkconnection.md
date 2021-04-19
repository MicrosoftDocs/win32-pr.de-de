---
description: Diagnostizieren der Netzwerk Konnektivität eines virtuellen Computers in einer Windows-netzwerkvirtualisierungsumgebung.
ms.assetid: c18f48bf-1f57-4a23-a495-462afad42750
title: Diagnosenetworkconnection-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DiagnoseNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 70760f771e3908265a4ac70ebc1cbdf957d652c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346905"
---
# <a name="diagnosenetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="10888-103">Diagnosenetworkconnection-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="10888-103">DiagnoseNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="10888-104">Diagnostizieren der Netzwerk Konnektivität eines virtuellen Computers in einer Windows-netzwerkvirtualisierungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="10888-104">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="10888-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="10888-105">Syntax</span></span>


```mof
uint32 DiagnoseNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  string                                     DiagnosticSettings,
  [out] string                                     DiagnosticInformation,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="10888-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10888-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10888-107">*Targetnetworkadapter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10888-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10888-108">Verweis auf eine [**MSVM- \_ ethernetportbereitungssettingdata**](msvm-ethernetportallocationsettingdata.md) , die den Zielnetzwerk Adapter beschreibt.</span><span class="sxs-lookup"><span data-stu-id="10888-108">Reference to an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) that describes the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="10888-109">*Diagnosticsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10888-109">*DiagnosticSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10888-110">Die zu verwendenden Diagnose Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="10888-110">The diagnostic settings to use.</span></span>

</dd> <dt>

<span data-ttu-id="10888-111">*DiagnosticInformation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="10888-111">*DiagnosticInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10888-112">Bei Erfolg werden die Diagnoseinformationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="10888-112">On success, returns the diagnostic information.</span></span>

</dd> <dt>

<span data-ttu-id="10888-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="10888-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10888-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="10888-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10888-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10888-115">Return value</span></span>

<span data-ttu-id="10888-116">Gibt bei Erfolg 0 oder 4096 zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="10888-116">Returns a 0 or 4096 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="10888-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="10888-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="10888-118">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="10888-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="10888-119">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="10888-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="10888-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="10888-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="10888-121">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="10888-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="10888-122">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="10888-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="10888-123">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="10888-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="10888-124">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="10888-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="10888-125">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="10888-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="10888-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10888-126">Requirements</span></span>



| <span data-ttu-id="10888-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10888-127">Requirement</span></span> | <span data-ttu-id="10888-128">Wert</span><span class="sxs-lookup"><span data-stu-id="10888-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10888-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10888-129">Minimum supported client</span></span><br/> | <span data-ttu-id="10888-130">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10888-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="10888-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10888-131">Minimum supported server</span></span><br/> | <span data-ttu-id="10888-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="10888-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="10888-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="10888-133">Namespace</span></span><br/>                | <span data-ttu-id="10888-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="10888-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="10888-135">MOF</span><span class="sxs-lookup"><span data-stu-id="10888-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10888-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="10888-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="10888-137">DLL</span><span class="sxs-lookup"><span data-stu-id="10888-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10888-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="10888-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="10888-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10888-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10888-140">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="10888-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

