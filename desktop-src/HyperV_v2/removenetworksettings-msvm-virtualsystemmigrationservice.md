---
description: Entfernt die Subnetze des Migrationsnetzwerks aus dem virtuellen System Migrationsdienst.
ms.assetid: 6ae8de07-552b-4525-8806-bfb9da73bd42
title: Removenetworksettings-Methode der Msvm_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.RemoveNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66b7a9fd1ce29d9dd645242ec7cda346f79a6f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343337"
---
# <a name="removenetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="3df1a-103">Removenetworksettings-Methode der MSVM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="3df1a-103">RemoveNetworkSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="3df1a-104">Entfernt die Subnetze des Migrationsnetzwerks aus dem virtuellen System Migrationsdienst.</span><span class="sxs-lookup"><span data-stu-id="3df1a-104">Removes migration network subnets from the virtual system migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df1a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3df1a-105">Syntax</span></span>


```mof
uint32 RemoveNetworkSettings(
  [in]  Msvm_VirtualSystemMigrationNetworkSettingData REF NetworkSettings[],
  [out] CIM_ConcreteJob                               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3df1a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3df1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df1a-107">*Network Settings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3df1a-107">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3df1a-108">Ein Array von eingebetteten Instanzen der [**MSVM \_ virtualsystemmigrationnetworksettingdata**](msvm-virtualsystemmigrationnetworksettingdata.md) -Klasse, die die zu entfernenden Netzwerksubnetze darstellen.</span><span class="sxs-lookup"><span data-stu-id="3df1a-108">An array of embedded instances of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that represent the network subnets to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="3df1a-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3df1a-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3df1a-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="3df1a-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3df1a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3df1a-111">Return value</span></span>

<span data-ttu-id="3df1a-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="3df1a-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3df1a-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3df1a-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3df1a-114">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="3df1a-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3df1a-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="3df1a-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3df1a-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="3df1a-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3df1a-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="3df1a-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3df1a-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="3df1a-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3df1a-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3df1a-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3df1a-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="3df1a-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3df1a-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="3df1a-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3df1a-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="3df1a-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3df1a-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="3df1a-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3df1a-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="3df1a-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3df1a-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="3df1a-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3df1a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3df1a-126">Requirements</span></span>



| <span data-ttu-id="3df1a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3df1a-127">Requirement</span></span> | <span data-ttu-id="3df1a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3df1a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3df1a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3df1a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3df1a-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3df1a-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3df1a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3df1a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3df1a-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3df1a-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3df1a-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="3df1a-133">Namespace</span></span><br/>                | <span data-ttu-id="3df1a-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3df1a-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3df1a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="3df1a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3df1a-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3df1a-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3df1a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3df1a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3df1a-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3df1a-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3df1a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3df1a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df1a-140">**Addnetworksettings**</span><span class="sxs-lookup"><span data-stu-id="3df1a-140">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="3df1a-141">**Modifynetworksettings**</span><span class="sxs-lookup"><span data-stu-id="3df1a-141">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="3df1a-142">**MSVM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="3df1a-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

