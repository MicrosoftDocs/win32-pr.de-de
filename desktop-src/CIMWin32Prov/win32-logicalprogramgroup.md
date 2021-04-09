---
description: Die Win32 \_ logicalprogramgroup&\# 8194; WMI-Klasse stellt eine Programmgruppe in einem Computersystem dar, auf dem Windows ausgeführt wird. Beispielsweise Zubehör oder Startup.
ms.assetid: e05b512d-92ab-4864-b8df-f4a8b66761c9
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroup-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroup
- Win32_LogicalProgramGroup.Caption
- Win32_LogicalProgramGroup.Description
- Win32_LogicalProgramGroup.InstallDate
- Win32_LogicalProgramGroup.Status
- Win32_LogicalProgramGroup.GroupName
- Win32_LogicalProgramGroup.Name
- Win32_LogicalProgramGroup.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db7c7484489ecbc87e908dc6eb1c3de156cda665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861500"
---
# <a name="win32_logicalprogramgroup-class"></a><span data-ttu-id="f358f-104">Win32 \_ logicalprogramgroup-Klasse</span><span class="sxs-lookup"><span data-stu-id="f358f-104">Win32\_LogicalProgramGroup class</span></span>

<span data-ttu-id="f358f-105">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ logicalprogramgroup** " stellt eine Programmgruppe in einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f358f-105">The **Win32\_LogicalProgramGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a program group in a computer system running Windows.</span></span> <span data-ttu-id="f358f-106">Beispielsweise Zubehör oder Startup.</span><span class="sxs-lookup"><span data-stu-id="f358f-106">For example, Accessories or Startup.</span></span>

