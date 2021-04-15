---
title: MSAD_DomainController-Klasse
description: Stellt den Domänen Controller (DC) dar, auf dem der WMI-Anbieter ausgeführt wird.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- MSAD_DomainController-Klasse Active Directory
- MSAD_DomainController Klasse Active Directory, beschrieben
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303071d3d268953687bc387709c74531f8b40584
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476848"
---
# <a name="msad_domaincontroller-class"></a><span data-ttu-id="80323-105">MSAD \_ Domain Controller-Klasse</span><span class="sxs-lookup"><span data-stu-id="80323-105">MSAD\_DomainController class</span></span>

<span data-ttu-id="80323-106">Stellt den Domänen Controller (DC) dar, auf dem der WMI-Anbieter ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80323-106">Represents the domain controller (DC) on which the WMI provider is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="80323-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="80323-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="80323-108">Member</span><span class="sxs-lookup"><span data-stu-id="80323-108">Members</span></span>

<span data-ttu-id="80323-109">Die **MSAD \_ Domain Controller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="80323-109">The **MSAD\_DomainController** class has these types of members:</span></span>

-   [<span data-ttu-id="80323-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="80323-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="80323-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80323-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="80323-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="80323-112">Methods</span></span>

<span data-ttu-id="80323-113">Die **MSAD \_ Domain Controller** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="80323-113">The **MSAD\_DomainController** class has these methods.</span></span>



| <span data-ttu-id="80323-114">Methode</span><span class="sxs-lookup"><span data-stu-id="80323-114">Method</span></span>                                                 | <span data-ttu-id="80323-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80323-115">Description</span></span>                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="80323-116">**Executekcc**</span><span class="sxs-lookup"><span data-stu-id="80323-116">**ExecuteKCC**</span></span>](executekcc-msad-domaincontroller.md) | <span data-ttu-id="80323-117">Ruft die Konsistenzprüfung auf, um die Replikations Topologie zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="80323-117">Invokes the Knowledge Consistency Checker to verify the replication topology.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="80323-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80323-118">Properties</span></span>

<span data-ttu-id="80323-119">Die **MSAD \_ Domain Controller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="80323-119">The **MSAD\_DomainController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80323-120">**CommonName**</span><span class="sxs-lookup"><span data-stu-id="80323-120">**CommonName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="80323-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="80323-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-123">Ruft den allgemeinen Namen des Server Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="80323-123">Gets the common name of the server object.</span></span>

</dd> <dt>

<span data-ttu-id="80323-124">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="80323-124">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="80323-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="80323-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80323-127">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80323-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80323-128">Ruft den X. 500-Pfad des [**NTDS-DSA-**](/windows/desktop/ADSchema/c-ntdsdsa) Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="80323-128">Gets the X.500 path of the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object.</span></span>

</dd> <dt>

<span data-ttu-id="80323-129">**Iswerben singtolocator**</span><span class="sxs-lookup"><span data-stu-id="80323-129">**IsAdvertisingToLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-130">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="80323-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80323-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-132">Ruft den-Wert ab, der angibt, ob der Serverlocatorpunkt-Dienst auf dem Domänen Controller ordnungsgemäß Ankündigungen sendet</span><span class="sxs-lookup"><span data-stu-id="80323-132">Gets the value that indicates whether the locator service on the DC is advertising correctly.</span></span> <span data-ttu-id="80323-133">**True** , wenn der Serverlocatorpunkt-Dienst auf dem Domänen Controller ordnungsgemäß Werbung macht. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="80323-133">**TRUE** if the locator service on the DC is advertising correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="80323-134">**Isgc**</span><span class="sxs-lookup"><span data-stu-id="80323-134">**IsGC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-135">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="80323-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80323-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-137">Ruft den-Wert ab, der angibt, ob der Domänen Controller ein globaler Katalogserver ist.</span><span class="sxs-lookup"><span data-stu-id="80323-137">Gets the value that indicates whether the DC is a Global Catalog server.</span></span> <span data-ttu-id="80323-138">**True** , wenn der Domänen Controller ein globaler Katalogserver ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="80323-138">**TRUE** if the DC is a Global Catalog server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="80323-139">**Isnextridpoolavailable**</span><span class="sxs-lookup"><span data-stu-id="80323-139">**IsNextRIDPoolAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-140">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="80323-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80323-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-142">Ruft den Wert ab, der angibt, ob der DC einen anderen RID-Pool abgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="80323-142">Gets the value that indicates whether the DC has obtained another RID pool.</span></span> <span data-ttu-id="80323-143">**True** , wenn der Domänen Controller einen anderen RID-Pool abgerufen hat und die Zuordnung von RIDs auf diesem DC fortgesetzt werden kann, auch wenn der aktuelle Pool von RIDs erschöpft ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="80323-143">**TRUE** if the DC has obtained another RID pool and allocation of RIDs on this DC can continue even if the current pool of RIDs is exhausted; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="80323-144">**Isregisteredindns**</span><span class="sxs-lookup"><span data-stu-id="80323-144">**IsRegisteredInDNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-145">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="80323-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80323-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-147">Ruft den Wert ab, der angibt, ob der DC ordnungsgemäß in DNS registriert ist.</span><span class="sxs-lookup"><span data-stu-id="80323-147">Gets the value that indicates whether the DC is registered correctly in DNS.</span></span> <span data-ttu-id="80323-148">**True** , wenn der Domänen Controller ordnungsgemäß in DNS registriert ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="80323-148">**TRUE** if the DC is registered correctly in DNS; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="80323-149">**Issysvolready**</span><span class="sxs-lookup"><span data-stu-id="80323-149">**IsSysVolReady**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-150">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="80323-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80323-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-152">Ruft den Wert ab, der angibt, ob SYSVOL ordnungsgemäß veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="80323-152">Gets the value that indicates whether the SysVol has published correctly.</span></span> <span data-ttu-id="80323-153">**True** , wenn SYSVOL ordnungsgemäß veröffentlicht wurde. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="80323-153">**TRUE** if the SysVol has published correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="80323-154">**Ntdsaguid**</span><span class="sxs-lookup"><span data-stu-id="80323-154">**NTDsaGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="80323-155">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="80323-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-157">Ruft die GUID ab, die dem [**NTDS-DSA-**](/windows/desktop/ADSchema/c-ntdsdsa) Objekt im Konfigurations Container zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="80323-157">Gets the GUID that is associated with the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object in the configuration container.</span></span> <span data-ttu-id="80323-158">Das **NTDS-DSA-** Objekt stellt den Active Directory-Domäne Dienst-DSA-Prozess auf dem Server dar.</span><span class="sxs-lookup"><span data-stu-id="80323-158">The **NTDS-DSA** object represents the Active Directory Domain Service DSA process on the server.</span></span>

