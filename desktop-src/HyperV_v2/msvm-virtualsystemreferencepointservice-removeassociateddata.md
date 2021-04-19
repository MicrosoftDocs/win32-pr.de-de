---
description: Entfernt das dem Bezugspunkt zugeordnete Datenprotokoll.
ms.assetid: b6206bda-c195-4c6f-9b80-508c20b53ce5
title: Removeassociateddata-Methode der Msvm_VirtualSystemReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c0d67502d349f0b0dac7cbf9a1998dcd6db0fb4a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353633"
---
# <a name="removeassociateddata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="22d3b-103">Removeassociateddata-Methode der MSVM \_ virtualsystemreferencepointservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="22d3b-103">RemoveAssociatedData method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="22d3b-104">Entfernt das dem Bezugspunkt zugeordnete Datenprotokoll.</span><span class="sxs-lookup"><span data-stu-id="22d3b-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="22d3b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22d3b-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="22d3b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22d3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22d3b-107">*Affectedreferencepoint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22d3b-107">*AffectedReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22d3b-108">Ein Verweis auf die [**MSVM \_ virtualsystemreferencepoint**](msvm-virtualsystemreferencepoint.md) -Instanz, die den zu entfernenden Bezugspunkt darstellt.</span><span class="sxs-lookup"><span data-stu-id="22d3b-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="22d3b-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="22d3b-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22d3b-110">Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="22d3b-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="22d3b-111">Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.</span><span class="sxs-lookup"><span data-stu-id="22d3b-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22d3b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22d3b-112">Return value</span></span>

<span data-ttu-id="22d3b-113">Bei Erfolg wird 0 (abgeschlossen ohne Fehler) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="22d3b-113">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="22d3b-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="22d3b-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22d3b-115">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="22d3b-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="22d3b-116">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="22d3b-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="22d3b-117">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="22d3b-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="22d3b-118">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="22d3b-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="22d3b-119">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="22d3b-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="22d3b-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="22d3b-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="22d3b-121">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="22d3b-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="22d3b-122">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="22d3b-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="22d3b-123">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="22d3b-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="22d3b-124">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="22d3b-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="22d3b-125">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="22d3b-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="22d3b-126">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="22d3b-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="22d3b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22d3b-127">Requirements</span></span>



| <span data-ttu-id="22d3b-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22d3b-128">Requirement</span></span> | <span data-ttu-id="22d3b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="22d3b-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d3b-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22d3b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="22d3b-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22d3b-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="22d3b-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22d3b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="22d3b-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="22d3b-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="22d3b-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="22d3b-134">Namespace</span></span><br/>                | <span data-ttu-id="22d3b-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="22d3b-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="22d3b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="22d3b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22d3b-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="22d3b-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="22d3b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="22d3b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22d3b-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="22d3b-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="22d3b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22d3b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d3b-141">**MSVM \_ virtualsystemreferencepointservice**</span><span class="sxs-lookup"><span data-stu-id="22d3b-141">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