<span data-ttu-id="f358f-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f358f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f358f-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="f358f-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f358f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f358f-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{D52706F2-8045-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroup : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   GroupName;
  string   Name;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="f358f-110">Member</span><span class="sxs-lookup"><span data-stu-id="f358f-110">Members</span></span>

<span data-ttu-id="f358f-111">Die **Win32 \_ logicalprogramgroup** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f358f-111">The **Win32\_LogicalProgramGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="f358f-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f358f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f358f-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f358f-113">Properties</span></span>

<span data-ttu-id="f358f-114">Die **Win32 \_ logicalprogramgroup** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f358f-114">The **Win32\_LogicalProgramGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f358f-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f358f-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f358f-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f358f-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f358f-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f358f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f358f-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f358f-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f358f-119">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f358f-119">A short textual description of the object.</span></span>

<span data-ttu-id="f358f-120">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f358f-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f358f-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f358f-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f358f-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f358f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f358f-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f358f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f358f-124">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f358f-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f358f-125">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f358f-125">A textual description of the object.</span></span>

<span data-ttu-id="f358f-126">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f358f-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f358f-127">**GroupName**</span><span class="sxs-lookup"><span data-stu-id="f358f-127">**GroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f358f-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f358f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f358f-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f358f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f358f-130">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| cwbemproviderglue Class Methods \| [**getallinstance**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="f358f-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="f358f-131">Name der Windows-Programmgruppe.</span><span class="sxs-lookup"><span data-stu-id="f358f-131">Name of the Windows program group.</span></span> <span data-ttu-id="f358f-132">Programm Gruppen werden als Datei Ordner in Win32 implementiert.</span><span class="sxs-lookup"><span data-stu-id="f358f-132">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="f358f-133">Beispiel: "Zubehör \\ System Tools"</span><span class="sxs-lookup"><span data-stu-id="f358f-133">Example: "Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="f358f-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f358f-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f358f-135">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f358f-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f358f-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f358f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f358f-137">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="f358f-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f358f-138">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f358f-138">Indicates when the object was installed.</span></span> <span data-ttu-id="f358f-139">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f358f-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f358f-140">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f358f-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f358f-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="f358f-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f358f-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f358f-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f358f-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f358f-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f358f-144">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| cwbemproviderglue Class Methods \| [**getallinstance**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="f358f-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="f358f-145">Vom Benutzer zugewiesener Name, gefolgt vom Gruppennamen.</span><span class="sxs-lookup"><span data-stu-id="f358f-145">User-assigned name followed by the group name.</span></span> <span data-ttu-id="f358f-146">Programm Gruppen werden als Datei Ordner in Win32 implementiert.</span><span class="sxs-lookup"><span data-stu-id="f358f-146">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="f358f-147">Beispiel: "alle Benutzer: Zubehör \\ System Tools"</span><span class="sxs-lookup"><span data-stu-id="f358f-147">Example: "All Users:Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="f358f-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="f358f-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f358f-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f358f-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f358f-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f358f-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f358f-151">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="f358f-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f358f-152">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="f358f-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="f358f-153">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f358f-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f358f-154">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="f358f-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f358f-155">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="f358f-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f358f-156">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="f358f-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f358f-157">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="f358f-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f358f-158">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="f358f-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f358f-159">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f358f-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f358f-160">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="f358f-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f358f-161">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f358f-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f358f-162">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="f358f-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f358f-163">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="f358f-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f358f-164">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f358f-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f358f-165">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f358f-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f358f-166">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="f358f-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f358f-167">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="f358f-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f358f-168">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="f358f-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f358f-169">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="f358f-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f358f-170">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="f358f-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f358f-171">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="f358f-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f358f-172">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="f358f-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f358f-173">**UserName**</span><span class="sxs-lookup"><span data-stu-id="f358f-173">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f358f-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f358f-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f358f-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f358f-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f358f-176">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| cwbemproviderglue Class Methods \| [**getallinstance**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="f358f-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="f358f-177">Benutzer, die auf die Windows-Programmgruppe zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="f358f-177">Users who can access the Windows program group.</span></span> <span data-ttu-id="f358f-178">Programm Gruppen werden als Datei Ordner in Win32 implementiert.</span><span class="sxs-lookup"><span data-stu-id="f358f-178">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="f358f-179">Beispiel: "alle Benutzer"</span><span class="sxs-lookup"><span data-stu-id="f358f-179">Example: "All Users"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f358f-180">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f358f-180">Remarks</span></span>

<span data-ttu-id="f358f-181">Die **Win32 \_ logicalprogramgroup** -Klasse wird von [**Win32 \_ programgrouporitem**](win32-programgrouporitem.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f358f-181">The **Win32\_LogicalProgramGroup** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="f358f-182">Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen.</span><span class="sxs-lookup"><span data-stu-id="f358f-182">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="f358f-183">Wenn Sie diese Klasse z. b. auf dem lokalen Computer auflisten, muss das Konto, unter dem Ihre Anwendung ausgeführt wird, über diese Berechtigung verfügen.</span><span class="sxs-lookup"><span data-stu-id="f358f-183">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="f358f-184">Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="f358f-184">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="f358f-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f358f-185">Requirements</span></span>



| <span data-ttu-id="f358f-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f358f-186">Requirement</span></span> | <span data-ttu-id="f358f-187">Wert</span><span class="sxs-lookup"><span data-stu-id="f358f-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f358f-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f358f-188">Minimum supported client</span></span><br/> | <span data-ttu-id="f358f-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f358f-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f358f-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f358f-190">Minimum supported server</span></span><br/> | <span data-ttu-id="f358f-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f358f-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f358f-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="f358f-192">Namespace</span></span><br/>                | <span data-ttu-id="f358f-193">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f358f-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f358f-194">MOF</span><span class="sxs-lookup"><span data-stu-id="f358f-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f358f-195"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f358f-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f358f-196">DLL</span><span class="sxs-lookup"><span data-stu-id="f358f-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f358f-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f358f-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f358f-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f358f-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f358f-199">**Win32- \_ programmgrouporitem**</span><span class="sxs-lookup"><span data-stu-id="f358f-199">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="f358f-200">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f358f-200">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

