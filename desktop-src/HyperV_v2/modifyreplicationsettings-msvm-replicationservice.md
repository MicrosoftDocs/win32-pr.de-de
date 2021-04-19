---
description: Ändert die Replikationseinstellungen für einen virtuellen Computer. Wenn ein Client diese Methode für einen virtuellen Replikat Computer aufruft, ändert er die Replikationseinstellungen der Replikations Beziehung mit dem erweiterten Replikat.
ms.assetid: e68514a5-f508-4047-8dcc-6a95f3e3353e
title: Modifyreplicationsettings-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyReplicationSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1c932f06350324e0d84559724f7ba0412dfb3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353829"
---
# <a name="modifyreplicationsettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="53a2d-104">Modifyreplicationsettings-Methode der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="53a2d-104">ModifyReplicationSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="53a2d-105">Ändert die Replikationseinstellungen für einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="53a2d-105">Modifies the replication settings for a virtual machine.</span></span> <span data-ttu-id="53a2d-106">Wenn ein Client diese Methode für einen virtuellen Replikat Computer aufruft, ändert er die Replikationseinstellungen der Replikations Beziehung mit dem erweiterten Replikat.</span><span class="sxs-lookup"><span data-stu-id="53a2d-106">When a client calls this method for a replica virtual machine, it modifies the replication settings of the replication relationship with the extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a2d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="53a2d-107">Syntax</span></span>


