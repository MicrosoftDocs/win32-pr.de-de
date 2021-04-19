---
description: Entfernt die angegebene Replikations Beziehung der virtuellen Maschine.
ms.assetid: 0D5013CE-7BAE-4A99-ABF2-F1ECC644A1B2
title: 'Msvm_ReplicationService:: removereplicationrelationshipex-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationshipEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c57ed7f9a88789d04a20de0fd199d460b47c1eb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346979"
---
# <a name="msvm_replicationserviceremovereplicationrelationshipex-method"></a><span data-ttu-id="2f963-103">MSVM \_ replicationservice:: removereplicationrelationshipex-Methode</span><span class="sxs-lookup"><span data-stu-id="2f963-103">Msvm\_ReplicationService::RemoveReplicationRelationshipEx method</span></span>

<span data-ttu-id="2f963-104">Entfernt die angegebene Replikations Beziehung der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="2f963-104">Removes the specified virtual machine replication relationship.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f963-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f963-105">Syntax</span></span>


```C++
uint32 RemoveReplicationRelationshipEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="2f963-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f963-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f963-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f963-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f963-108">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die Replikation entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f963-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to remove the replication.</span></span>

</dd> <dt>

<span data-ttu-id="2f963-109">*Replicationrelationship* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f963-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f963-110">Eine Zeichen folgen Darstellung einer eingebetteten Instanz der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, die die zu entfernende Replikations Beziehung definiert.</span><span class="sxs-lookup"><span data-stu-id="2f963-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship to remove.</span></span>

</dd> <dt>

<span data-ttu-id="2f963-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2f963-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f963-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="2f963-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="2f963-113">Dieser Verweis kann **null** sein, wenn der Task beendet ist.</span><span class="sxs-lookup"><span data-stu-id="2f963-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f963-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f963-114">Return value</span></span>

<span data-ttu-id="2f963-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="2f963-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2f963-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="2f963-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2f963-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="2f963-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2f963-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="2f963-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2f963-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="2f963-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2f963-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="2f963-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2f963-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="2f963-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2f963-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="2f963-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2f963-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="2f963-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2f963-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="2f963-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2f963-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="2f963-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2f963-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="2f963-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2f963-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="2f963-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2f963-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="2f963-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="2f963-129">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="2f963-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2f963-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f963-130">Remarks</span></span>

<span data-ttu-id="2f963-131">Bei einem virtuellen Replikat Computer kann die primäre Replikation nicht entfernt werden, wenn die erweiterte Replikation aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2f963-131">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f963-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f963-132">Requirements</span></span>



| <span data-ttu-id="2f963-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f963-133">Requirement</span></span> | <span data-ttu-id="2f963-134">Wert</span><span class="sxs-lookup"><span data-stu-id="2f963-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f963-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f963-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2f963-136">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="2f963-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2f963-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f963-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2f963-138">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f963-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2f963-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f963-139">Namespace</span></span><br/>                | <span data-ttu-id="2f963-140">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2f963-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="2f963-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2f963-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f963-142"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2f963-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f963-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2f963-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f963-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f963-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2f963-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f963-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f963-146">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="2f963-146">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="2f963-147">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="2f963-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

