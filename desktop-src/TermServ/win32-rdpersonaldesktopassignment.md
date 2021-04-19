---
title: Win32_RDPersonalDesktopAssignment-Klasse
description: Die Liste der persönlichen Desktop Zuweisungen.
ms.assetid: 3abf773d-8dc3-44ae-8887-1a1f38e29fbb
ms.tgt_platform: multiple
keywords:
- Win32_RDPersonalDesktopAssignment-Klasse Remotedesktopdienste
- Win32_RDPersonalDesktopAssignment Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDPersonalDesktopAssignment
- Win32_RDPersonalDesktopAssignment.Caption
- Win32_RDPersonalDesktopAssignment.Description
- Win32_RDPersonalDesktopAssignment.InstallDate
- Win32_RDPersonalDesktopAssignment.Name
- Win32_RDPersonalDesktopAssignment.Status
- Win32_RDPersonalDesktopAssignment.UserName
- Win32_RDPersonalDesktopAssignment.DomainName
- Win32_RDPersonalDesktopAssignment.FarmAlias
- Win32_RDPersonalDesktopAssignment.VMName
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088e7be5da0a62a0f5b7ed72f8a439661cc41c80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342406"
---
# <a name="win32_rdpersonaldesktopassignment-class"></a><span data-ttu-id="982bc-105">Win32- \_ rdpersonal Desktop-Zuweisungs Klasse</span><span class="sxs-lookup"><span data-stu-id="982bc-105">Win32\_RDPersonalDesktopAssignment class</span></span>

<span data-ttu-id="982bc-106">Die Liste der persönlichen Desktop Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="982bc-106">The list of personal desktop assignments.</span></span>

<span data-ttu-id="982bc-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="982bc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="982bc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="982bc-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDPersonalDesktopAssignment : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   UserName;
  string   DomainName;
  string   FarmAlias;
  string   VMName;
};
```

## <a name="members"></a><span data-ttu-id="982bc-109">Member</span><span class="sxs-lookup"><span data-stu-id="982bc-109">Members</span></span>

<span data-ttu-id="982bc-110">Die **Win32-Klasse \_ rdpersonaldesktopzuweisung** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="982bc-110">The **Win32\_RDPersonalDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="982bc-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="982bc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="982bc-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="982bc-112">Properties</span></span>

<span data-ttu-id="982bc-113">Die **Win32 \_ rdpersonaldesktopzuweisung** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="982bc-113">The **Win32\_RDPersonalDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="982bc-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="982bc-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982bc-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="982bc-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982bc-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="982bc-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982bc-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="982bc-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="982bc-118">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="982bc-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="982bc-119">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="982bc-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="982bc-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="982bc-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982bc-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="982bc-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982bc-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="982bc-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982bc-123">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="982bc-123">Description of the object.</span></span>

<span data-ttu-id="982bc-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="982bc-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="982bc-125">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="982bc-125">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982bc-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="982bc-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982bc-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="982bc-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="982bc-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="982bc-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="982bc-129">Der Domänen Name des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="982bc-129">Domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="982bc-130">**Farmalias**</span><span class="sxs-lookup"><span data-stu-id="982bc-130">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982bc-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="982bc-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982bc-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="982bc-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="982bc-133">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="982bc-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="982bc-134">Die Farm, der der persönliche Desktop zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="982bc-134">Farm in which personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="982bc-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="982bc-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982bc-136">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="982bc-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="982bc-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="982bc-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982bc-138">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="982bc-138">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="982bc-139">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="982bc-139">The date the object was installed.</span></span> <span data-ttu-id="982bc-140">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="982bc-140">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="982bc-141">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="982bc-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="982bc-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="982bc-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982bc-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="982bc-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982bc-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="982bc-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982bc-145">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="982bc-145">The name of the object.</span></span>

<span data-ttu-id="982bc-146">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="982bc-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="982bc-147">**Status**</span><span class="sxs-lookup"><span data-stu-id="982bc-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982bc-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="982bc-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982bc-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="982bc-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982bc-150">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="982bc-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="982bc-151">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="982bc-151">Current status of the object.</span></span> <span data-ttu-id="982bc-152">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="982bc-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="982bc-153">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="982bc-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="982bc-154">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="982bc-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="982bc-155">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="982bc-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="982bc-156">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="982bc-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="982bc-157">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="982bc-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="982bc-158">("OK")</span><span class="sxs-lookup"><span data-stu-id="982bc-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="982bc-159">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="982bc-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="982bc-160">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="982bc-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="982bc-161">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="982bc-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="982bc-162">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="982bc-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="982bc-163">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="982bc-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="982bc-164">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="982bc-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="982bc-165">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="982bc-165">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="982bc-166">**UserName**</span><span class="sxs-lookup"><span data-stu-id="982bc-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982bc-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="982bc-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982bc-168">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="982bc-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="982bc-169">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="982bc-169">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="982bc-170">Der Benutzername, dem der persönliche Desktop zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="982bc-170">User name to whom personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="982bc-171">**VMName**</span><span class="sxs-lookup"><span data-stu-id="982bc-171">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982bc-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="982bc-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982bc-173">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="982bc-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="982bc-174">Zugewiesener VM-Name.</span><span class="sxs-lookup"><span data-stu-id="982bc-174">Assigned VM name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="982bc-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="982bc-175">Requirements</span></span>



| <span data-ttu-id="982bc-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="982bc-176">Requirement</span></span> | <span data-ttu-id="982bc-177">Wert</span><span class="sxs-lookup"><span data-stu-id="982bc-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="982bc-178">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="982bc-178">Minimum supported client</span></span><br/> | <span data-ttu-id="982bc-179">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="982bc-179">None supported</span></span><br/>                                                                |
| <span data-ttu-id="982bc-180">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="982bc-180">Minimum supported server</span></span><br/> | <span data-ttu-id="982bc-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="982bc-181">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="982bc-182">Namespace</span><span class="sxs-lookup"><span data-stu-id="982bc-182">Namespace</span></span><br/>                | <span data-ttu-id="982bc-183">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="982bc-183">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="982bc-184">MOF</span><span class="sxs-lookup"><span data-stu-id="982bc-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="982bc-185"><dt>Tscpub. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="982bc-185"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="982bc-186">DLL</span><span class="sxs-lookup"><span data-stu-id="982bc-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="982bc-187"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="982bc-187"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

