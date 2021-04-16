---
description: Das Win32 \_ logicalprogramgroupitem-&\# 8194; Die WMI-Klasse stellt ein Element dar, das in einer Win32 \_ logicalprogramgroup enthalten ist, das nicht auch eine andere Win32 \_ logicalprogramgroup-Instanz ist.
ms.assetid: 70b127bf-4e94-4c1a-98ff-909bdfe0f009
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupItem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItem
- Win32_LogicalProgramGroupItem.Caption
- Win32_LogicalProgramGroupItem.Description
- Win32_LogicalProgramGroupItem.InstallDate
- Win32_LogicalProgramGroupItem.Status
- Win32_LogicalProgramGroupItem.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1afd78ba17e444520d8dec81eac05fffa103aede
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524275"
---
# <a name="win32_logicalprogramgroupitem-class"></a><span data-ttu-id="7b795-103">Win32 \_ logicalprogramgroupitem-Klasse</span><span class="sxs-lookup"><span data-stu-id="7b795-103">Win32\_LogicalProgramGroupItem class</span></span>

<span data-ttu-id="7b795-104">Die **Win32 \_ logicalprogramgroupitem** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt ein Element dar, das in einer [**Win32 \_ logicalprogramgroup**](win32-logicalprogramgroup.md) enthalten ist, das nicht auch eine andere **Win32 \_ logicalprogramgroup** -Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="7b795-104">The **Win32\_LogicalProgramGroupItem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an element contained by a [**Win32\_LogicalProgramGroup**](win32-logicalprogramgroup.md) that is not also another **Win32\_LogicalProgramGroup** instance.</span></span>

<span data-ttu-id="7b795-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7b795-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7b795-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="7b795-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b795-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b795-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{86E30E82-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItem : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="7b795-108">Member</span><span class="sxs-lookup"><span data-stu-id="7b795-108">Members</span></span>

<span data-ttu-id="7b795-109">Die **Win32 \_ logicalprogramgroupitem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7b795-109">The **Win32\_LogicalProgramGroupItem** class has these types of members:</span></span>

-   [<span data-ttu-id="7b795-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b795-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b795-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b795-111">Properties</span></span>

<span data-ttu-id="7b795-112">Die **Win32 \_ logicalprogramgroupitem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7b795-112">The **Win32\_LogicalProgramGroupItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b795-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7b795-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b795-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7b795-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b795-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7b795-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b795-116">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7b795-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7b795-117">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7b795-117">A short textual description of the object.</span></span>

<span data-ttu-id="7b795-118">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7b795-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b795-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7b795-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b795-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7b795-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b795-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7b795-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b795-122">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="7b795-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7b795-123">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7b795-123">A textual description of the object.</span></span>

<span data-ttu-id="7b795-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7b795-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b795-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7b795-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b795-126">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7b795-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7b795-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7b795-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b795-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="7b795-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7b795-129">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7b795-129">Indicates when the object was installed.</span></span> <span data-ttu-id="7b795-130">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7b795-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7b795-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7b795-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b795-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="7b795-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b795-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7b795-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b795-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7b795-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b795-135">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| cwbemproviderglue Class Methods \| [**getallinstance**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="7b795-135">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="7b795-136">Instanz innerhalb eines Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="7b795-136">Instance within a computer system.</span></span> <span data-ttu-id="7b795-137">Programm Gruppen werden als Datei Ordner in Win32 implementiert.</span><span class="sxs-lookup"><span data-stu-id="7b795-137">Program groups are implemented as file folders in Win32.</span></span> <span data-ttu-id="7b795-138">Vollständige Pfadnamen müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7b795-138">Full path names should be provided.</span></span>

<span data-ttu-id="7b795-139">Beispiel: "C: \\ Benutzer \\  \\ AppData \\ Roaming \\ Microsoft Windows \\ - \\ Startmenü \\ Programme \\ Zubehör \\ Notepad. lnk"</span><span class="sxs-lookup"><span data-stu-id="7b795-139">Example: "C:\\Users\\*someone*\\AppData\\Roaming\\Microsoft\\Windows\\Start Menu\\Programs\\Accessories\\NotePad.Lnk"</span></span>

</dd> <dt>

<span data-ttu-id="7b795-140">**Status**</span><span class="sxs-lookup"><span data-stu-id="7b795-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b795-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7b795-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b795-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7b795-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b795-143">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="7b795-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7b795-144">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="7b795-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="7b795-145">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7b795-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7b795-146">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="7b795-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7b795-147">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="7b795-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7b795-148">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="7b795-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7b795-149">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="7b795-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7b795-150">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="7b795-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7b795-151">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7b795-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7b795-152">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="7b795-152">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7b795-153">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="7b795-153">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7b795-154">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="7b795-154">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7b795-155">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="7b795-155">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b795-156">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="7b795-156">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7b795-157">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="7b795-157">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7b795-158">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="7b795-158">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7b795-159">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="7b795-159">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7b795-160">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="7b795-160">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7b795-161">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="7b795-161">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7b795-162">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="7b795-162">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7b795-163">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="7b795-163">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7b795-164">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="7b795-164">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="7b795-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7b795-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7b795-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b795-166">Remarks</span></span>

<span data-ttu-id="7b795-167">Die **Win32 \_ logicalprogramgroupitem** -Klasse wird von [**Win32 \_ programgrouporitem**](win32-programgrouporitem.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7b795-167">The **Win32\_LogicalProgramGroupItem** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="7b795-168">Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen.</span><span class="sxs-lookup"><span data-stu-id="7b795-168">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="7b795-169">Wenn Sie diese Klasse z. b. auf dem lokalen Computer auflisten, muss das Konto, unter dem Ihre Anwendung ausgeführt wird, über diese Berechtigung verfügen.</span><span class="sxs-lookup"><span data-stu-id="7b795-169">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="7b795-170">Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="7b795-170">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b795-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b795-171">Requirements</span></span>



| <span data-ttu-id="7b795-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b795-172">Requirement</span></span> | <span data-ttu-id="7b795-173">Wert</span><span class="sxs-lookup"><span data-stu-id="7b795-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b795-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b795-174">Minimum supported client</span></span><br/> | <span data-ttu-id="7b795-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b795-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b795-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b795-176">Minimum supported server</span></span><br/> | <span data-ttu-id="7b795-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b795-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b795-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b795-178">Namespace</span></span><br/>                | <span data-ttu-id="7b795-179">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7b795-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7b795-180">MOF</span><span class="sxs-lookup"><span data-stu-id="7b795-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b795-181"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7b795-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b795-182">DLL</span><span class="sxs-lookup"><span data-stu-id="7b795-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b795-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b795-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b795-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b795-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b795-185">**Win32- \_ programmgrouporitem**</span><span class="sxs-lookup"><span data-stu-id="7b795-185">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="7b795-186">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7b795-186">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

