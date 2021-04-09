---
description: Fügt einer virtuellen Systemkonfiguration Start Quellen hinzu, wenn Sie auf die \# Konfiguration des virtuellen Systems "&0034; Status&0034;" angewendet wird \# .
ms.assetid: 2d091554-73d4-47c6-a0c2-97644fc9abe9
title: Addbootsourcesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e20a1184e11113ba25ac060ec19dab5d2391b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128404"
---
# <a name="addbootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="1b4e2-103">Addbootsourcesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="1b4e2-103">AddBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="1b4e2-104">Fügt einer virtuellen Systemkonfiguration Start Quellen hinzu, wenn diese auf eine virtuelle Systemkonfiguration vom Typ "State" angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b4e2-104">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b4e2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b4e2-105">Syntax</span></span>


```mof
uint32 AddBootSourceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           BootSourceSettings[],
  [out] CIM_SettingData              REF ResultingBootSourceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1b4e2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b4e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b4e2-107">*Affectedconfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4e2-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e2-108">Ein [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) mit der betroffenen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b4e2-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e2-109">*Bootsourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4e2-109">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e2-110">Ein Array, das die Einstellungen für die Start Quelle enthält.</span><span class="sxs-lookup"><span data-stu-id="1b4e2-110">An array containing the boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e2-111">*Resultingbootsourcesettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b4e2-111">*ResultingBootSourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e2-112">Bei Erfolg wird ein [**CIM- \_ SettingData**](cim-settingdata.md) mit den resultierenden Start Quell Einstellungen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b4e2-112">On success, returns a [**CIM\_SettingData**](cim-settingdata.md) with the resulting boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e2-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b4e2-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e2-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="1b4e2-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b4e2-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b4e2-115">Return value</span></span>

<span data-ttu-id="1b4e2-116">Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b4e2-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1b4e2-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="1b4e2-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1b4e2-118">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="1b4e2-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1b4e2-119">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="1b4e2-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1b4e2-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="1b4e2-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1b4e2-121">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="1b4e2-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1b4e2-122">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1b4e2-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1b4e2-123">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="1b4e2-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1b4e2-124">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="1b4e2-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1b4e2-125">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="1b4e2-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1b4e2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b4e2-126">Requirements</span></span>



| <span data-ttu-id="1b4e2-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b4e2-127">Requirement</span></span> | <span data-ttu-id="1b4e2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1b4e2-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b4e2-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b4e2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1b4e2-130">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b4e2-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="1b4e2-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b4e2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1b4e2-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1b4e2-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1b4e2-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b4e2-133">Namespace</span></span><br/>                | <span data-ttu-id="1b4e2-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1b4e2-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1b4e2-135">MOF</span><span class="sxs-lookup"><span data-stu-id="1b4e2-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b4e2-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1b4e2-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b4e2-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1b4e2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b4e2-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1b4e2-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1b4e2-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b4e2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b4e2-140">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="1b4e2-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

