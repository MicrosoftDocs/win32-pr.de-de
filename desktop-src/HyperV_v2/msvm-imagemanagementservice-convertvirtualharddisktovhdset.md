---
description: Konvertiert eine virtuelle Festplatten Datei, indem eine neue VHD-Datei mit der vorhandenen virtuellen Festplatte erstellt wird.
ms.assetid: 04ae723e-e3c5-4640-a0e5-0e1b75bb2e6d
title: Convertvirtualharddisktovhdset-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDiskToVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6113a14f321ff7319f8be15767621db3a7e833de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960716"
---
# <a name="convertvirtualharddisktovhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="dd78d-103">Convertvirtualharddisktovhdset-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd78d-103">ConvertVirtualHardDiskToVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="dd78d-104">Konvertiert eine virtuelle Festplatten Datei, indem eine neue VHD-Datei mit der vorhandenen virtuellen Festplatte erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="dd78d-104">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd78d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd78d-105">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDiskToVHDSet(
  [in]  string              VirtualHardDiskPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="dd78d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd78d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd78d-107">*Virtualharddiskpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd78d-107">*VirtualHardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd78d-108">Zeichenfolge, die den Pfad zur virtuellen Festplatten Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="dd78d-108">String containing the path to the virtual hard disk file.</span></span> <span data-ttu-id="dd78d-109">Die neue VHD-Satz Datei hat denselben Dateinamen, aber mit dem. VHDs-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="dd78d-109">The new VHD Set file will have the same filename but with the .VHDS extension.</span></span>

</dd> <dt>

<span data-ttu-id="dd78d-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dd78d-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd78d-111">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="dd78d-111">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd78d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd78d-112">Return value</span></span>

<span data-ttu-id="dd78d-113">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="dd78d-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="dd78d-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="dd78d-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd78d-115">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="dd78d-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dd78d-116">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="dd78d-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dd78d-117">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="dd78d-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dd78d-118">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="dd78d-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dd78d-119">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="dd78d-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dd78d-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="dd78d-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dd78d-121">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="dd78d-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dd78d-122">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="dd78d-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dd78d-123">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="dd78d-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dd78d-124">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="dd78d-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dd78d-125">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="dd78d-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dd78d-126">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="dd78d-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="dd78d-127">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="dd78d-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dd78d-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd78d-128">Requirements</span></span>



| <span data-ttu-id="dd78d-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd78d-129">Requirement</span></span> | <span data-ttu-id="dd78d-130">Wert</span><span class="sxs-lookup"><span data-stu-id="dd78d-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd78d-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd78d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dd78d-132">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd78d-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="dd78d-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd78d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dd78d-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dd78d-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="dd78d-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd78d-135">Namespace</span></span><br/>                | <span data-ttu-id="dd78d-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="dd78d-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dd78d-137">MOF</span><span class="sxs-lookup"><span data-stu-id="dd78d-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd78d-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dd78d-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd78d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="dd78d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd78d-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd78d-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd78d-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd78d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd78d-142">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="dd78d-142">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