```mof
uint32 ModifyReplicationSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="53a2d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="53a2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53a2d-109">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53a2d-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53a2d-110">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die Replikationseinstellungen geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="53a2d-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication settings should be modified.</span></span>

</dd> <dt>

<span data-ttu-id="53a2d-111">*Replicationsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53a2d-111">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53a2d-112">Eine Zeichen folgen Darstellung der [**MSVM \_ replicationsettingdata**](msvm-replicationsettingdata.md) -Klasse, die die neuen Replikationseinstellungen definiert.</span><span class="sxs-lookup"><span data-stu-id="53a2d-112">A string representation of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the new replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="53a2d-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="53a2d-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53a2d-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="53a2d-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53a2d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53a2d-115">Return value</span></span>

<span data-ttu-id="53a2d-116">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="53a2d-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="53a2d-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="53a2d-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="53a2d-118">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="53a2d-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="53a2d-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="53a2d-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="53a2d-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="53a2d-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="53a2d-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="53a2d-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="53a2d-122">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="53a2d-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="53a2d-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="53a2d-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="53a2d-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="53a2d-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="53a2d-125">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="53a2d-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="53a2d-126">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="53a2d-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="53a2d-127">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="53a2d-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="53a2d-128">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="53a2d-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="53a2d-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="53a2d-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="53a2d-130">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="53a2d-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="53a2d-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53a2d-131">Remarks</span></span>

<span data-ttu-id="53a2d-132">**Modifyreplicationsettings** übernimmt eine [**MSVM- \_ replicationsettingdata**](msvm-replicationsettingdata.md) -Instanz (frsd) als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="53a2d-132">**ModifyReplicationSettings** takes an [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) instance (FRSD) as input.</span></span> <span data-ttu-id="53a2d-133">Die zugehörige frsd-Datei für die virtuelle Maschine als Host-zu-Host-Anbieter ist die Standardauswahl.</span><span class="sxs-lookup"><span data-stu-id="53a2d-133">The associated FRSD for the virtual machine as host-to-host provider is the default choice.</span></span> <span data-ttu-id="53a2d-134">Die Eingabe-frsd wird auf gültige Einstellungen für jede Eigenschaft für den Standardanbieter überprüft.</span><span class="sxs-lookup"><span data-stu-id="53a2d-134">Input FRSD is validated for valid settings for each property for the default provider.</span></span> <span data-ttu-id="53a2d-135">In dieser Tabelle werden die Validierungs Unterschiede in Bezug auf den externen Anbieter zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="53a2d-135">This table summarizes the validation differences with respect to the external provider.</span></span>



| <span data-ttu-id="53a2d-136">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="53a2d-136">Property</span></span>                                             | <span data-ttu-id="53a2d-137">Externe Anbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-137">External providers</span></span>                                 |
|------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="53a2d-138">Replicationprovider</span><span class="sxs-lookup"><span data-stu-id="53a2d-138">ReplicationProvider</span></span>                                  | <span data-ttu-id="53a2d-139">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-139">Same as default provider</span></span>                           |
| <span data-ttu-id="53a2d-140">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="53a2d-140">AuthenticationType</span></span>                                   | <span data-ttu-id="53a2d-141">Wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="53a2d-141">Ignored</span></span>                                            |
| <span data-ttu-id="53a2d-142">CertificateThumbPrint</span><span class="sxs-lookup"><span data-stu-id="53a2d-142">CertificateThumbPrint</span></span>                                | <span data-ttu-id="53a2d-143">Wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="53a2d-143">Ignored</span></span>                                            |
| <span data-ttu-id="53a2d-144">Rootcertifi-ethumschlag-Print (RO)</span><span class="sxs-lookup"><span data-stu-id="53a2d-144">RootCertificateThumbPrint (RO)</span></span>                       | <span data-ttu-id="53a2d-145">Wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="53a2d-145">Ignored</span></span>                                            |
| <span data-ttu-id="53a2d-146">Compressionaktiviert</span><span class="sxs-lookup"><span data-stu-id="53a2d-146">CompressionEnabled</span></span>                                   | <span data-ttu-id="53a2d-147">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-147">Same as default provider</span></span>                           |
| <span data-ttu-id="53a2d-148">Bypassproxyserver</span><span class="sxs-lookup"><span data-stu-id="53a2d-148">BypassProxyServer</span></span>                                    | <span data-ttu-id="53a2d-149">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-149">Same as default provider</span></span>                           |
| <span data-ttu-id="53a2d-150">Wiederherstellungsconnectionpoint</span><span class="sxs-lookup"><span data-stu-id="53a2d-150">RecoveryConnectionPoint</span></span>                              | <span data-ttu-id="53a2d-151">Ignoriert \* (kann sich ändern, wenn der Anbieter eine Anforderung hat)</span><span class="sxs-lookup"><span data-stu-id="53a2d-151">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="53a2d-152">Wiederherstellunghostsystem (RO)</span><span class="sxs-lookup"><span data-stu-id="53a2d-152">RecoveryHostSystem (RO)</span></span>                              | <span data-ttu-id="53a2d-153">Wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="53a2d-153">Ignored</span></span>                                            |
| <span data-ttu-id="53a2d-154">Primaryconnectionpoint (RO)</span><span class="sxs-lookup"><span data-stu-id="53a2d-154">PrimaryConnectionPoint (RO)</span></span>                          | <span data-ttu-id="53a2d-155">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-155">Same as default provider</span></span>                           |
| <span data-ttu-id="53a2d-156">Primaryhostsystem (RO)</span><span class="sxs-lookup"><span data-stu-id="53a2d-156">PrimaryHostSystem (RO)</span></span>                               | <span data-ttu-id="53a2d-157">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-157">Same as default provider</span></span>                           |
| <span data-ttu-id="53a2d-158">Wiederherstellserverportnummer</span><span class="sxs-lookup"><span data-stu-id="53a2d-158">RecoveryServerPortNumber</span></span>                             | <span data-ttu-id="53a2d-159">Ignoriert \* (kann sich ändern, wenn der Anbieter eine Anforderung hat)</span><span class="sxs-lookup"><span data-stu-id="53a2d-159">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="53a2d-160">Replicatehostkvpitems</span><span class="sxs-lookup"><span data-stu-id="53a2d-160">ReplicateHostKvpItems</span></span>                                | <span data-ttu-id="53a2d-161">Wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="53a2d-161">Ignored</span></span>                                            |
| <span data-ttu-id="53a2d-162">Applicationkonsistentsnapshotinterval</span><span class="sxs-lookup"><span data-stu-id="53a2d-162">ApplicationConsistentSnapshotInterval</span></span>                | <span data-ttu-id="53a2d-163">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-163">Same as default provider</span></span>                           |
| <span data-ttu-id="53a2d-164">Parameter recoveryhistory einen</span><span class="sxs-lookup"><span data-stu-id="53a2d-164">RecoveryHistory</span></span>                                      | <span data-ttu-id="53a2d-165">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-165">Same as default provider</span></span>                           |
| <span data-ttu-id="53a2d-166">Includdisks\[\]</span><span class="sxs-lookup"><span data-stu-id="53a2d-166">IncludedDisks\[\]</span></span>                                    | <span data-ttu-id="53a2d-167">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-167">Same as default provider</span></span>                           |
| <span data-ttu-id="53a2d-168">Autoresynchronizeaktivierte</span><span class="sxs-lookup"><span data-stu-id="53a2d-168">AutoResynchronizeEnabled</span></span>                             | <span data-ttu-id="53a2d-169">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-169">Same as default provider</span></span>                           |
| <span data-ttu-id="53a2d-170">Autoresynchronizeingetervalstart</span><span class="sxs-lookup"><span data-stu-id="53a2d-170">AutoResynchronizeIntervalStart</span></span>                       | <span data-ttu-id="53a2d-171">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-171">Same as default provider</span></span>                           |
| <span data-ttu-id="53a2d-172">Autoresynchronizzutervalend</span><span class="sxs-lookup"><span data-stu-id="53a2d-172">AutoResynchronizeIntervalEnd</span></span>                         | <span data-ttu-id="53a2d-173">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-173">Same as default provider</span></span>                           |
| <span data-ttu-id="53a2d-174">Enableschreiteorderkonservierungs ationacrossdisks (veraltet)</span><span class="sxs-lookup"><span data-stu-id="53a2d-174">EnableWriteOrderPreservationAcrossDisks (Deprecated)</span></span> | <span data-ttu-id="53a2d-175">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-175">Same as default provider</span></span>                           |
| <span data-ttu-id="53a2d-176">ReplicationInterval</span><span class="sxs-lookup"><span data-stu-id="53a2d-176">ReplicationInterval</span></span>                                  | <span data-ttu-id="53a2d-177">Identisch mit Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="53a2d-177">Same as default provider</span></span>                           |



 

## <a name="requirements"></a><span data-ttu-id="53a2d-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53a2d-178">Requirements</span></span>



| <span data-ttu-id="53a2d-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53a2d-179">Requirement</span></span> | <span data-ttu-id="53a2d-180">Wert</span><span class="sxs-lookup"><span data-stu-id="53a2d-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53a2d-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53a2d-181">Minimum supported client</span></span><br/> | <span data-ttu-id="53a2d-182">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53a2d-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="53a2d-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53a2d-183">Minimum supported server</span></span><br/> | <span data-ttu-id="53a2d-184">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53a2d-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="53a2d-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="53a2d-185">Namespace</span></span><br/>                | <span data-ttu-id="53a2d-186">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="53a2d-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="53a2d-187">MOF</span><span class="sxs-lookup"><span data-stu-id="53a2d-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53a2d-188"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="53a2d-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53a2d-189">DLL</span><span class="sxs-lookup"><span data-stu-id="53a2d-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53a2d-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53a2d-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53a2d-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53a2d-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a2d-192">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="53a2d-192">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

