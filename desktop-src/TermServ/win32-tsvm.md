---
title: Win32_TSVm-Klasse
description: Stellt einen Remotedesktop virtuellen Computer dar.
ms.assetid: 9e076963-1c02-4419-b4d5-9863a2bbb23b
ms.tgt_platform: multiple
keywords:
- Win32_TSVm-Klasse Remotedesktopdienste
- Win32_TSVm Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSVm
- Win32_TSVm.Caption
- Win32_TSVm.Description
- Win32_TSVm.InstallDate
- Win32_TSVm.Name
- Win32_TSVm.Status
- Win32_TSVm.VmName
- Win32_TSVm.EnlightmentSettings
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f419a888adef946d2a7b281919a9a9293eeca5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339312"
---
# <a name="win32_tsvm-class"></a><span data-ttu-id="f9998-105">Win32-Klasse "- \_ VM"</span><span class="sxs-lookup"><span data-stu-id="f9998-105">Win32\_TSVm class</span></span>

<span data-ttu-id="f9998-106">Stellt einen Remotedesktop virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="f9998-106">Represents a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="f9998-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f9998-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9998-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9998-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  string   EnlightmentSettings;
};
```

## <a name="members"></a><span data-ttu-id="f9998-109">Member</span><span class="sxs-lookup"><span data-stu-id="f9998-109">Members</span></span>

<span data-ttu-id="f9998-110">Die Win32-Klasse " **\_ ZVM** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f9998-110">The **Win32\_TSVm** class has these types of members:</span></span>

-   [<span data-ttu-id="f9998-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f9998-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f9998-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9998-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f9998-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="f9998-113">Methods</span></span>

<span data-ttu-id="f9998-114">Die Win32-Klasse " **\_ ZVM** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f9998-114">The **Win32\_TSVm** class has these methods.</span></span>



| <span data-ttu-id="f9998-115">Methode</span><span class="sxs-lookup"><span data-stu-id="f9998-115">Method</span></span>                                                                | <span data-ttu-id="f9998-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9998-116">Description</span></span>                                              |
|:----------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="f9998-117">**Dumpvminfo**</span><span class="sxs-lookup"><span data-stu-id="f9998-117">**DumpVmInfo**</span></span>](dumpvminfo-win32-tsvm.md)                           | <span data-ttu-id="f9998-118">Nur für Testzwecke.</span><span class="sxs-lookup"><span data-stu-id="f9998-118">For test purposes only.</span></span><br/>                       |
| [<span data-ttu-id="f9998-119">**Exportieren**</span><span class="sxs-lookup"><span data-stu-id="f9998-119">**Export**</span></span>](export-win32-tsvm.md)                                   | <span data-ttu-id="f9998-120">Ruft Informationen zur Sitzungs Überwachung des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="f9998-120">Gets Session Monitoring Information of the VM</span></span><br/> |
| [<span data-ttu-id="f9998-121">**Queryofflineinformation**</span><span class="sxs-lookup"><span data-stu-id="f9998-121">**QueryOfflineInformation**</span></span>](queryofflineinformation-win32-tsvm.md) | <span data-ttu-id="f9998-122">Fragt Eigenschaften nur ab, wenn Sie offline ist.</span><span class="sxs-lookup"><span data-stu-id="f9998-122">Queries properties only when it is offline.</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="f9998-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9998-123">Properties</span></span>

<span data-ttu-id="f9998-124">Die **Win32 \_** -Klasse "t-VM" verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f9998-124">The **Win32\_TSVm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9998-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f9998-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9998-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9998-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9998-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9998-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9998-128">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f9998-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f9998-129">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f9998-129">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f9998-130">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9998-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9998-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f9998-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9998-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9998-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9998-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9998-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9998-134">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f9998-134">Description of the object.</span></span>

<span data-ttu-id="f9998-135">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9998-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9998-136">**"Einlightmentsettings"**</span><span class="sxs-lookup"><span data-stu-id="f9998-136">**EnlightmentSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9998-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9998-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9998-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f9998-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f9998-139">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f9998-139">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f9998-140">Ein XML-BLOB, das die Einstellungen für die Aufklärung für den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="f9998-140">An XML BLOB that contains the enlightenment settings for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="f9998-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f9998-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9998-142">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f9998-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f9998-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9998-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9998-144">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="f9998-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f9998-145">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f9998-145">The date the object was installed.</span></span> <span data-ttu-id="f9998-146">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9998-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f9998-147">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9998-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9998-148">**Name**</span><span class="sxs-lookup"><span data-stu-id="f9998-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9998-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9998-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9998-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9998-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9998-151">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f9998-151">The name of the object.</span></span>

<span data-ttu-id="f9998-152">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9998-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9998-153">**Status**</span><span class="sxs-lookup"><span data-stu-id="f9998-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9998-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9998-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9998-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9998-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9998-156">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="f9998-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f9998-157">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f9998-157">Current status of the object.</span></span> <span data-ttu-id="f9998-158">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f9998-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f9998-159">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="f9998-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f9998-160">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="f9998-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f9998-161">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9998-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f9998-162">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="f9998-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f9998-163">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9998-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f9998-164">("OK")</span><span class="sxs-lookup"><span data-stu-id="f9998-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9998-165">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="f9998-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9998-166">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="f9998-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9998-167">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f9998-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9998-168">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f9998-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9998-169">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="f9998-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9998-170">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="f9998-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9998-171">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="f9998-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f9998-172">**VmName**</span><span class="sxs-lookup"><span data-stu-id="f9998-172">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9998-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9998-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9998-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9998-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9998-175">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f9998-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f9998-176">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="f9998-176">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9998-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9998-177">Requirements</span></span>



| <span data-ttu-id="f9998-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9998-178">Requirement</span></span> | <span data-ttu-id="f9998-179">Wert</span><span class="sxs-lookup"><span data-stu-id="f9998-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9998-180">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9998-180">Minimum supported client</span></span><br/> | <span data-ttu-id="f9998-181">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f9998-181">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="f9998-182">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9998-182">Minimum supported server</span></span><br/> | <span data-ttu-id="f9998-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9998-183">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="f9998-184">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9998-184">Namespace</span></span><br/>                | <span data-ttu-id="f9998-185">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f9998-185">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="f9998-186">MOF</span><span class="sxs-lookup"><span data-stu-id="f9998-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9998-187"><dt>"Zvmhost. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="f9998-187"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="f9998-188">DLL</span><span class="sxs-lookup"><span data-stu-id="f9998-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9998-189"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9998-189"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

