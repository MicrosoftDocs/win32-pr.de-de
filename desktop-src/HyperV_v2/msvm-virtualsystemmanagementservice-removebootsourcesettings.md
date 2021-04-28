---
description: 'RemoveBootSourceSettings-Methode der Msvm_VirtualSystemManagementService-Klasse: Entfernt Einstellungen für virtuelle Ressourcen aus einer Konfiguration des virtuellen Systems.'
ms.assetid: 0deb7719-e605-4ba5-9bb2-037d0cafee24
title: RemoveBootSourceSettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5407e56b761dd545d20b89e0a28742f9c542b15a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109398"
---
# <a name="removebootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="50ca4-103">RemoveBootSourceSettings-Methode der Msvm \_ VirtualSystemManagementService-Klasse</span><span class="sxs-lookup"><span data-stu-id="50ca4-103">RemoveBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="50ca4-104">Entfernt Einstellungen für virtuelle Ressourcen aus einer Konfiguration des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="50ca4-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="50ca4-105">Wenn sie auf Teile einer "aktuellen" Konfiguration des virtuellen Systems angewendet werden, können ressourcen des aktiven virtuellen Systems als Nebeneffekt entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="50ca4-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="50ca4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="50ca4-106">Syntax</span></span>


```mof
uint32 RemoveBootSourceSettings(
  [in]  CIM_SettingData REF BootSourceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="50ca4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="50ca4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50ca4-108">*BootSourceSettings* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="50ca4-108">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50ca4-109">Verweis auf ein Array von [**CIM \_ SettingData,**](cim-settingdata.md) das die zu entfernende Startquelleinstellung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="50ca4-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the boot source settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="50ca4-110">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="50ca4-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50ca4-111">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="50ca4-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50ca4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50ca4-112">Return value</span></span>

<span data-ttu-id="50ca4-113">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="50ca4-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="50ca4-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="50ca4-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="50ca4-115">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="50ca4-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="50ca4-116">**Fehler** (2)</span><span class="sxs-lookup"><span data-stu-id="50ca4-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="50ca4-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="50ca4-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="50ca4-118">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="50ca4-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="50ca4-119">**Ungültiger Zustand** (5)</span><span class="sxs-lookup"><span data-stu-id="50ca4-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="50ca4-120">**DMTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="50ca4-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="50ca4-121">**Methodenparameter überprüft** – Auftrag gestartet (4096)</span><span class="sxs-lookup"><span data-stu-id="50ca4-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="50ca4-122">**Reservierte Methode** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="50ca4-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="50ca4-123">**Herstellerspezifisch** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="50ca4-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="50ca4-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50ca4-124">Requirements</span></span>



| <span data-ttu-id="50ca4-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50ca4-125">Requirement</span></span> | <span data-ttu-id="50ca4-126">Wert</span><span class="sxs-lookup"><span data-stu-id="50ca4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50ca4-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50ca4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="50ca4-128">nur Windows 10 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50ca4-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="50ca4-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50ca4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="50ca4-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="50ca4-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="50ca4-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="50ca4-131">Namespace</span></span><br/>                | <span data-ttu-id="50ca4-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="50ca4-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="50ca4-133">MOF</span><span class="sxs-lookup"><span data-stu-id="50ca4-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50ca4-134"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="50ca4-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="50ca4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="50ca4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50ca4-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="50ca4-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="50ca4-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="50ca4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ca4-138">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="50ca4-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

