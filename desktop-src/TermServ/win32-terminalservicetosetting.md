---
title: Win32_TerminalServiceToSetting-Klasse
description: Stellt die Zuordnung zwischen einer Instanz der Win32 \_ Terminalservice-Klasse und der Einstellung einer bestimmten Win32 \_ terminalservicesetts-Eigenschaft dar.
ms.assetid: 4c206812-7549-4410-b6ba-1163f20d2bee
ms.tgt_platform: multiple
keywords:
- Win32_TerminalServiceToSetting-Klasse Remotedesktopdienste
- Win32_TerminalServiceToSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TerminalServiceToSetting
- Win32_TerminalServiceToSetting.Caption
- Win32_TerminalServiceToSetting.Description
- Win32_TerminalServiceToSetting.InstallDate
- Win32_TerminalServiceToSetting.Name
- Win32_TerminalServiceToSetting.Status
- Win32_TerminalServiceToSetting.Element
- Win32_TerminalServiceToSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d37a255b0a894ab257166f17c765f009d33b075
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391852"
---
# <a name="win32_terminalservicetosetting-class"></a><span data-ttu-id="16fe4-105">Win32 \_ terminalservicedesetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="16fe4-105">Win32\_TerminalServiceToSetting class</span></span>

<span data-ttu-id="16fe4-106">Die **Win32 \_ terminalservicedesetting** -WMI-Klasse stellt die Zuordnung zwischen einer Instanz der [**Win32 \_ Terminalservice**](win32-terminalservice.md) -Klasse und der Einstellung einer bestimmten [**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md) -Eigenschaft dar.</span><span class="sxs-lookup"><span data-stu-id="16fe4-106">The **Win32\_TerminalServiceToSetting** WMI class represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and the setting of a particular [**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) property.</span></span> <span data-ttu-id="16fe4-107">Zu den Konfigurationseinstellungen gehören Remotedesktop-Sitzungshost (RD-Sitzungshost) Server Modus, Lizenzierung, aktiver Desktop, Berechtigungs Funktion, Löschen von temporären Ordnern und temporären Ordnern pro Sitzung.</span><span class="sxs-lookup"><span data-stu-id="16fe4-107">Configuration settings include Remote Desktop Session Host (RD Session Host) server mode, Licensing, Active Desktop, Permissions Capability, Deletion of Temporary Folders and Temporary Folders-Per-Session.</span></span>

