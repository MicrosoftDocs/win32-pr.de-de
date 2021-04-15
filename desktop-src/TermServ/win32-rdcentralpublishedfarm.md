---
title: Win32_RDCentralPublishedFarm-Klasse
description: Die Liste der Farmen, von denen Desktops oder Anwendungen veröffentlicht wurden.
ms.assetid: 8fead659-42b4-4a10-892a-a6b616c47255
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedFarm-Klasse Remotedesktopdienste
- Win32_RDCentralPublishedFarm Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFarm
- Win32_RDCentralPublishedFarm.Caption
- Win32_RDCentralPublishedFarm.Description
- Win32_RDCentralPublishedFarm.InstallDate
- Win32_RDCentralPublishedFarm.Name
- Win32_RDCentralPublishedFarm.Status
- Win32_RDCentralPublishedFarm.Alias
- Win32_RDCentralPublishedFarm.FarmType
- Win32_RDCentralPublishedFarm.IsUserAdmin
- Win32_RDCentralPublishedFarm.RollbackEnabled
- Win32_RDCentralPublishedFarm.SecurityDescriptor
- Win32_RDCentralPublishedFarm.VmFarmSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9377053906168d4228e3b2cb8ae4f24cbb571634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476212"
---
# <a name="win32_rdcentralpublishedfarm-class"></a><span data-ttu-id="182fa-105">Win32 \_ rdcentralpublishedfarm-Klasse</span><span class="sxs-lookup"><span data-stu-id="182fa-105">Win32\_RDCentralPublishedFarm class</span></span>

<span data-ttu-id="182fa-106">Die Liste der Farmen, von denen Desktops oder Anwendungen veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="182fa-106">The list of farms from which desktops or applications have been published.</span></span>

<span data-ttu-id="182fa-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="182fa-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="182fa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="182fa-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedFarm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  uint32   FarmType;
  boolean  IsUserAdmin;
  boolean  RollbackEnabled;
  string   SecurityDescriptor;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="182fa-109">Member</span><span class="sxs-lookup"><span data-stu-id="182fa-109">Members</span></span>

<span data-ttu-id="182fa-110">Die **Win32-Klasse \_ rdcentralpublishedfarm** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="182fa-110">The **Win32\_RDCentralPublishedFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="182fa-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="182fa-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="182fa-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="182fa-112">Properties</span></span>

<span data-ttu-id="182fa-113">Die **Win32-Klasse \_ rdcentralpublishedfarm** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="182fa-113">The **Win32\_RDCentralPublishedFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="182fa-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="182fa-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182fa-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="182fa-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="182fa-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="182fa-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="182fa-117">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="182fa-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="182fa-118">Der Name der Farm, von der Desktops oder Anwendungen veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="182fa-118">The name of the farm from which desktops or applications have been published.</span></span>

</dd> <dt>

<span data-ttu-id="182fa-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="182fa-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182fa-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="182fa-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="182fa-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="182fa-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="182fa-122">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="182fa-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="182fa-123">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="182fa-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="182fa-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="182fa-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="182fa-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="182fa-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182fa-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="182fa-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="182fa-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="182fa-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="182fa-128">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="182fa-128">Description of the object.</span></span>

<span data-ttu-id="182fa-129">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="182fa-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="182fa-130">**Farmtyp**</span><span class="sxs-lookup"><span data-stu-id="182fa-130">**FarmType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182fa-131">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="182fa-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="182fa-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="182fa-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="182fa-133">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="182fa-133">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="182fa-134">Die Art der Farm:</span><span class="sxs-lookup"><span data-stu-id="182fa-134">The kind of farm:</span></span>

<dt>

<span id="RDSH"></span><span id="rdsh"></span>

<span data-ttu-id="182fa-135">**RDSH** (0)</span><span class="sxs-lookup"><span data-stu-id="182fa-135">**RDSH** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="182fa-136">**Tempvm** (1)</span><span class="sxs-lookup"><span data-stu-id="182fa-136">**TempVM** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="182fa-137">**Manualpersonalvm** (2)</span><span class="sxs-lookup"><span data-stu-id="182fa-137">**ManualPersonalVM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="182fa-138">**Autopersonalvm** (3)</span><span class="sxs-lookup"><span data-stu-id="182fa-138">**AutoPersonalVM** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="182fa-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="182fa-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182fa-140">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="182fa-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="182fa-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="182fa-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="182fa-142">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="182fa-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="182fa-143">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="182fa-143">The date the object was installed.</span></span> <span data-ttu-id="182fa-144">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="182fa-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="182fa-145">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="182fa-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="182fa-146">**Isuseradmin**</span><span class="sxs-lookup"><span data-stu-id="182fa-146">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182fa-147">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="182fa-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="182fa-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="182fa-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="182fa-149">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="182fa-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="182fa-150">**true** , wenn ein Benutzer bei der Verbindung der lokalen Administrator Gruppe hinzugefügt werden muss. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="182fa-150">**true** if a user needs to be added to local administrator group upon connection; otherwise, **false**.</span></span> <span data-ttu-id="182fa-151">Gilt nur für die Typen "manualpersonalvm" und "autopersonalvm".</span><span class="sxs-lookup"><span data-stu-id="182fa-151">Applicable only to ManualPersonalVm and AutoPersonalVM farm types.</span></span>

