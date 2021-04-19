---
description: Löscht einen Eintrag für eine VHD-Momentaufnahme in einer VHD-Satz Datei.
ms.assetid: 37d55a5f-209d-42ce-8f69-8b494055e263
title: Deletevhdsnapshot-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.DeleteVHDSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5c7f3f115825aedb3a21a8f33326a712c52e0780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350477"
---
# <a name="deletevhdsnapshot-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="48e99-103">Deletevhdsnapshot-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="48e99-103">DeleteVHDSnapshot method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="48e99-104">Löscht einen Eintrag für eine VHD-Momentaufnahme in einer VHD-Satz Datei.</span><span class="sxs-lookup"><span data-stu-id="48e99-104">Deletes a VHD Snapshot entry within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e99-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48e99-105">Syntax</span></span>


```mof
uint32 DeleteVHDSnapshot(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotId,
  [in]  boolean             PersistReferenceSnapshot,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="48e99-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48e99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48e99-107">*Vhdsetpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48e99-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e99-108">Zeichenfolge, die den Pfad zur VHD-Satz Datei enthält, die die betreffende Momentaufnahme enthält.</span><span class="sxs-lookup"><span data-stu-id="48e99-108">String containing the path to the VHD Set file containing the snapshot in question.</span></span>

</dd> <dt>

<span data-ttu-id="48e99-109">*Snapshotid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48e99-109">*SnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e99-110">Eine GUID, die die Momentaufnahme-ID für den zu löschenden Eintrag der VHD-Momentaufnahme darstellt.</span><span class="sxs-lookup"><span data-stu-id="48e99-110">A GUID representing the Snapshot ID for the VHD Snapshot entry to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="48e99-111">*Persistreferencesnapshot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48e99-111">*PersistReferenceSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e99-112">Gibt an, ob ein Verweis basierter Momentaufnahme Daten Satz nach dem Löschen der Momentaufnahme beibehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="48e99-112">Whether or not a reference-only snapshot record should be persisted after the snapshot is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="48e99-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="48e99-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48e99-114">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="48e99-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48e99-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48e99-115">Return value</span></span>

<span data-ttu-id="48e99-116">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="48e99-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="48e99-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="48e99-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="48e99-118">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="48e99-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="48e99-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="48e99-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="48e99-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="48e99-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="48e99-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="48e99-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="48e99-122">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="48e99-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="48e99-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="48e99-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="48e99-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="48e99-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="48e99-125">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="48e99-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="48e99-126">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="48e99-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="48e99-127">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="48e99-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="48e99-128">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="48e99-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="48e99-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="48e99-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="48e99-130">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="48e99-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="48e99-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48e99-131">Requirements</span></span>



| <span data-ttu-id="48e99-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48e99-132">Requirement</span></span> | <span data-ttu-id="48e99-133">Wert</span><span class="sxs-lookup"><span data-stu-id="48e99-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48e99-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48e99-134">Minimum supported client</span></span><br/> | <span data-ttu-id="48e99-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48e99-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="48e99-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48e99-136">Minimum supported server</span></span><br/> | <span data-ttu-id="48e99-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="48e99-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="48e99-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="48e99-138">Namespace</span></span><br/>                | <span data-ttu-id="48e99-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="48e99-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="48e99-140">MOF</span><span class="sxs-lookup"><span data-stu-id="48e99-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48e99-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="48e99-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="48e99-142">DLL</span><span class="sxs-lookup"><span data-stu-id="48e99-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48e99-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="48e99-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="48e99-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48e99-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e99-145">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="48e99-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




