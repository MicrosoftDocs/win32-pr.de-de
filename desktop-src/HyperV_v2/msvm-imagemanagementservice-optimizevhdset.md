---
description: Optimiert eine VHD-Datei Satz Datei, um weniger Speicherplatz zu verwenden.
ms.assetid: 2d2f4531-5d2d-4334-bcc2-d3d3c15b1f46
title: Optimizevhdset-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.OptimizeVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c360dcd8acf0a4721b8921cd2ca914c34002d078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862935"
---
# <a name="optimizevhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="b386b-103">Optimizevhdset-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="b386b-103">OptimizeVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="b386b-104">Optimiert eine VHD-Datei Satz Datei, um weniger Speicherplatz zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b386b-104">Optimizes a VHD Set file to use less disk space.</span></span>

## <a name="syntax"></a><span data-ttu-id="b386b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b386b-105">Syntax</span></span>


```mof
uint32 OptimizeVHDSet(
  [in]  string              VHDSetPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b386b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b386b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b386b-107">*Vhdsetpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b386b-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b386b-108">Ein voll qualifizierter Pfad, der den Speicherort der VHD-Satz Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="b386b-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="b386b-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b386b-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b386b-110">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="b386b-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b386b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b386b-111">Return value</span></span>

<span data-ttu-id="b386b-112">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="b386b-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="b386b-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="b386b-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b386b-114">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="b386b-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b386b-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="b386b-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b386b-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="b386b-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b386b-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="b386b-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b386b-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="b386b-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b386b-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="b386b-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b386b-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="b386b-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b386b-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="b386b-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b386b-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="b386b-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b386b-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="b386b-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b386b-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="b386b-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b386b-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="b386b-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b386b-126">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="b386b-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b386b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b386b-127">Requirements</span></span>



| <span data-ttu-id="b386b-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b386b-128">Requirement</span></span> | <span data-ttu-id="b386b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b386b-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b386b-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b386b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b386b-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b386b-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b386b-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b386b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b386b-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b386b-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b386b-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="b386b-134">Namespace</span></span><br/>                | <span data-ttu-id="b386b-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b386b-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b386b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b386b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b386b-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b386b-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b386b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b386b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b386b-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b386b-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b386b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b386b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b386b-141">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="b386b-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