</dd> <dt>

<span data-ttu-id="80323-159">**Prozentuofridslinks**</span><span class="sxs-lookup"><span data-stu-id="80323-159">**PercentOfRIDsLeft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-160">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80323-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80323-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-162">Ruft den Prozentsatz der RIDs ab, die im aktuellen RID-Pool auf diesem DC verbleiben.</span><span class="sxs-lookup"><span data-stu-id="80323-162">Gets the percentage of RIDs that are left in the current RID pool on this DC.</span></span>

</dd> <dt>

<span data-ttu-id="80323-163">**Sitename**</span><span class="sxs-lookup"><span data-stu-id="80323-163">**SiteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="80323-164">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="80323-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-166">Ruft den Standort ab, an dem der DC vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="80323-166">Gets the site in which the DC exists.</span></span>

</dd> <dt>

<span data-ttu-id="80323-167">**Timeofoldästrepladd**</span><span class="sxs-lookup"><span data-stu-id="80323-167">**TimeOfOldestReplAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-168">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="80323-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80323-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-170">Ruft den Zeitstempel des ältesten Replikations-Add-Vorgangs ab, der sich noch in der Warteschlange auf diesem Domänen Controller befindet.</span><span class="sxs-lookup"><span data-stu-id="80323-170">Gets the timestamp of the oldest replication add operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="80323-171">**Timeofoldästrepldel**</span><span class="sxs-lookup"><span data-stu-id="80323-171">**TimeOfOldestReplDel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-172">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="80323-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80323-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-174">Ruft den Zeitstempel des ältesten Replikations Löschvorgangs ab, der sich noch in der Warteschlange auf diesem Domänen Controller befindet.</span><span class="sxs-lookup"><span data-stu-id="80323-174">Gets the timestamp of the oldest replication delete operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="80323-175">**Timeofoldästreplmod**</span><span class="sxs-lookup"><span data-stu-id="80323-175">**TimeOfOldestReplMod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-176">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="80323-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80323-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-178">Ruft den Zeitstempel des ältesten Replikations Änderungs Vorgangs ab, der sich noch in der Warteschlange auf diesem Domänen Controller befindet.</span><span class="sxs-lookup"><span data-stu-id="80323-178">Gets the timestamp of the oldest replication modify operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="80323-179">**Timeofoldästreplsync**</span><span class="sxs-lookup"><span data-stu-id="80323-179">**TimeOfOldestReplSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-180">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="80323-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80323-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-182">Ruft den Zeitstempel des ältesten Replikations Synchronisierungs Vorgangs ab, der sich noch in der Warteschlange auf diesem Domänen Controller befindet.</span><span class="sxs-lookup"><span data-stu-id="80323-182">Gets the timestamp of the oldest replication sync operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="80323-183">**Timeofoldästreplupdrefs**</span><span class="sxs-lookup"><span data-stu-id="80323-183">**TimeOfOldestReplUpdRefs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80323-184">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="80323-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80323-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80323-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80323-186">Ruft den Zeitstempel des ältesten Replikations Aktualisierungs Vorgangs ab, der sich noch in der Warteschlange auf diesem Domänen Controller befindet.</span><span class="sxs-lookup"><span data-stu-id="80323-186">Gets the timestamp of the oldest replication update operation that is still in the queue on this domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80323-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80323-187">Requirements</span></span>



| <span data-ttu-id="80323-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80323-188">Requirement</span></span> | <span data-ttu-id="80323-189">Wert</span><span class="sxs-lookup"><span data-stu-id="80323-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80323-190">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80323-190">Minimum supported client</span></span><br/> | <span data-ttu-id="80323-191">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="80323-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="80323-192">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80323-192">Minimum supported server</span></span><br/> | <span data-ttu-id="80323-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80323-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80323-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="80323-194">Namespace</span></span><br/>                | <span data-ttu-id="80323-195">\\Microsoftactivedirectory-Stammverzeichnis</span><span class="sxs-lookup"><span data-stu-id="80323-195">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="80323-196">MOF</span><span class="sxs-lookup"><span data-stu-id="80323-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80323-197"><dt>ReplProv. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="80323-197"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="80323-198">DLL</span><span class="sxs-lookup"><span data-stu-id="80323-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80323-199"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80323-199"><dt>Replprov.dll</dt></span></span> </dl> |



 