</dd> <dt>

<span data-ttu-id="182fa-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="182fa-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182fa-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="182fa-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="182fa-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="182fa-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="182fa-155">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="182fa-155">The name of the object.</span></span>

<span data-ttu-id="182fa-156">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="182fa-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="182fa-157">**Rollback aktiviert**</span><span class="sxs-lookup"><span data-stu-id="182fa-157">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182fa-158">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="182fa-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="182fa-159">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="182fa-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="182fa-160">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="182fa-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="182fa-161">" **true** ", wenn die VM nach dem Abmelden des Benutzers automatisch auf eine Momentaufnahme zurückgesetzt wird andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="182fa-161">**true** to auto rollback VM to a snapshot after user logoff; otherwise, **false**.</span></span> <span data-ttu-id="182fa-162">Gilt nur für tempvm-Farm Typen.</span><span class="sxs-lookup"><span data-stu-id="182fa-162">Applicable only to TempVm farm types.</span></span>

</dd> <dt>

<span data-ttu-id="182fa-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="182fa-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182fa-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="182fa-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="182fa-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="182fa-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="182fa-166">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="182fa-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="182fa-167">Der Name der Sicherheits Beschreibung, die den Zugriff auf die Anwendung steuert (im SDDL-Format).</span><span class="sxs-lookup"><span data-stu-id="182fa-167">The name of the security descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="182fa-168">Die Verwendung einer leeren Zeichenfolge impliziert den gesamten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="182fa-168">Using an empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="182fa-169">**Status**</span><span class="sxs-lookup"><span data-stu-id="182fa-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182fa-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="182fa-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="182fa-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="182fa-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="182fa-172">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="182fa-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="182fa-173">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="182fa-173">Current status of the object.</span></span> <span data-ttu-id="182fa-174">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="182fa-174">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="182fa-175">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="182fa-175">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="182fa-176">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="182fa-176">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="182fa-177">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="182fa-177">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="182fa-178">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="182fa-178">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="182fa-179">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="182fa-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="182fa-180">("OK")</span><span class="sxs-lookup"><span data-stu-id="182fa-180">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="182fa-181">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="182fa-181">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="182fa-182">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="182fa-182">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="182fa-183">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="182fa-183">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="182fa-184">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="182fa-184">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="182fa-185">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="182fa-185">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="182fa-186">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="182fa-186">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="182fa-187">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="182fa-187">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="182fa-188">**Vmfarmsettings**</span><span class="sxs-lookup"><span data-stu-id="182fa-188">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182fa-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="182fa-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="182fa-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="182fa-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="182fa-191">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="182fa-191">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="182fa-192">Die Farm Einstellungen der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="182fa-192">The virtual machine farm settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="182fa-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="182fa-193">Requirements</span></span>



| <span data-ttu-id="182fa-194">Anforderung</span><span class="sxs-lookup"><span data-stu-id="182fa-194">Requirement</span></span> | <span data-ttu-id="182fa-195">Wert</span><span class="sxs-lookup"><span data-stu-id="182fa-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="182fa-196">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="182fa-196">Minimum supported client</span></span><br/> | <span data-ttu-id="182fa-197">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="182fa-197">None supported</span></span><br/>                                                                |
| <span data-ttu-id="182fa-198">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="182fa-198">Minimum supported server</span></span><br/> | <span data-ttu-id="182fa-199">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="182fa-199">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="182fa-200">Namespace</span><span class="sxs-lookup"><span data-stu-id="182fa-200">Namespace</span></span><br/>                | <span data-ttu-id="182fa-201">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="182fa-201">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="182fa-202">MOF</span><span class="sxs-lookup"><span data-stu-id="182fa-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="182fa-203"><dt>Tscpub. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="182fa-203"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="182fa-204">DLL</span><span class="sxs-lookup"><span data-stu-id="182fa-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="182fa-205"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="182fa-205"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

