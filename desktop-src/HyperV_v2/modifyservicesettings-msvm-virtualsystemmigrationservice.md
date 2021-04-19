---
description: Ändert die Einstellungsdaten für den Migrationsdienst.
ms.assetid: 5162fe88-dd39-4fe0-b8e9-e9b70c2b6a5c
title: Modifyservicesettings-Methode der Msvm_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e1e9dc96196752ec4408939adc418e7c43bc0c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356927"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="4e809-103">Modifyservicesettings-Methode der MSVM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="4e809-103">ModifyServiceSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="4e809-104">Ändert die Einstellungsdaten für den Migrationsdienst.</span><span class="sxs-lookup"><span data-stu-id="4e809-104">Modifies the setting data for the migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e809-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e809-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4e809-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e809-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e809-107">*Servicesettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e809-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e809-108">Eine eingebettete Instanz der [**MSVM \_ virtualsystemmanagementservicesettingdata**](msvm-virtualsystemmanagementservicesettingdata.md) -Klasse, die die neuen Dienst Einstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="4e809-108">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the new service settings.</span></span>

</dd> <dt>

<span data-ttu-id="4e809-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4e809-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e809-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="4e809-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e809-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e809-111">Return value</span></span>

<span data-ttu-id="4e809-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="4e809-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4e809-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="4e809-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4e809-114">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="4e809-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4e809-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="4e809-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4e809-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="4e809-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4e809-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="4e809-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4e809-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="4e809-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4e809-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="4e809-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4e809-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="4e809-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4e809-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="4e809-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4e809-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="4e809-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4e809-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="4e809-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4e809-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="4e809-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4e809-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="4e809-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4e809-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e809-126">Requirements</span></span>



| <span data-ttu-id="4e809-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e809-127">Requirement</span></span> | <span data-ttu-id="4e809-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4e809-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e809-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e809-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4e809-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e809-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4e809-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e809-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4e809-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e809-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4e809-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e809-133">Namespace</span></span><br/>                | <span data-ttu-id="4e809-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4e809-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4e809-135">MOF</span><span class="sxs-lookup"><span data-stu-id="4e809-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e809-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4e809-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e809-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4e809-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e809-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4e809-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4e809-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e809-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e809-140">**MSVM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="4e809-140">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

