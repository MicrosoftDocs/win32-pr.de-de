---
description: Generiert ein undurchsichtiges BLOB von Daten, das Kompatibilitätsinformationen für das angegebene System enthält.
ms.assetid: 5cfb50c4-d695-4867-ac6a-234ce5120a6d
title: Getsystemcompatibilityinfo-Methode der Msvm_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b0326dfb39123e508e9c5fefbd0404288cb97b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344258"
---
# <a name="getsystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="ef40f-103">Getsystemcompatibilityinfo-Methode der MSVM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="ef40f-103">GetSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="ef40f-104">Generiert ein undurchsichtiges BLOB von Daten, das Kompatibilitätsinformationen für das angegebene System enthält.</span><span class="sxs-lookup"><span data-stu-id="ef40f-104">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span> <span data-ttu-id="ef40f-105">Diese Methode wird in Verbindung mit der [**checksystemcompatibilityinfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) -Methode verwendet, um zu bestimmen, ob eine schnelle oder Live Migration eines virtuellen Computers zu einem anderen Host Computersystem möglich ist, ohne tatsächlich die Migration durchführen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="ef40f-105">This method is used in conjunction with the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method to determine whether a quick or live migration of a virtual machine to another hosting computer system is possible without actually attempting the migration.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef40f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef40f-106">Syntax</span></span>


```mof
uint32 GetSystemCompatibilityInfo(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] uint8                  CompatibilityInfo[]
);
```



## <a name="parameters"></a><span data-ttu-id="ef40f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef40f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef40f-108">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef40f-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef40f-109">Ein Verweis auf eine [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer darstellt, für den Kompatibilitätsinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ef40f-109">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to retrieve compatibility information for.</span></span> <span data-ttu-id="ef40f-110">Wenn sich dieser Parameter auf das hostingcomputersystem bezieht, können die im *compatibilityinfo* -Parameter zurückgegebenen Daten verwendet werden, um zu bestimmen, ob eine der virtuellen Maschinen auf dem Host Computersystem schnell zu einem anderen Host Computersystem migriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef40f-110">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityInfo* parameter can be used to determine whether any of the virtual machines on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="ef40f-111">*Compatibilityinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ef40f-111">*CompatibilityInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef40f-112">Ein undurchsichtiges BLOB von Daten, die an die [**checksystemcompatibilityinfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) -Methode auf einem anderen Host Computersystem weitergegeben werden können, um die Kompatibilität zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="ef40f-112">An opaque blob of data that can be passed to the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on another hosting computer system to confirm compatibility.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef40f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef40f-113">Return value</span></span>

<span data-ttu-id="ef40f-114">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="ef40f-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ef40f-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="ef40f-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ef40f-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="ef40f-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ef40f-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="ef40f-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ef40f-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="ef40f-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ef40f-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="ef40f-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ef40f-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="ef40f-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ef40f-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="ef40f-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ef40f-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="ef40f-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ef40f-123">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="ef40f-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ef40f-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="ef40f-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ef40f-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="ef40f-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ef40f-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="ef40f-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ef40f-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="ef40f-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ef40f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef40f-128">Requirements</span></span>



| <span data-ttu-id="ef40f-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef40f-129">Requirement</span></span> | <span data-ttu-id="ef40f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="ef40f-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef40f-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef40f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ef40f-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef40f-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ef40f-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef40f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ef40f-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef40f-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef40f-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef40f-135">Namespace</span></span><br/>                | <span data-ttu-id="ef40f-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ef40f-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ef40f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="ef40f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef40f-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ef40f-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef40f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ef40f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef40f-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef40f-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef40f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef40f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef40f-142">**MSVM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="ef40f-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




