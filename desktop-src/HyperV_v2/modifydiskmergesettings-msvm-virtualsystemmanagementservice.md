---
description: Ändert die Daten der Datenträger zusammenlaufseinstellung.
ms.assetid: 91775dc5-105a-4e38-a334-fb34dd4e59f8
title: Modifydiskmergesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyDiskMergeSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe737c084b4c1c76a411ce1d2eba513554b40f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373116"
---
# <a name="modifydiskmergesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="e6ff3-103">Modifydiskmergesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="e6ff3-103">ModifyDiskMergeSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="e6ff3-104">Ändert die Daten der Datenträger zusammenlaufseinstellung.</span><span class="sxs-lookup"><span data-stu-id="e6ff3-104">Modifies the disk merge setting data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6ff3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6ff3-105">Syntax</span></span>


```mof
uint32 ModifyDiskMergeSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e6ff3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6ff3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6ff3-107">*SettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6ff3-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff3-108">Eine eingebettete Instanz der [**MSVM \_ diskmergesettingdata**](msvm-diskmergesettingdata.md) -Klasse, die geänderte Einstellungsdaten für die Datenträger-Merge-Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="e6ff3-108">An embedded instance of the [**Msvm\_DiskMergeSettingData**](msvm-diskmergesettingdata.md) class that contains modified setting data for the disk merge function.</span></span>

</dd> <dt>

<span data-ttu-id="e6ff3-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e6ff3-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff3-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="e6ff3-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6ff3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6ff3-111">Return value</span></span>

<span data-ttu-id="e6ff3-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="e6ff3-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e6ff3-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="e6ff3-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6ff3-114">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="e6ff3-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e6ff3-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="e6ff3-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e6ff3-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="e6ff3-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e6ff3-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="e6ff3-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e6ff3-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="e6ff3-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e6ff3-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="e6ff3-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e6ff3-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="e6ff3-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e6ff3-121">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="e6ff3-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e6ff3-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="e6ff3-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e6ff3-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="e6ff3-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e6ff3-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="e6ff3-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e6ff3-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="e6ff3-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e6ff3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6ff3-126">Requirements</span></span>



| <span data-ttu-id="e6ff3-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6ff3-127">Requirement</span></span> | <span data-ttu-id="e6ff3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e6ff3-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ff3-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6ff3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e6ff3-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6ff3-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e6ff3-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6ff3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e6ff3-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6ff3-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6ff3-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6ff3-133">Namespace</span></span><br/>                | <span data-ttu-id="e6ff3-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e6ff3-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e6ff3-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e6ff3-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6ff3-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e6ff3-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6ff3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e6ff3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6ff3-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6ff3-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e6ff3-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6ff3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6ff3-140">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="e6ff3-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

