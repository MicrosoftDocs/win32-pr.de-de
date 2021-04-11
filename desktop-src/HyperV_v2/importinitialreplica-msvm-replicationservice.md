---
description: Importiert die anfängliche Replikation für einen virtuellen Computer.
ms.assetid: 151211fe-e58e-4fd4-87cd-cdb2ad55c0b1
title: Importinitialreplica-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ImportInitialReplica
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b60ab10c6387127c294a472c9e1e86be7fd84146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130701"
---
# <a name="importinitialreplica-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="fea58-103">Importinitialreplica-Methode der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="fea58-103">ImportInitialReplica method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="fea58-104">Importiert die anfängliche Replikation für einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="fea58-104">Imports the initial replication for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="fea58-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fea58-105">Syntax</span></span>


```mof
uint32 ImportInitialReplica(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 InitialReplicationImportLocation,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fea58-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fea58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fea58-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fea58-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fea58-108">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die anfängliche Replikation importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fea58-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the initial replication should be imported.</span></span>

</dd> <dt>

<span data-ttu-id="fea58-109">*Initialreplicationimportlocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fea58-109">*InitialReplicationImportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fea58-110">Der voll qualifizierte Pfad des Verzeichnisses, von dem aus die anfängliche Replikation importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fea58-110">The fully qualified path of the directory from which the initial replication is to be imported.</span></span> <span data-ttu-id="fea58-111">Dieser Wert darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="fea58-111">This cannot be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fea58-112">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fea58-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fea58-113">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="fea58-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fea58-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fea58-114">Return value</span></span>

<span data-ttu-id="fea58-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="fea58-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fea58-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="fea58-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fea58-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="fea58-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fea58-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="fea58-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fea58-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="fea58-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fea58-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="fea58-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fea58-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="fea58-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fea58-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="fea58-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fea58-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="fea58-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fea58-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="fea58-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fea58-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="fea58-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fea58-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="fea58-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fea58-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="fea58-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fea58-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="fea58-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="fea58-129">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="fea58-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fea58-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fea58-130">Requirements</span></span>



| <span data-ttu-id="fea58-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fea58-131">Requirement</span></span> | <span data-ttu-id="fea58-132">Wert</span><span class="sxs-lookup"><span data-stu-id="fea58-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fea58-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fea58-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fea58-134">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fea58-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fea58-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fea58-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fea58-136">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fea58-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fea58-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="fea58-137">Namespace</span></span><br/>                | <span data-ttu-id="fea58-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="fea58-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fea58-139">MOF</span><span class="sxs-lookup"><span data-stu-id="fea58-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fea58-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fea58-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fea58-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fea58-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fea58-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fea58-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fea58-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fea58-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fea58-144">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="fea58-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

