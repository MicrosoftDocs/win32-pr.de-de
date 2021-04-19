---
description: Exportiert den Verweis Punkt des virtuellen Systems.
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Exportreferencepoint-Methode der Msvm_VirtualSystemReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bedd051123e4f75d7438b2e3831a84204ff4aec3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106357152"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="81502-103">Exportreferencepoint-Methode der MSVM \_ virtualsystemreferencepointservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="81502-103">ExportReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="81502-104">Exportiert den Verweis Punkt des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="81502-104">Exports the reference point of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="81502-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="81502-105">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="81502-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="81502-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81502-107">*Referencepoint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81502-107">*ReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81502-108">Ein Verweis auf die [**MSVM \_ virtualsystemreferencepoint**](msvm-virtualsystemreferencepoint.md) -Instanz, die den zu exportierenden Referenzpunkt darstellt.</span><span class="sxs-lookup"><span data-stu-id="81502-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="81502-109">*Exportdirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81502-109">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81502-110">Der voll qualifizierte Pfad des Verzeichnisses, in das der Verweis Punkt exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="81502-110">The fully-qualified path of the directory to which the reference point is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="81502-111">*Exportsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81502-111">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81502-112">Eine Instanz von [**MSVM \_ virtualsystemreferencepointexportsettingdata**](msvm-virtualsystemreferencepointexportsettingdata.md) , die die Einstellungen für den Export Vorgang darstellt.</span><span class="sxs-lookup"><span data-stu-id="81502-112">An instance of [**Msvm\_VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="81502-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="81502-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81502-114">Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="81502-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="81502-115">Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.</span><span class="sxs-lookup"><span data-stu-id="81502-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81502-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81502-116">Return value</span></span>

<span data-ttu-id="81502-117">Bei Erfolg wird 0 (abgeschlossen ohne Fehler) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81502-117">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="81502-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="81502-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81502-119">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="81502-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="81502-120">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="81502-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="81502-121">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="81502-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="81502-122">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="81502-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="81502-123">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="81502-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="81502-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="81502-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="81502-125">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="81502-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="81502-126">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="81502-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="81502-127">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="81502-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="81502-128">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="81502-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="81502-129">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="81502-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="81502-130">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="81502-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="81502-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81502-131">Requirements</span></span>



| <span data-ttu-id="81502-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81502-132">Requirement</span></span> | <span data-ttu-id="81502-133">Wert</span><span class="sxs-lookup"><span data-stu-id="81502-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81502-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81502-134">Minimum supported client</span></span><br/> | <span data-ttu-id="81502-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81502-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="81502-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81502-136">Minimum supported server</span></span><br/> | <span data-ttu-id="81502-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="81502-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="81502-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="81502-138">Namespace</span></span><br/>                | <span data-ttu-id="81502-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="81502-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="81502-140">MOF</span><span class="sxs-lookup"><span data-stu-id="81502-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81502-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="81502-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81502-142">DLL</span><span class="sxs-lookup"><span data-stu-id="81502-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81502-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81502-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81502-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81502-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81502-145">**MSVM \_ virtualsystemreferencepointservice**</span><span class="sxs-lookup"><span data-stu-id="81502-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




