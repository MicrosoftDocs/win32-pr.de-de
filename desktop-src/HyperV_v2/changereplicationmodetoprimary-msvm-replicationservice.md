---
description: Ändert die erweiterte Replikations Beziehung zur primären Beziehung für einen virtuellen Replikat Computer. Der virtuelle Replikat Computer muss den Status "Failover committet" aufweisen.
ms.assetid: B593A155-B5E6-44E5-8835-09DEB1FF868E
title: 'Msvm_ReplicationService:: changereplicationmodetoprimary-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ChangeReplicationModeToPrimary
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0a18b3c9f1003ff7b263f5c6b7cc89abedccfd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346278"
---
# <a name="msvm_replicationservicechangereplicationmodetoprimary-method"></a><span data-ttu-id="04396-104">MSVM \_ replicationservice:: changereplicationmodetoprimary-Methode</span><span class="sxs-lookup"><span data-stu-id="04396-104">Msvm\_ReplicationService::ChangeReplicationModeToPrimary method</span></span>

<span data-ttu-id="04396-105">Ändert die erweiterte Replikations Beziehung zur primären Beziehung für einen virtuellen Replikat Computer.</span><span class="sxs-lookup"><span data-stu-id="04396-105">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="04396-106">Der virtuelle Replikat Computer muss den Status "Failover committet" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="04396-106">The replica virtual machine must be in a failover committed state.</span></span>

## <a name="syntax"></a><span data-ttu-id="04396-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="04396-107">Syntax</span></span>


```C++
uint32 ChangeReplicationModeToPrimary(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="04396-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="04396-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04396-109">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04396-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04396-110">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den diese Methode die erweiterte Replikations Beziehung zur primären Beziehung ändert.</span><span class="sxs-lookup"><span data-stu-id="04396-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which this method changes the extended replication relationship to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="04396-111">*Replicationrelationship* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04396-111">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04396-112">Eine Zeichen folgen Darstellung einer eingebetteten Instanz der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, die die erweiterte Replikations Beziehung definiert, die von dieser Methode in die primäre Beziehung geändert wird.</span><span class="sxs-lookup"><span data-stu-id="04396-112">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the extended replication relationship that this method changes to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="04396-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="04396-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04396-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="04396-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="04396-115">Dieser Verweis kann **null** sein, wenn der Task beendet ist.</span><span class="sxs-lookup"><span data-stu-id="04396-115">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04396-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04396-116">Return value</span></span>

<span data-ttu-id="04396-117">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="04396-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="04396-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="04396-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04396-119">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="04396-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="04396-120">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="04396-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="04396-121">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="04396-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="04396-122">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="04396-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="04396-123">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="04396-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="04396-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="04396-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="04396-125">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="04396-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="04396-126">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="04396-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="04396-127">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="04396-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="04396-128">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="04396-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="04396-129">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="04396-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="04396-130">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="04396-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="04396-131">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="04396-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="04396-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04396-132">Requirements</span></span>



| <span data-ttu-id="04396-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04396-133">Requirement</span></span> | <span data-ttu-id="04396-134">Wert</span><span class="sxs-lookup"><span data-stu-id="04396-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04396-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04396-135">Minimum supported client</span></span><br/> | <span data-ttu-id="04396-136">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="04396-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="04396-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04396-137">Minimum supported server</span></span><br/> | <span data-ttu-id="04396-138">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04396-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="04396-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="04396-139">Namespace</span></span><br/>                | <span data-ttu-id="04396-140">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="04396-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="04396-141">MOF</span><span class="sxs-lookup"><span data-stu-id="04396-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04396-142"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="04396-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04396-143">DLL</span><span class="sxs-lookup"><span data-stu-id="04396-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04396-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04396-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="04396-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04396-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04396-146">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="04396-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