<span data-ttu-id="16fe4-108">Die folgende Syntax wird durch den MOF-Code vereinfacht und umfasst alle definierten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="16fe4-108">The following syntax is simplified from MOF code and includes all defined properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="16fe4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="16fe4-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TERMINALSERVICETOSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceToSetting : CIM_ElementSetting
{
  string                           Caption;
  string                           Description;
  datetime                         InstallDate;
  string                           Name;
  string                           Status;
  Win32_TerminalService        REF Element;
  Win32_TerminalServiceSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="16fe4-110">Member</span><span class="sxs-lookup"><span data-stu-id="16fe4-110">Members</span></span>

<span data-ttu-id="16fe4-111">Die **Win32 \_ terminalservicetosetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="16fe4-111">The **Win32\_TerminalServiceToSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="16fe4-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16fe4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16fe4-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16fe4-113">Properties</span></span>

<span data-ttu-id="16fe4-114">Die **Win32 \_ terminalservicedesetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="16fe4-114">The **Win32\_TerminalServiceToSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16fe4-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="16fe4-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16fe4-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16fe4-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16fe4-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16fe4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16fe4-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="16fe4-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="16fe4-119">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="16fe4-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="16fe4-120">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="16fe4-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="16fe4-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="16fe4-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16fe4-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16fe4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16fe4-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16fe4-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16fe4-124">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="16fe4-124">Description of the object.</span></span>

<span data-ttu-id="16fe4-125">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="16fe4-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="16fe4-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="16fe4-126">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16fe4-127">Datentyp: **Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="16fe4-127">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="16fe4-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16fe4-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16fe4-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="16fe4-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="16fe4-130">Stellt die Instanz von [**Win32 \_ Terminalservice**](win32-terminalservice.md) dar, die mit der **Setting** -Eigenschaft konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="16fe4-130">Represents the instance of [**Win32\_TerminalService**](win32-terminalservice.md) that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="16fe4-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="16fe4-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16fe4-132">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="16fe4-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="16fe4-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16fe4-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16fe4-134">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="16fe4-134">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="16fe4-135">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="16fe4-135">The date the object was installed.</span></span> <span data-ttu-id="16fe4-136">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="16fe4-136">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="16fe4-137">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="16fe4-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="16fe4-138">**Name**</span><span class="sxs-lookup"><span data-stu-id="16fe4-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16fe4-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16fe4-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16fe4-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16fe4-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16fe4-141">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="16fe4-141">The name of the object.</span></span>

<span data-ttu-id="16fe4-142">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="16fe4-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="16fe4-143">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="16fe4-143">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16fe4-144">Datentyp: **Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="16fe4-144">Data type: **Win32\_TerminalServiceSetting**</span></span>
</dt> <dt>

<span data-ttu-id="16fe4-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16fe4-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16fe4-146">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="16fe4-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="16fe4-147">Stellt die Remotedesktopdienste Konfigurationseinstellungen dar, die auf den zugeordneten RD-Sitzungshost Server angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="16fe4-147">Represents the Remote Desktop Services configuration settings that can be applied to the associated RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="16fe4-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="16fe4-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16fe4-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16fe4-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16fe4-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16fe4-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16fe4-151">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="16fe4-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="16fe4-152">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="16fe4-152">Current status of the object.</span></span> <span data-ttu-id="16fe4-153">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="16fe4-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="16fe4-154">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="16fe4-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="16fe4-155">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="16fe4-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="16fe4-156">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="16fe4-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="16fe4-157">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="16fe4-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="16fe4-158">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="16fe4-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="16fe4-159">("OK")</span><span class="sxs-lookup"><span data-stu-id="16fe4-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="16fe4-160">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="16fe4-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="16fe4-161">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="16fe4-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="16fe4-162">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="16fe4-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="16fe4-163">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="16fe4-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="16fe4-164">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="16fe4-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="16fe4-165">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="16fe4-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="16fe4-166">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="16fe4-166">("Service")</span></span>


<span data-ttu-id="16fe4-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="16fe4-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="16fe4-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16fe4-168">Remarks</span></span>

<span data-ttu-id="16fe4-169">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="16fe4-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="16fe4-170">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="16fe4-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="16fe4-171">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="16fe4-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="16fe4-172">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="16fe4-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="16fe4-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16fe4-173">Requirements</span></span>



| <span data-ttu-id="16fe4-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16fe4-174">Requirement</span></span> | <span data-ttu-id="16fe4-175">Wert</span><span class="sxs-lookup"><span data-stu-id="16fe4-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16fe4-176">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16fe4-176">Minimum supported client</span></span><br/> | <span data-ttu-id="16fe4-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16fe4-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16fe4-178">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16fe4-178">Minimum supported server</span></span><br/> | <span data-ttu-id="16fe4-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16fe4-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16fe4-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="16fe4-180">Namespace</span></span><br/>                | <span data-ttu-id="16fe4-181">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="16fe4-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="16fe4-182">MOF</span><span class="sxs-lookup"><span data-stu-id="16fe4-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16fe4-183"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="16fe4-183"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="16fe4-184">DLL</span><span class="sxs-lookup"><span data-stu-id="16fe4-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16fe4-185"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16fe4-185"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16fe4-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16fe4-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16fe4-187">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="16fe4-187">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="16fe4-188">**Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="16fe4-188">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="16fe4-189">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="16fe4-189">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="16fe4-190">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="16fe4-190">**CIM\_ElementSetting**</span></span>](/windows/desktop/CIMWin32Prov/cim-elementsetting)
</dt> </dl>

 

