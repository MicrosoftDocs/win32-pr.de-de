---
description: Bearbeitet einen VHD-momentaufnahmeneintrag innerhalb einer VHD-Datei. Wenn die fragliche Momentaufnahme-ID bereits vorhanden ist, wird der vorhandene Momentaufnahme Eintrag mit dem neuen Eintrag überschrieben. Andernfalls wird der neue Eintrag der VHD-Satz Datei hinzugefügt.
ms.assetid: dd14960d-3fb8-4d47-986f-fbbbb08eb37d
title: Setvhdsnapshotinformation-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 54f5ac23cdf8f49532a05eee3fd23293715cd02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350476"
---
# <a name="setvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="eb476-105">Setvhdsnapshotinformation-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="eb476-105">SetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="eb476-106">Bearbeitet einen VHD-momentaufnahmeneintrag innerhalb einer VHD-Datei.</span><span class="sxs-lookup"><span data-stu-id="eb476-106">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="eb476-107">Wenn die fragliche Momentaufnahme-ID bereits vorhanden ist, wird der vorhandene Momentaufnahme Eintrag mit dem neuen Eintrag überschrieben.</span><span class="sxs-lookup"><span data-stu-id="eb476-107">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="eb476-108">Andernfalls wird der neue Eintrag der VHD-Satz Datei hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="eb476-108">Otherwise, the new entry will be added to the VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb476-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb476-109">Syntax</span></span>


```mof
uint32 SetVHDSnapshotInformation(
  [in]  string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="eb476-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb476-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb476-111">*Informationen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb476-111">*Information* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb476-112">Informationen zu VHD-Momentaufnahmen, die geändert oder in der VHD-Satz Datei hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eb476-112">VHD Snapshot Information to be changed or added in the VHD Set file.</span></span> <span data-ttu-id="eb476-113">Die Zeichenfolge ist eine eingebettete Instanz von [**MSVM \_ vhdsnapshotinformation**](msvm-vhdsnapshotinformation.md).</span><span class="sxs-lookup"><span data-stu-id="eb476-113">The string is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb476-114">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="eb476-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb476-115">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="eb476-115">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb476-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb476-116">Return value</span></span>

<span data-ttu-id="eb476-117">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="eb476-117">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="eb476-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="eb476-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eb476-119">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="eb476-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="eb476-120">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="eb476-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="eb476-121">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="eb476-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="eb476-122">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="eb476-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="eb476-123">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="eb476-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="eb476-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="eb476-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="eb476-125">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="eb476-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="eb476-126">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="eb476-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="eb476-127">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="eb476-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="eb476-128">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="eb476-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="eb476-129">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="eb476-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="eb476-130">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="eb476-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="eb476-131">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="eb476-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="eb476-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb476-132">Requirements</span></span>



| <span data-ttu-id="eb476-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb476-133">Requirement</span></span> | <span data-ttu-id="eb476-134">Wert</span><span class="sxs-lookup"><span data-stu-id="eb476-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb476-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb476-135">Minimum supported client</span></span><br/> | <span data-ttu-id="eb476-136">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb476-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="eb476-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb476-137">Minimum supported server</span></span><br/> | <span data-ttu-id="eb476-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="eb476-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="eb476-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb476-139">Namespace</span></span><br/>                | <span data-ttu-id="eb476-140">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="eb476-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eb476-141">MOF</span><span class="sxs-lookup"><span data-stu-id="eb476-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb476-142"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eb476-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb476-143">DLL</span><span class="sxs-lookup"><span data-stu-id="eb476-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb476-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eb476-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eb476-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb476-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb476-146">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="eb476-146">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




