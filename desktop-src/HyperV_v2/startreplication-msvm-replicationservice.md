---
description: Startet die Replikation eines virtuellen Computers.
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: Startreplikation-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.StartReplication
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4702b5b73a989e2889bf1da9e4d284afdfe5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343159"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="ebbea-103">Startreplikation-Methode der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="ebbea-103">StartReplication method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="ebbea-104">Startet die Replikation eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="ebbea-104">Starts the replication of a virtual machine.</span></span> <span data-ttu-id="ebbea-105">Wenn von einem Client diese Methode für einen virtuellen Replikat Computer aufgerufen wird, wird die Replikation mit dem erweiterten Replikat gestartet.</span><span class="sxs-lookup"><span data-stu-id="ebbea-105">When a client calls this method for a replica virtual machine, it starts the replication with extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebbea-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebbea-106">Syntax</span></span>


```mof
uint32 StartReplication(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  uint16                 InitialReplicationType,
  [in]  string                 InitialReplicationExportLocation,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ebbea-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebbea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebbea-108">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebbea-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebbea-109">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die Replikation gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ebbea-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be started.</span></span>

</dd> <dt>

<span data-ttu-id="ebbea-110">*Initialreplicationtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebbea-110">*InitialReplicationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebbea-111">Der Übertragungstyp, der zum Ausführen der ersten Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ebbea-111">The type of transfer to be used for performing the initial replication.</span></span>

<dt>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>

<span data-ttu-id="ebbea-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Netzwerkübertragung** (1)</span><span class="sxs-lookup"><span data-stu-id="ebbea-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Network Transfer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ebbea-113">Netzwerkübertragung.</span><span class="sxs-lookup"><span data-stu-id="ebbea-113">Network transfer.</span></span>

</dd> <dt>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>

<span data-ttu-id="ebbea-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Exportieren** (2)</span><span class="sxs-lookup"><span data-stu-id="ebbea-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Export** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ebbea-115">Export.</span><span class="sxs-lookup"><span data-stu-id="ebbea-115">Export.</span></span>

</dd> <dt>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>

<span data-ttu-id="ebbea-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Seeded-Netzwerkübertragung** (3)</span><span class="sxs-lookup"><span data-stu-id="ebbea-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Seeded Network Transfer** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ebbea-117">Seeded-Netzwerkübertragung.</span><span class="sxs-lookup"><span data-stu-id="ebbea-117">Seeded network transfer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ebbea-118">*Initialreplicationexportlocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebbea-118">*InitialReplicationExportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebbea-119">Wenn *initialreplicationtype* 2 (Export) ist, enthält dieser Parameter den voll qualifizierten Pfad des Verzeichnisses, in das die erste Replikation exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ebbea-119">If *InitialReplicationType* is 2 (Export), this parameter contains the fully qualified path of the directory to which the initial replication is to be exported.</span></span> <span data-ttu-id="ebbea-120">Dieser Parameter wird nicht für andere Werte von *initialreplicationtype* verwendet und kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="ebbea-120">This parameter is not used for other values of *InitialReplicationType*, and can be **Null**.</span></span> <span data-ttu-id="ebbea-121">Dieses Verzeichnis kann wieder verwendet werden, um die Replikation mehrerer virtueller Computer zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="ebbea-121">This directory can be reused for exporting multiple virtual machine replication.</span></span> <span data-ttu-id="ebbea-122">Diese Methode platziert die Replikation der virtuellen Computer in einem separaten Unterverzeichnis unter diesem Pfad.</span><span class="sxs-lookup"><span data-stu-id="ebbea-122">This method places each virtual machine replication in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="ebbea-123">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebbea-123">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebbea-124">Die geplante Startzeit für die erste Replikation über die Netzwerkverbindung mit dem Wiederherstellungs Server.</span><span class="sxs-lookup"><span data-stu-id="ebbea-124">The scheduled start time for the initial replication over the network connection to recovery server.</span></span> <span data-ttu-id="ebbea-125">Dieser Parameter wird ignoriert, wenn " *initialreplicationtype* " den Wert "2 (Export)" hat.</span><span class="sxs-lookup"><span data-stu-id="ebbea-125">This parameter is ignored when *InitialReplicationType* is 2 (Export).</span></span> <span data-ttu-id="ebbea-126">Wenn dieser Parameter **null** ist, wird die erste Replikation sofort gestartet.</span><span class="sxs-lookup"><span data-stu-id="ebbea-126">If this parameter is **Null**, the initial replication starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="ebbea-127">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ebbea-127">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebbea-128">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="ebbea-128">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebbea-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebbea-129">Return value</span></span>

<span data-ttu-id="ebbea-130">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="ebbea-130">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ebbea-131">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="ebbea-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ebbea-132">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="ebbea-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ebbea-133">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="ebbea-133">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ebbea-134">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="ebbea-134">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ebbea-135">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="ebbea-135">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ebbea-136">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="ebbea-136">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ebbea-137">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="ebbea-137">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ebbea-138">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="ebbea-138">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ebbea-139">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="ebbea-139">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ebbea-140">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="ebbea-140">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ebbea-141">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="ebbea-141">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ebbea-142">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="ebbea-142">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ebbea-143">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="ebbea-143">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ebbea-144">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="ebbea-144">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ebbea-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebbea-145">Requirements</span></span>



| <span data-ttu-id="ebbea-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebbea-146">Requirement</span></span> | <span data-ttu-id="ebbea-147">Wert</span><span class="sxs-lookup"><span data-stu-id="ebbea-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebbea-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ebbea-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ebbea-149">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebbea-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ebbea-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ebbea-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ebbea-151">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebbea-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ebbea-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="ebbea-152">Namespace</span></span><br/>                | <span data-ttu-id="ebbea-153">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ebbea-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ebbea-154">MOF</span><span class="sxs-lookup"><span data-stu-id="ebbea-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebbea-155"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ebbea-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebbea-156">DLL</span><span class="sxs-lookup"><span data-stu-id="ebbea-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebbea-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ebbea-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ebbea-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebbea-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebbea-159">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="ebbea-159">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

