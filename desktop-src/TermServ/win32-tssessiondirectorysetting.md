---
title: Win32_TSSessionDirectorySetting-Klasse
description: Stellt die Zuordnung zwischen einer Instanz der Win32 \_ Terminalservice-Klasse und einer Instanz der Win32 \_ tssessiondirectory-Klasse dar.
ms.assetid: b6350f7b-386f-4f6b-8ab1-29d5d21fae02
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionDirectorySetting-Klasse Remotedesktopdienste
- Win32_TSSessionDirectorySetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectorySetting
- Win32_TSSessionDirectorySetting.Caption
- Win32_TSSessionDirectorySetting.Description
- Win32_TSSessionDirectorySetting.InstallDate
- Win32_TSSessionDirectorySetting.Name
- Win32_TSSessionDirectorySetting.Status
- Win32_TSSessionDirectorySetting.Element
- Win32_TSSessionDirectorySetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 667f501ff850cb7ee8c40448de11c06898ab8a85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040196"
---
# <a name="win32_tssessiondirectorysetting-class"></a><span data-ttu-id="e3a2b-105">Win32- \_ Klasse "tssessiondirectorysetting"</span><span class="sxs-lookup"><span data-stu-id="e3a2b-105">Win32\_TSSessionDirectorySetting class</span></span>

<span data-ttu-id="e3a2b-106">Stellt die Zuordnung zwischen einer Instanz der [**Win32 \_ Terminalservice**](win32-terminalservice.md) -Klasse und einer Instanz der [**Win32 \_ tssessiondirectory**](win32-tssessiondirectory.md) -Klasse dar.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-106">Represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and an instance of the [**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) class.</span></span>

<span data-ttu-id="e3a2b-107">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a2b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3a2b-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TSSESSIONDIRECTORYSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectorySetting : CIM_ElementSetting
{
  string                       Caption;
  string                       Description;
  datetime                     InstallDate;
  string                       Name;
  string                       Status;
  Win32_TerminalService    REF Element;
  Win32_TSSessionDirectory REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="e3a2b-109">Member</span><span class="sxs-lookup"><span data-stu-id="e3a2b-109">Members</span></span>

<span data-ttu-id="e3a2b-110">Die Win32-Klasse " **\_ tssessiondirectorysetting** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e3a2b-110">The **Win32\_TSSessionDirectorySetting** class has these types of members:</span></span>

-   [<span data-ttu-id="e3a2b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3a2b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3a2b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3a2b-112">Properties</span></span>

<span data-ttu-id="e3a2b-113">Die Win32-Klasse " **\_ tssessiondirectorysetting** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-113">The **Win32\_TSSessionDirectorySetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3a2b-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3a2b-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3a2b-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3a2b-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3a2b-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e3a2b-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e3a2b-118">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="e3a2b-119">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3a2b-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3a2b-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3a2b-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3a2b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3a2b-123">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-123">Description of the object.</span></span>

<span data-ttu-id="e3a2b-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3a2b-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3a2b-126">Datentyp: **Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-126">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="e3a2b-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3a2b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3a2b-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e3a2b-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e3a2b-129">Stellt die Instanz von **Win32 \_ Terminalservice** dar, die mit der **Setting** -Eigenschaft konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-129">Represents the instance of **Win32\_TerminalService** that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="e3a2b-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3a2b-131">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e3a2b-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3a2b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3a2b-133">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="e3a2b-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="e3a2b-134">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-134">The date the object was installed.</span></span> <span data-ttu-id="e3a2b-135">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e3a2b-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3a2b-137">**Name**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3a2b-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3a2b-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3a2b-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3a2b-140">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-140">The name of the object.</span></span>

<span data-ttu-id="e3a2b-141">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3a2b-142">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3a2b-143">Datentyp: **Win32 \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-143">Data type: **Win32\_TSSessionDirectory**</span></span>
</dt> <dt>

<span data-ttu-id="e3a2b-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3a2b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3a2b-145">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e3a2b-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e3a2b-146">Stellt die RD-Verbindungsbroker Einstellungen dar, die auf den zugeordneten RD-Sitzungshost Server angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-146">Represents the RD Connection Broker settings that can be applied to the associated RD Session Host Server.</span></span>

</dd> <dt>

<span data-ttu-id="e3a2b-147">**Status**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3a2b-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3a2b-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3a2b-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3a2b-150">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="e3a2b-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="e3a2b-151">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-151">Current status of the object.</span></span> <span data-ttu-id="e3a2b-152">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e3a2b-153">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="e3a2b-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e3a2b-154">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="e3a2b-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e3a2b-155">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e3a2b-156">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e3a2b-157">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="e3a2b-158">("OK")</span><span class="sxs-lookup"><span data-stu-id="e3a2b-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e3a2b-159">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="e3a2b-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e3a2b-160">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="e3a2b-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e3a2b-161">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="e3a2b-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e3a2b-162">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e3a2b-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e3a2b-163">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="e3a2b-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e3a2b-164">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="e3a2b-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e3a2b-165">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="e3a2b-165">("Service")</span></span>


<span data-ttu-id="e3a2b-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e3a2b-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e3a2b-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3a2b-167">Remarks</span></span>

<span data-ttu-id="e3a2b-168">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-168">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e3a2b-169">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-169">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e3a2b-170">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-170">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e3a2b-171">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e3a2b-171">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a2b-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3a2b-172">Requirements</span></span>



| <span data-ttu-id="e3a2b-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3a2b-173">Requirement</span></span> | <span data-ttu-id="e3a2b-174">Wert</span><span class="sxs-lookup"><span data-stu-id="e3a2b-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a2b-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3a2b-175">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a2b-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3a2b-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e3a2b-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3a2b-177">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a2b-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3a2b-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3a2b-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3a2b-179">Namespace</span></span><br/>                | <span data-ttu-id="e3a2b-180">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e3a2b-180">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="e3a2b-181">MOF</span><span class="sxs-lookup"><span data-stu-id="e3a2b-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3a2b-182"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e3a2b-182"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3a2b-183">DLL</span><span class="sxs-lookup"><span data-stu-id="e3a2b-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3a2b-184"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3a2b-184"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a2b-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3a2b-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a2b-186">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-186">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="e3a2b-187">**Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-187">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="e3a2b-188">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="e3a2b-188">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

