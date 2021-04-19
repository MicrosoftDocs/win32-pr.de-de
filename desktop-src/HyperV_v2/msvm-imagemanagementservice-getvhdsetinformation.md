---
description: Ruft Informationen zu einer VHD-Datei ab.
ms.assetid: efdfd4c6-b762-4369-add3-e152652c6802
title: Getvhdsetinformation-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSetInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cdcf4a354e6d6b47b6a67c071daf8883905f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348209"
---
# <a name="getvhdsetinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="acc72-103">Getvhdsetinformation-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="acc72-103">GetVHDSetInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="acc72-104">Ruft Informationen zu einer VHD-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="acc72-104">Retrieves information about a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="acc72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="acc72-105">Syntax</span></span>


```mof
uint32 GetVHDSetInformation(
  [in]  string              VHDSetPath,
  [in]  uint32              AdditionalInformation[],
  [out] string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="acc72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="acc72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acc72-107">*Vhdsetpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="acc72-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acc72-108">Ein voll qualifizierter Pfad, der den Speicherort der VHD-Satz Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="acc72-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="acc72-109">*AdditionalInformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="acc72-109">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acc72-110">Ein Array, das angibt, welche zusätzlichen Informationen über die VHD-Satz Datei erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="acc72-110">An array specifying what additional information should be gathered about the VHD Set file.</span></span> <span data-ttu-id="acc72-111">Jeder Eintrag im Array ist ein Typ zusätzlicher Informationen.</span><span class="sxs-lookup"><span data-stu-id="acc72-111">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="acc72-112">Wenn dieser Parameter NULL ist, werden keine zusätzlichen Informationen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="acc72-112">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="acc72-113">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="acc72-113">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="acc72-114">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="acc72-114">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Paths"></span><span id="paths"></span><span id="PATHS"></span>

<span data-ttu-id="acc72-115">**Pfade** (2)</span><span class="sxs-lookup"><span data-stu-id="acc72-115">**Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="acc72-116">*Informationen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="acc72-116">*Information* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acc72-117">Bei erfolgreicher Ausführung enthält dieses Objekt die Informationen für die angeforderte VHD-Satz Datei.</span><span class="sxs-lookup"><span data-stu-id="acc72-117">If successful, this object contains the information for the requested VHD Set file.</span></span> <span data-ttu-id="acc72-118">Dabei handelt es sich um eine eingebettete Instanz von [**MSVM \_ vhdsetinformation**](msvm-vhdsetinformation.md).</span><span class="sxs-lookup"><span data-stu-id="acc72-118">This is an embedded instance of [**Msvm\_VHDSetInformation**](msvm-vhdsetinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="acc72-119">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="acc72-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acc72-120">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="acc72-120">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acc72-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="acc72-121">Return value</span></span>

<span data-ttu-id="acc72-122">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="acc72-122">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="acc72-123">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="acc72-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="acc72-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="acc72-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="acc72-125">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="acc72-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="acc72-126">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="acc72-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="acc72-127">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="acc72-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="acc72-128">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="acc72-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="acc72-129">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="acc72-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="acc72-130">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="acc72-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="acc72-131">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="acc72-131">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="acc72-132">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="acc72-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="acc72-133">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="acc72-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="acc72-134">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="acc72-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="acc72-135">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="acc72-135">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="acc72-136">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="acc72-136">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="acc72-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acc72-137">Requirements</span></span>



| <span data-ttu-id="acc72-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acc72-138">Requirement</span></span> | <span data-ttu-id="acc72-139">Wert</span><span class="sxs-lookup"><span data-stu-id="acc72-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acc72-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="acc72-140">Minimum supported client</span></span><br/> | <span data-ttu-id="acc72-141">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acc72-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="acc72-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="acc72-142">Minimum supported server</span></span><br/> | <span data-ttu-id="acc72-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="acc72-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="acc72-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="acc72-144">Namespace</span></span><br/>                | <span data-ttu-id="acc72-145">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="acc72-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="acc72-146">MOF</span><span class="sxs-lookup"><span data-stu-id="acc72-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acc72-147"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="acc72-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="acc72-148">DLL</span><span class="sxs-lookup"><span data-stu-id="acc72-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acc72-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="acc72-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="acc72-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acc72-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc72-151">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="acc72-151">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




