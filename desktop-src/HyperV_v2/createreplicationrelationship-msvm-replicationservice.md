---
description: Erstellt eine neue Replikations Beziehung für eine virtuelle Maschine. Wenn ein Client diese Methode für einen virtuellen Replikat Computer aufruft, wird die Replikations Beziehung auf den angegebenen Anbieter ausgeweitet.
ms.assetid: 44d3b5aa-46c2-4fe9-9a1d-6ee699d3640d
title: Methode "samatereplicationrelationship" der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CreateReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c44628aef9aa278170a1292a74621419bb6256b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348112"
---
# <a name="createreplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="bab09-104">Methode "kreatereplicationrelationship" der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="bab09-104">CreateReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="bab09-105">Erstellt eine neue Replikations Beziehung für eine virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="bab09-105">Creates a new replication relationship for a virtual machine.</span></span> <span data-ttu-id="bab09-106">Wenn ein Client diese Methode für einen virtuellen Replikat Computer aufruft, wird die Replikations Beziehung auf den angegebenen Anbieter ausgeweitet.</span><span class="sxs-lookup"><span data-stu-id="bab09-106">When a client calls this method for a replica virtual machine, it extends the replication relationship to the specified provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab09-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bab09-107">Syntax</span></span>


```mof
uint32 CreateReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bab09-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bab09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab09-109">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bab09-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab09-110">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die Replikation aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bab09-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="bab09-111">*Replicationsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bab09-111">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab09-112">Eine Zeichen folgen Darstellung einer Instanz der [**MSVM \_ replicationsettingdata**](msvm-replicationsettingdata.md) -Klasse, die die Replikationseinstellungen für die neue Replikations Beziehung definiert, die für den virtuellen Computer erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bab09-112">A string representation of an instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings for the new replication relationship to be created for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="bab09-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bab09-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bab09-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="bab09-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bab09-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bab09-115">Return value</span></span>

<span data-ttu-id="bab09-116">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="bab09-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bab09-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="bab09-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bab09-118">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="bab09-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bab09-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="bab09-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bab09-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="bab09-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bab09-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="bab09-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bab09-122">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="bab09-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bab09-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="bab09-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bab09-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="bab09-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bab09-125">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="bab09-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bab09-126">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="bab09-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bab09-127">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="bab09-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bab09-128">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="bab09-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bab09-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="bab09-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="bab09-130">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="bab09-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bab09-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bab09-131">Remarks</span></span>

<span data-ttu-id="bab09-132">" **Miatereplicationrelationship** " nimmt eine [**MSVM- \_ replicationsettingdata**](msvm-replicationsettingdata.md) -Instanz (frsd) als Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="bab09-132">**CreateReplicationRelationship** takes an [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) instance (FRSD) as input.</span></span> <span data-ttu-id="bab09-133">Die zugehörige frsd-Datei für die virtuelle Maschine als Host-zu-Host-Anbieter ist die Standardauswahl.</span><span class="sxs-lookup"><span data-stu-id="bab09-133">The associated FRSD for the virtual machine as host-to-host provider is the default choice.</span></span> <span data-ttu-id="bab09-134">Die Eingabe-frsd wird auf gültige Einstellungen für jede Eigenschaft für den Standardanbieter überprüft.</span><span class="sxs-lookup"><span data-stu-id="bab09-134">Input FRSD is validated for valid settings for each property for the default provider.</span></span> <span data-ttu-id="bab09-135">In dieser Tabelle werden die Validierungs Unterschiede in Bezug auf den externen Anbieter zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="bab09-135">This table summarizes the validation differences with respect to the external provider.</span></span>



| <span data-ttu-id="bab09-136">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bab09-136">Property</span></span>                                             | <span data-ttu-id="bab09-137">Externe Anbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-137">External providers</span></span>                                 |
|------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="bab09-138">Replicationprovider</span><span class="sxs-lookup"><span data-stu-id="bab09-138">ReplicationProvider</span></span>                                  | <span data-ttu-id="bab09-139">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-139">Same as default provider</span></span>                           |
| <span data-ttu-id="bab09-140">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="bab09-140">AuthenticationType</span></span>                                   | <span data-ttu-id="bab09-141">Wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bab09-141">Ignored</span></span>                                            |
| <span data-ttu-id="bab09-142">CertificateThumbPrint</span><span class="sxs-lookup"><span data-stu-id="bab09-142">CertificateThumbPrint</span></span>                                | <span data-ttu-id="bab09-143">Wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bab09-143">Ignored</span></span>                                            |
| <span data-ttu-id="bab09-144">Rootcertifi-ethumschlag-Print (RO)</span><span class="sxs-lookup"><span data-stu-id="bab09-144">RootCertificateThumbPrint (RO)</span></span>                       | <span data-ttu-id="bab09-145">Wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bab09-145">Ignored</span></span>                                            |
| <span data-ttu-id="bab09-146">Compressionaktiviert</span><span class="sxs-lookup"><span data-stu-id="bab09-146">CompressionEnabled</span></span>                                   | <span data-ttu-id="bab09-147">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-147">Same as default provider</span></span>                           |
| <span data-ttu-id="bab09-148">Bypassproxyserver</span><span class="sxs-lookup"><span data-stu-id="bab09-148">BypassProxyServer</span></span>                                    | <span data-ttu-id="bab09-149">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-149">Same as default provider</span></span>                           |
| <span data-ttu-id="bab09-150">Wiederherstellungsconnectionpoint</span><span class="sxs-lookup"><span data-stu-id="bab09-150">RecoveryConnectionPoint</span></span>                              | <span data-ttu-id="bab09-151">Ignoriert \* (kann sich ändern, wenn der Anbieter eine Anforderung hat)</span><span class="sxs-lookup"><span data-stu-id="bab09-151">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="bab09-152">Wiederherstellunghostsystem (RO)</span><span class="sxs-lookup"><span data-stu-id="bab09-152">RecoveryHostSystem (RO)</span></span>                              | <span data-ttu-id="bab09-153">Wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bab09-153">Ignored</span></span>                                            |
| <span data-ttu-id="bab09-154">Primaryconnectionpoint (RO)</span><span class="sxs-lookup"><span data-stu-id="bab09-154">PrimaryConnectionPoint (RO)</span></span>                          | <span data-ttu-id="bab09-155">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-155">Same as default provider</span></span>                           |
| <span data-ttu-id="bab09-156">Primaryhostsystem (RO)</span><span class="sxs-lookup"><span data-stu-id="bab09-156">PrimaryHostSystem (RO)</span></span>                               | <span data-ttu-id="bab09-157">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-157">Same as default provider</span></span>                           |
| <span data-ttu-id="bab09-158">Wiederherstellserverportnummer</span><span class="sxs-lookup"><span data-stu-id="bab09-158">RecoveryServerPortNumber</span></span>                             | <span data-ttu-id="bab09-159">Ignoriert \* (kann sich ändern, wenn der Anbieter eine Anforderung hat)</span><span class="sxs-lookup"><span data-stu-id="bab09-159">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="bab09-160">Replicatehostkvpitems</span><span class="sxs-lookup"><span data-stu-id="bab09-160">ReplicateHostKvpItems</span></span>                                | <span data-ttu-id="bab09-161">Wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bab09-161">Ignored</span></span>                                            |
| <span data-ttu-id="bab09-162">Applicationkonsistentsnapshotinterval</span><span class="sxs-lookup"><span data-stu-id="bab09-162">ApplicationConsistentSnapshotInterval</span></span>                | <span data-ttu-id="bab09-163">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-163">Same as default provider</span></span>                           |
| <span data-ttu-id="bab09-164">Parameter recoveryhistory einen</span><span class="sxs-lookup"><span data-stu-id="bab09-164">RecoveryHistory</span></span>                                      | <span data-ttu-id="bab09-165">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-165">Same as default provider</span></span>                           |
| <span data-ttu-id="bab09-166">Includdisks\[\]</span><span class="sxs-lookup"><span data-stu-id="bab09-166">IncludedDisks\[\]</span></span>                                    | <span data-ttu-id="bab09-167">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-167">Same as default provider</span></span>                           |
| <span data-ttu-id="bab09-168">Autoresynchronizeaktivierte</span><span class="sxs-lookup"><span data-stu-id="bab09-168">AutoResynchronizeEnabled</span></span>                             | <span data-ttu-id="bab09-169">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-169">Same as default provider</span></span>                           |
| <span data-ttu-id="bab09-170">Autoresynchronizeingetervalstart</span><span class="sxs-lookup"><span data-stu-id="bab09-170">AutoResynchronizeIntervalStart</span></span>                       | <span data-ttu-id="bab09-171">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-171">Same as default provider</span></span>                           |
| <span data-ttu-id="bab09-172">Autoresynchronizzutervalend</span><span class="sxs-lookup"><span data-stu-id="bab09-172">AutoResynchronizeIntervalEnd</span></span>                         | <span data-ttu-id="bab09-173">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-173">Same as default provider</span></span>                           |
| <span data-ttu-id="bab09-174">Enableschreiteorderkonservierungs ationacrossdisks (veraltet)</span><span class="sxs-lookup"><span data-stu-id="bab09-174">EnableWriteOrderPreservationAcrossDisks (Deprecated)</span></span> | <span data-ttu-id="bab09-175">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-175">Same as default provider</span></span>                           |
| <span data-ttu-id="bab09-176">ReplicationInterval</span><span class="sxs-lookup"><span data-stu-id="bab09-176">ReplicationInterval</span></span>                                  | <span data-ttu-id="bab09-177">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="bab09-177">Same as default provider</span></span>                           |



 

## <a name="requirements"></a><span data-ttu-id="bab09-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bab09-178">Requirements</span></span>



| <span data-ttu-id="bab09-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bab09-179">Requirement</span></span> | <span data-ttu-id="bab09-180">Wert</span><span class="sxs-lookup"><span data-stu-id="bab09-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bab09-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bab09-181">Minimum supported client</span></span><br/> | <span data-ttu-id="bab09-182">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bab09-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bab09-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bab09-183">Minimum supported server</span></span><br/> | <span data-ttu-id="bab09-184">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bab09-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bab09-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="bab09-185">Namespace</span></span><br/>                | <span data-ttu-id="bab09-186">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="bab09-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bab09-187">MOF</span><span class="sxs-lookup"><span data-stu-id="bab09-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bab09-188"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bab09-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bab09-189">DLL</span><span class="sxs-lookup"><span data-stu-id="bab09-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bab09-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bab09-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bab09-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bab09-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab09-192">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="bab09-192">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="bab09-193">**Removereplicationrelationshipex**</span><span class="sxs-lookup"><span data-stu-id="bab09-193">**RemoveReplicationRelationshipEx**</span></span>](removereplicationrelationshipex-msvm-replicationservice.md)
</dt> </dl>

 

