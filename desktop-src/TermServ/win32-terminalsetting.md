---
title: Win32_TerminalSetting-Klasse
description: Stellt die Einstellungen dar, die auf ein Terminal angewendet werden können.
ms.assetid: e709aa60-f8fd-4e83-a5a1-d682ff469d23
ms.tgt_platform: multiple
keywords:
- Win32_TerminalSetting-Klasse Remotedesktopdienste
- Win32_TerminalSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TerminalSetting
- Win32_TerminalSetting.Caption
- Win32_TerminalSetting.Description
- Win32_TerminalSetting.InstallDate
- Win32_TerminalSetting.Name
- Win32_TerminalSetting.Status
- Win32_TerminalSetting.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa29438ddea518c9f17e35fdafc3b9a912694d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341026"
---
# <a name="win32_terminalsetting-class"></a><span data-ttu-id="d87b6-105">Win32 \_ TerminalSetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="d87b6-105">Win32\_TerminalSetting class</span></span>

<span data-ttu-id="d87b6-106">Die **Win32 \_ TerminalSetting** -WMI-Klasse stellt die Einstellungen dar, die auf ein Terminal angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d87b6-106">The **Win32\_TerminalSetting** WMI class represents the settings that can be applied to a terminal.</span></span>

<span data-ttu-id="d87b6-107">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="d87b6-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d87b6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d87b6-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TerminalSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="d87b6-109">Member</span><span class="sxs-lookup"><span data-stu-id="d87b6-109">Members</span></span>

<span data-ttu-id="d87b6-110">Die **Win32 \_ TerminalSetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d87b6-110">The **Win32\_TerminalSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="d87b6-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d87b6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d87b6-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d87b6-112">Properties</span></span>

<span data-ttu-id="d87b6-113">Die **Win32 \_ TerminalSetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d87b6-113">The **Win32\_TerminalSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d87b6-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d87b6-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d87b6-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d87b6-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d87b6-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d87b6-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d87b6-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d87b6-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d87b6-118">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d87b6-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="d87b6-119">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d87b6-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d87b6-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d87b6-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d87b6-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d87b6-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d87b6-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d87b6-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d87b6-123">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="d87b6-123">Description of the object.</span></span>

<span data-ttu-id="d87b6-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d87b6-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d87b6-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d87b6-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d87b6-126">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d87b6-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d87b6-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d87b6-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d87b6-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="d87b6-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d87b6-129">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d87b6-129">The date the object was installed.</span></span> <span data-ttu-id="d87b6-130">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d87b6-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d87b6-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d87b6-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d87b6-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="d87b6-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d87b6-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d87b6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d87b6-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d87b6-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d87b6-135">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="d87b6-135">The name of the object.</span></span>

<span data-ttu-id="d87b6-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d87b6-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d87b6-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="d87b6-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d87b6-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d87b6-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d87b6-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d87b6-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d87b6-140">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="d87b6-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="d87b6-141">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="d87b6-141">Current status of the object.</span></span> <span data-ttu-id="d87b6-142">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d87b6-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d87b6-143">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="d87b6-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d87b6-144">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="d87b6-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d87b6-145">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d87b6-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d87b6-146">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="d87b6-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d87b6-147">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d87b6-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="d87b6-148">("OK")</span><span class="sxs-lookup"><span data-stu-id="d87b6-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d87b6-149">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="d87b6-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d87b6-150">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="d87b6-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d87b6-151">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="d87b6-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d87b6-152">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="d87b6-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d87b6-153">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="d87b6-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d87b6-154">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="d87b6-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d87b6-155">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="d87b6-155">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d87b6-156">**Terminal Name**</span><span class="sxs-lookup"><span data-stu-id="d87b6-156">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d87b6-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d87b6-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d87b6-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d87b6-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d87b6-159">Der Name des Terminals.</span><span class="sxs-lookup"><span data-stu-id="d87b6-159">The name of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d87b6-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d87b6-160">Remarks</span></span>

<span data-ttu-id="d87b6-161">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="d87b6-161">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d87b6-162">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="d87b6-162">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d87b6-163">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d87b6-163">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d87b6-164">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d87b6-164">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d87b6-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d87b6-165">Requirements</span></span>



| <span data-ttu-id="d87b6-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d87b6-166">Requirement</span></span> | <span data-ttu-id="d87b6-167">Wert</span><span class="sxs-lookup"><span data-stu-id="d87b6-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d87b6-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d87b6-168">Minimum supported client</span></span><br/> | <span data-ttu-id="d87b6-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d87b6-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d87b6-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d87b6-170">Minimum supported server</span></span><br/> | <span data-ttu-id="d87b6-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d87b6-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d87b6-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="d87b6-172">Namespace</span></span><br/>                | <span data-ttu-id="d87b6-173">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d87b6-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d87b6-174">MOF</span><span class="sxs-lookup"><span data-stu-id="d87b6-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d87b6-175"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d87b6-175"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d87b6-176">DLL</span><span class="sxs-lookup"><span data-stu-id="d87b6-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d87b6-177"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d87b6-177"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d87b6-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d87b6-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d87b6-179">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="d87b6-179">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="d87b6-180">**Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="d87b6-180">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="d87b6-181">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="d87b6-181">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

