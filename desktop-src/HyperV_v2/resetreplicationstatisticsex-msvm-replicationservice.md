---
description: Setzt Replikations Statistiken zurück, die der angegebenen Replikations Beziehung der angegebenen virtuellen Maschine zugeordnet sind.
ms.assetid: 6E49A7C0-2F60-444E-964E-420470EE1538
title: 'Msvm_ReplicationService:: recationstatisticsex-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c1acb234660e71636b4a69a697b11385d65cf1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866384"
---
# <a name="msvm_replicationserviceresetreplicationstatisticsex-method"></a><span data-ttu-id="30cbb-103">MSVM \_ replicationservice:: remintreplicationstatisticsex-Methode</span><span class="sxs-lookup"><span data-stu-id="30cbb-103">Msvm\_ReplicationService::ResetReplicationStatisticsEx method</span></span>

<span data-ttu-id="30cbb-104">Setzt Replikations Statistiken zurück, die der angegebenen Replikations Beziehung der angegebenen virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="30cbb-104">Resets replication statistics that are associated with the specified replication relationship of the specified virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="30cbb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="30cbb-105">Syntax</span></span>


```C++
uint32 ResetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="30cbb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30cbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30cbb-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30cbb-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cbb-108">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die die Replikat aktivierte virtuelle Maschine darstellt.</span><span class="sxs-lookup"><span data-stu-id="30cbb-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the replica-enabled virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="30cbb-109">*Replicationrelationship* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30cbb-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cbb-110">Eine Zeichen folgen Darstellung einer eingebetteten Instanz der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, die die Replikations Beziehung definiert, für die die Replikations Statistiken zurückgesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30cbb-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to reset the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="30cbb-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="30cbb-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30cbb-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="30cbb-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="30cbb-113">Dieser Verweis kann **null** sein, wenn der Task beendet ist.</span><span class="sxs-lookup"><span data-stu-id="30cbb-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30cbb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30cbb-114">Return value</span></span>

<span data-ttu-id="30cbb-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="30cbb-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="30cbb-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="30cbb-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="30cbb-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="30cbb-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="30cbb-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="30cbb-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="30cbb-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="30cbb-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="30cbb-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="30cbb-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="30cbb-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="30cbb-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="30cbb-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="30cbb-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="30cbb-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="30cbb-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="30cbb-124">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="30cbb-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="30cbb-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="30cbb-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="30cbb-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="30cbb-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="30cbb-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="30cbb-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="30cbb-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="30cbb-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="30cbb-129">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="30cbb-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="30cbb-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30cbb-130">Requirements</span></span>



| <span data-ttu-id="30cbb-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30cbb-131">Requirement</span></span> | <span data-ttu-id="30cbb-132">Wert</span><span class="sxs-lookup"><span data-stu-id="30cbb-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30cbb-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30cbb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="30cbb-134">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="30cbb-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="30cbb-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30cbb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="30cbb-136">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30cbb-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="30cbb-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="30cbb-137">Namespace</span></span><br/>                | <span data-ttu-id="30cbb-138">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="30cbb-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="30cbb-139">MOF</span><span class="sxs-lookup"><span data-stu-id="30cbb-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30cbb-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="30cbb-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="30cbb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="30cbb-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30cbb-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="30cbb-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="30cbb-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30cbb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30cbb-144">**Getreplicationstatisticsex**</span><span class="sxs-lookup"><span data-stu-id="30cbb-144">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="30cbb-145">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="30cbb-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

